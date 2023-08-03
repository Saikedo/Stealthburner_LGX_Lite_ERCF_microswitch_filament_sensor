# Stealthburner CW2 LGX Lite Mount with Microswitch Filament Sensor for ERCF

**Note:** The original idea and base CAD models originated from the repository [LGX_Lite_Stealthburner_CW2_style_mount](https://github.com/Eytecz/LGX_Lite_Stealthburner_CW2_style_mount/tree/main). After several unsuccessful attempts to integrate it with a hall effect sensor (which repeatedly failed after a few days), I decided to create a mount that employs a microswitch. I'll provide instructions for mounting the microswitch; however, for detailed assembly instructions, you should refer to the aforementioned repository.

![Main Image](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/combinedMain1.jpg)

The filament sensor requires two components:

* D2F-01L Switch (Other switches with similar dimensions should work just fine)
* 6x3mm magnet (You don't actually require a magnet; anything with dimensions of 6mmx3mm should suffice). It's crucial to have the cylinder's radius as close to 6mm as possible. The height doesn't need to be as precise, but aim for less than 3mm.

# Printing Instructions
For printing, utilize the default Voron parts printing settings. There's no need for additional supports or alterations in settings.

# Assembly Instructions and Tips

# Step 1: Magnet Insertion
Insert the magnet into the magnet hole in the Front_body_LGX_Lite_Stealthburner_ERCF. Ensure that the magnet can move freely within the hole and encounters no resistance. The magnet should protrude into the filament hole by about 1.25mm.

 ![Insert magnet instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/InsertMagnet1.jpg)

# Step 2: Button Wiring
Solder two wires to the button and feed the wires through the holes at the back of the button hole in the Rear_body_LGX_Lite_Stealthburner_ERCF part. I will discuss my personal wiring preferences at the end of this document.

 ![Button wiring instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/buttonWiringHoles1.jpg)

# Step 3: Button Insertion
Begin inserting the button into the Rear_body_LGX_Lite_Stealthburner_ERCF part. It might be a tight fit and require some force to fully insert, but make sure that it goes all the way in. After insertion, the button should protrude by about 0.75mm from the front.

 ![Button insertion instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/insertButton1.jpg)

# Step 4: Self Tapping Screws (Optional)
I designed holes in the Rear_body_LGX_Lite_Stealthburner_ERCF to enable screwing in the button with M2x8mm self-tapping screws. I personally used [these screws](https://www.amazon.com/gp/product/B00YBMRAH4/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1). Note, however, that this step should be optional since the button should already be snugly fitted into the part and will later be sandwiched between the two parts. Despite this, I conducted all my testing with the screws, so proceed without them at your own risk.

 ![Self tapping screws instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/selfTappingScrews1.jpg)

# Step 5: Initial Testing
Position the two parts together and hold them firmly. Insert a filament into the filament hole and listen for a clicking sound from the button when inserting the filament. Verify that the button is properly unclicking when removing the filament.

# Button Wiring
The Rear_body_LGX_Lite_Stealthburner_ERCF part features holes for all three prongs of the button, so you can wire it in any way you prefer. Below is my personal wiring method.

I wired the button in a normally open position (no voltage if the button isn't pressed). With this setup, the filament sensor will report no filament if the sensor wires aren't connected or if there are any issues with the wiring. I personally use the EBB36 (Version 1.2) canBus board, so the diagram below demonstrates wiring to the EBB36 board, but you can connect this to any other pin as well.

 ![Button wiring instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/buttonWiring1.jpg)

Use the following Klipper code for ERCF (place this in ercf_hardware.cfg):

```
[filament_switch_sensor toolhead_sensor]
pause_on_runout: False		# Must be False
switch_pin: ^!YOUR_PIN  # If you have EBB36 and wired it similarly to the diagram above, this line will be switch_pin: ^!EBBCan:PB9
```


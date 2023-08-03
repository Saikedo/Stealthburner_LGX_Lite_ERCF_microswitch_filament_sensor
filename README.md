# Stealthburner CW2 LGX Lite mount with microswitch filament sensor for ERCF

Note: The original idea and the base cad models came from the following repository [LGX_Lite_Stealthburner_CW2_style_mount](https://www.google.com](https://github.com/Eytecz/LGX_Lite_Stealthburner_CW2_style_mount/tree/main)https://github.com/Eytecz/LGX_Lite_Stealthburner_CW2_style_mount/tree/main). After numerous attempts, I was unable to make it work with a hall effect sensor (It was constantly failing after few days) and because of that, I decided to make a mount that uses a micro switch. I will list the instructions for mounting the microswitch but you should refer to the repository mentioned above for more detailed assembly instructions.

![Main Image](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/combinedMain.jpg)

Filament sensor requires two parts

* D2F-01L Switch (Other switches with similar dimensions should work just fine)
* 6x3 magnet (You don`t really need a magnet, anything with 6mmx3mm should work). It is very important to have the radius of the cylinder as close to 6mm as possible. Height does not need to be as accurate but aim for < 3mm.

# Assembly instructions and tips

#1: Magnet Insertion
Insert the magnet into the Front_body_LGX_Lite_Stealthburner_ERCF magnet hole. Make sure the magnet can move freely within the hole. There must be no resistance when moving the magnet. The magnet should enter the filament hole by about 1.25mm.

 ![Insert magnet instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/InsertMagnet.jpg)

#2: Button Wiring
Solder two wires to the button and pass the wires through the holes at the back of the button hole in Rear_body_LGX_Lite_Stealthburner_ERCF part. I will talk more about my personal preference for wiring at the end of this document.

 ![Button wiring instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/buttonWiringHoles.jpg)

#3: Button Insertion
Start inserting the button into Rear_body_LGX_Lite_Stealthburner_ERCF part. It might be a tight fit and require a little bit of force to insert it all the way but make sure that it goes all the way in. After insertion, the button should protrude
by about 0.75mm from the front.

 ![Button insertion instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/insertButton.jpg)

#4: Self Tapping Screws(Optional)
I left holes in Rear_body_LGX_Lite_Stealthburner_ERCF to allow screwing in the button with M2x8mm self tapping screws. I peronsally used [these screws](https://www.amazon.com/gp/product/B00YBMRAH4/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1). Note that this step should be optional since the button should already be snuggly fitted into the part and later on it will get sandwiched between the two parts. Regardless, I did all my testing with the screws so skip this step at your own risk.

 ![Self tapping screws instruction photo](https://github.com/Saikedo/Stealthburner_LGX_Lite_ERCF_microswitch_filament_sensor/blob/main/IMAGES/selfTappingScrews.jpg)

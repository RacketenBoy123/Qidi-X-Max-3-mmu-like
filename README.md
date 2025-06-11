# Qidi-X-Max-3 mmu-like
 A fan-made MMU/AMS-like system for the Qidi X Max 3
 It is fully created in G-code and uses the FreeDi replacement system for the Qidi printer as a base. For instructions on how to install FreeDi, go here: : [FreeDi](https://github.com/Phil1988/FreeDi/tree/master)

 I also recommend that you upgrade the internal eMMC module to a 32GB one.

# Hardware needed
As of the hardware side you only need:

1. 1 x Bigtreetech SKR Pico
2. 1 to 4 Nema 17 (E series) Motors (Recommended: [Nema 17 Motors](https://www.amazon.de/dp/B0B93PNYCP?ref=ppx_yo2ov_dt_b_fed_asin_title)) and 1 to 4 longer dupont cables 
3. 1 to 4 Extruders with mounting hardware (Recommended: [Dual drive extruder](https://www.amazon.de/dp/B0865SLWQ5?ref=ppx_yo2ov_dt_b_fed_asin_title))
4. PTFE Tubing and fittings (Recommended: [5m PTFE tuning and fittings](https://www.amazon.de/FULARR%C2%AE-Professionell-Teflonrohr-Fitting-Verbinder/dp/B07R9JXQF4/ref=sr_1_26?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3SBDBWJSZR1MG&dib=eyJ2IjoiMSJ9.Jenjyhu5zRrNzp9kz3MHe8qOatKZwjhqRLRJnPKSWHxhBQ0qgppRghjO32BWphyT9NebFXynXLC66PK71bzVECucnrxg4sjhDzP6UxV0qtZlodXNcX_QxvVEPF248UnVuGGKND7N5GI1WTaMLljy9b2asiCG5c6yNXTcNL-nvsGYTUkmw1ReUUjn1G8AwaMmoe1yvJa-Dc0_pY9qHIWlbAG_K3n0YeIDoy5-YtGEFUXgY3mWD1Ux8LTqD_L14_42H1-rvkmftmQEpe6EbTrs23NZjB3h-orzqJ0lubBEkzo.9yMlFL-osIWTJ43IJvhn0VmoFHn0bqrM6Tg0ho1lEXM&dib_tag=se&keywords=ptfe+schlauch&qid=1749646232&sprefix=ptfe+schlauch%2Caps%2C161&sr=8-26))
5. 16 M3 Heated inserts and 16 M3x7mm screws
6. 1x 5 to 5.5mm diameter spring

Optional:

7. 1 x Ikea Samla 22L box [Link](https://www.ikea.com/de/de/p/samla-box-mit-deckel-transparent-s69440822/#content)
8. Sealing for the Samla box
9. 1 x PVC Pipe, 33mm or 40mm diamater and 32cm length
10. 1 x Hygrometer
11. Silicat

# Disclaimer
Before you print or install anything, be sure to install FreeDi and the matching version of Klipper on your SKR Pico. After that, you can proceed.
A disclaimer before you start: the AMS riser, toolhead, filament cutter, Samla box filament holder, and nozzle wiper are all from different creators. Most of these files I edited and changed to make them work better, but please still support the original creators. All of the original links are in the folders as a text file or in this installation guide. Thanks.
If anthing doesnt work for you or theres a bug in the gcode, please contact me.


# Installation
The first step is printing the needed adapters and hardware. I recommend printing these parts all in either ABS or ASA to make them more heat resistant.
If you don’t know how to proceed at any step, please look at the included pictures or message me. Included pictures are in the /assets/images folder and named after what they might help with assembling. 
Go through the stl_files folder and download the following STL files and print them the amount stated below:


### Ams Riser

1. 1x 4-way_splitter-flat.stl
2. 1x xmax-mmu-lf.stl
3. 1x xmax-mmu-lr.stl
4. 1x xmax-mmu-rf.stl
5. 1x xmax-mmu-rr.stl
6. 8x mmu-xmax_joiner-clip-x8-v1.stl

After printing the needed hardware for the riser, go through the "732980-x-max-3-automatic-multi-material-riser-ec3e07c0-a392-4935-88c6-fceb8f445ebd.pdf" or click this [Link](https://www.printables.com/model/732980-x-max-3-automatic-multi-material-riser/files) to see how to assemble the printed pieces. For that, push the heat-set inserts into the designed holes on the side of the riser pieces with a soldering iron.


### MCU Holder

1. 1x Back_Spool_Holder_Adapter.stl
2. 1x MCU_Holder v2.stl
3. 1x ams_cover.stl (Optional)

Detach the spool holder from the backside of the printer.
Then take the "Back_Spool_Holder_Adapter.stl" and the "MCU_Holder v2.stl" and screw them together. Now place the MCU over the screw holes of the holder, with the heat-set inserts, and screw the SKR Pico onto the holder.
Now place the adapter in the slot that is now free at the back of the printer and slide it down.
Before this step, be sure to power off the printer. Now you just need to open the back plate of the printer, take a USB cable, attach it to the mainboard of the printer, fish it through the vent cutouts, and plug it into the SKR Pico.
After that, make sure to close everything back up, power on the printer, and configure the SKR Pico via SSH [Tutorial](https://www.youtube.com/watch?v=hfD1LAOoBJc).


### Toolhead

This segment contains a replacement for the toolhead cover, to make it more accessible, and a filament cutter that replaces the stock filament guide and adds a place for a knife blade. The STL files also contain a "Cutter_Stop.stl", which is a plug to push into one of the holes in the front of the chassis, which, when equipped with a heat-set insert and a screw, will push the filament cutter in and cut the filament when needed.

1. 1x Cutter_Stop.stl
2. 1x Filament_cutter.stl
3. 1x Filament_cutter_arm.stl

Optional:

4. 1x qidi_front_adapter_short.stl
5. 1x Qidi_front_cover v2.stl
6. You also need magnets with a 10mm daimeter

After printing these parts, unload the filament out of the printhead, power off the printer, and take off the front cover of the toolhead. Take out the original PTFE tube and the original fitting.
Before you now place in the replacement, make sure to screw in one of the fittings (the silver one) into the big hole at the top. I recommend using a bit of heat from a heat gun to preheat the hole so the printed part won’t snap in two.
Now place the "Filament_cutter.stl" onto the printhead; the square pillar should align with the square cutout right beneath the filament inlet.
After that, take the "Filament_cutter_arm.stl", place a small knife blade into the slot on the side, with the hole at one end facing up. After that, take the arm and align the hole at one end with the further back hole of the "Filament_cutter.stl" and put a screw through both of these. Now take the spring and place it on the sideways hole on the "Filament_cutter.stl", the small hole that doesn’t go through and points towards the "Filament_cutter_arm.stl". After that, take another screw and place it in the other hole on the "Filament_cutter.stl" as a stop for the "Filament_cutter_arm.stl" so it doesn’t open too wide.

![Printhead_2](https://github.com/user-attachments/assets/1a51c996-59f1-4b15-bea3-7bf37f9cd834)

At the end put a heat-set insert in the  "Cutter_Stop.stl", put a screw in the insert and let it stick out about 25mm and then push the block in the square hole at the end of the light strip, with the srew further to the top.

![Stop_1](https://github.com/user-attachments/assets/88e39223-ea54-45d5-b39f-c957716f62e2)

After that, you can optionally install the magnetic printhead cover. For that, follow this [Link](https://www.printables.com/model/952804-filament-cutter-for-x-plussmartmax-3-toolhead).


### Poop Bucket

1. 1x Bucket_Filament.stl

![Bucket_3](https://github.com/user-attachments/assets/3313671b-0a14-4e39-aca4-a3b73abe4a86)

To install this, slide it into the flat steel at the back of the printer (internally) and follow the included pictures.


### Nozzle Wiper

1. 1x Wipe_arm.stl
2. 1x Wipe_clamp.stl

![Wiper_1](https://github.com/user-attachments/assets/b66817f8-82fd-45c5-8e31-cb8e2a4183b0)

Follow the included pictures and this [Link](https://www.printables.com/model/722217-qidi-x-max-3-nozzle-scrub-holder)


### Filament Storage

1. 2x Ikea_box_holder.stl
2. 1x to 4x angled_feeder_outside_m6_for_greater_gap.stl

Optional:

3. 2x PVC_Adapter.stl (Optional)
4. 3x Spool Trenner.stl (Optional for 33mm diameter PVC Pipe only)
5. samla_clips.stl (Optional)

![Samla_1](https://github.com/user-attachments/assets/4088078d-d6ad-4876-bd78-3f4300d83510)

Follow this [Link](https://www.thingiverse.com/thing:1752874)

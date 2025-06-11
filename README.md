# Qidi-X-Max-3 mmu-like
 A fan made mmu/ams like system for the Qidi X Max 3
 It is fully created in gcode and uses the FreeDi replacement system for the Qidi printer as a base. For instructions on how to install FreeDi go here: [FreeDi](https://github.com/Phil1988/FreeDi/tree/master)

 I also recommend for you to upgrade the internal emmc module to a 32gb one.

# Hardware needed
 As of the hardware side you only need:

1. 1 x Bigtreetech SKR Pico
2. 1 to 4 Nema 17 (E series) Motors (Recommended: [Nema 17 Motors](https://www.amazon.de/dp/B0B93PNYCP?ref=ppx_yo2ov_dt_b_fed_asin_title))
2.1 1 to 4 longer dupont cables 
3. 1 to 4 Extruders with mounting hardware (Recommended: [Dual drive extruder](https://www.amazon.de/dp/B0865SLWQ5?ref=ppx_yo2ov_dt_b_fed_asin_title))
4. PTFE Tubing and fittings (Recommended: [5m PTFE tuning and fittings](https://www.amazon.de/FULARR%C2%AE-Professionell-Teflonrohr-Fitting-Verbinder/dp/B07R9JXQF4/ref=sr_1_26?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3SBDBWJSZR1MG&dib=eyJ2IjoiMSJ9.Jenjyhu5zRrNzp9kz3MHe8qOatKZwjhqRLRJnPKSWHxhBQ0qgppRghjO32BWphyT9NebFXynXLC66PK71bzVECucnrxg4sjhDzP6UxV0qtZlodXNcX_QxvVEPF248UnVuGGKND7N5GI1WTaMLljy9b2asiCG5c6yNXTcNL-nvsGYTUkmw1ReUUjn1G8AwaMmoe1yvJa-Dc0_pY9qHIWlbAG_K3n0YeIDoy5-YtGEFUXgY3mWD1Ux8LTqD_L14_42H1-rvkmftmQEpe6EbTrs23NZjB3h-orzqJ0lubBEkzo.9yMlFL-osIWTJ43IJvhn0VmoFHn0bqrM6Tg0ho1lEXM&dib_tag=se&keywords=ptfe+schlauch&qid=1749646232&sprefix=ptfe+schlauch%2Caps%2C161&sr=8-26))
5. 16 M3 Heated inserts and 16 M3x7mm screws

Optional
6. 1 x Ikea Samla 22L box [Link](https://www.ikea.com/de/de/p/samla-box-mit-deckel-transparent-s69440822/#content)
7. Sealing for the Samla box
8. 1 x PVC Pipe, 36mm diamater and 35cm length
9. 1 x Hygrometer
10. Silicat

# Installation
Before you print or install anything, be sure to install FreeDi and the matching version of klipper on your SKR Pico. After that you can proceed.

The first step is printing the needed adapters and hardware.
Go through the stl_files folder and download the following stl files and print them the amount stated below:

1. Ams Riser

1x 4-way_splitter-flat.stl

1x xmax-mmu-lf.stl

1x xmax-mmu-lr.stl

1x xmax-mmu-rf.stl

1x xmax-mmu-rr.stl

8x mmu-xmax_joiner-clip-x8-v1.stl

After printing the needed hardware for the riser, go through the "732980-x-max-3-automatic-multi-material-riser-ec3e07c0-a392-4935-88c6-fceb8f445ebd.pdf" or click this [Link](https://www.printables.com/model/732980-x-max-3-automatic-multi-material-riser/files) to see how to assamble the printed pieces. For that push the heatset insers into the designed holes on the side of the riser pieces with an solder iron.

2. MCU Holder

1x Back_Spool_Holder_Adapter.stl

1x MCU_Holder v2.stl

1x ams_cover.stl (Optional)

Detach the spoolholder from the backside of the printer.
Then take the "Back_Spool_Holder_Adapter.stl" and the "MCU_Holder v2.stl" and screw them together. Now place the mcu over the scre holes of the holder, with the heatset inserts, and screw the SKR Pico onto the holder.
Now place the adapter in the slot thats now free at the back of the printer and slide it down.
Before this step, be sure to power off the printer. Now you just need to open the back plate of the printer, take a usb cable, attach it to the mainboard of the printer, fish it though the vent cut outs and plug it into the SKR Pico.
After that make shure to close everything back up, power on the printer and configure the SKR Pico via ssh [Tutorial](https://www.youtube.com/watch?v=hfD1LAOoBJc).
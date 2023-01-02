# Front Decontaminator
# !!! work in progress !!!

This mod adds a nozzle brush and a purge bucket to Voron 2.4 printer's front side. It is a variation of the famous Decontaminator Purge Bucket & Nozzle Scrubber by edwardyeeks, it does the same thing but on the front.

https://github.com/VoronDesign/VoronUsers/tree/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_&_Nozzle_Scrubber

![complete](https://github.com/Thomas-3D/Front_Decontaminator/blob/main/images/complete.jpg)

The parts don't collide with Nevermore Filter mod.

## But why on the front?
cons: 
- You need to remove your Z-endstop and move the bed to the back, so you need the new TAP toolhead
- bucket is only on one side of the brush
- you can see dirt in the bucket

pro:
- You can see dirt in the bucket
- easier to empty the bucket, no matter where the toolhead is parked

## BOM

**Brush Holder**
Size | Qty
--- | ---
M3x4-16 SHCS | 2
M3x10 SHCS | 2
M3 T-Nut | 2
Ø6x3 Magnet | 2
copper brush | 1

The two screws for the bucket need to be magnetic and can be longer. The screwholes are open on the underside.

## Printed parts

These parts are close to the heated bed, I used ABS with standard Voron settings. This is:
- 0.4mm nozzle
- 0.2mm layer height
- 40% infill
- no supports necessary
- 4 perimeters
- 5 top and bottom layers

The parts are designed for the front-right side. For the left side mirror the parts in your slicer.

## LDO-kit specific parts

LDO ships longer bed spacers with their V2.4 kits, the printed parts need to be higher.


## Changes in printer.cfg

for my(!) 350 build:
- [stepper_y]
- ...
- position_min: -7  # this is where the toolhead touches the front door
- position_endstop: 350
- position_max: 350

[include nozzle_scrub.cfg]
- modify nozzle_scrub macro


## Installation

- make changes to printer.cfg
- loosen bed screws
- home and move printhead to Y=0
- align the front edge of the buildplate with your nozzle
- install magnets to brush holder (if they are loose you can glue them in afterwards through holes in the top)
- cut brush to 40mm and press it in brush holder
- mount brush holder with 2x M3x10 and T-nuts to the side of the bed extrusion
- screw 2x SHCS in the bucket, threads are printed in

![brush_holder](https://github.com/Thomas-3D/Front_Decontaminator/blob/main/images/brush_holder.jpg)

![bucket_underside](https://github.com/Thomas-3D/Front_Decontaminator/blob/main/images/bucket_underside.jpg)

## Testing and feedback

I can only verify the 350mm LDO version works. Please give me feedback if your version works or how it can be improved.

Tag me on Voron Discord: Justheretolookpretty#3570

Have fun!

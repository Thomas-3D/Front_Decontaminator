# Front Decontaminator
# !!! work in progress !!!

This mod adds a nozzle brush and purge bucket to your Voron 2.4 printer's front side. It is a variation of the Decontaminator Purge Bucket & Nozzle Scrubber by edwardyeeks, it does the same thing but on the front.

https://github.com/VoronDesign/VoronUsers/tree/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_&_Nozzle_Scrubber

This mod doesn't collide with Nevermore Filter mod.

## But why on the front?
cons: 
- You need to remove your Z-endstop and move your bed to the back, so you need the new TAP toolhead
- Bucket only on one side of the brush
- You can see dirt in the bucket

pro:
- You can see dirt in the bucket
- Easier to empty the bucket, no matter where the toolhead is parked

## BOM

**Brush Holder**
Size | Qty
--- | ---
M3x10 SHCS | 2
M3 T-Nut | 2
Ø6x3 Magnet | 2
copper brush | 1

**Bucket**
Size | Qty
--- | ---
M3x4-16 SHCS | 2

These two screws need to be magnetic and can be longer. The screwholes are open on the underside.

## Printed parts

These parts are close to the heated bed, so I used ABS with standard Voron PIF settings. This is:
- 0.4mm nozzle
- 0.2mm layer height
- 40% infill
- no supports necessary
- 4 perimeters
- 5 top and bottom layers

The parts are designed for the front-right side. For the left side mirror the parts in your slicer.

## LDO-kit specific parts

LDO ships longer bed spacers with their V2.4 kits, so the printed parts are higher.

## Installation

- make changes to printer.cfg
- loosen bed screws
- home and move printhead to Y=0
- align the front edge of the buildplate with your nozzle
- install magnets to brush holder (if they are loose you can glue the afterward through the hole in the top)
- cut brush to 40mm and press it in the holder
- mount brush holder with 2x M3x10 and T-nuts to the side of the bed extrusion
- screw 2x SHCS in the bucket, threads are printed in


## Changes in printer.cfg

for my 350 build (use at own risk):
- [stepper_y]
- position_min: -7  # this is where the toolhead touches the front door
- position_endstop: 350
- position_max: 350

## Testing and feedback

I can only verify the 350mm LDO version works. Please give me feedback if your version works and how it can be improved.

Discord Justheretolookpretty#3570

# Custom Hardware for Automation
Pozzo Group Custom Automation Hardware. Dimensions are consistent with SLAS standards (slas.org) 

## Purpose
We are creating a place to store and share files for custom hardware and labware created for the laboratory automation including use with Opentrons Pippetting Robot and other tools. 

## Required Components
1. A .stl or 3D print files (if the component can be 3D printed)
2. Expected measurements of the final print
3. Code needed for the addition of the labware into opentrons robot
4. Any special instructions for printing, loading, or using the print

Recommended format is:
```
plate_name = '#####'
if plate_name not in labware.list():
    custom_plate = labware.create(
        #####,                        # name of your labware
        grid=(X, Y),                  # specify amount of (columns, rows)
        spacing=(#, #),               # distances (mm) between each (column, row)
        diameter=#,                   # diameter (mm) of each well on the plate
        depth=#,                      # depth (mm) of each well on the plate
        volume=#)
```
</br>
Using the Opentrons Jupyter notebook, the new plate can be added using 

        custom_container = labware.load('3x6_plate', '1')

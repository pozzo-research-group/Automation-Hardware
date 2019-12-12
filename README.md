# OT2CustomHardware
Pozzo Group OT2 Hardware 

## Purpose
We are creating a place to store and share files for custom hardware and labware created for the Opentrons Pippetting Robot. 

## Required Components
- If the component can be 3D printed, then a .stl or print files
- expected measurements of the final print
- code needed for the addition of the labware into opentrons robot\
Recommended format is:\ 
`plate_name = '3x6_plate'\
if plate_name not in labware.list():\
    custom_plate = labware.create(\
        plate_name,                    # name of you labware\
        grid=(3, 6),                    # specify amount of (columns, rows)\
        spacing=(12, 12),               # distances (mm) between each (column, row)\
        diameter=5,                     # diameter (mm) of each well on the plate\
        depth=10,                       # depth (mm) of each well on the plate\
        volume=200)\
 `\
 which can then be added to the Opentrons Jupyter notebook using `custom_container = labware.load('3x6_plate', '1')`

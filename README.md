# OT2CustomHardware
Pozzo Group OT2 Hardware 

## Purpose
We are creating a place to store and share files for custom hardware and labware created for the Opentrons Pippetting Robot. 

## Required Components
- If the component can be 3D printed, then a .stl or print files
- Expected measurements of the final print
- Code needed for the addition of the labware into opentrons robot\
\
Recommended format is:\ 
`plate_name = '#####'\
if plate_name not in labware.list():\
    custom_plate = labware.create(\
        #####,                    # name of you labware\
        grid=(X, Y),                    # specify amount of (columns, rows)\
        spacing=(#, #),               # distances (mm) between each (column, row)\
        diameter=#,                     # diameter (mm) of each well on the plate\
        depth=#,                       # depth (mm) of each well on the plate\
        volume=#)\
 `\
 Using the Opentrons Jupyter notebook, the new plate can be added using `custom_container = labware.load('3x6_plate', '1')`

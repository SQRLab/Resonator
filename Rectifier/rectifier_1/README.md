# rectifier_1
These are the designs for a half-wave rectifier on a printed circuit board to convert AC to DC power. For simulations of this circuit, navigate to Resonator/Simulation/LTSpice. This design was created in KiCAD, which is a PCB design software that is free to download here (https://www.kicad.org/download/). In order to view this design, clone this repository and double click the .pro file. This will prompt KiCAD to start and provide a directory to all of the design files. 

### gerber_files
This folder contains the plot and drill files to fabricate the printed circuit board. For most fabrication services, you will need to download this folder as a zip file and upload it to the service's website for ordering. Drill and Plot files are the files that describe the different layers of the board, the routing details, and how to cut the board. 

### rectifier_1-backups
Default folder created by KiCAD to store unsaved backups of the design. 

### uw_logo.pretty
This is a footprint library containing UW and SQRL logos drawn in silkscreen. Silkscreen is the layer of paint that is on top of the board. This is mostly for asthetic, so it is not required to properly view or fabricate the design. If you would like to add the uw_logo.pretty library, go to the "Footprint Editor" and go to "File -> Import Footprint". This will prompt you to upload a footprint from this folder. Save the footprint to a new footprint library or one of the many available ones. Then in the PCB editor, you will be able to "Add Footprint" on the right side-bar and place the footprint on your printed circuit board.  

### rectifier_1.kicad_pcb
This is the pcb file where components are placed and routed. 

### rectifier_1.kicad_pro
This is the main project file containing a directory to all design files and tools in KiCAD.

### rectifier_1.kicad_sch
This is the schematic file containing the circuit diagram and component symbols. 


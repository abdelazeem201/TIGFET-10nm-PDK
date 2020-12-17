## TIGFET10nm Open Source Predictive Process Design Kit v1.0  [MIT License]

Copyright (c) [2019] [Laboratory for NanoIntegrated Systems]

This is a physical design kit for TIGFET 10nm Silicon Nanowire Device. The design kit is derived using TCAD based device simulations and realistic assumptions made for largescale
production of TIGFET-based systems.

This kit consists of a SPICE model
and full custom physical design files including a Design Rule
Manual, a Design Rule Check, and a Layout Versus Schematic
decks for Calibre®. The repository also hosts implementation of basic logic gates and Full Adder design using TIGFET devices

### TIGFET10nm PDK Directory Structure

* calibre/ -> SVRF rules for Mentor Graphics Calibre
* cdslib/  -> Technology libraires for Cadence Virtuoso
* hspice/  -> Simulation models for Synopsys HSPICE
* docs/    -> Documentation

For more detail about the key assumptions made while designing this PDK, please refer following publication.

[*Ganesh Gore, Patsy Cadareanu, Edouard Giacomin, and Pierre-Emmanuel Gaillardon "A Predictive Process Design Kit for Three-Independent-Gate Field-Effect Transistors", 2019 IFIP/IEEE 27th International Conference on Very Large Scale Integration (VLSI-SoC), 6-9 October 2019.*](https://ieeexplore.ieee.org/abstract/document/8920358/)

### Design Kit Installation and Usage
  1) Set the variable PDK_DIR to where the PDK folder is.
  setenv PDK_DIR "../TIGFET-10nm-PDK" (for a csh/tcsh shell)
		 
  2) Change to the directory where you want to start Virtuoso and do:
     source $PDK_DIR/cdslib/setup/setup.csh
     Note that this script copies all of the required user files (.cdsinit,
     cds.lib, and Calibre runset files) to the current working directory
     if they do not already exist.

  3) In the current directory, edit the PDK_DIR variable in the launch_tigfet10nm.sh script to point to where PDK folder is located (as in step 1). 
	
  4) Source your setup scripts for Cadence Virtuoso, Mentor Graphics Calibre, and Synopsys HSPICE and launch Cadence Virtuoso using the script *launch_tigfet10nm.sh*

  ```bash
   cd <Directory_directory>
   source $PDK_DIR/cdslib/setup/setup.csh
   source launch_tigfet10nm.sh
   ```

> In case of any doubts/questions/suggestions, please raise issue on GitHub or send email to pierre-emmanuel.gaillardon@utah.edu or ganesh.gore@utah.edu.

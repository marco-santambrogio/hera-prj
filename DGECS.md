# DGECS #
This wiki page illustrates how to use the DGECS tool (currently supporting combinatorial 8bit or 32bit circuits evolved over the Xilinx Virtex-4 XC4VFX12 FPGA).
This page provides brief and schematic information; more details will be soon provided as a scientific paper (under review at [RAW2012](http://www.ece.lsu.edu/vaidy/raw/)) or a technical report.

## Python Sources ##
DGECS is a tool for exporting hardware circuits evolved with HERA to a generic vhdl description, which may be included in any custom design. The python sources may be found in the [HERA git repository](http://code.google.com/p/hera-prj/source/browse/#git%2Fsrc%2Fdgecs) under the folder src/dgecs. The tool has a PyQt gui, which can be launched simply by running, under the src/dgecs directory:

$ ./dgecs.py

The gui should be quite intuitivei. The tool allows to define the contents of the LUTs constituting the individual (refer to the [HERA publications](http://code.google.com/p/hera-prj/wiki/Publications) for details regarding how the individuals are composed); this can be done by hand or by loading the values from a file. This file can be created by copying and pasting the LUTs contents provided in the output of the evolution process. The tools then allows to generate a vhdl description of the individual and to save it to a new folder of choice.

## Reference component ##
To synthesize the component for using it in a Xilinx-based design, a reference component is provided under the [Downloads page](http://code.google.com/p/hera-prj/downloads/list). Currently, at least the following reference components are provided:
  * [dgecs\_component\_8bit.tar.bz2](http://code.google.com/p/hera-prj/downloads/detail?name=dgecs_component_8bit.tar.bz2&can=2&q=) -> for synthesising 8bit exported circuits
To use the reference components, just substitute the vhdl files with the ones generated by DGECS and use a suitable tool (e.g., Xilinx ISE) to synthesize the component. The archive also provides the device drivers.
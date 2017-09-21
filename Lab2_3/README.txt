Instructions for loading the required software modules for TSEA26.

LINUX MINT SYSTEMS:
> module add /site/edu/mintmodules/kurs/TSEA26 # All software except MATLAB
> module add prog/matlab/9.0                   # MATLAB

CENTOS SYSTEMS:
> module add TSEA26                            # TSEA26 sim/asm tools
> module add mentor                            # ModelSim and HDL compilers
> module add synopsys/dc2014.09                # Design Compiler
 (Matlab is available without module load on CentOS)
A small change is needed to the file util/dc_synthesize.tcl to run
datapath synthesis on CentOS. Check that file for more details.

Detailed notes:
* Design compiler MUST be run in 64-bit mode on Linux Mint as of
2016-09-20. This is handled by the -64 flag in the Makefile.


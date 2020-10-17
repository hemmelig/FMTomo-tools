# Setting up for an FMTomo run
The FMTomo documentation covers all aspects of the package, including descriptions of all the required input files and their formats. It should always be used as a first point of reference.

General process
===============
1. Create a new run directory by making a copy of the base run directory and giving it a name
2. Create the input pick files and a station file using the ``obspy2fmtomo`` notebook
3. Create a starting (1-D) velocity model - make a copy of the ``ak135.vel`` file and add any local layers.
4. Set up the propagation and inversion grids by editing the ``grid3dg.in`` file.
5. Specify the input source, receiver, pick files in the ``obsdata.in`` file.

Input files
===========
The input files are fairly self-explanatory, but here are some short notes:

`frechgen.in` - controls inversion of subsets of, e.g., source locations, or velocity layers.

`mode_set.in` - controls general run parameters. Each option is described in detail in the default file.

`residuals.in` - just points at data files. Don't change.

`scorrect.in` - points to input files required for source corrections.

`tomo3d.in` - controls inversion. Each option is described in detail in the default file.

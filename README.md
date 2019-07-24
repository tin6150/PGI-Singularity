# PGI-Singularity
Contains:
Portland Group(PGI) compilers, NetCDF libraries for C and Fortran




to create binaries that can be run from the host without explicity calling singularity:

creating binaries
./createlinks ./cmaq.img 
		// need at least pgf90 for cmaq

Note that resulting binary need pgi library inside the container, so may want to use 
-Bstatic_pgi 




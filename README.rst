PGI-Singularity
===============

Contains:
Portland Group(PGI) compilers, NetCDF libraries for C and Fortran




to create binaries that can be run from the host without explicity calling singularity:

creating binaries
./createlinks ./cmaq.img 
		// need at least pgf90 for cmaq

Note that resulting binary need pgi library inside the container, so may want to use 
-Bstatic_pgi 


TMP
===


libnetcdff


/Downloads/netcdf-c-4.7.0/docs/old/netcdf-f90.texi

Starting with version 3.6.2, another method of building the netCDF
Fortran libraries becomes available. With the
--enable-separate-fortran option to configure, the user can specify
that the C library should not contain the Fortran functions. In these
cases an additional library, libnetcdff.a (note the extra ''f'') will
be built. This library contains the Fortran functions.   



DOCKER
======

if decide to build docker container first, this is a good reference:
https://hub.docker.com/r/johntfoster/netcdf/dockerfile

the layer approach would safe time in build time during dev cycles.
also it should allow for binary name of container or alias to execute exactly one of pgc++, pgf90, etc.
skirting the singularity problem.


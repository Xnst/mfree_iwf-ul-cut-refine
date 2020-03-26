
# The files and what they do:

## root-dir directories

- **Debug/** : think it is the debug directory. Som quick runs
- **doc/** : This document
- **img/** : images for the README-file
- **Release/** : where the final executable will be created. cd here
and run make to have the executable file. When run a new directory is
created for the result files.
- **src/** : The source code.

## Release/

To make an executable (default *refine_paper*) run 

    make all

and all will happen. 

To clean up write

    make clean

- makefile : mothership of all makefiles. Where the name of the
  executable is set 
- objects.mk
- sources.mk
- src/subdir.mk
- src/benchmark/subdir.mk

.mk = all additional makefiles

## src/

Nearly all source code files comes in a pair: *.cpp* and *.h*.
- *.cpp* : source code in c++
- *.h* : "help"-file with declarations.

### refine_cut_main

The **main** function. Here the test are chosen. The test cases can be
viewed in the paper this code is written for.

### benchmarks/

directory with the benchmark test setups:

- test_benches
- test_cuttings
- test_density
- material_library


### simulation_data

Go to place for structure of all simulation data. physical constants
and stuff.


### material

gives you the:

- EOS
- Jaumann stress rate tensor

### plasticity

Hard loads johnson_cook_sima_2010 

Based on a radial return calculates

- Checks if in elastic domain
- new Yield stress
	- updates plastic strain levels in the particle points too
- increase in temperature
	- updates the temperature in the particle points too


### johnson_cook_Sima_2010

The yield model Johnson-Cook modified by Sima to cope with strain
softening at some temperatures. Typical behaviour for Ti-alloys.

### adaptivity

### body

### contact

### cont_mech

### correctors

### derivatives

### grid

### kernel

### leap_frog

### logger

### particle

### precomp_shape_functions

### simulation_time

### solver

### thermal

### tool

### vtk_writer


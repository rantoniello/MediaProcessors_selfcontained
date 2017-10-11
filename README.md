# MediaProcessors_selfcontained
This is just a self-contained wrapper provided to facilitate the compilation and  installation of the MediaProcessors project.  It provides all the dependencies and a simple makefile to be able to build/clean  in one step.

*INSTRUCTIONS*

Recursively clone this repository to obtain full source of submodules:

> $ git clone --recursive https://github.com/rantoniello/MediaProcessors_selfcontained.git

Change to the just cloned directory:

> $ cd MediaProcessors_selfcontained

Type 'make' to build and install all the 3rd-party dependencies and also the MediaProcessors's libs.

> $ make

It will take several minutes to compile and install all.

The installation will take place on-site, namely, inside <...>/MediaProcessors_selfcontained/ folder.
The concrete path is:

> <..>/MediaProcessors_selfcontained/_install_dir_x86/

**No** file will be installed outside this folder on your file-system.

To clean all:

> $ make clean

if you want to compile a particular library, for example the 'utils' library of MediaProcessors submodule, type:

> $ make x86_utils

To clean that library:

> $ make x86_utils_clean

Note that we just use [ARCHITECTURE_(e.g. 'x86_')][name-of-library(e.g. 'utils')] [_clean(only add this suffix to clean)]; 
we do not need to use the path.

Other examples to build/clean particular libs.:

> $ make x86_procs\
> $ make x86_procs_clean\
> $ make x86_codecs\
> $ make x86_codecs_clean\
> ...

Application examples source codes are available at

> <..>/MediaProcessors_selfcontained/MediaProcessors/examples/

Each example is compiled automatically and the corresponding binary is installed at

> <...>/MediaProcessors_selfcontained/_install_dir_x86/bin

To run, let's say, the 'codecs_muxers_loopback' example, just type:

> LD_LIBRARY_PATH=<...>/MediaProcessors_selfcontained/_install_dir_x86/lib <...>/MediaProcessors_selfcontained/_install_dir_x86/bin/mediaprocs_codecs_muxers_loopback

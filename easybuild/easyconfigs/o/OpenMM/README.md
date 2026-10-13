# OpenMM

-   [OpenMM Website](https://openmm.org/)

## General information

OpenMM is a high-performance toolkit for molecular simulation. You can use it as
an application, a library, or a flexible programming environment. It include 
extensive language bindings for Python, C, C++, and Fortran.

In the early days of LUMI, we used native installs on LUMI, combining with Cray Python.
As it turned out that installing Python software uncontainerized on the Lustre filesystem
puts too much stress on the filesystem and can also drastically reduce the performance of 
the software, we stopped offering those recipes (the 7.5.1 recipes below).

We currently offer a recipe based on [`lumi-container-wrapper`](../../l/lumi-container-wrapper/index.md)
and Conda in a recipe that is very easy to adapt to different versions of OpenMM and Python, but does not
offer complete reproducibility as only the versions of these packages are specified. The EasyConfig is
very easy to customise.


## EasyBuild

-   [OpenMM in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/o/OpenMM)


### Version 7.5.1 for CPE GNU 21.08

-   The EasyConfig is derived from the EasyBuilders one
-   Include a patch to fix problem when building with Doxygen 1.9 used in 
    `buildtools`


### Version 7.5.1 for CPE Cray 21.08

One of the test fail (segfault), be aware of it if you are using this version.

-   The EasyConfig is derived from the EasyBuilders one
-   Include a patch to fix problem when building with Doxygen 1.9 used in 
    `buildtools`


### Version 8.6.0 with lumi-container-wrapper

-   EasyConfig is a LUST-development. The installation is done using a Bundle EasyConfig and
    `post_install_cmds` as we needed a generic EasyBlock that can work without sources.
    We wanted to avoid developing an EasyBlock specifically for installations with lumi-container-wrapper.

-   The EasyConfig can easily be used as a template to play around with other versions of OpenMM and
    Python. It is also easy to extend the installation with other packages as the definition file
    for lumi-container-wrapper is also generated in the EasyConfig, so it is a single file solution.

-   The resulting module offers the same functionality as the (undocumented ) CSC `openmm` modules.


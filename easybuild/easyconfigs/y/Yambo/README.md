# Yambo technical information

-   [Yambo web site](http://www.yambo-code.org)

-   [Yambo on GitHub](https://github.com/yambo-code/yambo)

    -   [GitHub releases](https://github.com/yambo-code/yambo/releases)
    
    -   [GitHub tags for subreleases](https://github.com/yambo-code/yambo/tags)


## General notes

-   Yambo likes to install missing dependencies itself and will download them automatically.
    This does not always work. We've seen cases where the configuration that Yambo tried on 
    LUMI did not build.

    To find out what versions of dependencies Yambo prefers, go into the source distribution
    and check `lib/archive/package.list`. Newer versions do not always work and errors can
    also be linking errors, not just runtime errors.


## EasyBuild

-   [Support for Yambo in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/y/Yambo)

-   [Support for Yambo in the CSCS repository](https://github.com/eth-cscs/production/tree/master/easybuild/easyconfigs/y/Yambo)

-   [Spack support for Yambo](https://packages.spack.io/package.html?name=yambo)


### 5.2.3 for CPE 23.09 and 24.03, CPU-only

-   The EasyConfig is mostly a LUST development.


### 5.2.4 for CPE 25.03, CPU-only

-   The EasyConfig is a trivial port of the 5.2.3 EasyConfig in 24.03

-   Yambo 5.3.0 was available at that time, but not supported in either Spack or EasyBuild,
    and there were issues with the installation of the internal DeviceXlib, which was not
    properly compiled, so we cannot offer this version at the moment.
    
    Yambo 5.3.0 is also the first version using this library, so it comes as no surprise 
    that we didn't see similar issues in previous versions of Yambo.


### 5.3.0-cpeGNU-25.03-SLEPc-double, CPU-only and 5.3.0-cpeGNU-26.03-SLEPc-double, CPU-only

-   The EasyConfig builds on the EasyConfig for 5.2.4 in 25.03 and combines with the configuration
    used for 5.3.0 with SLEPc in the foss toolchains in the EasyBuilders repository (as the latter
    was co-developed by the Yambo developers and hence is likely OK).

-   Used bug fix releases of the same PETSc and SLEPc release for 26.03 and switched to EB6-compatible
    parameters.


### 5.3.0-cpeGNU-26.03, CPU-only

-   Derived from 5.3.0-cpeGNU-26.03-SLEPc-double and Yambo-5.3.0-foss-2024a.eb, so hopefully OK as
    these were co-developed with the developers.

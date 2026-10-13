# Voro++ technical information

Voro++ hasn't had an official release since 2013 We cannot guarantee
compatibility with future compiler versions. There is some activity though
on GitHub but without true new releases.

-   [Voro++ webs site](https://math.lbl.gov/voro++/)

    -   [Downloads from the Voro++ web site](https://math.lbl.gov/voro++/download/)

-   [Voro++ on GitHub](https://github.com/chr1shr/voro)


## EasyBuild

-   [Voro++ support in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/v/Voro%2B%2B)

-   [voropp package in Spack](https://packages.spack.io/package.html?name=voropp)

    Spack also contains a patch that adds support for CMake and also supports installing
    from the current GitHub master.


### Version 0.4.6 for 26.03 and later

-   The EasyConfig is derived from the EasyBuilders one.

Should a shared library be needed, one way is to use the Spack CMake patch and build with
CMake instead. The newer GitHub commits also include CMake support by default.

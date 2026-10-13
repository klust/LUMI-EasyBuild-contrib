 mctc-lib information


-   [mctc-lib](https://grimme-lab.github.io/mctc-lib/)

-   [mctc-lib on GitHub](https://github.com/grimme-lab/mctc-lib)

    -   [GitHub releases](https://github.com/grimme-lab/mctc-lib/releases)


## EasyBuild

-   [Support in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/m/mctc-lib)

-   [Spack package mctc-lib](https://packages.spack.io/package.html?name=mctc-lib)


### Version 0.5.0 for 25.03

-   The EasyConfig is based on the one from the EasyBuilders, but adapted to the LUMI
    toolchains.


### Version 0.5.2 for 26.03

-   The EasyConfig is a straightforward port of the one for 0.5.0 in 25.03, but we switched
    to EB6-compatible parameters and implemented more robust sanity checks.

-   NOTE: We tried a cpeCray version, but that one fails in one test in the test step, so
    the EasyConfig was not yet added. Substitute `cpeGNU` for `cpeCray` and build with
    `--skip-test-step` or `--ignore-test-failure` if you want to try anyway.

About airss-feedstock
=====================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/airss-feedstock/blob/main/LICENSE.txt)

Home: https://www.mtg.msm.cam.ac.uk/Codes/AIRSS

Package license: GPL-2.0-only

Summary: Ab initio Random Structure Searching (AIRSS) is a very simple, yet powerful and highly parallel, approach to structure prediction.

Documentation: https://airss-docs.github.io/

Current build status
====================


<table>
    
  <tr>
    <td>Azure</td>
    <td>
      <details>
        <summary>
          <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=18811&branchName=main">
            <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airss-feedstock?branchName=main">
          </a>
        </summary>
        <table>
          <thead><tr><th>Variant</th><th>Status</th></tr></thead>
          <tbody><tr>
              <td>linux_64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=18811&branchName=main">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airss-feedstock?branchName=main&jobName=linux&configuration=linux%20linux_64_" alt="variant">
                </a>
              </td>
            </tr>
          </tbody>
        </table>
      </details>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-airss-green.svg)](https://anaconda.org/conda-forge/airss) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/airss.svg)](https://anaconda.org/conda-forge/airss) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/airss.svg)](https://anaconda.org/conda-forge/airss) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/airss.svg)](https://anaconda.org/conda-forge/airss) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-airss--with--default--names-green.svg)](https://anaconda.org/conda-forge/airss-with-default-names) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/airss-with-default-names.svg)](https://anaconda.org/conda-forge/airss-with-default-names) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/airss-with-default-names.svg)](https://anaconda.org/conda-forge/airss-with-default-names) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/airss-with-default-names.svg)](https://anaconda.org/conda-forge/airss-with-default-names) |

Installing airss
================

Installing `airss` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Once the `conda-forge` channel has been enabled, `airss, airss-with-default-names` can be installed with `conda`:

```
conda install airss airss-with-default-names
```

or with `mamba`:

```
mamba install airss airss-with-default-names
```

It is possible to list all of the versions of `airss` available on your platform with `conda`:

```
conda search airss --channel conda-forge
```

or with `mamba`:

```
mamba search airss --channel conda-forge
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search airss --channel conda-forge

# List packages depending on `airss`:
mamba repoquery whoneeds airss --channel conda-forge

# List dependencies of `airss`:
mamba repoquery depends airss --channel conda-forge
```

Difference between `airss` and `airss-with-default-names`
=========================================================

The AIRSS package is consisted of many small binaries and scripts.
Installing all of them in `bin` folder of the environment may not be ideal and is likely to cause conflicts with other packages. 

Hence, in the default package `airss`, only the following tools are exposed:
```
airss.pl
buildcell
cabal
crud.pl
cryan
gencell
rescat
respack
resplit
```

Nevertheless, all of the executables can still be accessed with the `airss` executable acting as the main entry point.

For example,  `airss castep_relax` runs the `castep_relax` script.

On the other hand, the `airss-with-default-names` installs all tools in the environment.

About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/), [GitHub](https://github.com/),
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/),
[Drone](https://cloud.drone.io/welcome), and [TravisCI](https://travis-ci.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [Anaconda-Cloud](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating airss-feedstock
========================

If you would like to improve the airss recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/airss-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@awvwgk](https://github.com/awvwgk/)



Purpose of the fork is to try out improving performance and adapt the api to something I easier to use. 

This will come with a lot of loss of functionality as what is kept is a reflection of what I want.

Also abandons backwards compability for py <3.10 

Main/dev:
[![Documentation Status](https://readthedocs.org/projects/pynastran-git/badge/?version=1.4)](http://pynastran-git.readthedocs.io/en/latest/?badge=latest)
[![Linux Status](https://github.com/SteveDoyle2/pyNastran/workflows/CI/badge.svg)](https://github.com/SteveDoyle2/pyNastran/actions?query=workflow%3ACI+branch%3Amaster)
[![Coverage Status](https://codecov.io/gh/SteveDoyle2/pyNastran/branch/main/graph/badge.svg)](https://codecov.io/gh/SteveDoyle2/pyNastran)

Also, check out the:
  * [![PyPi Version](https://img.shields.io/pypi/v/pynastran.svg)](https://pypi.python.org/pypi/pyNastran)
  * [Discussion forum](http://groups.google.com/group/pynastran-discuss) (intended for questions about the latest release)
  * [Developer forum](http://groups.google.com/group/pynastran-dev) (intended for questions about the main branch)
  * [Docs](https://pynastran-git.readthedocs.io/en/1.4/)
  * [Code of Conduct](https://github.com/SteveDoyle2/pyNastran/blob/main/code_of_conduct.md)
  * [Contributing](https://github.com/SteveDoyle2/pyNastran/blob/main/contributing.rst)

for more detailed information.

### Blogs
  * [Flutter Analysis in pyNastran](https://www.m4-engineering.com/flutter-analysis-with-pynastran/)


### Code of Conduct

Everyone interacting in the setuptools project’s codebase, issue trackers, chat room/Discord, and mailing lists is expected to follow the [Code of Conduct](https://github.com/SteveDoyle2/pyNastran/blob/main/code_of_conduct.md).


# Overview

pyNastran is an interface library to the various Nastran file formats (BDF, OP2, OP4).
Using the BDF interface, you can read/edit/write Nastran geometry without worrying about
field formatting.  Many checks are also performed to verify that your model is correct.
Using the OP2 interface, you can read large result files quickly and efficiently.
Additionally, you can also extract a subset of the result data and write OP2/F06 result
files.  For a more detailed list of features, see:
  * [Features](https://pynastran-git.readthedocs.io/en/1.4/quick_start/features.html#overview)

# News

<!---

I yet again went down a bit of rabbit hole to improve the speed of the BDF, 
but this time I'm much happier with the results.  Still, getting back to parity
takes a lot of time and it's not quite there.  It does simplify MSC HDF5 
integration, so once I've added methods for updating more complicated objects
(e.g., PBARL, PCOMP, RBE3), HDF5 will be next. If you want to test it out, 
it's not included with the official release, but is found in 
``pyNastran.dev.bdf_vectorized3``, so not my first attempt :)

This should be hidden...

### v1.5.0  has NOT been released (2024/3/25)

BDF:
 - removed axisymmetric cards deprecated in NX (AXIC, AXIF, CCONEAX, PCONEAX, PRESAX, TEMPAX, ...)
 - added ```bdf run_jobs filename dirname --test```
 - added 
F06:
 - added gui for flutter post-processing
OP2:
 - added NX trim/flutter tables
 - added kinetic energy
--->
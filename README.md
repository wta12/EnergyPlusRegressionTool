EnergyPlus Regressions
======================

[![Documentation Status](https://readthedocs.org/projects/energyplusregressiontool/badge/?version=latest)](https://energyplusregressiontool.readthedocs.io/en/latest/?badge=latest)
[![Build Status](https://travis-ci.org/Myoldmopar/EnergyPlusRegressionTool.svg?branch=master)](https://travis-ci.org/Myoldmopar/EnergyPlusRegressionTool)

Overview
--------

This library is provides tools for performing regressions between EnergyPlus builds.
Developers often propose changes to EnergyPlus for:

 - New feature development
 - Defect repair
 - Refactoring for structure or performance
 - Etc.

When a developer proposes these changes, they must be tested.
The continuous integration system over on EnergyPlus handles this, and provides results, but there can be a long time delay waiting on those results, depending on how busy CI is at that moment.
This tool provides a way to run these regressions locally.
In addition, because this tool isn't intermingled with the CI structure, enhancements to the regression analysis can be added quickly to this tool to provide developers with more information.
These can be rolled upstream into the CI code, but must be done with much more care to avoid breaking CI.

Platform Support
----------------

This tool is written to be functional on all three major platforms, but Windows and Mac have known issues.
On Windows the multiprocessing code does not work, causing the runs to be executed serially, which means a long testing time.
On Mac the results tab is currently not showing the results files, making it fairly useless, at least until I write the results to file, in which case they _could_ be processed externally.

In general, this tool works amazingly well on Ubuntu 18.04.
And it is super easy to set up an EnergyPlus build development environment on Ubuntu.
So if at all possible, use this platform, in a VM or whatever, to use this tool.
I'll keep pushing on the tool on all these platforms, but my focus will always be on Ubuntu for the time being.

Usage/Installation
------------------

For setting up a development environment to actually _work_ on this tool, see the next section.
If you are not interested in _developing_ this tool, and only looking to _use_ it for your EnergyPlus work, read on here.

For this case, the dependencies for this tool are typically installed into the _system_ Python 3 installation, and this _system_ Python 3 is used to execute the program.
Instructions for this are coming:

- Here
- and here.

Development
-----------

For the case of developing this tool, the instructions are fairly similar, but you will generally set up a separate Python environment to install the dependencies so you don't mess with the _system_ Python.
Instructions for this are coming:

- Here
- and here.

Documentation
-------------

Further program documentation, including user guide and typical workflows, are available in the documentation.
This documentation is written using RST with Sphinx, and published on [ReadTheDocs](https://energyplusregressiontool.readthedocs.io/en/latest/).

Testing
-------

Very little automated testing has been done, but will be added, to ensure it runs properly.
Meaningless as they are, the existing "unit tests" are run by [Travis](https://travis-ci.org/Myoldmopar/EnergyPlusRegressionTool).

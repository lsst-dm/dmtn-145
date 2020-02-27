.. image:: https://img.shields.io/badge/dmtn--145-lsst.io-brightgreen.svg
   :target: https://dmtn-145.lsst.io
.. image:: https://travis-ci.com/lsst-dm/dmtn-145.svg
   :target: https://travis-ci.com/lsst-dm/dmtn-145

#############################################
Bringing Rubin Observatory software together 
#############################################

DMTN-145
========

In the last two years the software landscape on Rubin Observatory construction project  has changed dramatically. We are transitioning from siloed software teams to a  more integrated approach. LSST has Labview, C++, Python and Java components which use a variety of build systems and have uneven test harnesses. As we approach deployment on the mountain we would like to converge on build and versioning for all systems. In addition we intend to use  a Foreman, Puppet and Kubernetes based deployment system.   In this talk we will outline the vision for software build and deployment across all Rubin Observatory subsystems and where we currently are with it. 

Links
=====

- Live drafts: https://dmtn-145.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-145

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-145

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf

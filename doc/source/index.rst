.. PySpotCam documentation master file, created by
   sphinx-quickstart on Thu Aug 30 16:48:34 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

=====================================
Welcome to PySpotCam's documentation!
=====================================

This module provides a Python interface to the SpotCam driver from `SPOT Imaging Solutions`_

Installation
============

You need to install the driver from `SPOT Imaging Solutions`_.

To install PySpotCam, download the `package`_ and run the command 

.. code-block:: sh

   python setup.py install

You can also directly **move** the :file:`PySpotCam` directory to a location
that Python can import from (directory in which scripts 
using :mod:`PySpotCam` are run, etc.)

Usage
=====

Here is a small example ::

    from PySpotCam.spot import SpotClass

    Spot = SpotClass()

    Spot.BitDepth = max(Spot.BitDepths) # Set the BitDepth to the max value
    Spot.ExternalTriggerMode = 1
    Spot.SetExposure(gain=1, time=2)

    image = Spot.GetImage()

    print Spot.VersionInfo2

Almost all the functions described in the SPOTCam API are implemented. See the :doc:`description` part.

Contact
=======

Please send bug reports or feedback to `Pierre Cladé`_.


Contents:
=========

.. toctree::
   :maxdepth: 2

   Description of the PySpotCam functions <description>

.. _SPOT Imaging Solutions: http://www.spotimaging.com/
.. _package: http://pypi.python.org/pypi/PySpotCam/
.. _Pierre Cladé: mailto:pierre.clade@spectro.jussieu.fr


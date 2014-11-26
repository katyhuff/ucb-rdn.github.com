MocDown 
=======

**Primary Developer:**  jeffseif_Website

**Source Code:** MocDown_Source_

**Source Website:** MocDown_Website_

Description
***********

MocDown is an efficient tool which loosely couples simulations for neutron
transport, isotopic transmutation, thermo-fluids, and the equilibrium core
composition search within advanced nuclear reactor cores.  The development of
MocDown focused on facilitating both fast runtime (by employing concurrent
threading and efficient regex parsing when possible) and fast post-processing
(with simple and consistent hierarchical storage of result files).  MocDown
also employs object-oriented programming in Python 3 for flexible modification
with external libraries.

|
|
|
|

.. figure:: mocdown_coupling.png
   :width: 700px
   :scale: 50 %
   :alt: Three coupled models in MocDown

   Figure 1: MocDown couples three models for self-consistent simulations: 
   thermo-fluids, neutron transport, and transmutation and recycling.

|
|
|
|

.. figure:: mocdown_accel.png
   :width: 700px
   :scale: 50 %
   :alt: Acceleration scheme, equilibrium cycle

   Figure 2: The MocDown accelerated recycling scheme efficiently finds the 
   equilibrium cycle, whose isotopic composition matches that of its successor.

|
|
|
|


.. figure:: mocdown_rbwrth.png
   :width: 700px
   :scale: 50 %
   :alt: RBWR-Th core

   Figure 3: The RBWR-Th is a fuel-self-sustaining nuclear reactor core design 
   which operates with only thorium as its charge.  MocDown has been 
   successfully used to simulate this design.


.. _jeffseif_Website: https://jeffseif.github.com/
.. _MocDown_Source: https://github.com/jeffseif/MocDown
.. _MocDown_Website: https://jeffseif.github.com/MocDown

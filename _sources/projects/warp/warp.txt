WARP
====

**Primary Developer:**  :doc:`../../people/bergmann_ryan`

**Source Code:** not currently available online. 

Description
***********

WARP (Weaving All the Random Particles, also a nod to NVIDIA’s vocabulary on GPU 
execution), is a continuous-energy, general 3D monte carlo neutron transport 
code that runs on NVIDIA GPUs.  Supercomputing is moving towards more 
energy-efficient hardware, like GPUs, and their programming/execution models 
require CPU-optimized algorithms to be retooled in order to take full advantage 
of the cards' substantial processing power.  WARP aims to be the first step in 
developing a full-featured, general purpose reactor simulation tool for GPUs.  
It is still in an early development phase, and has only been tested in simple 
geometries and materials.  

Speedup over Serpent 2.1.15 is about 1:1 on a Macbook 
Pro (NVIDIA Geforce GT 630M / 2.6GHz Intel i7) and about 3:1 on the cluster 
(NVIDIA Tesla C2075 / 2.0GHz AMD Opteron 6128) *at the moment* - memory 
optimizations and overhead pruning still needs to be done.  PyNE is used to read 
in ACE-formatted cross sections, which are then passed to CUDA C/C++ via an 
embedded python interpreter.


|

.. figure:: warp_geom.png
   :width: 700px
   :scale: 50 %
   :alt: A reactor geometry that WARP is capable of representing.

   Figure 1: WARP is capable of representing simple materials and 3D reactor 
   geometries.

|

   .. image:: warp_serp_u235_spectra.png
      :height: 210px
   .. image:: warp_serp_homogenized_fuel_spectra.png
      :height: 210px

   Figure 2: WARP results compare very well to the results in Serpent for a 
   block of uranium-235 and a block of homogenized fuel. 

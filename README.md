# splotch_gizmo

My modification of the SPLOTCH visualization program for GIZMO simulations. For 
an example look in parameterfiles/demo_cosmo_bak.par.  There you will need to edit:

---
infile=/full/path/to/snapshot_

fidx=80

simtype=8

---

*infile* only requires the full path and snapshot format, not the number or extension.

*fidx* is the snapshot number, assumed to be in padded (e.g. "000") format.

*simtype=8* is GIZMO HDF5.

Copied below is the README downloaded with the package.

#                         Splotch                  

  Authors of Splotch:

    Martin Reinecke:  martin@mpa-garching.mpg.de

    Klaus Dolag:      kdolag@mpa-garching.mpg.de

    Claudio Gheller:  cgheller@cscs.ch

    Marzia Rivi:      m.rivi@ucl.ac.uk

    Timothy Dykes:    timothy.dykes@myport.ac.uk

    Mel Krokos:       mel.krokos@port.ac.uk

Splotch is written in the C++ language. To install it you have just to
1) unpack the tar.gz
2) Edit the Makefile
3) "make"

Please Check your compiler for the OpenMP flags if you want to use
OpenMP functionality (-fopenmp for g++).

If you have an MPI environment installed, you can also enable
the USE_MPI option.

To run it on your simulations, have a look into the demo.par
file and set the parameters you prefer.

If you want to visualize simulations created by the Gadget code
(http://www.mpa-garching.mpg.de/~volker/gadget/index.html),
you will have to set the Gadget parameter SnapFormat = 2.
Endian conversion will be performed if requested in the Splotch parameter file.


# Copyrights and Acknowledgements

Splotch is free software, distributed under the GNU General Public License.
This implies that you may freely distribute and copy the software.
You may also modify it as you wish, and distribute these modified
versions as long as you indicate prominently any changes you made in the
original code, and as long as you leave the copyright notices, and
the no-warranty notice intact. Please read the General Public License
for more details. Note that the authors retain their copyright on the code.

Splotch uses parts of the Ray++ ray tracing library, which is distributed
under the GNU Library (or Lesser) General Public License.

#Requested Acknowledgement

The authors kindly ask you to acknowledge the use of the Splotch package
in your publications in the following form:

At the first image produced with Splotch, a footnote placed in the main
body of the paper referring to the Splotch web site - currently
http://www.mpa-garching.mpg.de/~kdolag/Splotch
Please also refere to the paper
K. Dolag, M. Reinecke, C. Gheller and S. Imboden:
"Splotch:  Visualizing Cosmological Simulations",
NJP, Volume 10, Issue 12, pp. 125006 (2008)

.. role:: underlined
   :class: underlined

**************************
:underlined:`Introduction`
**************************

.. _library-about:

``pySYD`` is an open-source asteroseismology package that adapts the same well-tested methodology 
from the well-known and widely-used `IDL`-based ``SYD`` pipeline. In addition to not needing a license
to perform rigorous asteroseismic analyses, we have expanded the capabilities and features to
include:

 - automated background model comparison and selection
 - parallel processing and other easy compatabilities for running many stars
 - easily customizable with command-line friendly interface
 - modular and adaptable across different applications
 - saves reproducible samples for future analyses (i.e. seeds)


-----

.. _library-about-benchmark:

Reproducible *Kepler* mision results
#####################################

In order to ensure the reproducibility of scientific results from the *Kepler* mission, we
ran ``pySYD`` on ~100 *Kepler* legacy stars (defined :term:`here <Kepler legacy sample>`) 
observed in short-cadence and compared the output to ``SYD`` results from [S2017a]_. 
The same time series and power spectra were used for both analyses, which are publicly available
and hosted online c/o KASOC [#]_. 

The resulting values are compared for the two methods below for :term:`numax` (:math:`\rm \nu_{max}`, 
left) and :term:`dnu` (:math:`\Delta\nu`, right). 

.. image:: ../_static/comparison.png
  :width: 680
  :alt: Comparison of the `pySYD` and `SYD` pipelines

The residuals show no strong systematics to within <0.5% in Dnu and <~1% in numax, which 
is smaller than the typical random uncertainties. This confirms that the open-source `Python` 
package ``pySYD`` provides consistent results with the legacy IDL version that has been 
used extensively in the literature.

.. TODO:: Add script or jupyter notebook to reproduce this figure.

-----

.. _library-about-related:

Related Tools
#############

``pySYD`` provides general purpose tools for performing asteroseismic analysis in the frequency domain.
Several tools have been developed to solve related scientific and data analysis problems. We have compiled 
a list of software packages that perform similar or complementary analyses.

 * ``AMP``:
    - language: 
    - reference:
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``A2Z``: determining global parameters of the oscillations of solar-like stars
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2010A%26A...511A..46M>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``Background``: an extension of ``DIAMONDS`` that fits the background signal of solar-like oscillators 
    - language: `c++11`
    - reference: no
    - documentation: no
    - publicly available: `yes <https://github.com/EnricoCorsaro/Background>`_ 
    - requires license: no

 * ``CAN``: on the detection of Lorentzian profiles in a power spectrum
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2009A%26A...506.1043G>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``COR``: on detecting the large separation in the autocorrelation of stellar oscillation times series
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2009A%26A...508..877M>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``DIAMONDS``: high-DImensional And multi-MOdal NesteD Sampling
    - language: `c++11`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2014A%26A...571A..71C>`_ 
    - documentation: `yes <https://diamonds.readthedocs.io/en/latest/>`_ 
    - publicly available: `yes <https://github.com/EnricoCorsaro/DIAMONDS>`_ 
    - requires license: n/a

 * ``DLB``:
    - language: `?`
    - reference: no
    - documentation: n/a
    - publicly available: no
    - requires license: n/a 

 * ``FAMED``: Fast & AutoMated pEakbagging with Diamonds
    - language: `IDL` (currently being developed in `Python`)
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2020A%26A...640A.130C>`_ 
    - documentation: `yes <https://famed.readthedocs.io/en/latest/>`_ 
    - publicly available: `yes <https://github.com/EnricoCorsaro/FAMED>`_ 
    - requires license: yes

 * Flicker Flipper?: 
    - language:
    - reference:
    - documentation: 
    - publicly available: 
    - requires license: n/a

 * ``KAB``: automated asteroseismic analysis of solar-type stars
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2010arXiv1003.4167K>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a
  
 * ``lightkurve``: a friendly Python package for making discoveries with *Kepler* & TESS
    - language: `Python`
    - reference: no
    - documentation: `yes <https://docs.lightkurve.org>`_ 
    - publicly available: `yes <https://github.com/lightkurve/lightkurve>`_ 
    - requires license: no 

 * ``OCT``: automated pipeline for extracting oscillation parameters of solar-like main-sequence stars
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2010MNRAS.402.2049H>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``ORK``: using the comb response function method to identify spacings
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2008ApJ...676.1248B>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``QML``: a power-spectrum autocorrelation technique to detect global asteroseismic parameters
    - language: `?`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2011arXiv1104.0631V>`_ 
    - documentation: no
    - publicly available: no
    - requires license: n/a

 * ``PBjam``: a python package for automating asteroseismology of solar-like oscillators
    - language: `Python`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2021AJ....161...62N>`_ 
    - documentation: `yes <https://pbjam.readthedocs.io/en/latest/>`_ 
    - publicly available: `yes <https://github.com/grd349/PBjam>`_ 
    - requires license: no 

 * ``SYD``: automated extraction of oscillation parameters for *Kepler* observations of solar-type stars
    - language: `IDL`
    - reference: `yes <https://ui.adsabs.harvard.edu/abs/2009CoAst.160...74H>`_ 
    - documentation: no
    - publicly available: no
    - requires license: yes


.. important:: 

    If your software is not listed or if something listed is incorrect/missing, please 
    open a pull request to add it, we aim to be inclusive of all *Kepler*-, K2- and TESS-
    related tools!

-----

References
##########


.. bibliography:: ../references.bib

   verner2011
   boole1854

.. [#] `Kepler Asteroseismic Science Operations Center <https://kasoc.phys.au.dk>`_ 

.. [C2014] `Chaplin et al., 2014 <https://ui.adsabs.harvard.edu/abs/2014ApJS..210....1C>`_ 
.. [H2011] `Huber et al., 2011 <https://ui.adsabs.harvard.edu/abs/2011ApJ...743..143H>`_ 
.. [L2017] `Lund et al., 2017 <https://ui.adsabs.harvard.edu/abs/2017ApJ...835..172L>`_ 
.. [S2017a] `Serenelli et al., 2017 <https://ui.adsabs.harvard.edu/abs/2017ApJS..233...23S>`_ 
.. [S2017b] `Silva Aguirre et al., 2017 <https://ui.adsabs.harvard.edu/abs/2017ApJ...835..173S>`_ 
.. [Y2018] `Yu et al., 2018 <https://ui.adsabs.harvard.edu/abs/2018ApJS..236...42Y>`_ 

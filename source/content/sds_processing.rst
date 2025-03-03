#################################################################
GRACE-FO Science Data Processing System
#################################################################

Since GRACE's launch in March 2002, the official GRACE Science Data System (SDS)
continuously releases monthly gravity solutions from three different processing centers.
GRACE-FO data will also be distributed in these processing centers (links to each can be found
in Section 7.1):
- Jet Propulsion Laboratory (JPL)
- Center for Space Research at University of Texas, Austin (CSR)
- GeoforschungsZentrum Potsdam (GFZ)

Deriving month-to-month gravity field variations from GRACE and GRACE-FO observations
requires a complex inversion of relative ranging observations between the two spacecraft, in
combination with precise orbit determination via GPS and various corrections for spacecraft
accelerations not related to gravity changes (Figure 1). GRACE and GRACE-FO data appear in
three different processing centers because many parameter choices and solution strategies that
are possible. GFZ, CSR, and JPL explore these solution strategies differently. The differences in
the resulting Level-2 gravity fields have helped to better understand the characteristics of the
various approaches, and differences between the centers’ processing strategies have generally
decreased over the Releases.
The varied solutions from JPL, CSR, and GFZ can be used to infer the uncertainty in Level-2
and Level-3 GRACE and GRACE-FO fields that arises from the choice of solution strategy.
Recent papers (e.g., Sakumura et al., 2014) found that the ensemble mean (simple arithmetic
mean of JPL, CSR, GFZ fields) was effective in reducing the noise in the gravity field solutions
within the available scatter of the solutions. We recommend that users average all three data
center's solutions (JPL, CSR, GFZ).

.. figure:: ../figures/fig1_SDS_flow_GRACE_FO.png
    :align: center
    :alt: alternate text
    :figclass: align-center

3.1 Level-1 Processing
=======================
Collectively, the processing from Level-0 to Level-1B is called the Level-1 Processing. Please
refer to the GRACE and GRACE-FO Level-1B Data Product User Handbooks for more
information on Level-1 processing.

3.2 Level-2 Processing
=======================
GRACE and GRACE-FO Level-2 gravity field data products contain a set of spherical harmonic
coefficients of the “geopotential”. “Geopotential” refers to the exterior potential gravity field of
the Earth system, which includes its entire solid and fluid (including oceans and atmosphere)
components. The geopotential at a fixed location is variable in time due to mass movement and
exchange between the Earth system components. The continuum of variations of the geopotential is represented by theoretically continuous variation of the geopotential coefficients. Following
conventional methods (Heiskanen & Moritz 1967), at a field point that is exterior to the Earth
system, the potential of gravitational attraction between a unit mass and the Earth system may be
represented using an infinite spherical harmonic series. Though the exact spherical harmonic
expansion of the geopotential requires an infinite series of harmonics, the expansion is
effectively limited to a maximum degree (approx. 60-100 for GRACE and GRACE-FO monthly
fields, and >150 for long-term mean fields). Degree 60 corresponds to spatial length scales of
about 330 km.
Three centers are part of the GRACE Ground System and generate the spherical harmonic fields
for the Level-2 data product: CSR, GFZ and JPL. Their output includes spherical harmonic
coefficients of the gravity field, as well as the dealiasing fields used in the data processing. For a
detailed description of the Earth gravity field estimates provided by the Level-2 processing and
the background gravity models used, please refer to the Level-2 Gravity Field Product User
Handbooks for each center.

3.3 Level-3 Processing
=======================
3.3.1 Overview

Observed monthly changes in gravity are caused by monthly changes in mass. Most of the monthly gravity changes are caused by changes in water storage in hydrologic reservoirs, by moving ocean, atmospheric and land ice masses, and by mass exchanges between these Earth system compartments. As such, gravity measurements from space provide a precise measure of mass redistribution of Earth’s water cycle. Their vertical extent is measured in equivalent water height (also known as equivalent water thickness). 
The transformation of the gravity potential into Earth surface mass changes requires the application of various steps to account for a number of different processes including the removal of correlated and random errors, glacial isostatic adjustment (GIA), as well as other background model corrections. 

The land and ocean grids (also known as mass concentration blocks or simply, “mascons”) are typically processed with domain-optimized filters that are tuned to best filter out noise while preserving real geophysical signals. The key processing steps from Level-2 spherical harmonic data to Level-3 gridded mascon solutions are summarized in Figure 2. 

.. figure:: ../figures/fig2_flowchart_L3_processing.png
    :align: center
    :alt: alternate text
    :figclass: align-center


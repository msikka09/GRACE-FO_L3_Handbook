#################################################################
Science Data Calibration and Validation 
#################################################################

Unlike most NASA Earth Observing missions, it is not possible for GRACE and GRACE-FO science measurements to be directly calibrated to ground measurements. For example, missions that measure specific regions in the electromagnetic spectrum use a radiometer for calibration, there is no equivalent instrument to calibrate the gravity-related range rate measurements. 

However, there are a few methods to validate GRACE and GRACE-FO Level-3 data products. The first approach involves comparing the data against independent proxy data. The second approach uses a “null test” or “quiet region” to estimate noise floors. The third approach harnesses a priori information from known mass variations, which can be obtained with radar altimetry measures of large water bodies such as lakes or reservoirs (Table 1).

.. list-table:: Table 1: The main techniques or quantities that can be used to validate GRACE and GRACE-FO observations. The approaches to validate GRACE data can be broken into categories based on whether the data product covers land, ocean or land-ice. 
   :widths: 25 25
   :header-rows: 1

   * - Validation
     -   
   * - Over land / inland lakes
     - lake level; ‘quiet’ desert regions to identify noise floor
   * - Over oceans
     - bottom pressure recorders (BPR); ‘quiet’ ocean regions to identify noise floor
     

4.1 Validation with ocean bottom pressure recorders
======================================================
Ocean bottom pressure recorders (BPRs) can be used as a proxy for direct comparison with Level-3 GRACE and GRACE-FO data. BPRs measure the mass of the overlying water column plus that of the atmosphere. Validation with independent BPR measurements give some indication of the quality of the available GRACE estimates, although the sparseness of the available BPR sites limits the generality of conclusions. The BPR data variance can be associated with short-scale, localized effects, which may not be fully resolved in relatively coarse resolution estimates provided by GRACE and GRACE-FO. An effective way to overcome the issues caused by the difference in spatial resolutions between BPRs and GRACE is to average out the effects of eddies from multiple BPRs when such array data is available.

For instance, Morrison et al. (2007) compare Arctic BPR measurements from two instruments in about 4,250 m depth with GRACE. The study shows differences of 3.10 cm RMS mainly at 1–2 month time scales, with higher agreement at monthly to sub-annual time-scales. Some of the difference is likely due to comparing the Arctic BPR measurements point measurements with the inherent spatial averages of the satellite observations. This issue can be addressed by averaging the BPR measurements across locations.

Another challenge in using BPRs to validate GRACE and GRACE-FO solutions arises because of the relatively small signal of bottom pressure variations. Peralta-Ferriz et al. (2014) find that even with optimizing GRACE solutions to reduce leakage from major glacial melt regions of their study area (Greenland, Iceland, and Svalbard), the amplitude of the hydrologic signals from the terrestrial Arctic watersheds (Ob, Yenisey, Pechora, etc.) are larger than the ocean gravity change, and thus may leak into the oceanic signals measured by GRACE and GRACE-FO.  

4.2 Validation with the null test
======================================================
The second approach for validating GRACE and GRACE-FO data involves using a “null test” in which GRACE and GRACE-FO time series are examined over regions of known small or zero water movement. Any detected mass movement in these regions can be attributed to noise. Because of its large scale, the Sahara desert is one of the best possible candidates to conduct a null test experiment. Boy et al. (2012) conduct a null test validation experiment over the Sahara and Libya deserts.  They estimate that the errors of GRACE continental water storage are about 10 to 20 mm over their study area.  On the other hand, even in very dry regions like these there may be long-term changes due to aquifer and groundwater changes that are real signals, and therefore care should be taken to assume a ‘zero-signal’ region.

4.3 Validation with known mass variations
======================================================
A third way to validate GRACE and GRACE-FO solutions is to compare mass estimates with known mass variations. As a result of several decades of radar altimetry, water Level-variations of major lakes and reservoirs are monitored with a precision of a few centimeters. These induced volume variations should be equivalent to the mass variations as retrieved by GRACE and GRACE-FO, if thermal expansion is neglected (or otherwise accounted for). 

Longuevergne et al. (2013) use a priori information on reservoir storage from radar altimetry and conduct an analysis testing effects of location and areal extent of reservoirs within a basin on basin-wide average water storage changes, with application to the lower Nile (Lake Nasser) and Tigris-Euphrates basins as examples. Findings suggest that the impact of the concentrated mass on water storage changes depends on the location and areal extent of the reservoirs, the basin area, and GRACE processing. Forward modeling shows that if reservoir storage is assumed to be uniformly distributed, then the result may be an underestimation (when near the basin center) or overestimation (near the basin margin) by up to a factor of 2, depending on reservoir location and areal extent. In addition, mass changes outside a basin of interest may contribute significantly because of leakage into the basin. 

As findings from Longuevergne et al. (2013) and others suggest, GRACE and GRACE-FO estimates in regions with lakes and reservoirs require careful interpretation because of the significant storage volumes, small spatial footprint (often unresolved by GRACE and GRACE-FO) and relatively short time response (compared to groundwater), especially when attempting to separate changes in GWS in agricultural regions where both surface and groundwater are used conjunctively. 

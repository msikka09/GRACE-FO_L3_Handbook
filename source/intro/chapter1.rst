#################################################################
The Gravity Recovery and Climate Experiment Follow-on (GRACE-FO)
#################################################################

***************************************************
Introduction
***************************************************

The Gravity Recovery and Climate Experiment Follow-on (GRACE-FO) mission succeeds the GRACE mission, which launched on March 17, 2002. In more than 15 years of operation, GRACE provided pioneering observations of global mass flux that significantly contributed to our understanding of large-scale changes in polar ice, soil moisture, surface and ground water storage, and ocean mass distribution. GRACE-FO launched on May 21, 2018, and its primary mission goal is to continue the tracking of Earth's mass movements and changes, in particular those related to water. The GRACE-FO mission is a partnership between NASA and the German Research Centre for Geosciences (GFZ). 
This GRACE-FO Level-3 Data Handbook is designed to guide both experienced and beginner users in understanding and using Level-3 GRACE and GRACE-FO data products. The three main objectives of this document are to, 1) provide an overview of the GRACE-FO mission including the instrument design, science data processing, and calibration and validation procedures, 2) provide a description of the available Level-3 GRACE-FO data products and featured science and applications of Level-3 GRACE and GRACE-FO data, and 3) provide a set of step by step, reproducible use cases intended to serve as a reference for users who are interested in GRACE-FO Level-3 data products. 

***************************************************
Instrument Design
***************************************************

The instruments on GRACE and GRACE-FO were designed to enable measurements of the mean and time-variable components of the Earth’s gravity field variations. They can detect gravitational differences on the planet's surface equivalent to that of a 300-km disk of water only one centimeter thick. GRACE-FO uses the same method to measure gravitational fields as the GRACE mission. Unique to the GRACE missions, the two satellites are the measurement instrument. GRACE-FO’s two satellites follow each other in orbit around the Earth, separated by about 137 miles (220 km). Small changes in the distance between the two satellites, which result from the variable pull of gravity on each as they pass over the Earth’s surface, make up the measurement. Both satellites are capable of flying either in the lead or trailing positions, forward or backward into the residual atmospheric wind. The mass of each GRACE-FO satellite is approximately 600 kg, including about 30 kg of nitrogen fuel propellant used for orbit control maneuvers.

A microwave ranging system measures the variations of the separation distance of the satellites to within one micron, about the diameter of a blood cell. The instrument is a K-Band Ranging System and it precisely measures the changes in the separation between the two GRACE satellites using phase tracking of K- and Ka-band microwave signals sent between the two satellites in a configuration known as DOWR (Dual One Way Ranging). Each satellite transmits carrier phase to the other at two frequencies, allowing for ionospheric corrections. K-band has a radio frequency of about 24 GHz and Ka-band is near 32 GHz. The range variations can be reconstructed from these phase measurements and its numerically derived derivatives, along with other mission and ancillary data, is subsequently analyzed to compute the parameters of an Earth gravity field model that reflects the planetary mass distribution for a particular month.  
Spatial and temporal variations in the Earth’s gravity field affect the twin spacecraft differently, causing changes in the distance between the spacecraft as they orbit the Earth. For instance, when the GRACE-FO satellite pair pass over an area of the Earth with a positive gravitational anomaly, the change in gravitational field affects the lead satellite first, pulling it away from the trailing satellite. As the satellites continue, the trailing satellite is pulled toward the lead satellite as it passes over the gravity anomaly. 
The microwave ranging instrument used by GRACE and GRACE-FO is referenced to a ultrastable quartz clock and coupled with precise Satellite Global Positioning System (GPS) receivers, which determine the position of the satellite over the Earth to within a centimeter or less. 
A highly accurate electrostatic, temperature-controlled accelerometer, which is located at each satellite’s center of mass, measures the non-gravitational accelerations of the satellites, which include air drag, solar radiation pressure, and attitude control activator operation. Measuring the non-gravitational forces on each satellite in this way serves to ensure that only accelerations caused by gravity are considered in the distance measurements. The Star Camera Assembly is comprised of star cameras (three on GRACE-FO, two on GRACE) mounted close to the accelerometer on each satellite to provide the precise attitude references for the satellites.
In addition to the microwave ranging system (which is based on the corollary instrument on GRACE), GRACE-FO also has an experimental laser ranging instrument, which is designed to make the measurement of the separation distance between the two spacecraft (the primary measurement) even more precise. This advanced laser instrument could improve the accuracy of inter-spacecraft ranging by tenfold or more and lead to significantly enhanced gravity measurements and future missions.


***************************************************
GRACE-FO Science Data Processing System
***************************************************

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



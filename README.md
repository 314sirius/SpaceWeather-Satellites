# SpaceWeather-Satellites

Data source: https://omniweb.gsfc.nasa.gov/form/omni_min.html

# Space Weather Data Analysis (OMNI Dataset)

## Data Dictionary

| Column Name | Description | Units |
| :--- | :--- | :--- |
| **Year** | Year of observation | Year |
| **Day** | Day of the year (Decimal Day / DOY) | Day (1-366) |
| **Hour** | hour of observation (Universal Time) | Hour (0-23) |
| **Minute** | Minute of observation | Minute (0-59) |
| **Field_Mag_average, nT** | Scalar background magnetic field magnitude ($|B|$) | nT (Nanotesla) |
| **Bz_GSE, nT** | Z-component of the Interplanetary Magnetic Field (IMF) in GSE coordinates | nT (Nanotesla) |
| **Speed, km/s** | Solar wind bulk speed | km/s |
| **Proton_Density, n/cc** | Solar wind proton density | $n/cm^3$ |
| **Flow_Pressure, nPa** | Solar wind dynamic pressure | nPa (Nanopascals) |
| **S/C, Xgse, Re** | Spacecraft X-position in Geocentric Solar Ecliptic coordinates | Re (Earth Radii) |
| **S/C, Ygse, Re** | Spacecraft Y-position in Geocentric Solar Ecliptic coordinates | Re (Earth Radii) |
| **S/C, Zgse, Re** | Spacecraft Z-position in Geocentric Solar Ecliptic coordinates | Re (Earth Radii) |
| **AE-index, nT** | Auroral Electrojet index (measures geomagnetic activity in the auroral zone) | nT (Nanotesla) |
| **SYM/H, nT** | Symmetric Disturbance index for the H-component (measures ring current intensity) | nT (Nanotesla) |
| **Proton_Flux_10** | Integral proton flux above 10 MeV | $p/cm^2 \cdot s \cdot sr$ |
| **Proton_Flux_30** | Integral proton flux above 30 MeV | $p/cm^2 \cdot s \cdot sr$ |
| **Proton_Flux_60** | Integral proton flux above 60 MeV | $p/cm^2 \cdot s \cdot sr$ |

---

## Key Parameters for Analysis

* **Bz_GSE:** A critical parameter for predicting geomagnetic storms. Negative (southward) Bz values indicate that the IMF is coupling with Earth's magnetic field.
* **GSE Coordinates:** The Geocentric Solar Ecliptic system, where the X-axis points from the Earth towards the Sun.
* **Proton Flux:** Essential for radiation environment assessment, particularly important for satellite safety and manned missions (like Artemis).

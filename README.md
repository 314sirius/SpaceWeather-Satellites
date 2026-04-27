# SpaceWeather-Satellites

# Data sources

OMNIWeb: High Resolution OMNI: https://omniweb.gsfc.nasa.gov/form/omni_min.html

Solar Flares dataset: https://www.lmsal.com/solarsoft/latest_events_archive.html

GCAT: General Catalog of Artificial Space Objects: https://planet4589.org/space/gcat/web/sites/index.html


# Space Weather Data Analysis (OMNI Dataset)

## Data Dictionary

| Column Name | Description | Units |
| :--- | :--- | :--- |
| **Year** | Year of observation | Year |
| **Day** | Day of the year (Decimal Day / DOY) | Day (1-366) |
| **Hour** | Hour of observation (Universal Time) | Hour (0-23) |
| **Minute** | Minute of observation | Minute (0-59) |
| **Field_Mag_average, nT** | Scalar background magnetic field magnitude (B) | nT (Nanotesla) |
| **Bz_GSE, nT** | Z-component of the Interplanetary Magnetic Field (IMF) in GSE coordinates. A negative value (Southward) is a key trigger for geomagnetic storms. | nT (Nanotesla) |
| **Speed, km/s** | Solar wind bulk speed. Typical values: 300–800 km/s. | km/s |
| **Proton_Density, n/cc** | Number of protons per cubic centimeter in the solar wind. | $p/cm^3$ |
| **Flow_Pressure, nPa** | Solar wind dynamic pressure ($P = \rho v^2$). High pressure compresses the Earth's magnetosphere. | nPa (Nanopascals) |
| **S/C, Xgse, Re** | Spacecraft X-position in Geocentric Solar Ecliptic coordinates | Re (Earth Radii) |
| **S/C, Ygse, Re** | Spacecraft Y-position in Geocentric Solar Ecliptic coordinates | Re (Earth Radii) |
| **S/C, Zgse, Re** | Spacecraft Z-position in Geocentric Solar Ecliptic coordinates | Re (Earth Radii) |
| **AE-index, nT** | Auroral Electrojet index. Measures global electrojet activity in the auroral zone (indicates intensity of auroras). | nT (Nanotesla) |
| **SYM/H, nT** | Symmetric Disturbance index for the H-component. Similar to Dst, it measures the intensity of the ring current (geomagnetic storm strength) | nT (Nanotesla) |
| **Proton_Flux_10** | Integral flux of solar protons above 10MeV energy thresholds. Critical for satellite electronics and astronaut safety | $p/cm^2 \cdot s \cdot sr$ |
| **Proton_Flux_30** | Integral proton flux above 30 MeV | $p/cm^2 \cdot s \cdot sr$ |
| **Proton_Flux_60** | Integral proton flux above 60 MeV | $p/cm^2 \cdot s \cdot sr$ |

---

## Key Parameters for Analysis

* **Bz_GSE:** A critical parameter for predicting geomagnetic storms. Negative (southward) Bz values indicate that the IMF is coupling with Earth's magnetic field.
* **GSE Coordinates:** The Geocentric Solar Ecliptic system, where the X-axis points from the Earth towards the Sun.
* **Proton Flux:** Essential for radiation environment assessment, particularly important for satellite safety and manned missions (like Artemis).

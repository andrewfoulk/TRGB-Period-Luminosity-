# TRGB Period–Luminosity Analysis in Globular Clusters

📄 **Research Paper:** [TRGB Period–Luminosity Analysis](ASTR%20310%20P-L%20Relationship%20in%20TRGB%20Stars.pdf)

This project investigates whether **Tip of the Red Giant Branch (TRGB) stars** exhibit a measurable **period–luminosity relationship** that could be used for astronomical distance measurements.

The analysis combines **astronomical survey data, time-series photometry, and statistical modeling** to study pulsation periods of red giant branch stars across several globular clusters.

This work was completed as part of an observational astronomy research project at the **University of Maryland**.

---

## Scientific Motivation

Standard candles are fundamental tools for measuring astronomical distances and constraining cosmological parameters. Cepheid variables use the **Leavitt Law (period–luminosity relation)** to determine distances, but alternative distance indicators are actively studied to address discrepancies such as the **Hubble tension**.

TRGB stars are promising candidates because their luminosity is nearly constant at the helium flash stage of stellar evolution. This project explores whether **secondary pulsation periods in TRGB stars correlate with luminosity**, potentially enabling a new distance indicator.

---

## Key Techniques

- Time-series analysis with **Lomb–Scargle periodograms**
- **Monte Carlo simulation** for uncertainty estimation
- Astronomical catalog querying (**SIMBAD**, **ZTF DR22**)
- Color–magnitude diagram (CMD) analysis
- Scientific computing with **NumPy, SciPy, Pandas, Astropy**

---

## Dataset

The analysis uses data from several astronomical catalogs and surveys:

- **SIMBAD** – identification of RGB stars in globular clusters  
- **Zwicky Transient Facility (ZTF DR22)** – time-series photometric observations  
- **Literature distance measurements** for globular clusters

Candidate TRGB stars were identified using **color–magnitude diagram selection criteria** based on absolute I-band magnitude and color index.

---

## Methods

The project uses several techniques commonly applied in computational astrophysics.

### 1. TRGB Star Selection
Stars were selected from globular clusters using:

- Right ascension and declination constraints
- ZTF observational limits
- Absolute magnitude thresholds for TRGB stars

### 2. Time-Series Analysis

Pulsation periods were extracted from ZTF light curves using **Lomb–Scargle periodograms**, a method designed for analyzing unevenly sampled astronomical data.

Key steps included:

- Computing power spectra across candidate frequencies
- Identifying dominant pulsation periods
- Filtering alias periods using **prominence thresholds**

### 3. Period Uncertainty Estimation

Period uncertainties were estimated using **Monte Carlo simulations**:

- Noise proportional to the periodogram signal-to-noise ratio was injected
- The highest power period was recomputed across **1000 trials**
- The standard deviation of the resulting period distribution was used as the uncertainty

### 4. Luminosity Calculation

Absolute magnitudes were calculated using the **distance modulus**:

\[
M = m - 5\log(D/10)
\]

where:

- \(M\) = absolute magnitude  
- \(m\) = apparent magnitude  
- \(D\) = distance (parsecs)

---

## Results

A total of **36 red giant branch stars** were analyzed across **8 globular clusters**.

Key findings:

- Only **8 stars** exhibited strong periodic signals.
- Periods ranged approximately from **100 to 400 days**.
- No statistically significant **global period–luminosity relationship** was observed.

These results suggest that TRGB stars do **not follow a universal period–luminosity relation**, consistent with previous literature on red giant variability.

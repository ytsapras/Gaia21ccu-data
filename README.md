# Gaia21ccu — Photometric Light Curves

This repository contains multi-band photometric observations of **Gaia21ccu**, a long-duration binary gravitational microlensing event observed towards the Galactic plane.

The data accompany the microlensing analysis presented in:

**Tsapras et al., *The curious case of microlensing event Gaia21ccu: A binary-lens event in the Galactic Plane with complex post-peak features*** (Astronomy & Astrophysics, manuscript under revision).

The light curves are provided to facilitate independent microlensing modelling and further analysis.

## Data

The repository contains **17 CSV light curves** from the following observational programmes:

- **ASAS-SN:** $g$-band photometry
- **Gaia:** $G$-band photometry
- **Las Cumbres Observatory (LCO):** $g$- and $i$-band photometry
- **REM:** $g$, $r$, $i$, and $z$ photometry, including ROS2 datasets
- **ROAD Observatory:** $B$, $V$, and $I$ photometry
- **OGLE:** $i$-band photometry from two datasets

Each CSV file has the same three-column format:

| Column | Description |
|---|---|
| `time` | Observation epoch, expressed as a Julian Date |
| `magnitude` | Observed apparent magnitude in the corresponding passband |
| `error` | Magnitude uncertainty associated with the measurement |

Example:

```text
time,magnitude,error
2459370.4642477,11.10524357996056,0.0360651822685154
2459370.46425,11.12620549501326,0.0355829563113959
```

The files contain processed photometry, in a common format,and ready to be analyzed; some datasets have been calibrated, rebinned, or had their originally-reported uncertainties adjusted. They should therefore not necessarily be interpreted as raw, unmodified instrumental measurements.

Photometric zero points and passbands differ between observatories. Their magnitudes should not be combined directly without accounting for these differences. The exact time convention of each contributing dataset should also be checked when performing precision timing analyses.

## Modelling

The accompanying paper presents binary-lens modelling with annual microlens parallax and orbital motion using [pyLIMA](https://github.com/ebachelet/pyLIMA).

The final analysis uses **4,480 cleaned measurements from 17 datasets**, with dataset-dependent photometric uncertainty renormalisation following Yee et al. (2012).

The uncertainties in the files are those supplied with the processed light curves and should not automatically be assumed to be identical to the final renormalised uncertainties adopted in the published model comparison. The corresponding error-scaling prescriptions and coefficients are described in the paper.

## Access and citation

The light curves can be downloaded individually or together through GitHub's **Code → Download ZIP** option.

If you use these data in a publication, please cite the Gaia21ccu paper and acknowledge the relevant contributing surveys and observatories.

**Repository:** https://github.com/ytsapras/Gaia21ccu-data

The full bibliographic reference will be updated following publication.

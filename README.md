# NASA Exoplanet Archive: Discovery Analytics

**Python scientific-data analysis project** using the [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/), TAP/ADQL queries, Pandas and Matplotlib.

## Research question

How do reported discovery methods and exoplanet characteristics vary across the confirmed-planet catalogue, and what biases and missing data limit interpretation?

## What is in this repository?

- **[`exoplanet_archive_analysis.ipynb`](exoplanet_archive_analysis.ipynb)**: clean analysis covering catalogue retrieval, duplicate checks, missingness, discovery trends, survey methods, method-by-year comparisons, and radius versus orbital period. A generated summary reports results for the *current downloaded snapshot*.
- [`NASA_Exoplanet_Discovery_Analytics.ipynb`](NASA_Exoplanet_Discovery_Analytics.ipynb): original exploratory notebook preserved unchanged. Saved outputs reported 6,336 planets and 22 selected columns when that run was made. That is **historical output**, not a current archive count.
- [`requirements.txt`](requirements.txt): Python dependency list.
- Other files (p5 JavaScript and HTML) are legacy files from an older, unrelated project. They are not used in the astronomy analysis and are retained for now to avoid deleting earlier work.

## Run it

```bash
python -m venv .venv
source .venv/bin/activate    # Windows: .venv\\Scripts\\activate
python -m pip install -r requirements.txt
jupyter notebook
```

Open `exoplanet_archive_analysis.ipynb` and choose **Run All**. The notebook needs internet access to query the NASA archive via `https://exoplanetarchive.ipac.caltech.edu/TAP/sync`.

The notebook prints the retrieval time and row count. Numbers may change as the archive updates. All figures and interpretation are produced dynamically from the downloaded data.

## Scope and limitations

- Uses the **Planetary Systems Composite Parameters** table (`pscomppars`); values may be drawn from different studies or sources.
- The plots show the **catalogued and confirmed population**, not an unbiased sample of planets in the Galaxy.
- Method counts reflect survey sensitivities, observational strategy and confirmation biases.
- Missing values are reported rather than replaced with made-up measurements.
- The scatter plot excludes entries lacking positive reported radius and orbital period. It should not be interpreted as an occurrence-rate measurement.
- The repository is a research-portfolio analysis, **not a peer-reviewed publication**.

## Suggested next steps

Propagate uncertainties, model observational selection functions, incorporate host-star distributions, and develop interpretable statistical comparisons between discovery channels.

**Author:** Sesha Sai Sreya Koduru · [GitHub profile](https://github.com/sreya2702)

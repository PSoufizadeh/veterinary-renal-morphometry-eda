# Veterinary Renal Morphometry — Exploratory Data Analysis

[![Article DOI](https://img.shields.io/badge/DOI-10.1111%2Fvru.70287-087F8C)](https://doi.org/10.1111/vru.70287)

Python-based data preparation and exploratory analysis of CT-derived renal morphology and volumetry in healthy dogs and cats.

**Repository maintainer:** Parham Soufizadeh, DVM

## Research context

This repository accompanies *Quantitative Evaluation of Renal Morphology and Volumetry in Healthy Dogs and Cats Using CT and Advanced Statistical Models*, Veterinary Radiology & Ultrasound. The study examines renal length, width, volume and CT attenuation (Hounsfield units), alongside anatomical measurements including body weight, L2 vertebral length and aortic diameter.

## Analytical scope

| Component | Tools | Availability |
|---|---|---|
| Data preparation and categorical encoding | pandas, scikit-learn | Notebook 01 |
| Interactive exploratory analysis and descriptive statistics | D-Tale | Notebook 02 |
| Predictive Power Score (PPS), exploratory only | D-Tale | Interactive interface in notebook 02 |
| Additional exploratory reports | ydata-profiling, Sweetviz | Optional cells in notebook 02 |
| Spearman rank correlation | IBM SPSS Statistics 26.0 | External to this repository |
| Linear regression and paired Wilcoxon comparisons | GraphPad Prism 9.5.1 | External to this repository |

PPS is used as a complementary descriptive metric to explore potentially nonlinear relationships, not as a clinical prediction model or inferential procedure. For all scientific findings, tables, figures and interpretation, refer to the associated article: [10.1111/vru.70287](https://doi.org/10.1111/vru.70287).

## Repository structure

```text
notebooks/
  01_data_preparation.ipynb
  02_exploratory_analysis.ipynb
requirements.txt
requirements-optional.txt
CITATION.cff
.gitignore
README.md
```

## Local usage

Use a dedicated Python environment (Python 3.10 recommended for compatibility testing).

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

Place an authorised Excel workbook at `data/renal_raw.xlsx` locally. Expected categorical fields are `Species`, `Breed`, `Sex` and `Reproductive status`; the remaining measurements follow the local research workbook. Review all fields for identifiers before running. Run notebook 01, then notebook 02. D-Tale opens a local interactive interface. Optional reporting libraries can be installed with `python -m pip install -r requirements-optional.txt` and enabled in notebook 02.

The original analysis used D-Tale 1.61.0. The public notebooks use a modernised dependency setup and have not been verified to reproduce the original software environment or study results. The original notebooks also imported pandasgui without using it; that unused import has been removed. Notebook outputs and local absolute paths have been removed; label encoding is retained and nominal variables are marked as categorical for exploration. No SPSS or Prism files were supplied or recreated.

## Data and confidentiality

Clinical records, imaging files, derived datasets, generated reports and numerical study results are intentionally excluded. This repository is not a clinical decision tool or a complete reproduction package. Do not commit local data or executed notebooks containing outputs. For research enquiries contact [Parham Soufizadeh](https://www.linkedin.com/in/parham-soufizadeh).

## Citation

Modarres Tonekabony, S. H., Soufizadeh, P., & Molazem, M. *Quantitative Evaluation of Renal Morphology and Volumetry in Healthy Dogs and Cats Using CT and Advanced Statistical Models*. Veterinary Radiology & Ultrasound. https://doi.org/10.1111/vru.70287

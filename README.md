MSR 2026 - Beyond Code Quality: Understanding Integration Failures in
Agentic Pull Requests
Author: Anonymous 
Platform: macOS
Python: 3.11
Environment: venv

Folder Structure
data_processed/: Cleaned or filtered data for analysis
src/: Python scripts for preprocessing and utilities
notebooks/: Jupyter notebooks for exploration and analysis
figures/ and tables/: Output visualizations and tables

Next Step

Download the MSR 2026 dataset into data_raw/ and document the download source and date.

Data Provenance

Dataset: AIDev – Studying AI Coding Agents on GitHub
Source URL: https://huggingface.co/datasets/hao-li/AIDev
Downloaded by: Bernard Barnieh
Date/Time: 2025-10-27 – 02:59 UTC

Files:

AIDev_pop.zip – raw dataset archive (subset of full AIDev)
AIDev_pop_SHA256.txt – SHA-256 checksum
Checksum:
'f36668ddf22403a332f978057d527cf285b01468bc3431b04094a7bafa6aba59'

Data provenance 02

Source: MSR 2026 Mining Challenge (AIDev dataset)
Primary file used: data_raw/all_pull_request.parquet
Download date/time:
Checksums recorded in: data_raw/AIDev_pop_SHA256.txt
Raw files are never edited.

Reproduce

# from repo root
python -m src.01_preprocess
jupyter nbconvert --to notebook --inplace --execute notebooks/01_exploration.ipynb
jupyter nbconvert --to notebook --inplace --execute notebooks/03_agent_failure_modes_analysis.ipynb
jupyter nbconvert --to notebook --inplace --execute notebooks/03_agent_failure_modes_sampling.ipynb
jupyter nbconvert --to notebook --inplace --execute notebooks/04_rq2_early_risk_prediction_agentic.ipynb




**Citation:**  
Li, H., Zhang, H., & Hassan, A. E. (2025). *The Rise of AI Teammates in Software Engineering (SE) 3.0: How Autonomous Coding Agents Are Reshaping Software Engineering.* arXiv:2507.15003. https://doi.org/10.48550/arXiv.2507.15003  

**License:** Research-only usage under MSR 2026 Mining Challenge rules.  
Do not modify raw files; all processing outputs are stored in `data_working/`.

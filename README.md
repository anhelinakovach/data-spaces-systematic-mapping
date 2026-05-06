# Systematic Mapping Study on Data Spaces
[![DOI](https://img.shields.io/badge/DOI-10.1016/j.cosrev.2025.100819-blue)](https://doi.org/10.1016/j.cosrev.2025.100819)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Studies](https://img.shields.io/badge/Primary%20Studies-149-green)]()
[![Period](https://img.shields.io/badge/Coverage-2016--2025-orange)]()

This repository contains the complete dataset of primary studies and classification materials for the systematic mapping study presented in:
> **Understanding Data Spaces: A Systematic Mapping Study of Foundations, Technical Building Blocks, and Sectoral Adoption**
>
> Anhelina Kovach, Leticia Montalvillo, Jorge Lanza, Pablo Sotres, Aitor Urbieta
>
> *Computer Science Review*, 59, 100819, 2026
>
> DOI: [10.1016/j.cosrev.2025.100819]([https://doi.org/PLACEHOLDER](https://doi.org/10.1016/j.cosrev.2025.100819))

## Abstract
Data spaces are emerging as a key paradigm for enabling sovereign, secure, and interoperable data sharing across sectors. Beyond data governance, they represent a transformation in communication architectures—where communication is no longer merely about establishing connections, but about \textit{who is allowed to share what, under which conditions, and for what purpose}. Despite growing attention, the research landscape remains fragmented and under-synthesized. This paper presents a Systematic Mapping Study (SMS) of 149 peer-reviewed publications, analyzing the conceptual foundations, technical building blocks, and sectoral adoption of data spaces. Following established SMS methodologies, we classify the literature across key technical themes defined by the Data Spaces Support Centre (DSSC) and assess methodological maturity, technical novelty, and application domains. Our findings show that 46.3\% of studies address data value creation enablers, 30.8\% focus on data interoperability, and 22.9\% explore data sovereignty. The study provides a structured synthesis of current research and offers guidance for advancing federated, trust-aware communication infrastructures. 

## Key Findings
**Maturity gap.** 64.4% of studies remain at conceptual stages (Opinion, Conceptual, or Experience papers); only 5.4% provide concrete real-world evaluations.

**Building block imbalance.** Data Value Creation Enablers dominate the literature (46.3%), while Data Sovereignty receives less attention (22.9%). Only 34.9% of studies integrate multiple building blocks, indicating limited cross-cutting research.

**Sectoral adoption.** Manufacturing leads adoption (22.8%), followed by Mobility/Transportation (16.8%), Healthcare (14.1%), and Energy (6.7%). Several domains such as Agriculture and Tourism remain largely underexplored.

**Architectural landscape.** The field traces an evolution from the IDSA and Gaia-X reference architecture models to the emergence of standardized data space connector implementations (EDC, DSC, Trusted Connector, TRUE Connector).

**Emerging technologies.** Key supporting technologies identified across studies include Digital Twins (Asset Administration Shell), Distributed Ledger Technologies, Privacy-Enhancing Technologies, Digital Product Passports, and AI/ML-based solutions.

## Research Questions
The systematic mapping study addresses four research questions:
- **RQ1:** What is the methodological maturity and technical novelty of data space research, and how has it evolved?
- **RQ2:** What is the coverage, evolution, and interrelation of technical building blocks in data space research?
- **RQ3:** What is the coverage, technical novelty, and interrelation of data interoperability in data space research?
- **RQ4:** What is the coverage, technical novelty, and interrelation of data sovereignty in data space research?
- **RQ5:** What is the coverage, technical novelty, and interrelation of data value creation enablers in data space research?
- **RQ6:** Which sectors received most attention and how is this attention evolving?

 ## Repository Structure

```
.
├── README.md                          # This file
├── data/
│   ├── README.md                      # Dataset documentation and schema
│   ├── primary-studies.xlsx           # Full dataset (Excel)
│   ├── primary-studies.json           # Full dataset (JSON)
│   └── studies-classification.pdf     # Visual classification summary
``` 

## Dataset Overview

The dataset contains **149 primary studies** on data spaces published between **2016 and April 2025**, identified through a systematic search across six electronic databases: IEEE Xplore, ACM Digital Library, Springer Link, ScienceDirect, MDPI, and Wiley Online Library.

Each study is classified along four main facets:

| Facet | Description |
|-------|-------------|
| **Building Blocks** | Technical contribution area based on the [DSSC Blueprint v2.0](https://dssc.eu/page/blueprint): Data Interoperability, Data Sovereignty, Data Value Creation Enablers |
| **Research Type** | Methodological maturity: Opinion, Experience, Conceptual, Solution, Validation, Evaluation |
| **Sector** | Application domain: Manufacturing, Healthcare, Energy, Mobility/Transportation, Agriculture, Tourism, Generic, etc. |
| **Architecture** | Reference architecture alignment: IDSA, Gaia-X, FIWARE, NA |

Additional metadata includes underlying technologies, connector types, associated research projects, and identified challenges. See [`data/README.md`](./data/README.md) for the complete schema documentation.

## Citation

If you use this dataset or find this work useful, please cite:

```bibtex
@article{KOVACH2026100819,
title = {Understanding data spaces: A Systematic Mapping Study of foundations, technical building blocks, and sectoral adoption},
journal = {Computer Science Review},
volume = {59},
pages = {100819},
year = {2026},
issn = {1574-0137},
doi = {https://doi.org/10.1016/j.cosrev.2025.100819},
author = {Anhelina Kovach and Leticia Montalvillo and Jorge Lanza and Pablo Sotres and Aitor Urbieta},
}
```

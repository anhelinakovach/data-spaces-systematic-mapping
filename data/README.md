# Dataset: Primary Studies on Data Spaces

This directory contains the dataset from the systematic mapping study presented in:
> **Understanding Data Spaces: A Systematic Mapping Study of Foundations, Technical Building Blocks, and Sectoral Adoption**
>
> Anhelina Kovach, Leticia Montalvillo, Jorge Lanza, Pablo Sotres, Aitor Urbieta
>
> *Computer Science Review*, 59, 100819, 2026
>
> DOI: [10.1016/j.cosrev.2025.100819]([https://doi.org/PLACEHOLDER](https://doi.org/10.1016/j.cosrev.2025.100819))

The dataset includes **149 primary studies** focused on data spaces, published between **2016 and April 2025**, identified through systematic searches across IEEE Xplore, ACM Digital Library, Springer Link, ScienceDirect, MDPI, and Wiley Online Library.

## Citation

If you use this dataset, please cite both the paper and the dataset:
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

## Files

| File | Format | Description |
|------|--------|-------------|
| [`primary-studies.xlsx`](primary-studies.xlsx) | Excel | Complete dataset with all classification facets and bibliographic metadata |
| [`primary-studies.json`](primary-studies.json) | JSON | Machine-readable version of the full dataset |
| [`studies-classification.pdf`](studies-classification.pdf) | PDF | Visual summary of the primary studies classified across the main facets |

## Dataset Summary

| Dimension | Value |
|-----------|-------|
| Total primary studies | 149 |
| Coverage period | 2016 – April 2025 |
| Source databases | IEEE Xplore, ACM Digital Library, Springer Link, ScienceDirect, MDPI, Wiley Online Library |
| Classification facets | Building Blocks, Research Type, Sector, Architecture |
| Publication types | Journal Articles, Conference Papers, Workshop Papers |

## Data Schema
Each record in the dataset represents one primary study and contains the fields described below.

### Bibliographic Information

| Field | Type | Description |
|-------|------|-------------|
| `Title` | string | Paper title |
| `Authors` | array of objects | Author details (see [Author Object](#author-object) below) |
| `Year` | integer | Publication year (2016–2025) |
| `Site` | object | Venue information (see [Venue Object](#venue-object) below) |
| `DOI` | string | Digital Object Identifier (URL format) |
| `Abstract` | string | Paper abstract |
| `Keywords` | array of strings | Author-provided keywords |
| `Type` | string | Publication type: `Journal Article`, `Conference Paper`, `Workshop Paper` |
| `Database` | string | Source database where the paper was found (e.g., `IEEE Xplore`, `Springer Link`) |

#### Author Object

| Field | Type | Description |
|-------|------|-------------|
| `Name` | string | Full author name |
| `Affiliation` | string | Institutional affiliation |
| `Country` | string | Author's country |

#### Venue Object

| Field | Type | Description |
|-------|------|-------------|
| `Name` | string | Conference/journal acronym or short name |
| `Details` | string | Full conference/journal name and additional information |

### Classification Facets

#### Building Blocks & Novelty

Based on the [Data Spaces Support Centre (DSSC) Blueprint v2.0](https://dssc.eu/page/blueprint) framework, with adaptations described in the paper. Each study is assigned an array of building block objects.

> **Note on taxonomy adaptations:** The classification extends the DSSC Blueprint taxonomy. For example, ODRL policy specification falls under Usage Control in this study (covering specification, negotiation, and enforcement of usage policies), whereas in the Blueprint it is categorized under Data Offering.

Each building block object contains:

| Field | Type | Description |
|-------|------|-------------|
| `Block` | string | Main category (see values below) |
| `Section.Name` | string | Specific building block within the category |
| `Section.Novelty` | string | Assessment of the study's contribution novelty for this block |

**Block values and their sub-blocks:**

| Block | Sub-blocks (Section.Name) |
|-------|--------------------------|
| **Data Interoperability** | Data Models, Data Exchange, Provenance and Traceability |
| **Data Sovereignty** | Identity Management, Trust Framework, Usage Control |
| **Data Value Creation Enablers** | Data Offering, Publication and Discovery, Value Creation Services |

#### Research Type

| Value | Description |
|-------|-------------|
| `Opinion` | Viewpoints on future directions without concrete solutions |
| `Experience` | Lessons learned from practical engagement |
| `Conceptual` | Conceptual frameworks or taxonomies |
| `Solution` | Technical solution proposals |
| `Validation` | Solutions validated in controlled/laboratory settings |
| `Evaluation` | Solutions evaluated in real-world or industrial settings |

#### Sector

| Field | Type | Description |
|-------|------|-------------|
| `Type` | string | Primary application domain |
| `Subdomain` | array of strings | Specific application areas within the domain |

**Sector values:** Manufacturing, Healthcare, Energy, Mobility, Agriculture, Tourism, Generic, among others.

#### Architecture

Array of strings indicating alignment with reference architectures:

| Value | Description |
|-------|-------------|
| `IDSA` | International Data Spaces Association Reference Architecture Model |
| `Gaia-X` | Gaia-X Federation Services architecture |
| `FIWARE` | FIWARE-based architecture |
| `NA` | Not applicable or not specified |

### Additional Fields

| Field | Type | Description |
|-------|------|-------------|
| `Technologies` | array of strings | Emerging/supporting technologies: Digital Twins (`DT`), Distributed Ledger Technology (`DLT`), Privacy Enhancing Technologies (`PETs`), `AI/ML`, Digital Product Passport (`DPP`), etc. |
| `Process` | string | Methodology or process contribution, following the [IDS RAM v4.0](https://github.com/International-Data-Spaces-Association/IDS-RAM_4_0) process definitions |
| `Challenges` | array of strings | Identified challenges and limitations |
| `Project Context` | string | Associated research project or initiative |
| `Connector Types` | array of strings | Data space connector used: `DSC` (Data Space Connector), `EDC` (Eclipse Dataspace Components Connector), `Trusted Connector`, `TRUE Connector`, `NA` |
| `Description` | string | Summary of the study's contribution and focus |
| `Comments` | string | Additional notes and observations |

## Coding Conventions

| Convention | Usage |
|------------|-------|
| `"NA"` | Information is not applicable or not specified in the study |
| `[]` (empty array) | Multi-value fields with no applicable values |
| `null` | Optional single-value fields that are missing |

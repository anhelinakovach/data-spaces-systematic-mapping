# Dataset of primary studies
This directory contains the dataset from our systematic mapping study on data spaces, including 149 primary studies focused on data spaces published from 2016 up to April 2025.

## Files overview
- [`primary-studies.xlsx`](primary-studies.xlsx): Excel format.
- [`primary-studies.json`](primary-studies.json): JSON format.
- [`studies-classification.pdf`](studies-classification.pdf): PDF format, visual summary of the set of primary studies classified across the main classification facets.

## Data structure
### Bibliographic information
- **Title** (string): Paper title.
- **Authors** (array): Author details including name, affiliation, and country.
- **Year** (integer): Publication year.
- **Site** (object): Venue information (conference/journal name and details).
- **DOI** (string): Digital Object Identifier (URL format).
- **Abstract** (string): Paper abstract.
- **Keywords** (array): Author-provided keywords.
- **Type** (string): Publication type (Journal Article, Conference Paper, Workshop Paper).
- **Database** (string): Source database where paper was found (e.g., IEEE Xplore, Springer Link).

### Classification facets
#### Building Blocks & Novelty
Based on the [Data Spaces Support Centre (DSSC) Blueprint v2.0 framework](https://dssc.eu/page/blueprint). It is an array of objects containing:
- **Block** (string): Main category.
  - Data Interoperability
  - Data Sovereignty
  - Data Value Creation Enablers
- **Section** (object): Specific building block.
  - **Name**: Specific building block (see taxonomy below).
  - **Novelty**: Assessment of contribution novelty.

##### Building Blocks Taxonomy
*Data Interoperability:*
- Data Models
- Data Exchange
- Provenance and Traceability

*Data Sovereignty:*
- Identity Management
- Trust Framework
- Usage Control

*Data Value Creation Enablers:*
- Data Offering
- Publication and Discovery
- Value Creation Services

#### Research Type
- Opinion, Experience, Conceptual, Solution, Validation, Evaluation.

#### Sector
Object containing:
- **Type** (string): Primary application domain.
  - Manufacturing, Healthcare, Energy, Transportation, Agriculture, Tourism, Generic, etc.
- **Subdomain** (array): Specific application areas within the domain.

### Additional Fields

#### Architecture Types
Array of strings representing the underlying reference architecture:
- IDSA, Gaia-X, FIWARE, NA.

#### Technologies
Array of emerging/supporting technologies, such as:
- Digital Twins (DT), Distributed Ledger Technology (DLT), Privacy Enhancing Technologies (PETs), AI/ML, etc.

#### Process
Methodology or process contribution, following the processes defined in the [International Data Spaces (IDS) Reference Architecture Model (RAM) v4.0](https://github.com/International-Data-Spaces-Association/IDS-RAM_4_0). 

#### Challenges
An array of identified challenges and limitations.

#### Project Context
Associated research project or initiative.

#### Connector Types
An array of the data space connector used in the study.
- Data Space Connector (DSC), Eclipse Dataspace Components (EDC) Connector, Trusted Connector, TRUE Connector, NA.

#### Comments
Additional notes and observations.

#### Description
Summary of study contribution and focus.

## Coding Conventions

### Missing or Not Applicable Data
- **"NA"**: Used when information is not applicable or not specified.
- **Empty arrays []**: Used for multi-value fields with no applicable values.
- **null**: Used for optional single values that are missing.

### Author Information
Each author object contains:
- **Name**: Full author name.
- **Affiliation**: Institution affiliation.
- **Country**: Author's country.

### Venue Information
Site object contains:
- **Name**: Conference/journal acronym or short name.
- **Details**: Full conference/journal name and additional details.
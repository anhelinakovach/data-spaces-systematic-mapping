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
#### Building Blocks (DSSC Blueprint framework)
Array of objects containing:
- **Block** (string): Main category.
  - Data Interoperability
  - Data Sovereignty
  - Data Value Creation Enablers
- **Section** (object): Specific building block.
  - **Name**: Specific building block (see taxonomy below).
  - **Novelty**: Assessment of contribution novelty.

**Building Blocks Taxonomy:**
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
- Data Discovery
- Value Creation Services

#### Research Type (Maturity level)
- Opinion, Experience, Conceptual, Solution, Validation, Evaluation.

#### Sector classification
Object containing:
- **Type** (string): Primary application domain.
  - Manufacturing, Healthcare, Energy, Transportation, Agriculture, Tourism, Generic, etc.
- **Subdomain** (array): Specific application areas within the domain.
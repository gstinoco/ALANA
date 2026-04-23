# ALANA: Airbnb Listings Atlas of North America :bar_chart:

<div align="center">

<img src="docs/logo/logo.png" alt="ALANA logo" width="680" style="margin: 20px 0;">

[![GitHub](https://img.shields.io/badge/GitHub-Repository-black.svg)](https://github.com/gstinoco/ALANA) [![Dataset](https://img.shields.io/badge/Dataset-Airbnb%20Listings-blue.svg)](#open_file_folder-dataset-overview) [![Format](https://img.shields.io/badge/Format-CSV-1f6feb.svg)](#file_cabinet-repository-structure) [![Schema](https://img.shields.io/badge/Schema-English%20Standardized-0A7B83.svg)](#bookmark-data-dictionary) [![Countries](https://img.shields.io/badge/Countries-3-success.svg)](#open_file_folder-dataset-overview) [![Rows](https://img.shields.io/badge/Rows-181856-success.svg)](#open_file_folder-dataset-overview) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Historical Airbnb listing records for Canada, Mexico, and the United States**

*A consolidated and standardized North American dataset for exploratory analysis, comparative research, and data-driven tourism studies*

### :link: Quick Links
[![Quick Start](https://img.shields.io/badge/Quick-Start-green)](#rocket-quick-start) [![Requirements](https://img.shields.io/badge/Setup-Requirements-blue)](#package-installation--requirements) [![Dataset](https://img.shields.io/badge/Data-Dataset-blue)](#open_file_folder-dataset-overview) [![Formats](https://img.shields.io/badge/Data-Formats-purple)](#file_cabinet-data-formats) [![Structure](https://img.shields.io/badge/Repo-Structure-purple)](#open_file_folder-project-architecture) [![Methodology](https://img.shields.io/badge/Research-Methodology-darkgreen)](#books-methodology) [![Quality](https://img.shields.io/badge/Data-Quality-darkgreen)](#white_check_mark-data-quality-and-standardization) [![Authors](https://img.shields.io/badge/Project-Authors-blue)](#scientist-authors) [![Acknowledgments](https://img.shields.io/badge/Support-Acknowledgments-darkgreen)](#pray-acknowledgments) [![Contact](https://img.shields.io/badge/Contact-Support-blue)](#email-contact--support) [![FAQ](https://img.shields.io/badge/Help-FAQ-lightgrey)](#speech_balloon-faq)

</div>

---

## :clipboard: Table of Contents
- [Overview](#star2-overview)
- [Scope and Features](#sparkles-scope-and-features)
- [Installation & Requirements](#package-installation--requirements)
- [Quick Start](#rocket-quick-start)
- [Usage Guide](#book-usage-guide)
- [Data Formats](#file_cabinet-data-formats)
- [Project Architecture](#open_file_folder-project-architecture)
- [Methodology](#books-methodology)
- [Dataset Overview](#open_file_folder-dataset-overview)
- [Data Dictionary](#bookmark-data-dictionary)
- [Data Quality and Standardization](#white_check_mark-data-quality-and-standardization)
- [Limitations](#warning-limitations)
- [Recommended Use](#compass-recommended-use)
- [Authors](#scientist-authors)
- [Citation and Usage Notes](#memo-citation-and-usage-notes)
- [License](#page_with_curl-license)
- [Acknowledgments](#pray-acknowledgments)
- [Contact & Support](#email-contact--support)
- [FAQ](#speech_balloon-faq)

---

## :star2: Overview

**ALANA** stands for **Airbnb Listings Atlas of North America**. This repository publishes a cleaned and consolidated dataset of historical Airbnb listings covering three countries:

- **Canada**
- **Mexico**
- **United States**

The goal of the project is to make historical short-term rental data easier to inspect, compare, and reuse across research and analytical workflows. This repository centers on country-level consolidated CSV files with a shared schema.

The dataset is suitable for:

- exploratory data analysis,
- descriptive statistical summaries,
- region-level comparisons within countries,
- cross-country comparisons across North America,
- temporal analysis using month and year fields, and
- downstream data pipelines that benefit from a standardized tabular structure.

Each row represents a **listing observation captured at a specific month and year**, not necessarily a permanently unique property across the entire repository. The same listing may therefore appear across different temporal snapshots.

Included in this repository:

- `Canada.csv`: final consolidated dataset for Canada
- `Mexico.csv`: final consolidated dataset for Mexico
- `USA.csv`: final consolidated dataset for the United States
- `LICENSE`: MIT license for repository contents

Repository URL:

- `https://github.com/gstinoco/ALANA`

### :wrench: Key Capabilities
- **:globe_with_meridians: North American coverage**: three harmonized datasets for Canada, Mexico, and the United States.
- **:label: Shared schema**: the final files use consistent English column names and aligned field semantics.
- **:broom: Prepared dataset**: malformed rows, broken structures, and naming inconsistencies were corrected during preparation.
- **:calendar: Time-aware records**: each listing record preserves a month and year reference for historical analysis.

### :microscope: Typical Use Cases

| Area | Example question | Expected use |
|------|------------------|--------------|
| **Tourism studies** | How do listing volumes vary across regions and years? | Grouping by `Region`, `Month`, and `Year` |
| **Urban analytics** | Which accommodation types appear more frequently in specific territories? | Aggregation by `Type` and `Region` |
| **Economic exploration** | How do captured prices differ across countries or states? | Descriptive summaries on `Price` |
| **Platform studies** | How does review activity vary by listing type or geography? | Analysis of `Reviews` by `Type` and `Region` |

---

## :sparkles: Scope and Features

### :open_file_folder: Final Published Assets
- `Canada.csv`
- `Mexico.csv`
- `USA.csv`

### :triangular_ruler: Harmonized Final Schema

All final CSV files follow the same structure:

```text
Region, Name, Type, Guests, Bedrooms, Price, Reviews, Month, Year
```

### :bar_chart: What This Dataset Supports
- Country-level and region-level descriptive analysis.
- Cross-country integration into a single table.
- Time-aware summaries using `Month` and `Year`.
- Filtering by accommodation type, guest capacity, price, and review activity.
- Use in spreadsheets, statistical software, Python, R, SQL, and dashboard workflows.

### :white_check_mark: Why This Repository Is Useful
- The repository provides direct access to the consolidated country-level datasets.
- The naming and schema are consistent across countries.
- The files are lightweight enough to load directly in common analysis environments.

---

## :package: Installation & Requirements

This is a dataset repository, so **no installation is required** to access the published files.

### :computer: Recommended Tools
- Spreadsheet software such as Excel or LibreOffice Calc
- Python with `pandas`
- R with `readr` or `data.table`
- SQL databases or notebook-based analytics environments

### :clipboard: Optional Python Dependency

```bash
pip install pandas
```

### :white_check_mark: Installation Verification

```bash
python -c "import pandas as pd; print('Environment ready')"
```

---

## :rocket: Quick Start

<table>
  <thead>
    <tr>
      <th align="left" width="170">Step</th>
      <th align="left">What to do</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>1) Choose a file</b></td>
      <td>Select <code>Canada.csv</code>, <code>Mexico.csv</code>, or <code>USA.csv</code> depending on the country you want to study.</td>
    </tr>
    <tr>
      <td><b>2) Load the dataset</b></td>
      <td>Open it in your preferred environment such as Python, R, Excel, LibreOffice Calc, or a database workflow.</td>
    </tr>
    <tr>
      <td><b>3) Start analyzing</b></td>
      <td>Use the shared schema directly for summaries, visualizations, filtering, or integration across countries.</td>
    </tr>
  </tbody>
</table>

### :computer: Example In Python

```python
import pandas as pd

usa = pd.read_csv("USA.csv")

print(usa.head())
print(usa.columns.tolist())
print(usa.groupby("Type").size().sort_values(ascending=False).head())
```

### :bar_chart: Example Combining All Countries

```python
import pandas as pd

canada = pd.read_csv("Canada.csv").assign(Country="Canada")
mexico = pd.read_csv("Mexico.csv").assign(Country="Mexico")
usa = pd.read_csv("USA.csv").assign(Country="United States")

north_america = pd.concat([canada, mexico, usa], ignore_index=True)
print(north_america.shape)
```

---

## :book: Usage Guide

### :gear: Single-Country Analysis

Use one file when your objective is limited to a specific country:

- `Canada.csv` for Canadian listings
- `Mexico.csv` for Mexican listings
- `USA.csv` for listings in the United States

### :test_tube: Cross-Country Analysis

To compare multiple countries:

1. Load the three consolidated files.
2. Add a `Country` column to each table.
3. Concatenate them into a single dataframe or table.
4. Perform grouped analysis by `Country`, `Region`, `Type`, `Month`, or `Year`.

### :mag: Typical Analytical Workflows
- Count listings by `Region`.
- Track listing volumes by `Month` and `Year`.
- Compare prices by `Type` or `Country`.
- Identify records with `No Reviews`.
- Explore the distribution of guest capacity using `Guests`.

---

## :file_cabinet: Data Formats

### :page_facing_up: Published CSV Files

Each CSV file is a flat tabular dataset with one row per listing record and the following columns:

- `Region`
- `Name`
- `Type`
- `Guests`
- `Bedrooms`
- `Price`
- `Reviews`
- `Month`
- `Year`

### :bookmark_tabs: Semantic Notes
- `Region` identifies the state, province, or territorial unit within the country-level file.
- `Name` keeps the visible listing title captured during extraction.
- `Type`, `Bedrooms`, and `Month` were standardized to English.
- `Reviews` may contain the standardized label `No Reviews`.
- Rows should be interpreted as historical listing records tied to a time reference, not as a deduplicated panel of unique properties.

---

## :open_file_folder: Project Architecture

```text
ALANA/
├── Canada.csv
├── Mexico.csv
├── USA.csv
├── LICENSE
├── README.md
└── docs/
    ├── logo/
    │   └── logo.png
    └── team/
        ├── gtinoco.webp
        └── nstinoco.webp
```

### :books: Architecture Notes
- The repository contains the three consolidated country-level datasets, the license, the main README, and the visual assets used by the documentation.
- `docs/` stores assets used by the README.

---

## :books: Methodology

The dataset published in this repository is the result of a multi-stage extraction and review workflow designed to recover historical Airbnb listing information at the subnational level and later consolidate it into country-level datasets. The process followed five broad stages:

1. Analysis of Airbnb search URLs and filtering strategies.
2. Extraction of HTML source code from search result pages.
3. Extraction of individual HTML pages for each listing.
4. Parsing of relevant HTML structures and structured data extraction.
5. Manual review, correction, and formatting into spreadsheet-ready records.

### :mag: Stage 1. Search URL Analysis and Filter Design

The first stage focused on defining search strategies capable of retrieving as many listings as possible. To do this, multiple layers of Airbnb filters were analyzed and combined in a mutually exclusive way to improve coverage and reduce missed results.

- Property-related filters were used to separate listings by accommodation type, such as houses, apartments, and rooms.
- Exclusivity-related filters were incorporated when available.
- House-rule filters such as pets allowed, smoking allowed, and events allowed were used to expand search combinations.
- Service and amenity filters such as WiFi, kitchen, or laundry were added as an additional search layer.

After defining the filter combinations, the search requests sent through the Airbnb platform were analyzed via the `GET` method in order to build the required URLs programmatically.

### :globe_with_meridians: Stage 2. Extraction of Search Result HTML

Once the search URLs were defined, a custom browser-based application was developed in Java using JavaFX to automate access to Airbnb search result pages and capture their HTML source code.

- The application iterated through the generated search URLs.
- JavaScript queries were executed inside the JavaFX browser environment to obtain the relevant page information.
- The captured data were processed to reconstruct the HTML source of each search result page.
- Each search result page was stored independently for later analysis.

These stored files were then manually inspected to identify the structural patterns necessary to extract the individual listing URLs contained in the search results.

### :house: Stage 3. Extraction of Individual Listing HTML

After collecting the URLs of individual listings, a second JavaFX-based browser application was used to visit each listing page and retrieve its HTML source.

- Each listing URL was opened remotely.
- JavaScript was again used to obtain the page content.
- The content was processed to reconstruct the corresponding HTML.
- Each listing page was stored in an independent file for detailed parsing.

This stage made it possible to move from search-result pages to listing-specific source material containing the attributes of each accommodation.

### :microscope: Stage 4. HTML Parsing and Structured Data Extraction

The individual HTML files were manually analyzed in order to detect the relevant tags, patterns, and structural elements where the desired listing attributes were embedded.

- A Java script was developed to process the files one by one.
- The script extracted the required fields from the HTML and stored them in an intermediate text-based format.
- Pattern matching relied on the `Shift-Or` string-processing method to keep the parsing stage efficient and close to linear behavior.

At the end of this phase, the extracted information was available in a plain-text representation suitable for validation and further transformation.

### :pencil2: Stage 5. Manual Review and Spreadsheet Formatting

The extracted records were then reviewed manually in order to improve the quality of the dataset before publication.

- Corrupted records were corrected when possible.
- Structural issues in listing entries were adjusted.
- Repeated listings were removed.
- Obvious noise and records associated with unavailable or invalid listings were filtered out.

After this review stage, a Java script converted the curated information into spreadsheet-ready files. Those reviewed records were then used to build the consolidated country-level CSV files distributed in this repository.

### :hammer_and_wrench: Final Publication Workflow
- Historical records were consolidated at the country level.
- Column names and categorical labels were standardized.
- Numeric fields were normalized where appropriate.
- Invalid, broken, empty, or clearly corrupted rows were removed or repaired when feasible.

---

## :open_file_folder: Dataset Overview

### :bar_chart: Current Coverage

| File | Country | Rows |
| --- | --- | ---: |
| `Canada.csv` | Canada | 30,640 |
| `Mexico.csv` | Mexico | 58,965 |
| `USA.csv` | United States | 92,251 |

### :bar_chart: Aggregate Size

| Metric | Value |
| --- | ---: |
| Countries | 3 |
| Final CSV files | 3 |
| Total rows | 181,856 |
| Shared columns per file | 9 |

### :mag: Coverage Notes
- These files represent historical extraction snapshots rather than live Airbnb data.
- Geographic coverage varies because listing availability differs by region and extraction context.
- The repository organizes the available data at the country level.

---

## :bookmark: Data Dictionary

| Column | Final representation | Description |
| --- | --- | --- |
| `Region` | Text | State, province, or territorial unit associated with the listing |
| `Name` | Text | Public-facing title or name of the listing |
| `Type` | Text | Standardized accommodation type in English |
| `Guests` | Integer | Reported guest capacity |
| `Bedrooms` | Text | Standardized bedroom description, for example `2 bedrooms` |
| `Price` | Decimal-formatted numeric | Captured listing price at extraction time |
| `Reviews` | Integer or `No Reviews` | Review count or standardized missing-review marker |
| `Month` | Text | Reference month in English |
| `Year` | Integer | Reference year |

### :information_source: Formatting Notes
- `Guests` is normalized as an integer.
- `Year` is normalized as an integer.
- `Reviews` is normalized as an integer when a numeric value exists.
- `Price` is intentionally preserved in decimal-formatted numeric form.
- `Bedrooms` remains textual to preserve its descriptive meaning after normalization.
- Records are sorted chronologically to facilitate temporal inspection and downstream analysis.

---

## :white_check_mark: Data Quality and Standardization

During repository preparation, the final files were cleaned and standardized to improve consistency, usability, and portability:

- Column names were translated and aligned to English.
- Category labels in `Type`, `Bedrooms`, and `Month` were standardized.
- Review labels were normalized to the English marker `No Reviews`.
- Integer-style normalization was applied to `Guests`, `Reviews`, and `Year` where applicable.
- File naming inconsistencies for regional sources were corrected during preprocessing.
- Malformed, truncated, empty, duplicated, or structurally broken records were reviewed and handled before consolidation.
- Country-level files were checked for schema consistency after consolidation.

---

## :warning: Limitations

- This dataset is **not** an official Airbnb product.
- The files reflect historical extraction outputs and should not be interpreted as current platform conditions.
- Currency is not explicitly documented inside the CSV files.
- Some listings may have missing values in fields such as `Type` or `Reviews`.
- `Price` should be interpreted cautiously because it reflects captured values at extraction time.
- Listing names are not guaranteed to be globally unique identifiers.
- The same accommodation can appear in multiple time snapshots when it remained available across periods.

---

## :compass: Recommended Use

- Use `Canada.csv`, `Mexico.csv`, and `USA.csv` as the primary entry points for analysis.
- Add a `Country` field manually if you want to combine all three datasets.
- Treat the repository as a cleaned historical dataset rather than a real-time market feed.
- Document any additional transformations you apply after cloning or downloading the files.

---

## :scientist: Authors

<div align="center">

### :star2: Project Authors
*Researchers contributing to the ALANA dataset*

</div>

<table align="center">
  <thead>
    <tr>
      <th align="center" width="120">Photo</th>
      <th align="left">Author</th>
      <th align="left">Contribution</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" width="120">
        <img src="docs/team/nstinoco.webp" alt="Dr. Narciso Salvador Tinoco Guerrero" width="96" height="96" style="border-radius: 50%;">
      </td>
      <td>
        <b>Dr. Narciso Salvador Tinoco Guerrero</b>
      </td>
      <td>
        Data extraction, review, and research support
      </td>
    </tr>
    <tr>
      <td align="center" width="120">
        <img src="docs/team/gtinoco.webp" alt="Dr. Gerardo Tinoco Guerrero" width="96" height="96" style="border-radius: 50%;">
      </td>
      <td>
        <b>Dr. Gerardo Tinoco Guerrero</b>
      </td>
      <td>
        Data processing, standardization, consolidation, and repository curation
      </td>
    </tr>
  </tbody>
</table>

---

## :memo: Citation and Usage Notes

If you use this repository in academic, technical, or applied work:

- cite the repository `https://github.com/gstinoco/ALANA` or the archived release you used,
- indicate the access date,
- describe any additional cleaning, enrichment, or filtering steps you performed,
- clarify that the dataset is not an official Airbnb publication, and
- describe the extraction and review workflow summarized in this README when methodological context is needed.

### Suggested Citation

```text
Tinoco-Guerrero, G., and Tinoco Guerrero, N. S. (2026). ALANA: Airbnb Listings Atlas of North America. GitHub repository. https://github.com/gstinoco/ALANA
```

### BibTeX

```bibtex
@misc{tinoco2026alana,
  author       = {Narciso Salvador Tinoco Guerrero and Gerardo Tinoco-Guerrero},
  title        = {ALANA: Airbnb Listings Atlas of North America},
  year         = {2026},
  howpublished = {\url{https://github.com/gstinoco/ALANA}},
  note         = {GitHub repository}
}
```

---

## :page_with_curl: License

This repository is distributed under the **MIT License**.

- See the [`LICENSE`](LICENSE) file for the full text.
- The intended public repository location is `https://github.com/gstinoco/ALANA`.

---

## :pray: Acknowledgments

<div align="center">

### :heart: Institutional Support and Collaborations
*We gratefully acknowledge the institutions and collaborations that support the research environment around this project*

</div>

### :classical_building: Institutional Support

<table align="center" width="100%" cellspacing="14">
  <tr>
    <td width="33%" valign="top">
      <div style="border: 1px solid #d0d7de; border-radius: 12px; padding: 16px;">
        <div align="center">
          <b>🎓 UMSNH</b><br/>
          <sub>Universidad Michoacana de San Nicolas de Hidalgo</sub><br/><br/>
          <a href="http://www.umich.mx"><img alt="Website" src="https://img.shields.io/badge/Website-UMSNH-1A3A6B?style=flat-square"></a>
          <img alt="Type: University" src="https://img.shields.io/badge/Type-University-1A3A6B?style=flat-square">
        </div>
        <br/>
        <b>Support highlights</b>
        <ul>
          <li>Academic environment for research development</li>
          <li>Institutional support for scientific work and dissemination</li>
        </ul>
      </div>
    </td>
    <td width="33%" valign="top">
      <div style="border: 1px solid #d0d7de; border-radius: 12px; padding: 16px;">
        <div align="center">
          <b>🔬 SECIHTI</b><br/>
          <sub>Secretaria de Ciencia, Humanidades, Tecnologia e Innovacion</sub><br/><br/>
          <img alt="Type: Government" src="https://img.shields.io/badge/Type-Government-2D6A4F?style=flat-square">
          <img alt="Support: Research" src="https://img.shields.io/badge/Support-Scientific%20Research-40916C?style=flat-square">
        </div>
        <br/>
        <b>Support highlights</b>
        <ul>
          <li>Support for science, humanities, technology, and innovation activities</li>
          <li>Contribution to an open and research-oriented ecosystem</li>
        </ul>
      </div>
    </td>
    <td width="33%" valign="top">
      <div style="border: 1px solid #d0d7de; border-radius: 12px; padding: 16px;">
        <div align="center">
          <b>🏢 SIIIA MATH</b><br/>
          <sub>Soluciones en Ingenieria e Inteligencia Artificial</sub><br/><br/>
          <a href="http://www.siiia.com.mx"><img alt="Website" src="https://img.shields.io/badge/Website-SIIIA%20MATH-0B1B3A?style=flat-square"></a>
          <img alt="Type: Research and Industry" src="https://img.shields.io/badge/Type-Research%20%26%20Industry-0B1B3A?style=flat-square">
        </div>
        <br/>
        <b>Support highlights</b>
        <ul>
          <li>Applied perspective for data-driven research</li>
          <li>Collaboration between academic and technical environments</li>
        </ul>
      </div>
    </td>
  </tr>
</table>

### :handshake: Collaborations

- Collaboration between academic research and applied technical practice helped shape the preparation and publication of this dataset.
- The project benefits from an environment that connects data extraction, standardization, and open dissemination workflows.

---

## :email: Contact & Support

<div align="center">

*Contact channels for academic questions, repository issues, and collaboration opportunities*

[![Issues](https://img.shields.io/badge/GitHub-Issues-24292f?style=flat-square&logo=github)](https://github.com/gstinoco/ALANA/issues)
[![Email](https://img.shields.io/badge/Email-Support-blue?style=flat-square)](mailto:gerardo.tinoco@umich.mx)

</div>

<table align="center" width="100%" cellspacing="14">
  <tr>
    <td valign="top" style="border: 1px solid #d0d7de; border-radius: 12px; padding: 16px;">
      <div align="center">
        <b>Primary Contact</b><br/>
        <sub>Repository coordination and research inquiries</sub>
      </div>
      <br/>
      <b>Dr. Gerardo Tinoco-Guerrero</b><br/>
      <sub>Morelia, Michoacan, Mexico</sub>
      <br/><br/>
      <div align="center">
        <a href="mailto:gerardo.tinoco@umich.mx"><img alt="Email" src="https://img.shields.io/badge/Email-gerardo.tinoco%40umich.mx-blue?style=flat-square"></a>
        <a href="http://www.siiia.com.mx"><img alt="SIIIA MATH" src="https://img.shields.io/badge/Affiliation-SIIIA%20MATH-0B1B3A?style=flat-square"></a>
        <a href="http://www.umich.mx"><img alt="UMSNH" src="https://img.shields.io/badge/Affiliation-UMSNH-1A3A6B?style=flat-square"></a>
      </div>
    </td>
  </tr>
  <tr>
    <td valign="top" style="border: 1px solid #d0d7de; border-radius: 12px; padding: 16px;">
      <div align="center">
        <b>Additional Academic Contact</b><br/>
        <sub>Methodological questions and academic communication</sub>
      </div>
      <br/>
      <b>Dr. Narciso Salvador Tinoco Guerrero</b><br/>
      <sub>Morelia, Michoacan, Mexico</sub>
      <br/><br/>
      <div align="center">
        <a href="mailto:narciso.tinoco@umich.mx"><img alt="Email" src="https://img.shields.io/badge/Email-narciso.tinoco%40umich.mx-blue?style=flat-square"></a>
        <a href="http://www.umich.mx"><img alt="UMSNH" src="https://img.shields.io/badge/Affiliation-UMSNH-1A3A6B?style=flat-square"></a>
      </div>
    </td>
  </tr>
  <tr>
    <td valign="top" style="border: 1px solid #d0d7de; border-radius: 12px; padding: 16px;">
      <div align="center">
        <b>Support Channels</b><br/>
        <sub>Bug reports, documentation issues, and collaboration requests</sub>
      </div>
      <br/>
      <div align="center">
        <a href="https://github.com/gstinoco/ALANA/issues"><img alt="Open an Issue" src="https://img.shields.io/badge/Open-Issue-24292f?style=flat-square&logo=github"></a>
        <a href="mailto:gerardo.tinoco@umich.mx"><img alt="Send Email" src="https://img.shields.io/badge/Send-Email-blue?style=flat-square"></a>
        <a href="mailto:gerardo.tinoco@umich.mx?subject=ALANA%20Collaboration"><img alt="Request Collaboration" src="https://img.shields.io/badge/Request-Collaboration-2E8B57?style=flat-square"></a>
      </div>
      <br/>
      <ul>
        <li><b>Issues</b> for repository problems or suggested improvements</li>
        <li><b>Email</b> for academic, technical, or reuse-related questions</li>
        <li><b>Collaboration</b> for research partnerships and related initiatives</li>
      </ul>
    </td>
  </tr>
</table>

---

## :speech_balloon: FAQ

### What is ALANA?
ALANA stands for **Airbnb Listings Atlas of North America**.

### What does this repository contain?
It contains three final consolidated CSV files, one per country, plus repository documentation describing the schema, preparation process, and extraction methodology.

### Are the data current?
No. The repository contains historical extraction snapshots, not live Airbnb data.

### Can the three country files be merged?
Yes. They share the same schema and can be concatenated after adding a `Country` column if needed.

### Is additional cleaning required before analysis?
In most cases, the final files are ready for direct analysis, although your specific workflow may still require custom transformations.

---

<div align="center">

*Supporting open and reusable historical tourism data for research and analysis*

[![GitHub stars](https://img.shields.io/github/stars/gstinoco/ALANA?style=social)](https://github.com/gstinoco/ALANA/stargazers) [![GitHub forks](https://img.shields.io/github/forks/gstinoco/ALANA?style=social)](https://github.com/gstinoco/ALANA/network/members) [![GitHub watchers](https://img.shields.io/github/watchers/gstinoco/ALANA?style=social)](https://github.com/gstinoco/ALANA/watchers)

<br/>

<b>If this dataset supports your work, please consider giving the repository a star.</b>

</div>

# 📊 Sanctions Through Statistics

**Personal portfolio version of Sanctions Through Statistics, originally developed as a team project (PompeuFarrers) for the Data4Good Hackathon 2026 at Hertie School.**

> **Hertie School · Data4Good Festival 2026**
>
> **Challenge 2 — Tracking Power: What We Can and Can't See**
> 
> Built with **Python · Pandas · OpenSanctions · API · Data Analysis**

---

## Project Overview

Politically Exposed Persons (PEPs) are individuals who hold or have held prominent public positions and are an important part of transparency and anti-money-laundering efforts.

However, PEP and sanctions data is fragmented across countries, with differences in coverage, government structures and enforcement.

This project investigates one main question:

> **Is there a pattern behind PEPs with sanctions?**

We analysed the relationship between PEP populations and sanctions across **ten globally influential countries**, selected based on population and relevance, and additionally included **Spain** as our national context.

The goal was not simply to identify sanctioned individuals, but to understand how sanctions exposure varies across countries and what those differences might reveal about political and geopolitical structures.

---

## What We Did

We developed a complete analytical workflow combining OpenSanctions PEP and sanctions data with external population data:

- Downloaded and processed OpenSanctions PEP data.
- Extracted PEPs by country.
- Matched PEPs against sanctions data using the **OpenSanctions Match API**.
- Filtered matches to improve the reliability of the results.
- Calculated the percentage of PEPs with sanctions for each country.
- Compared sanctions counts with population size.
- Analysed sanctions per capita across different country groups.
- Interpreted the results in their geopolitical and institutional context.

The analysis was designed to distinguish between the **number of PEPs in a country** and the **proportion of those PEPs appearing in sanctions datasets**.

---

## Data Processing

The workflow can be summarised as:

1. **OpenSanctions PEP dataset**  
   Download and clean the global PEP dataset.

2. **Country filtering**  
   Extract PEPs associated with each country under analysis.

3. **Entity matching**  
   Use the OpenSanctions Match API to identify potential matches between PEPs and sanctioned entities.

4. **Filtering**  
   Apply matching and country criteria to obtain higher-confidence results.

5. **Analysis**  
   Calculate the percentage of PEPs matched with sanctions and compare countries.

6. **Population analysis**  
   Combine sanctions data with population data to investigate sanctions per capita.

---

## Results

The results show substantial differences in the proportion of PEPs appearing in sanctions datasets.

| Country | PEPs | Matches | Percentage |
| ------- | ---: | ------: | ---------: |
| 🇺🇸 United States | 58,307 | 1,828 | 3.14% |
| 🇨🇳 China | 13,276 | 882 | 6.64% |
| 🇷🇺 Russia | 13,950 | 3,383 | 24.25% |
| 🇬🇧 United Kingdom | 7,038 | 70 | 0.99% |
| 🇩🇪 Germany | 9,248 | 25 | 0.37% |
| 🇰🇷 South Korea | 2,465 | 7 | 0.28% |
| 🇫🇷 France | 59,698 | 65 | 0.10% |
| 🇯🇵 Japan | 2,864 | 1 | 0.03% |
| 🇸🇦 Saudi Arabia | 543 | 33 | 6.08% |
| 🇮🇱 Israel | 820 | 12 | 1.46% |
| 🇪🇸 Spain | 1,750 | 10 | 0.57% |

The results show that countries with larger PEP populations do not necessarily have higher sanction-match percentages.

For example, the United States and France have very large PEP populations but relatively low match percentages, while Russia, China and Saudi Arabia show substantially higher proportions.

---


## Population & Sanctions

We also examined the relationship between sanctions and population size.

Countries with the highest sanctions-per-capita coefficients were predominantly **small countries and island states**, where relatively small populations can amplify per-capita measures.

However, some larger countries also showed elevated coefficients, suggesting that population alone cannot explain the distribution of sanctions.

This points towards additional factors such as **geopolitical position, economic influence and international enforcement dynamics**.

---

## Key Findings

### PEP population does not directly predict sanctions exposure

Countries with large numbers of PEPs do not necessarily have high proportions of sanctioned PEPs.

Government size and complexity appear to influence the number of PEPs recorded, while other factors may influence their representation in sanctions datasets.

### Sanctions exposure varies strongly across countries

The proportion of PEPs matched to sanctions varies considerably between countries, with Russia showing a substantially higher ratio than countries such as France, Germany or Japan.

### Sanctions data reflects geopolitical context

The distribution of sanctions cannot be interpreted independently from international relations and the countries or institutions responsible for issuing sanctions.

### Per-capita measures require caution

Small countries can appear disproportionately high in sanctions-per-capita rankings because relatively small absolute numbers are divided by very small populations.

---

## Conclusions

This project shows that transparency datasets such as PEP and sanctions lists reveal information about **global power structures as well as individual accountability**.

Sanction exposure among PEPs is unevenly distributed and appears to be influenced by factors including:

- Government structure
- Geopolitical alignment
- International relations
- Enforcement dynamics
- Population size

Importantly, **sanctions data should not be interpreted as a direct measure of corruption or wrongdoing**.

Meaningful analysis requires combining sanctions data with political, institutional and demographic context.

The project also highlights the importance of more transparent and globally consistent public data on political power and accountability.

---

## My Contribution

As part of Team PompeuFarrers, my work focused on the data analysis and processing pipeline:

- Processed and analysed OpenSanctions PEP and sanctions datasets.
- Worked with the OpenSanctions API for entity matching.
- Developed the data-processing workflow used to compare PEPs and sanctions across countries.
- Applied filtering and matching criteria to improve the reliability of the results.

---

## Project Files

- `SanctionsThroughStatistics.ipynb` : Contains the complete data-processing and analysis workflow.

- `Report.pdf` : Detailed explanation of the methodology, findings and conclusions.

- `SanctionsThroughStatistics_Slides.pdf` : Final presentation developed for the Data4Good Hackathon.

---

## Team

**PompeuFarrers**

- Emma Leroux
- Mikel Carbonés
- Pep Margarit
- Guillem Arevalo
- Natalia Grandas
- Livia Fernández

---

## Data & Tools

- **OpenSanctions** — PEP and sanctions data and entity matching
- **Python**
- **Pandas**
- **Requests**
- **Data analysis & visualisation**

---

## Limitations

The results should be interpreted with caution.

PEP and sanctions datasets differ in coverage and data quality across countries. A match indicates an entity appearing in both datasets; it does not by itself establish wrongdoing or corruption.

Similarly, differences in sanctions exposure may reflect geopolitical and institutional factors rather than differences in underlying behaviour.

---

# LACES: Adaptive Data Collection for Latin-American Community-sourced Evaluation of Stereotypes

> Guido Ivetta, Pietro Palombini, Sofía Martinelli, Marcos J Gomez, M. María Echeveste, Sunipa Dev, Vinodkumar Prabhakaran, & Luciana Benotti. (2026)

Pre-print 🔗 : [https://arxiv.org/abs/2510.24958](https://arxiv.org/abs/2510.24958)

If you use or discuss our survey in your work, please use the following citation:

```bibtex
@misc{ivetta2026adaptivedatacollectionlatinamerican,
      title={Adaptive Data Collection for Latin-American Community-sourced Evaluation of Stereotypes (LACES)}, 
      author={Guido Ivetta and Pietro Palombini and Sofía Martinelli and Marcos J Gomez and M. María Echeveste and Sunipa Dev and Vinodkumar Prabhakaran and Luciana Benotti},
      year={2026},
      eprint={2510.24958},
      archivePrefix={arXiv},
      primaryClass={cs.CY},
      url={https://arxiv.org/abs/2510.24958}, 
}
```

---

Welcome to the official repository for **LACES**, a stereotype association dataset specifically curated for 15 Latin American countries. This dataset was developed to bridge the geo-cultural gap in Natural Language Processing (NLP) resources, which often focus on U.S. and English-centric demographics.

---

## 🌏 Overview

**LACES** contains **4,789 stereotype associations** manually created and annotated by 83 participants from across Latin America. Unlike traditional static datasets, LACES was built using a **novel adaptive data collection methodology**. This approach integrates the sourcing of new stereotypes and the validation of existing ones into a single, unified workflow, resulting in a more diverse and efficient resource.

### Key Features

* **Broad Coverage**: Includes 120 identities and 842 attributes across various sociodemographic axes.

* **Multilingual**: Contains 2,437 pairs in Spanish and 2,352 in English.

* **Adaptive Sampling**: The methodology prioritizes in-group representation, validation coverage for sparse data, and real-time session recency.

* **High Precision**: Despite having fewer data points than larger benchmarks, LACES contains a higher percentage of **unique concepts** compared with similar benchmarks.

---

## 📊 Dataset Topic Distribution

The stereotypes in LACES cover a wide range of topics, categorized to facilitate detailed analysis.

| Topic | Frequency ($n$) | In-Group (IG) % | IG Association Sample | Out-Group (OG) % | OG Association Sample |
| --- | --- | --- | --- | --- | --- |
| **Cooking and Food** | 792 | 39.64% | (CHL, piscola) | 60.36% | (PRY, tortafrita) |
| **Positive Traits** | 641 | 27.78% | (URY, hospitable) | 72.22% | (JPN, problem solvers) |
| **Geography, Buildings, Landmarks** | 609 | 26.21% | (MEX, archaeology) | 73.79% | (BRA, Cristo Luz) |
| **Economy** | 591 | 8.88% | (PER, cheap tourism) | 91.12% | (AUS, work & holiday) |
| **People & Everyday Life** | 571 | 13.08% | (CRI, ecological) | 86.92% | (CHN, work culture) |
| **Tradition, Art, History** | 388 | 26.27% | (CHL, rodeo) | 73.73% | (GRC, sirtaki) |
| **Negative Traits** | 338 | 23.66% | (COL, fallacious) | 76.34% | (DEU, rigid minded) |
| **Politics & Governance** | 239 | 18.57% | (ARG, best education) | 81.43% | (CUB, public health) |
| **Sports & Recreation** | 223 | 50.65% | (COL, football fans) | 49.35% | (RUS, athletes) |
| **Other** | 137 | 16.67% | (BRA, dental health) | 83.33% | (ISL, attractive people) |
| **Public Figures & Pop Culture** | 130 | 63.64% | (URY, Gardel) | 36.36% | (CUB, Fidel Castro) |
| **Neutral Traits** | 130 | 34.57% | (PAN, serious) | 65.43% | (IRL, quiet people) |

---

## 📂 Data Structure

The primary data file is located at `LACES_DATASET.csv`. Each entry is a JSON object representing an original datapoint or an unfolded association.

### Field Descriptions

| Field | Type | Description |
| --- | --- | --- |
| `annotator_nationalities` | List | Self-reported nationalities of the annotator. |
| `annotator_regions` | List | Self-reported regions. |
| `annotator_understood_languages` | List | Language codes (e.g., `"en"`, `"es"`, `"pt"`). |
| `data_point_nationality` | String | Nationality featured in the validation pair. |
| `data_point_attribute` | String | Attribute featured in the validation pair. |
| `data_point_language` | String | Language of the text (e.g., `"es"`). |
| `stereotype_score` | Integer | Likert scale (1–5) for "known association in my region." |
| `new_association` | Boolean | `true` if unfolded from an association; `false` if original. |

---

## ⚖️ License

This dataset is released under the **CC BY-SA 4.0** license.

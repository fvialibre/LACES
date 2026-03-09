Paper link: [https://arxiv.org/abs/2510.24958](https://arxiv.org/abs/2510.24958)

# LACES: Adaptive Data Collection for Latin-American Community-sourced Evaluation of Stereotypes

Welcome to the official repository for **LACES**, a stereotype association dataset specifically curated for 15 Latin American countries. This dataset was developed to bridge the geo-cultural gap in Natural Language Processing (NLP) resources, which often focus on U.S. and English-centric demographics.

---

## 🌏 Overview

**LACES** contains **4,789 stereotype associations** manually created and annotated by 83 participants from across Latin America. Unlike traditional static datasets, LACES was built using a **novel adaptive data collection methodology**. This approach integrates the sourcing of new stereotypes and the validation of existing ones into a single, unified workflow, resulting in a more diverse and efficient resource.

### Key Features

* **Broad Coverage**: Includes 120 identities and 842 attributes across various sociodemographic axes.

* **Multilingual**: Contains 2,437 pairs in Spanish and 2,352 in English.

* **Adaptive Sampling**: The methodology prioritizes in-group representation, validation coverage for sparse data, and real-time session recency.

* **High Precision**: Despite having fewer data points than larger benchmarks, LACES contains a higher percentage of **unique concepts (29.74%)**.

---

## 📊 Dataset Topic Distribution

The stereotypes in LACES cover a wide range of topics, categorized to facilitate detailed analysis.

| Topic | Frequency (n) | In-Group (IG) % | Example (Nationality, Attribute) |
| --- | --- | --- | --- |
| **Cooking and Food** | 792 | 39.64% | (CHL, piscola) |
| **Positive Traits** | 641 | 27.78% | (URY, hospitable) |
| **Geography & Landmarks** | 609 | 26.21% | (MEX, archaeology) |
| **Economy** | 591 | 8.88% | (PER, cheap tourism) |
| **People & Everyday Life** | 571 | 13.08% | (CRI, ecological) |
| **Tradition, Art, History** | 388 | 26.27% | (CHL, rodeo) |
| **Negative Traits** | 338 | 23.66% | (COL, fallacious) |
| **Sports & Recreation** | 223 | 50.65% | (COL, football fans) |

---

## 📂 Data Structure

The primary data file is located at `data/unfolded_logs.jsonl`. Each entry is a JSON object representing an original datapoint or an unfolded association.

### Field Descriptions

| Field | Type | Description |
| --- | --- | --- |
| `source` | String | Event of origin: `"khipu"` or `"hackaton"`. |
| `timestamp` | String | ISO 8601 datetime of the record. |
| `token_id` | String | Unique identifier for the annotator. |
| `annotator_nationalities` | List | Self-reported nationalities of the annotator. |
| `annotator_regions` | List | Self-reported regions. |
| `annotator_understood_languages` | List | Language codes (e.g., `"en"`, `"es"`, `"pt"`). |
| `data_point_nationality` | String | Nationality featured in the validation pair. |
| `data_point_attribute` | String | Attribute featured in the validation pair. |
| `data_point_language` | String | Language of the text (e.g., `"es"`). |
| `stereotype_score` | Integer | Likert scale (1–5) for "known association in my region." |
| `new_association` | Boolean | `true` if unfolded from an association; `false` if original. |

---

## 📜 Citation

If you use this dataset in your research, please cite our paper:

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

## ⚖️ License

This dataset is released under the **CC BY-SA 4.0** license.

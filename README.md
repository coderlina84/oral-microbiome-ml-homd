# Machine Learning Classification of Periodontal Pathogens via HOMD Biomarkers

## Abstract
Periodontitis is a chronic inflammatory oral disease driven by dysbiosis within the subgingival microbiome. Identifying genomic signatures that distinguish high-risk pathogens from benign commensal flora is critical for computational bioinformatic diagnostics. 

In this study, genomic metadata—including base composition (GC%), sequence length, and contig counts—was extracted from the NIH Human Oral Microbiome Database (HOMD). Bacterial taxa were labeled by disease risk based on membership in inflammatory red and orange bacterial complexes (*Porphyromonas*, *Treponema*, *Tannerella*, *Prevotella*, *Fusobacterium*, *Aggregatibacter*). 

A Random Forest classifier was trained on an 80/20 train-test split. The model identified **GC content (58% feature importance)** and **total sequence length (28%)** as the primary predictive genomic biomarkers separating pathogens from commensals. Pathogens exhibited a lower mean GC content (39.14% vs. 45.70%) and distinct sequence length constraints. These findings demonstrate that machine learning models can effectively isolate risk-associated DNA signatures using database metadata without requiring full raw sequence alignment.

---

## Key Results & Biomarker Importance

| Genomic Feature | Random Forest Importance | Biological Significance |
| :--- | :--- | :--- |
| **GC Content (GC%)** | **58%** | Major nucleotide composition divergence in key pathogens. |
| **Total Sequence Length** | **28%** | Genome streamlining in specialized subgingival bacteria. |
| **Contig Count** | **14%** | Secondary signal related to assembly complexity. |

### Summary Statistics (HOMD Database)
* **Commensal / Normal Flora:** Mean GC% = 45.70%, Mean Length = 2.49 Mb
* **High-Risk Pathogens:** Mean GC% = 39.14%, Mean Length = 2.46 Mb

---

## Feature Importance Plot

![Biomarker Feature Importance](homd_final_importance.png)

---

## Tech Stack & Dependencies
* **Language:** Python 3.x
* **Libraries:** pandas, numpy, matplotlib, scikit-learn
* **Data Source:** [Human Oral Microbiome Database (HOMD)](https://www.homd.org/)

---

## How to Run the Code

1. Clone this repository:
   ```bash
   git clone [https://github.com/coderlina84/oral-microbiome-ml-homd.git](https://github.com/coderlina84/oral-microbiome-ml-homd.git)

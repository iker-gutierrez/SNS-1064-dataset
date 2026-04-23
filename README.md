# SNS-1064: Clinical dataset for RAG-based QA

SNS-1064 is a structured Spanish clinical dataset designed for Retrieval-Augmented Generation (RAG) and question answering (QA) systems. It is derived from six clinical practice guidelines from the Spanish National Health System.

## Dataset Overview

- Samples: 1,064 QA instances  
- Domains: anxiety, diabetes, stroke (ictus), palliative care  
- Structure:
  - `guidebook` — source document  
  - `topic` — clinical context  
  - `question` — main question  
  - `subquestion` — optional refinement  
  - `judgement` — short clinical answer  
  - `evidence` — supporting text  
  - `considerations` — optional interpretation  

The dataset explicitly separates answers from their supporting evidence, enabling grounded and explainable QA.

---

## Repository Contents

- `dataset.csv` — full dataset  
- `train_df.csv` — training split (80%)  
- `test_df.csv` — test split (20%, manually curated)  
- `clinical_guidebooks_txt.zip` — source texts (TXT format)  
- `datasetting.ipynb` — dataset construction pipeline  
- `paper.pdf` — full description of the dataset  

---

## Construction Pipeline

The dataset is built using a rule-based pipeline:

1. PDF → TXT conversion.
2. Text cleaning (whitespace and bullet removal)
3. Regex-based text segmentation.
4. Sample filtering (removal of non-informative placeholders).
5. Manual curation (entire test set, partial training set).

---

## Use Case

SNS-1064 is designed for:
- RAG-based clinical QA
- evidence-grounded generation
- explainable NLP in healthcare

The separation between `judgement` and `evidence` supports traceability and interpretability, which are critical in medical applications.

---

## Remarks

- The test set is fully curated to ensure reliable evaluation  .
- Some noise may remain in the training set.

- 
(See `paper.pdf` for full details.)

---

## Contact

Iker Gutierrez Fandiño  
University of the Basque Country (EHU)  
igutierrez134@ikasle.ehu.eus


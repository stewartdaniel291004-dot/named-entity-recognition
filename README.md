
# Named Entity Recognition (NER)

## Project Overview
This project explores Named Entity Recognition (NER) using Python
and spaCy. It identifies people, organizations, and locations in
news-style text and compares rule-based recognition with a
pretrained spaCy model.

## Objectives
- Identify named entities in text.
- Implement rule-based NER using spaCy EntityRuler.
- Extract entities using a pretrained spaCy model.
- Visualize detected entities using displaCy.
- Evaluate entity recognition against CoNLL-2003 annotations.
- Compare performance across entity categories.

## Technologies
- Python
- spaCy
- Pandas
- Matplotlib
- Hugging Face Datasets
- CoNLL-2003

## Methods
### Rule-Based NER
Uses manually defined entity patterns. It is transparent and
easy to customize but may miss entities not included in the rules.

### Model-Based NER
Uses spaCy's pretrained English model to identify entities
from context.

## Preliminary Evaluation
Evaluation was performed on the first 500 examples of the
CoNLL-2003 test split.

| Entity | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Person (PER) | 0.833 | 0.597 | 0.696 |
| Organization (ORG) | 0.312 | 0.255 | 0.281 |
| Location (LOC) | 0.758 | 0.719 | 0.738 |
| Miscellaneous (MISC) | 0.397 | 0.385 | 0.391 |

These are preliminary entity-level results, not full-test-set
benchmark scores. Differences in annotation schemes and entity
boundaries may affect the comparison.

## Limitations
- The evaluation uses only a subset of the test dataset.
- spaCy's model was trained separately from CoNLL-2003.
- Entity-category mappings may not perfectly match.
- Rule-based performance depends on the patterns supplied.

## Future Improvements
- Evaluate the complete test split.
- Improve entity-span alignment and label mapping.
- Compare multiple pretrained NER models.
- Expand rule-based patterns.

## Files
- `named_entity_recognition.ipynb` — project notebook
- `ner_evaluation_results.csv` — preliminary evaluation results

## Author
Stewart Daniel

# ESG-En Dataset Samples

- Dataset name: `ESG-En`
- Source: `dataset/Cls_reports/Manufacturing/`
- Base files: each split was sampled from the corresponding `train.csv`
- Sampling: each file contains 100 sampled rows
- Note: only rows with non-empty labels were sampled
- Included metadata: `id`, `year`, `report`, `sector`, `industry`, `company`, `sentence`, `token_count`, `label`, `label_source`

- `ESG-En_bronze_sample_100.csv`
  - from `bronze/train.csv`
- `ESG-En_bronze_plus_sample_100.csv`
  - from `bronze_plus/train.csv`
- `ESG-En_silver_sample_100.csv`
  - from `silver/train.csv`
- `ESG-En_silver_plus_sample_100.csv`
  - from `silver_plus/train.csv`

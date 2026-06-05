# ESG-En Public Release

This folder contains only the materials that are currently intended for public release.

## Folder Structure

- `prompt_templates/`
  - ESG relevance, E/S/G/I labeling, debate, and judge prompt templates
- `labeling_guidelines/`
  - Label definitions and step-by-step decision criteria
- `agent_response_samples/`
  - Sample agent response CSV files
- `dataset_samples/`
  - Public sample CSV files for `ESG-En`

## Notes

- Code, full datasets, model files, and complete experimental outputs are not included.
- The sample files are intended to show the structure and output format for public reference.
- The agent samples are aligned to the same 20 `id` values across files.
- Step 1-3 agent samples are provided as separate `A/B/C/judge` files rather than merged outputs.
- The dataset samples were re-sampled from `train.csv` and include richer metadata such as `year`, `report`, `industry`, `token_count`, and `label_source`.
- The public dataset name is presented as `ESG-En`.

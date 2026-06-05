
# ESG-En Sample Artifact Release

This repository provides sample artifacts associated with the paper **“TRAE: Trustworthy Automated ESG Annotation via Multi-Agent Consensus and Confidence Assessment.”** It is intended to support transparency and public reference by sharing representative prompts, annotation guidelines, agent response samples, and dataset samples from the ESG-En construction process.

This folder contains only the materials that are currently intended for public release. The complete code and data resources will be released in the final version.

## Folder Structure

- `agent_response_samples/`
  - Sample agent response CSV files
- `dataset_samples/`
  - Public sample CSV files for `ESG-En`
- `labeling_guidelines/`
  - Label definitions and step-by-step decision criteria
- `prompt_templates/`
  - ESG relevance, E/S/G/I labeling, debate, and judge prompt templates


## Notes

- Code, full datasets, setting files, and complete experimental outputs are not included in this preliminary release.
- The sample files are intended to show the structure and output format for public reference.
- The agent samples are aligned to the same 20 `id` values across files.
- Step 1--3 agent samples are provided as separate `A/B/C/judge` files rather than merged outputs.
- The dataset samples include 100 examples for each public sample file and provide metadata such as `year`, `report`, `industry`, `token_count`, and `label_source`.
- The public dataset name is presented as `ESG-En`.


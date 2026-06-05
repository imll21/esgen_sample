# Agent Response Samples

- Sampling: same 20 `id` values reused across Step 1, Step 2, Step 3 outputs
- Format: separate files by agent role so each file preserves the original per-agent response shape

- `step1_A_sample.csv`
  - Step 1 relevance sample with original responses from agent A
- `step1_B_sample.csv`
  - Step 1 relevance sample with original responses from agent B
- `step1_C_sample.csv`
  - Step 1 relevance sample with original responses from agent C
- `step2_A_sample.csv`
  - Step 2 label sample with original responses from agent A
- `step2_B_sample.csv`
  - Step 2 label sample with original responses from agent B
- `step2_C_sample.csv`
  - Step 2 label sample with original responses from agent C
- `step3_debate_A_sample.csv`
  - Step 3 debate claim sample from agent A
- `step3_debate_B_sample.csv`
  - Step 3 debate claim sample from agent B
- `step3_debate_C_sample.csv`
  - Step 3 debate claim sample from agent C
- `step3_judge_sample.csv`
  - Final judge response sample
  - Includes `final_label`, `judge_confidence`, and `rationale`

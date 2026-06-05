# ESG Labeling Guidelines

## Overview

This public document contains the core operating criteria for the sentence-level ESG annotation pipeline.

Pipeline:
1. Step 1: ESG relevance decision (`Yes` / `No`)
2. Step 2: ESG label classification (`E` / `S` / `G` / `I`)
3. Step 3: Debate on disagreement cases followed by final judgment by the judge

## Label Definitions

- `E` (Environmental): Environmental issues such as climate change, carbon emissions, energy use, resource efficiency, waste, pollution, water use, biodiversity, and environmentally related products or technologies
- `S` (Social): Social issues such as labor, occupational safety, working conditions, human rights, diversity, supply chain social issues, customer safety, privacy, and community contribution
- `G` (Governance): Governance issues such as board oversight, audit, ethics, regulatory compliance, risk management, disclosure transparency, taxation, and compensation policy
- `I` (Irrelevant): General business descriptions, vague promotional language, or financial and marketing statements without meaningful ESG context

## Step 1. Relevance Criteria

- `Yes`: The sentence contains a concrete policy, activity, outcome, risk, system, or structure directly related to ESG
- `No`: The sentence is only a product description, general business performance statement, abstract slogan, or business content not directly tied to ESG
- `confidence`: Score in the range `0` to `1`
  - `0.90-1.00`: Very clear
  - `0.70-0.89`: Minor ambiguity
  - `0.50-0.69`: Weak evidence
  - `<0.50`: Very uncertain
- `keywords`: Key evidence words or phrases
- `rationale`: One or two sentences explaining the decision

## Step 2. Labeling Criteria

- Exactly one label must be selected
- `span` should be a short evidence phrase taken directly from the sentence
- If the sentence does not clearly map to Environmental, Social, or Governance, assign `I`
- Prefer explicit textual evidence over speculative interpretation

## Step 3. Debate and Judge

- In the debate stage, each annotator defends its prior label
- Only the sentence and the existing span/rationale may be used; no external knowledge should be introduced
- The judge makes the final decision using the following criteria
  1. Whether the evidence span is a literal substring in the sentence
  2. Whether the rationale logically connects the span and the label
  3. Whether the label precisely matches the label definition
  4. Whether the argument is sufficiently specific
  5. Whether the argument is more persuasive than competing claims

## Output Fields

### Step 1

- `relevance`
- `confidence`
- `keywords`
- `rationale`

### Step 2

- `label`
- `confidence`
- `span`
- `rationale`

### Step 3

- `final_label`
- `judge_confidence`
- `rationale` or `notes`



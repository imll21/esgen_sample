# ESG Labeling Guidelines

## Overview

This public document contains the core operating criteria for the sentence-level ESG annotation pipeline.

Pipeline:
1. Step 1: ESG relevance decision (`Yes` / `No`)
2. Step 2: ESG label classification (`E` / `S` / `G` / `I`)
3. Step 3: Debate on disagreement cases followed by final judgment by the judge

## Label Definitions

- `E` (Environmental): Environmental factors such as green management, climate change, carbon emissions, natural resources, waste, resource use, energy conservation, Carbon / GHG Emissions (Scope 1, 2, 3, Intensity), Product Carbon Footprint, Air Quality, Toxic Emissions & Hazardous Waste, Energy Management (energy use, efficiency, renewable energy), Financing Environmental Impact, Transition Risks (policy & legal, technology, market, reputation), Water & Wastewater Management / Water Stress, Materials Sourcing & Efficiency, Biodiversity & Land Use / Ecological Impacts, Waste & Packaging / Electronic Waste, Environmental Compliance, Physical Risks - Acute (floods, storms, wildfires), Physical Risks - Chronic (sea level rise, temperature & precipitation changes), Resource Efficiency (efficiency, recycling, water saving, building efficiency), Opportunities in Clean Tech / Renewable Energy / Green Building, Products & Services (low-carbon products, adaptation solutions, R&D innovation), Markets (new market access, government incentives, green finance), Resilience (resilient infrastructure, supply chain stability, resource substitution), Capital Deployment (climate-related investment & financing), Internal Carbon Price, etc.
- `S` (Social): Social factors such as human capital, community service, workers, working environment, suppliers, community contribution, human rights, gender and diversity, customer satisfaction, information protection, employment, labor management / labor practices, occupational health & safety / employee health & safety, training & education / human capital development, employee engagement, diversity & inclusion / equal opportunity / non-discrimination, freedom of association & collective bargaining, child labor, forced or compulsory labor, supply chain labor standards / supplier social assessment, human rights assessment, rights of indigenous peoples, security practices (human rights in security), community relations / local communities / human rights & community relations, controversial sourcing, public policy (participation, lobbying), socioeconomic compliance, customer health & safety / product safety & quality, product labeling & marketing practices / selling practices, customer welfare / consumer financial protection, customer privacy / data security, responsible investment (social responsibility in finance), access & affordability / access to finance / access to health care, opportunities in nutrition & health, reputation risk (stakeholder concern, consumer preference shifts), etc.
- `G` (Governance): Governance factors such as ethical management, shareholder rights, board of directors, audit organization, stakeholders, dividends, regulatory compliance, taxation, board structure & composition, nomination & selection of the highest governance body, chair of the board / independence of chair, role of board in overseeing impacts, delegation of responsibility for managing impacts, role of board in sustainability reporting, conflicts of interest, communication of critical concerns, collective knowledge of the board, board performance evaluation, ownership & control, accounting & financial transparency, business ethics (anti-corruption, integrity), competitive behavior, management of legal & regulatory environment, critical incident risk management, systemic risk management, remuneration policies (executive pay policies), process to determine remuneration, annual total compensation ratio, pay linked to climate performance, tax transparency, compliance with laws & regulations, membership associations, capital deployment, etc.
- `I` (Irrelevant): Not materially ESG-related (General business descriptions, vague promotional language, or financial and marketing statements without meaningful ESG context)

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



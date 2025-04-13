## Inspiration

The LMSYS Chatbot Arena dataset provides rich insights into how users prefer one chatbot response over another — but it's also full of subtle human biases. We noticed that users tend to favor longer, more confident-sounding responses, even when they aren't better in quality. This inspired us to ask: can we build a model that learns *true preference, not **biased preference*?

---

## What it does

Our project predicts which of two chatbot responses a user is more likely to prefer, while actively correcting for human biases like verbosity and self-enhancement. It extracts handcrafted features to quantify these biases and trains a model that focuses on content quality, not style.

---

## How we built it

We began by exploring the data and identifying common biases in human judgments. Then, we engineered features to detect:
•⁠  ⁠*Verbosity bias* (⁠ verbosity_diff ⁠, ⁠ avg_sentence_len ⁠, prompt-aware ratios)
•⁠  ⁠*Self-enhancement bias* (⁠ self_ref_diff ⁠, ⁠ self_promo_diff ⁠, ⁠ fp_ratio_diff ⁠)

We also categorized prompts using regex to provide contextual understanding (e.g., ⁠ computation ⁠, ⁠ qa ⁠, ⁠ creation ⁠). We used these features to train a classifier and visualized the outcomes using Plotly.

---

## Challenges we ran into

•⁠  ⁠Distinguishing between *useful elaboration* and *unnecessary verbosity*
•⁠  ⁠Designing features that could generalize across very different prompt types
•⁠  ⁠Avoiding overfitting to surface-level patterns like response position or phrasing

---

## Accomplishments that we're proud of

•⁠  ⁠Built a feature-driven pipeline that directly combats bias in training signals
•⁠  ⁠Successfully reduced the model’s reliance on biased cues like length and self-promotion
•⁠  ⁠Created clean, interactive visualizations to explain and validate our approach

---

## What we learned

•⁠  ⁠Even subtle biases in training labels can deeply affect downstream models
•⁠  ⁠Carefully engineered features can teach models to *focus on substance over style*
•⁠  ⁠Modeling fairness isn't just about data — it’s about framing, awareness, and design

---

## What's next for Debiasing Chatbot Preferences

•⁠  ⁠Add LLM-generated bias scores or saliency maps to capture stylistic influence
•⁠  ⁠Incorporate embedding-based similarity metrics (e.g., semantic alignment)
•⁠  ⁠Train an end-to-end hybrid model combining embeddings with handcrafted debiasing features
•⁠  ⁠Extend this approach to other evaluation datasets where human preferences are involved

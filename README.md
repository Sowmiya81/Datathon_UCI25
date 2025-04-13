# Datathon_UCI25

🏁 Objective
Predict which of two chatbot responses a user would prefer based on a given prompt, by analyzing response content, structure, tone, and relevance.

📊 Workflow
Data Exploration & Cleaning

Removed HTML, special characters, and foreign language using RegEx.

Standardized text for uniformity.

Vectorization & Similarity

Used Bag of Words (BoW) and Doc2Vec for text vectorization.

Computed similarity metrics like Jaccard, Cosine, and BoW overlap.

Feature Engineering

Extracted:

Word counts, sentence length

Verbosity and valuable content ratios

Sentiment scores

Self-reference and promotional tone indicators

Bias Handling

Modeled verbosity bias and self-enhancement bias to prevent misleading patterns.

Designed specific features to neutralize superficial tone-based preferences.

Model Training

Trained a Random Forest classifier using the engineered features.

Achieved 67% accuracy on the test set.

🔍 Key Insights
Verbosity difference is the most important predictor.

Content-rich and concise responses are more likely to be preferred.

Tone and sentiment have low influence.

Manual category tags contribute negligibly.

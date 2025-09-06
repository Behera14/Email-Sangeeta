
# Support Email Clustering (Unsupervised)

This repo clusters support emails into categories using TF-IDF + KMeans.

## What I did
- Combined `subject` + `body` into `text`
- TF-IDF vectorization
- KMeans clustering (k=6)
- Inspected top terms and sample emails per cluster
- Mapped cluster numbers to human-readable categories

## Files generated
- predictions.csv  (original columns + cluster + category)
- kmeans_model.pkl
- tfidf_vectorizer.pkl
- requirements.txt

## How to run
1. Upload `Sample_Support_Emails_Dataset.csv` to Colab
2. Run the notebook cells in order
3. Download `predictions.csv` and upload to GitHub for submission

We received a set of customer support emails without labels. Goal: group similar emails to create actionable categories (e.g., Billing, Login issues, Downtime, API Integration). Approach: TF-IDF vectorization on combined subject + body followed by KMeans clustering. I inspected top terms and sample messages per cluster and mapped clusters to human-readable categories.

Approach & steps (paste):

Load dataset; combine subject + body into text.

TF-IDF vectorization (unigrams + bigrams).

KMeans clustering (k=6). I validated k via elbow and silhouette plots.

Inspected top terms per cluster & sample emails and assigned category names.

Generated predictions.csv with cluster and category columns.

What I submit (paste):

predictions.csv: each email with its cluster number and category name.

notebook.ipynb: full reproducible notebook.

requirements.txt & README.md.

Limitations & next steps (paste):

This is unsupervised; clusters may mix subtypes. Next steps: manually label a small set per cluster and train a supervised classifier (better accuracy). Use transformer models (DistilBERT) for more robust performance on short texts.

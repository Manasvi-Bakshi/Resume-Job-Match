# 🔍 SmartHire: Resume & Job Matching 

Welcome to SmartHire, a project built to explore how we can use NLP techniques to smartly pair resumes with the right job descriptions. Think of it as the brain behind smarter hiring tools, built as part of my NLP lab project.

##  Dataset 

This dataset was first used at Bitfest 2025 Datathon and is available via Kaggle.
Here is the [link](https://www.kaggle.com/datasets/saugataroyarghya/resume-dataset) to the dataset and big Thank You! for providing the dataset.

The structured dataset (`resume_data.csv`) contains:

- 9,544 resumes  
- 35 columns including skills, education, experience, and job postings  
- A special `matched_score` field that indicates how well each resume aligns with a job  


##  Project Implementation

- Created **text embeddings** for resumes and job descriptions using **MiniLM** and fine tuned **BERT**
- Trained a **neural network (MLP)** to predict how well a resume matches a job
- Improved the neural network using **Dropout Regularisation, Early Stopping and Cross Validation**
- Compared model variants to see what works best
- Evaluated performance with real metrics

##  Evaluation Results  

| Model                    | MAE    | MSE    | R² Score | Pearson Corr | Spearman Corr |
|-------------------------|--------|--------|-----------|----------------|-----------------|
| MiniLM + Simple MLP     | 0.0724 | 0.0096 | 0.6491    | 0.8195         | 0.8150          |
| MiniLM + Improved MLP   | 0.0683 | 0.0088 | 0.6806    | 0.8252         | 0.8257          |
| BERT + Improved MLP     | 0.0714 | 0.0081 | 0.7001    | 0.8486         | 0.8432          |

---

##  Running this on Colab  

1. Upload your `kaggle.json` API key when prompted  
2. Run the notebook – it’ll handle everything else:  
   - Install packages  
   - Download and preprocess data  
   - Generate embeddings  
   - Train and evaluate models  
3. View the results – including similarity visualizations and model metrics  

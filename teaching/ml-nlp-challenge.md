---
layout: teaching
title: "ML + NLP Challenge"
---

### Project Overview

This is a **3-hour in-class challenge** where teams of up to 2 students will build an end-to-end pipeline that combines Natural Language Processing with a Machine-Learning classifier to predict the political orientation of news articles (`left`, `lean left`, `center`, `lean right`, `right`).

All teams work on **the same data**, so that differences in results come only from your methodological choices: cleaning, preprocessing, features, model and tuning.

The deliverable is a **working model**, **predictions on a hidden test set**, and **reproducible code**.

### Timeline & Milestones

| Phase | Duration | What Happens | Deliverables |
|---|---|---|---|
| **In-class challenge** | **3 hours** (during class) | Instructors available for hints. Explore and clean the data, set up a baseline, iterate on models. | A runnable prototype (notebook) that trains a model, evaluates it on your own validation split, and predicts the test set. |
| **Immediate check-in** | **≈ 15 min** before the challenge ends | Each group announces the best-performing model discovered (validation macro-F1). Brief discussion of challenges and next steps. | One-sentence summary of the top model and its metric. |
| **Post-class refinement** | until **25 November 2026, 23:59** | Continue training, fine-tune hyper-parameters, conduct error analysis, improve reproducibility. No further instructor input is allowed. | One submission per group on Lola (see below): a notebook that follows the good-practice guidelines and your test-set predictions. |

### Starter Kit

The starter kit is in the [course repository](https://github.com/AugusteDebroise/class-ressources/tree/main/exercises/ml-nlp-challenge) and will also be sent by email. It contains:

- `README.md` – detailed instructions and rules: **read it first**
- `starter_notebook.ipynb` – notebook skeleton with the sections to complete and a **baseline model** (TF-IDF + Logistic Regression)
- `data/train_dataset.csv` – 5,600 labelled articles (`id`, `Title`, `Text`, `Bias`)
- `data/test_dataset.csv` – 2,183 articles **without labels** (`id`, `Title`, `Text`): you predict them, and your score is computed on their hidden labels

Both datasets are **raw**: the articles were scraped from the web and have not been cleaned. Inspecting and cleaning them is part of the challenge. Since the test set has no labels, **split the training set yourselves** to compare your models, and predict **every** row of the test set.

### Good Notebook Practices

To ensure that the submitted notebook can be executed by anyone (instructor, future students, or yourself weeks later), follow these conventions:

**1. Reproducibility**

- Set a global random seed at the top of the notebook (e.g., `np.random.seed(42); torch.manual_seed(42)`)
- Record the exact package versions used (e.g., `pip freeze > requirements.txt`)
- Store any trained artefacts (model weights, vectorizers) using deterministic filenames (e.g., `model_v1.pkl`)

**2. Run From Start to Finish**

- The notebook must be executable cell-by-cell from the first cell without manual edits in the middle
- Avoid hidden state: do not rely on variables created in previous interactive sessions
- Include a "Setup" section that installs packages (if needed) and loads data

**3. Comments & Documentation**

- Use Markdown cells liberally to explain *why* a step is performed, not just *what* is done
- Add inline comments (`# comment`) in code cells for non-obvious lines
- Summarise results (tables, plots) in a concluding Markdown cell that interprets the numbers

**4. Clear Cell Structure**

- Section headers (`# Section`) in code cells to mirror the logical flow (e.g., `# 1. Data Loading`)
- Keep each cell focused on a single logical operation (loading, cleaning, modelling, evaluation)

### Evaluation Criteria

- **Performance** – macro-F1 (accuracy also reported) on the hidden labels of the test set, compared to the baseline
- **Correctness** – code runs end-to-end and reproduces the submitted predictions
- **Pipeline completeness** – data cleaning, preprocessing, model training, prediction, and serialization
- **Documentation & reproducibility** – clear README, environment file, and notebook best practices
- **Critical thinking** – brief discussion of how the labels were produced, what your model may really be learning, the limits of the data, and potential misuse

Using any other copy of this dataset or of its labels is cheating. Notebooks may be re-run to check that they reproduce the submitted predictions.

### Submission Procedure

**Deadline: 25 November 2026, 23:59.** Submissions are made on **Lola**, **one submission per group**. Nothing needs to be uploaded to GitHub.

Upload a single `.zip` file containing:

1. your completed notebook, runnable top to bottom;
2. `test_dataset_predicted.csv`: the test set with an added `Bias` column holding your prediction for every row (the starter notebook writes it for you);
3. a `README.md`: team members, description of your approach, setup instructions, results;
4. a `requirements.txt` (`pip freeze > requirements.txt`).

You do not need to include the training and test datasets.

### Helpful Tips

- Start with the baseline (TF-IDF + Logistic Regression) to obtain a quick score, then try a more complex approach (e.g., fine-tuned DistilBERT) if time permits.
- Modularise the pipeline using `sklearn.pipeline.Pipeline` objects or separate functions — this simplifies later refinements and guarantees the same preprocessing at training and prediction time.
- Document any external resources (pre-trained weights, extra libraries) in the README.
- Keep the notebook clean and runnable from top to bottom; remove stray print statements or debugging code before submitting.

### Learning Objectives

- Full end-to-end NLP + ML pipeline implementation
- Speed, teamwork, rapid prototyping

[Back to Data Management](/teaching/data-management)

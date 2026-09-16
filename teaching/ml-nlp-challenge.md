---
layout: teaching
title: "ML + NLP Challenge"
---

### Project Overview

This is a **3-hour in-class challenge** where teams of up to 2 students will build an end-to-end pipeline that combines Natural Language Processing with a Machine-Learning classifier to predict the political orientation (e.g., left, centre, right) of news articles.

The deliverable is a **working model**, a **performance evaluation**, and **reproducible code**.

### Timeline & Milestones

| Phase | Duration | What Happens | Deliverables |
|---|---|---|---|
| **In-class challenge** | **3 hours** (during class) | Instructors available for hints. Explore data, set up a baseline, iterate on models. | A runnable prototype (script or notebook) that trains a model and outputs predictions on a validation split. |
| **Immediate check-in** | **≈ 15 min** before the challenge ends | Each group announces the best-performing model discovered (validation accuracy/F1). Brief discussion of challenges and next steps. | One-sentence summary of the top model and its metric. |
| **Post-class refinement** | **48 hours** (deadline: TBD) | Continue training, fine-tune hyper-parameters, conduct error analysis, improve reproducibility. No further instructor input is allowed. | Fully committed GitHub repository (see below) with a notebook that follows the good-practice guidelines. |

### Materials & Repository

- Each team will receive a private GitHub Classroom repository (link: TBD) containing:
  - `data/` – sample training/validation CSV files
  - `src/` – starter scripts for data loading, preprocessing, and a baseline model
  - `requirements.txt` – required Python packages (scikit-learn, transformers, pandas, …)
  - `README.md` – template with sections for description, setup, results, and usage

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

- **Correctness** – code runs end-to-end and reproduces reported numbers
- **Performance** – validation metric (accuracy / macro-F1) compared to baseline
- **Pipeline completeness** – data preprocessing, model training, prediction, and serialization
- **Documentation & reproducibility** – clear README, environment file, commit history, and notebook best practices
- **Ethical awareness** – brief discussion of bias, data limits, or potential misuse

### Submission Procedure

1. Commit all source files, notebooks, `requirements.txt`, and the final `README.md` to the main branch of your GitHub Classroom repo.
2. Tag the final commit with `v1.0-final` to help instructors locate the correct version.
3. Ensure the repository is visible to teaching staff.
4. No additional zip files or external links are required.

### Helpful Tips

- Start with the baseline (e.g., TF-IDF + Logistic Regression) to obtain a quick score, then try a more complex approach (e.g., fine-tuned DistilBERT) if time permits.
- Modularise the pipeline using `sklearn.pipeline.Pipeline` objects or separate functions — this simplifies later refinements.
- Document any external resources (pre-trained weights, extra libraries) in the README.
- Keep the notebook clean and runnable from top to bottom; remove stray print statements or debugging code before the final commit.

### Learning Objectives

- Full end-to-end NLP + ML pipeline implementation
- Speed, teamwork, rapid prototyping

[Back to Data Management](/teaching/data-management)

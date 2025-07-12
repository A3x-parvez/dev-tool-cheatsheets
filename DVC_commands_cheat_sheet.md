# 📦 DVC (Data Version Control) Commands Cheat Sheet

> This file summarizes essential DVC commands with their descriptions. It's designed to accompany my recent DVC learning tutorial for quick reference and practice.

---

## 📖 What is DVC?

**DVC (Data Version Control)** is an open-source tool for managing data science and machine learning projects. It helps you:
- Version large datasets and models
- Reproduce experiments
- Track metrics and pipelines
- Collaborate effectively on ML projects

---

## 🔧 Basic Setup

| Command | Description |
|--------|-------------|
| `dvc init` | Initializes a DVC repository in the current directory (creates `.dvc/`). |
| `git add .dvc .gitignore` | Track DVC metadata with Git (DVC works alongside Git). |
| `git commit -m "Initialize DVC"` | Save the initial DVC setup. |

---

## 📁 Data Management

| Command | Description |
|--------|-------------|
| `dvc add data.csv` | Adds `data.csv` under DVC tracking. It creates a `.dvc` file and updates `.gitignore`. |
| `dvc status` | Checks whether data or pipeline stages have changed. |
| `dvc remove data.csv.dvc` | Stops tracking a data file or directory with DVC. |
| `dvc unprotect data.csv` | Removes read-only DVC protection for manually editing files. |

---

## 🚚 Remote Storage Setup

| Command | Description |
|--------|-------------|
| `dvc remote add -d myremote s3://mybucket/path` | Adds a default remote storage (e.g., S3, GCS, SSH, local). |
| `dvc remote modify myremote access_key_id 'xxx'` | Adds credentials to remote (S3 in this example). |
| `dvc push` | Uploads data to the remote storage. |
| `dvc pull` | Downloads data from the remote. |
| `dvc fetch` | Downloads data without modifying workspace. |

---

## 🧪 Pipeline & Experiments

| Command | Description |
|--------|-------------|
| `dvc stage add -n preprocess -d script.py -o output.csv python script.py` | Defines a pipeline stage named `preprocess`. |
| `dvc repro` | Reproduces the pipeline if dependencies or inputs changed. |
| `dvc dag` | Visualizes the pipeline as a directed acyclic graph (DAG). |
| `dvc exp run` | Runs and tracks an experiment. |
| `dvc exp show` | Displays experiment results with metrics. |
| `dvc exp apply <exp-id>` | Applies a specific experiment to your workspace. |

---

## 📊 Metrics & Plots

| Command | Description |
|--------|-------------|
| `dvc metrics show` | Displays tracked metrics (e.g., accuracy, loss). |
| `dvc plots show` | Visualizes tracked plots over experiments. |
| `dvc plots diff` | Compares plots between experiments. |

---

## 🗂 Versioning & Collaboration

| Command | Description |
|--------|-------------|
| `git add file.dvc` | Version control the metadata file via Git. |
| `git push` | Push code + DVC metadata to Git. |
| `dvc push` | Push actual data to DVC remote. |
| `dvc pull` | Pull data from remote when cloning a repo. |

---

## 🧹 Cleaning Up

| Command | Description |
|--------|-------------|
| `dvc gc` | Garbage collects unused files (careful in shared projects!). |
| `dvc destroy` | Removes DVC from your project (irreversible!). |

---

## 📎 Best Practices

- Use **`dvc add`** for any large file (>50MB).
- Always commit `.dvc` files with Git.
- Set up **remote storage** early (local or cloud).
- Run `dvc push` after every important update.
- Use `dvc.yaml` and `dvc.lock` for pipelines, not manual scripts.

---

## 📚 Resources

- [Official DVC Docs](https://dvc.org/doc)
- [DVC GitHub](https://github.com/iterative/dvc)
- [DVC Examples](https://github.com/iterative/dvc-examples)

---

### 👤 Author: Rijwanool Karim  
🔗 Linkdin - [Rijwanool karim](https://www.linkedin.com/in/rijwanool-karim)  
💻 Github - [A3x-parvez](https://github.com/rijwanoolkarim)

---

> 🔁 This cheat sheet is part of my personal DVC learning series. Feel free to fork, modify, and use it in your own ML projects!

---


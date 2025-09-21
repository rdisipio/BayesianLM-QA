# BayesianLM-QA

> **BayesianLM-QA: Uncertainty-aware question answering with Bayesian reasoning on top of pretrained language models.**

This project provides **lightweight, reproducible blueprints** showing how Bayesian reasoning can make language models more trustworthy.  
The focus is not scale, but **clarity**: simple, end-to-end examples that demonstrate how an AI system can say *“I don’t know”* when uncertainty is high.  

---

## ✦ Features
- **Bayesian Iris classifier**: classic sanity check with NUTS/MCMC.  
- **Frozen encoder + Bayesian head**: add calibrated uncertainty to multiple-choice QA.  
- **Bayesian LoRA adapters**: parameter-efficient fine-tuning with Laplace or variational posteriors.  
- **Abstention & calibration**: selective risk curves, reliability diagrams, conformal refusal.  

---

## ✦ Installation

This project uses [Pipenv](https://pipenv.pypa.io/).

### 1. Clone the repo
```bash
git clone https://github.com/yourname/BayesianLM-QA.git
cd BayesianLM-QA
```

### 2. Create the environment
```bash
pipenv --python 3.13
pipenv install
pipenv install --dev
```

### 3. Register the Jupyter kernel
```bash
pipenv run python -m ipykernel install --user --name=bayesianlm-qa
```

---

## ✦ Quick Start

### Example: Run a Jupyter notebook
```bash
pipenv run jupyter notebook
```
Open one of the provided notebooks:
- `notebooks/iris_bayes_mlp.ipynb`  
- `notebooks/bayesian_head_mcq.ipynb`  
- `notebooks/bayesian_lora_mcq.ipynb`  

Each notebook includes:
- Model definition  
- Inference (Laplace / VI / MCMC)  
- Plots: posterior predictive, reliability diagram, selective risk  

---

## ✦ Notes on Apple Silicon (M2/M3/M4)

- **PyTorch**: Official wheels include MPS backend for acceleration.  
- **NumPyro/JAX**: CPU wheels are stable on macOS. GPU/Metal is still experimental.  
- **Laplace-torch**: Works out of the box on Mac.  

For small-scale demos (Iris, MCQ QA), CPU speed is more than enough.  

---

## ✦ Development

Run formatters and linters:
```bash
pipenv run fmt
```

---

## ✦ License
MIT License

---

## ✦ Citation
If you use or adapt these examples, please cite as:

```bibtex
@misc{bayesianlmqa2025,
  title  = {BayesianLM-QA: Uncertainty-aware Question Answering with Bayesian Reasoning},
  author = {Riccardo Di Sipio},
  year   = {2025},
  note   = {Workable exemplars for ethical AI and calibrated refusal in LLMs}
}
```

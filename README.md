# Enhancing Reasoning Capabilities in Large Language Models

## Team Members:
1. Anudeep Eloori  
2. Navaneeth Rajarapu  
3. Satya Narayana  

---

## Objective

This project aims to fine-tune an open-source LLM on datasets that combine coding and reasoning tasks to improve its problem-solving abilities. We hypothesize that incorporating reasoning capabilities will enhance performance not only in reasoning-specific tasks but also in code understanding, debugging, and general inference.

---

## How to Run

### Steps to follow for inferencing model:
1. Load the model using HuggingFace's pipeline in text generation mode.
2. Specify the model name.

---

## Project Structure

### 1. Model_Testing.ipynb
- **Function**: Loads and tests different LLMs:
  - `navaneeth45/Qwen2.5-1.5B-thinking-reasoning-model-V1`
  - `navaneeth45/code-reason-tuned-llama-3.1-8b`
  - `navaneeth45/gemma2-2B-thinking-reasoning-model-V1`
- **Inputs**: Text prompts with reasoning or coding context.
- **Outputs**: Model-generated responses.
- **Instructions to Run**:
  - Install dependencies: `transformers`, `torch`, `datasets`
  - Choose a model from Hugging Face
  - Run cells sequentially to generate outputs

### 2. Evaluation_and_testing_modified.ipynb
- **Function**: Compares outputs of various models using reasoning metrics and trustworthiness tests
- **Datasets Used**:
  - ServiceNow V1 Subset – diverse reasoning tasks
  - Stereoset – fairness and bias analysis
- **Evaluation Metrics**:
  - Robustness (accuracy across diverse prompts)
  - Bias (Stereoset score)
  - Reliability (performance consistency)
- **Instructions to Run**:
  - Ensure model-generated outputs are available
  - Run the notebook to compute scores and compare models

---

## Accessing Fine-Tuned Models via GitHub Branches

The repository is organized using branches, each corresponding to a specific fine-tuned model:

- `main`: General project files and evaluation notebooks
- `Qwen2.5-1.5B-thinking-reasoning-model-V1`: Contains the Qwen-based reasoning model
- `code-reason-tuned-llama-3.1-8b`: Contains the LLaMA 3.1 8B fine-tuned for reasoning and coding
- `gemma2-2B-thinking-reasoning-model-V1`: Contains the Gemma2-2B reasoning fine-tuned model

To explore each model:
1. Navigate to the repository on GitHub.
2. Use the **"Branch"** dropdown menu.
3. Select the respective branch to view that model’s files and configurations.

This structure ensures clean isolation between different model versions and makes the repository easy to explore and maintain so we did in this way.


---

## Base Model Details

- **Base Model**: `Qwen/Qwen2.5-1.5B-Instruct`
- **Library**: `transformers`
- **Fine-tuned Model**: `Qwen2.5-1.5B-thinking-reasoning-model-V0`

### Training Procedure

This model was trained with SFT (Supervised Fine-Tuning) using the LoRA method.

#### Framework Versions

- TRL: 0.15.2  
- Transformers: 4.48.3  
- PyTorch: 2.5.1+cu124  
- Datasets: 3.3.2  
- Tokenizers: 0.21.0  

---

## Citation

Cite TRL as:

```bibtex
@misc{vonwerra2022trl,
  title        = {{TRL: Transformer Reinforcement Learning}},
  author       = {Leandro von Werra and Younes Belkada and Lewis Tunstall and Edward Beeching and Tristan Thrush and Nathan Lambert and Shengyi Huang and Kashif Rasul and Quentin Gallouédec},
  year         = 2020,
  journal      = {GitHub repository},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/huggingface/trl}}
}
```


## Fine-Tuned Models

---

### 1. Qwen2.5-1.5B-thinking-reasoning-model-V1

- **Base Model**: `Qwen/Qwen2.5-1.5B-Instruct`
- **Fine-tuned Model**: `navaneeth45/Qwen2.5-1.5B-thinking-reasoning-model-V1`
- **Library**: `transformers`
- **Training Approach**: Supervised Fine-Tuning (SFT) with LoRA
- **Primary Focus**: General reasoning, math reasoning, and logic-driven QA tasks

#### Framework Versions

- TRL: 0.15.2  
- Transformers: 4.48.3  
- PyTorch: 2.5.1+cu124  
- Datasets: 3.3.2  
- Tokenizers: 0.21.0

---

### 2. Code-Reason-Tuned-LLaMA-3.1-8B

- **Base Model**: `meta-llama/Meta-Llama-3-8B-Instruct`
- **Fine-tuned Model**: `navaneeth45/code-reason-tuned-llama-3.1-8b`
- **Library**: `transformers`
- **Training Approach**: LoRA-based fine-tuning with a blend of code and reasoning samples
- **Primary Focus**: Code completion with embedded step-by-step logical reasoning

#### Framework Versions

- TRL: 0.15.2  
- Transformers: 4.48.3  
- PyTorch: 2.5.1+cu124  
- Datasets: 3.3.2  
- Tokenizers: 0.21.0

---

### 3. Gemma2-2B-Thinking-Reasoning-Model-V1

- **Base Model**: `google/gemma-2b-it`
- **Fine-tuned Model**: `navaneeth45/gemma2-2B-thinking-reasoning-model-V1`
- **Library**: `transformers`
- **Training Approach**: Fine-tuning with curated reasoning prompts from multi-domain sources
- **Primary Focus**: Small-footprint LLM with reasoning competency for lightweight deployment

#### Framework Versions

- TRL: 0.15.2  
- Transformers: 4.48.3  
- PyTorch: 2.5.1+cu124  
- Datasets: 3.3.2  
- Tokenizers: 0.21.0

Team Members:

1. Anudeep Eloori,
2. Navaneeth Rajarapu,
3. Satya Narayana

Objective:

This project aims to fine-tune an open-source LLM on datasets that combine coding and reasoning tasks to improve its problem-solving abilities. We hypothesize that incorporating reasoning capabilities will enhance performance not only in reasoning-specific tasks but also in code understanding, debugging, and general inference.


How to run:

Steps to follow for inferencing model.
1. Load the model using HuggingFace's pipeline in text generation mode.
2. Specify the model name.

Project Structure

1. Model_Testing.ipynb
Function: Loads and tests different LLMs (navaneeth45/Qwen2.5-1.5B-thinking-reasoning-model-V1, navaneeth45/code-reason-tuned-llama-3.1-8b and navaneeth45/gemma2-2B-thinking-reasoning-model-V1).

Inputs: Text prompts with reasoning or coding context.

Outputs: Model-generated responses.

Instructions to Run:

Install dependencies (transformers, torch, datasets).

Choose a model from Hugging Face (e.g., 1. navaneeth45/Qwen2.5-1.5B-thinking-reasoning-model-V1 2. navaneeth45/code-reason-tuned-llama-3.1-8b  3. navaneeth45/gemma2-2B-thinking-reasoning-model-V1).

Run cells sequentially to generate outputs for evaluation.

2. Evaluation_and_testing_modified.ipynb
Function: Compares the outputs of various models using reasoning metrics and trustworthiness tests.

Datasets Used:

ServiceNow V1 Subset: Diverse reasoning tasks.

Stereoset: For fairness and bias analysis.

Evaluation Metrics:

Robustness (accuracy across diverse prompts)

Bias (Stereoset score)

Reliability (performance consistency)

Instructions to Run:

Ensure the output generations are available.

Run cells to compute scores and compare models.



---
base_model: Qwen/Qwen2.5-1.5B-Instruct
library_name: transformers
model_name: Qwen2.5-1.5B-thinking-reasoning-model-V0

---

# Model Card for Qwen2.5-1.5B-thinking-reasoning-model-V0

This model is a fine-tuned version of [Qwen/Qwen2.5-1.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-1.5B-Instruct).
It has been trained using [TRL](https://github.com/huggingface/trl).



## Training procedure



This model was trained with SFT(Supervised fine-tuning LoRA method).

### Framework versions

- TRL: 0.15.2
- Transformers: 4.48.3
- Pytorch: 2.5.1+cu124
- Datasets: 3.3.2
- Tokenizers: 0.21.0

## Citations



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

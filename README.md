
# code-reason-tuned-llama-3.1-8b

Fine-tuned LoRA adapter for Meta's LLaMA 3.1 8B model, designed to integrate coding and reasoning tasks.

---

## Model Information
 
- **Fine-Tuned Model**: `navaneeth45/code-reason-tuned-llama-3.1-8b`  
- **Library**: `transformers`

---

## Contents

- `adapter_config.json`, `adapter_model.safetensors`  
- `tokenizer_config.json`, `tokenizer.json`, `vocab.json`  
- `added_tokens.json`, `merges.txt`, `special_tokens_map.json`  
- `training_args.bin`

---

## Overview

- **LoRA Adapter**: Injects additional parameters to enhance the model’s reasoning through code.
- **Training Focus**: Mixed dataset of reasoning questions and coding problems in a 1:1 ratio.
- **Motivation**: Research shows that when models are trained to reason, their coding performance also improves significantly.
- **Use Case**: Ideal for tasks involving logic-driven code understanding, explanation, and debugging.

---

## Training Procedure

Supervised fine-tuning (SFT) with LoRA adapters on a hybrid dataset combining reasoning and programming problems.

### Framework Versions

- TRL: 0.15.2  
- Transformers: 4.48.3  
- PyTorch: 2.5.1+cu124  
- Datasets: 3.3.2  
- Tokenizers: 0.21.0

---

## Citation

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

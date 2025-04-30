
# gemma2-2B-thinking-reasoning-model-V1

LoRA fine-tuned version of Google's Gemma 2B model, enhanced for lightweight logical reasoning tasks.

---

## Model Information
 
- **Fine-Tuned Model**: `navaneeth45/gemma2-2B-thinking-reasoning-model-V1`  
- **Library**: `transformers`

---

## Contents

- `adapter_config.json`, `adapter_model.safetensors`  
- `tokenizer_config.json`, `tokenizer.json`, `vocab.json`  
- `added_tokens.json`, `merges.txt`, `special_tokens_map.json`  
- `training_args.bin`

---

## Overview

- **LoRA Adapter**: Injects reasoning capacity into a compact, efficient 2B parameter model.
- **Training Data**: Blend of reasoning-based questions and structured prompts from reasoning-heavy tasks (ServiceNow, math problems, etc.).
- **Goal**: Offer reasoning capability in scenarios with limited computational resources.
- **Performance**: Provides accurate, concise step-by-step answers while maintaining efficiency.

---

## Training Procedure

Supervised fine-tuning (SFT) using the LoRA method for reasoning adaptability in small-scale deployments.

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

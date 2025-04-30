
# Qwen2.5-1.5B-thinking-reasoning-model-V1

Fine-tuned LoRA adapter for the Qwen2.5 1.5B model to enhance logical reasoning capabilities.

---

## Model Information

- **Fine-Tuned Model**: `navaneeth45/Qwen2.5-1.5B-thinking-reasoning-model-V1`  
- **Library**: `transformers`

---

## Contents

- `adapter_config.json`, `adapter_model.safetensors`  
- `tokenizer_config.json`, `tokenizer.json`, `vocab.json`  
- `added_tokens.json`, `merges.txt`, `special_tokens_map.json`  
- `training_args.bin`

---

## Overview

- **LoRA Adapter**: Adds ~8M parameters on top of the base model.  
- **Training Objective**: Improve multi-step reasoning and logical inference.  
- **Dataset Type**: Chain-of-thought and domain-specific tasks.  
- **Result**: Produces more coherent and structured answers with logical steps.

---

## Training Procedure

Supervised fine-tuning (SFT) using LoRA.

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

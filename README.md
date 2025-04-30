
# gemma2-2B-thinking-reasoning-model-V1

This folder holds the LoRA adapter for the Gemma2 2-billion-parameter model, tuned on reasoning datasets.
---
base_model: google/gemma-2b-it
library_name: transformers
model_name: gemma2-2B-thinking-reasoning-model-V1

---

## Training procedure

This model was trained with SFT.

## Contents

- **adapter_config.json, adapter_model.safetensors**  
- **added_tokens.json**  
- **special_tokens_map.json, tokenizer*_*.json**  
- **training_args.bin**  
- **runs/** (training logs & checkpoints)

## What’s Happening Here

- **Base**: Gemma2-2B, a compact LLM optimized for low-resource inference.
- **Objective**: Improve its chain-of-thought (CoT) performance on logic puzzles.
- **Data**: Standard CoT datasets plus synthetic tasks we generated via templating.



### Framework versions

- TRL: 0.16.0
- Transformers: 4.50.2
- Pytorch: 2.6.0+cu124
- Datasets: 3.5.0
- Tokenizers: 0.21.1

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

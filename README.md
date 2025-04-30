# Qwen2.5-1.5B-thinking-reasoning-model-V1

Fine-tuned LoRA adapter for the Qwen2.5 1.5B model, targeting logical reasoning tasks.
---
base_model: Qwen/Qwen2.5-1.5B-Instruct
library_name: transformers
model_name: Qwen2.5-1.5B-thinking-reasoning-model-V1



## Contents

- **adapter_config.json, adapter_model.safetensors**  
- **added_tokens.json, merges.txt, special_tokens_map.json**  
- **tokenizer_config.json, tokenizer.json, vocab.json**  
- **training_args.bin**  
- **runs/**

## What’s Happening Here

- **Adapter**: Injects ~8M parameters into the base Qwen2.5.  
- **Training**: Uses mixed CoT + domain-specific prompts.  
- **Outcome**: Better step-by-step answers while preserving base fluency.



## Training procedure

This model was trained with SFT.

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

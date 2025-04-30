Team Members:

1. Anudeep Eloori,
2. Navaneeth Rajarapu,
3. Satya Narayana



How to run:

Steps to follow for inferencing model.
1. Load the model using HuggingFace's pipeline in text generation mode.
2. Specify the model name.
## Quick start

```python
from transformers import pipeline

question = "If you had a time machine, but could only go to the past or the future once and never return, which would you choose and why?"
generator = pipeline("text-generation", model="navaneeth45/Qwen2.5-1.5B-thinking-reasoning-model-V0", device="cuda")
output = generator([{"role": "user", "content": question}], max_new_tokens=128, return_full_text=False)[0]
print(output["generated_text"])
```

Alternately you can directly run all the cells in inference.ipynb and change the prompts if needed.


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

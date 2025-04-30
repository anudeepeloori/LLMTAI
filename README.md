# code-reason-tuned-llama-3-1-8b

This folder contains a LoRA adapter fine-tuned on the LLaMA-3 (8B) base model for code reasoning tasks.

## Contents

- **adapter_config.json**  
  LoRA hyperparameters (rank, alpha, dropout, etc.)

- **adapter_model.safetensors**  
  Learned adapter weights.

- **special_tokens_map.json, tokenizer_config.json, tokenizer.json**  
  Any added tokens or tokenizer overrides used during fine-tuning.

- **training_args.bin**  
  Serialized training arguments (batch size, learning rate, epochs, etc.)


## What’s Happening Here

1. **Fine-tuning**:  
   We applied LoRA to inject a lightweight adapter into the frozen LLaMA-3 base. Training data consisted of code+chain-of-thought examples (e.g. Python puzzles with step-by-step solutions).

2. **Special Tokens**:  
   We added markers like '<Think>' so the model can learn to separate reasoning steps from code snippets.

3. **Output**:  
   Checkpoints live under `runs/`. Each run directory has:
   - `pytorch_model.bin` (adapter only)  
   - `trainer_state.json` (loss curves, hyperparameters)  
   - `eval_results.json` (if you ran evaluation during training)



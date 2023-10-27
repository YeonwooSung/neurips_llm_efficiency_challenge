# NeurIPS LLM Efficiency Challenge

## Submission Overview

I am submitting 3 submissions for A100 track.

### 1. mistral-7b with CoT

Codes and dockerfile for this are in the `a100_submission_1` directory.
To run the evaluation, just use the "a100_submission_1/Dockerfile".
This version is a finetuned PEFT model, which uses `mistralai/Mistral-7B-v0.1` model.

Training details:

    1) use CoT dataset for finetuning
    2) use PEFT QLoRA
    3) train with SFTTrainer

### 2. mistral-instruct-7b with CoT & NEFTune

Codes and dockerfile for this submission are in the `a100_submission_2` directory.
To run the evaluation, just use the "a100_submission_2/Dockerfile".

Training details:

    1) use CoT dataset for finetuning
    2) use PEFT QLoRA
    3) train with SFTTrainer
    4) use NEFTune for robustness

### 3. mistral-7b with CoT & NEFTune

Codes and dockerfile to run this submission are in the `a100_submission_3` directory.
To run the evaluation, just use the "a100_submission_3/Dockerfile".

Training details:

    1) use CoT dataset for finetuning
    2) use PEFT QLoRA
    3) train with SFTTrainer
    4) use NEFTune for robustness

## Training Methodology

Basically, I am trying to use the llama_recipes for submission, and using `trl SFTTrainer` for training.
I am currently running the training with Google Colab with the notebooks in [notebooks](./notebooks) folder.

- Using SFTTrainer from trl
    - Supervised Fine Tuning
    - Use Dolly-5K template as instruction template
- Adapt [NEFT](https://github.com/huggingface/trl/issues/870) to enhance robustness

## Additional Info

email address: `neos960518@gmail.com`

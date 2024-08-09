# Whisper-finetune-kyrgyz

This model is a fine-tuned version of `openai/whisper-medium` on the `common_voice_17_0` dataset. It achieves the following results on the evaluation set:

- **Loss:** 0.3735
- **WER:** 32.0036%

## Model Description

This model was fine-tuned to recognize and transcribe Kyrgyz speech using the Mozilla Common Voice dataset (version 17.0). The base model is `openai/whisper-medium`, and the fine-tuning process involved adjusting the model to better capture the nuances of the Kyrgyz language.

## Intended Uses & Limitations

*More information needed.*

## Training and Evaluation Data

*More information needed.*

## Training Procedure

### Training Hyperparameters

The following hyperparameters were used during training:

- **learning_rate:** 1e-05
- **train_batch_size:** 16
- **eval_batch_size:** 8
- **seed:** 42
- **optimizer:** Adam with betas=(0.9, 0.999) and epsilon=1e-08
- **lr_scheduler_type:** linear
- **lr_scheduler_warmup_steps:** 500
- **training_steps:** 1000
- **mixed_precision_training:** Native AMP

### Training Results

| Training Loss | Epoch  | Step  | Validation Loss | WER     |
|---------------|--------|-------|-----------------|---------|
| 0.0404        | 4.6948 | 1000  | 0.3735          | 32.0036%|

## Framework Versions

The following versions of frameworks were used:

- **Transformers:** 4.42.3
- **Pytorch:** 2.3.0+cu121
- **Datasets:** 2.20.0
- **Tokenizers:** 0.19.1

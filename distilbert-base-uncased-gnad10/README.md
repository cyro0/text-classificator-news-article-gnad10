---
library_name: peft
license: apache-2.0
base_model: distilbert/distilbert-base-uncased
tags:
- generated_from_trainer
metrics:
- f1
- accuracy
model-index:
- name: distilbert-base-uncased-gnad10
  results: []
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# distilbert-base-uncased-gnad10

This model is a fine-tuned version of [distilbert/distilbert-base-uncased](https://huggingface.co/distilbert/distilbert-base-uncased) on an unknown dataset.
It achieves the following results on the evaluation set:
- Loss: 0.7690
- F1: 0.8361
- Accuracy: 0.8366

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 0.001
- train_batch_size: 8
- eval_batch_size: 8
- seed: 42
- optimizer: Use OptimizerNames.ADAMW_TORCH with betas=(0.9,0.999) and epsilon=1e-08 and optimizer_args=No additional optimizer arguments
- lr_scheduler_type: linear
- num_epochs: 10

### Training results

| Training Loss | Epoch | Step  | Validation Loss | F1     | Accuracy |
|:-------------:|:-----:|:-----:|:---------------:|:------:|:--------:|
| 0.9207        | 1.0   | 1156  | 0.8170          | 0.7276 | 0.7267   |
| 0.7585        | 2.0   | 2312  | 0.7201          | 0.7647 | 0.7636   |
| 0.6734        | 3.0   | 3468  | 0.7268          | 0.7761 | 0.7743   |
| 0.6406        | 4.0   | 4624  | 0.7344          | 0.7920 | 0.7918   |
| 0.5782        | 5.0   | 5780  | 0.6773          | 0.8030 | 0.8035   |
| 0.5229        | 6.0   | 6936  | 0.6293          | 0.8165 | 0.8152   |
| 0.4514        | 7.0   | 8092  | 0.6392          | 0.8248 | 0.8259   |
| 0.3757        | 8.0   | 9248  | 0.6606          | 0.8204 | 0.8210   |
| 0.298         | 9.0   | 10404 | 0.7235          | 0.8308 | 0.8317   |
| 0.2449        | 10.0  | 11560 | 0.7690          | 0.8361 | 0.8366   |


### Framework versions

- PEFT 0.14.0
- Transformers 4.48.3
- Pytorch 2.6.0+cu118
- Datasets 3.2.0
- Tokenizers 0.21.0
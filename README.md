# DistilBERT Fine-Tuning with LoRA on GNAD10

This repository contains code and resources for fine-tuning the DistilBERT language model using Low-Rank Adaptation (LoRA) on the GNAD10 dataset. The goal is to classify news articles into 9 distinct categories efficiently while reducing computational overhead with LoRA.

## Dataset: GNAD10
The [GNAD10](community-datasets/gnad10) dataset  consists of 10,000 German news articles categorized into 9 classes. Each sample includes the news text and category label.

## Model: DistilBERT with LoRA
DistilBERT is a lighter version of BERT that retains much of its performance while being faster and requiring fewer resources. LoRA (Low-Rank Adaptation) is used to fine-tune DistilBERT efficiently by injecting small trainable layers into frozen transformer weights, reducing GPU memory requirements.

## Features
- Fine-tuning DistilBERT using LoRA for efficient training
- Classification of German news articles into 9 categories
- Dataset preprocessing and tokenization
- Model training and evaluation scripts

## Installation

### Prerequisites

* Python 3.11.x
* All dependencies listed in requirements.txt

### Installation commands
Clone the repository, create virtual environment, activate environment and install dependencies:

```bash
git clone https://github.com/cyro0/text-classificator-news-article-gnad10.git
```
```bash
cd text-classificator-news-article-gnad10
```
```bash
python -m venv .venv
```
```bash
.venv\Scripts\activate
```
```bash
pip install -r requirements.txt
```

## Results

### Training
| Training Loss | Epoch | Step  | Validation Loss | F1    | Accuracy |
|--------------|-------|-------|----------------|-------|----------|
| 0.9207       | 1.0   | 1156  | 0.8170         | 0.7276 | 0.7267   |
| 0.7585       | 2.0   | 2312  | 0.7201         | 0.7647 | 0.7636   |
| 0.6734       | 3.0   | 3468  | 0.7268         | 0.7761 | 0.7743   |
| 0.6406       | 4.0   | 4624  | 0.7344         | 0.7920 | 0.7918   |
| 0.5782       | 5.0   | 5780  | 0.6773         | 0.8030 | 0.8035   |
| 0.5229       | 6.0   | 6936  | 0.6293         | 0.8165 | 0.8152   |
| 0.4514       | 7.0   | 8092  | 0.6392         | 0.8248 | 0.8259   |
| 0.3757       | 8.0   | 9248  | 0.6606         | 0.8204 | 0.8210   |
| 0.298        | 9.0   | 10404 | 0.7235         | 0.8308 | 0.8317   |
| 0.2449       | 10.0  | 11560 | 0.7690         | 0.8361 | 0.8366   |

### Evaluation per class
| Category       | Sample Count | F1  | Accuracy |
|---------------|-------|----------|--------------|
| WEB          | 21  | 0.9598   | 0.9226       |
| PANORAMA     | 21  | 0.8493   | 0.7381       |
| INTERNATIONAL | 19  | 0.8731   | 0.7748       |
| WIRTSCHAFT   | 18  | 0.8629   | 0.7589       |
| SPORT        | 15  | 0.9916   | 0.9833       |
| INLAND       | 13  | 0.8475   | 0.7353       |
| ETAT         | 9   | 0.8644   | 0.7612       |
| WISSENSCHAFT | 8   | 0.9143   | 0.8421       |
| KULTUR       | 7   | 0.8866   | 0.7963       |

## References
- [GNAD10 Dataset](community-datasets/gnad10)
- [DistilBERT](https://huggingface.co/distilbert/distilbert-base-uncased)
- [GNAD10 trained DisitlBERT](https://huggingface.co/cyrp/distilbert-base-uncased-gnad10)
- [LoRA](https://arxiv.org/pdf/2106.09685)

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Contributions
Contributions are welcome! Feel free to open issues or submit pull requests.

# LLaMA-Customer-Support-Assistant

Fine-tuned LLaMA 3.2 model for customer support using Unsloth optimization. Trained on Bitext's 27K customer service dataset. Optimized for M1 Mac.

## Features
- 2x faster training with Unsloth optimization
- LoRA fine-tuning
- Memory-efficient for M1 Macs
- Automated customer support responses
- Order cancellation and status handling

## Dataset
- Source: [Bitext Customer Support Dataset](https://github.com/bitext/customer-support-llm-chatbot-training-dataset)
- CSV: [27K Customer Support Responses](https://raw.githubusercontent.com/bitext/customer-support-llm-chatbot-training-dataset/main/data/Bitext_Sample_Customer_Support_Training_Dataset_27K_responses-v11.csv)

## Project Structure
```
LLaMA-Customer-Support-Assistant/
├── fine_tuning.ipynb          # Training notebook
├── test_model.ipynb           # Testing notebook
├── customer_support_model/    # Model outputs
├── dataset/                   # CSV dataset
└── README.md
```

## Installation
```bash
# Create conda environment
conda create -n llm_env python=3.10
conda activate llm_env

# Install PyTorch for M1
conda install pytorch torchvision torchaudio -c pytorch

# Install dependencies
pip install transformers datasets accelerate peft
pip install unsloth
```

## Usage
1. Start Jupyter:
```bash
jupyter notebook
```

2. Execute notebooks:
- Run `fine_tuning.ipynb` for training
- Run `test_model.ipynb` for testing

## Model Details
- Base Model: unsloth/Llama-3.2-3B-Instruct
- Optimization: Unsloth + MPS backend
- Fine-tuning: LoRA
- Training Parameters:
  - Batch size: 1
  - Learning rate: 1e-4
  - Epochs: 1
  - Max sequence length: 256

## Requirements
- M1/M2 Mac
- 8GB+ RAM
- Python 3.10+
- PyTorch with MPS support

## Acknowledgments
- [Unsloth](https://github.com/unslothai/unsloth) for optimization
- [Bitext](https://github.com/bitext) for the dataset

## License
MIT

## Citation
```bibtex
@misc{bitext2023customer,
    title={Customer Support LLM Training Dataset},
    author={Bitext},
    year={2023},
    publisher={GitHub},
    url={https://github.com/bitext/customer-support-llm-chatbot-training-dataset}
}
```

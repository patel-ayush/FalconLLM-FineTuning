# Fine-Tuning Falcon-7B Model with Qlora

This repository contains a Jupyter notebook where the Falcon-7B model is fine-tuned using the Qlora algorithm. The Falcon-7B model is an advanced, autoregressive, decoder-only Language Model (LLM) that is a smaller variant of the Falcon-40B model. It consists of 7 billion parameters and is trained on 1,500 billion tokens.

### QLORA
- **Quantized Low-Rank Adapters (QLoRa)**: An algorithm to expedite fine-tuning of Large Language Models (LLMs).
- **Adds minimal trainable parameters**: Reduces memory footprint during fine-tuning.
- **4-bit NormalFloat quantization**: Evenly distributes values in quantization bins.
- **Double quantization**: Further saves memory by quantizing quantization constants.
- **Paging with NVIDIA unified memory**: Handles CPU-GPU data transfers.
- **Benefits**: Drastically reduces memory requirements, prevents GPU memory exhaustion, and maintains near-par performance with standard fine-tuning.

## Dataset

The dataset used for this project is a subset of the [Open Assistant dataset](https://huggingface.co/datasets/OpenAssistant/oasst1/tree/main). It only contains the highest-rated paths in the conversation tree, amounting to a total of 9,846 samples. 

## Training Parameters

The Falcon-7B model was fine-tuned with the following parameters:

- Learning Rate: `2e-4`
- Max Steps: `200`
![](https://api.wandb.ai/links/nakish/g0i211ur)
## Dependencies

- [Hugging Face Transformers](https://github.com/huggingface/transformers)
- [PyTorch](https://pytorch.org/)
- [Qlora](https://github.com/qlora)


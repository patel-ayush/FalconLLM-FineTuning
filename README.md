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

## Results
<table>
  <tr>
    <th>Level</th>
    <th>Query</th>
    <th>Output</th>
  </tr>
  <tr>
   <td>Easy</td>
   <td>What is the capital of France?</td>
   <td>Paris is the capital of France</td> 
  </tr>
  <tr>
   <td>Easy</td>
   <td>Who wrote the book '1984'?</td>
   <td>George Orwell</td> 
  </tr>
  <tr>
   <td>Easy</td>
   <td>Describe the process of photosynthesis</td>
   <td>Photosynthesis is the process by which plants use sunlight to make food.</td> 
  </tr>
  <tr>
   <td>Easy</td>
   <td>What is the formula for calculating the area of a circle?</td>
   <td>The formula for calculating the area of a circle is:
A = πr2</td> 
  </tr>
 
  <tr>
    <td>Intermediate</td>
    <td>Could you explain the main ideas behind quantum physics?</td>
    <td>The main idea behind quantum physics is that the world is made up of particles that are constantly in motion. These particles are called quarks, and they are the building blocks of matter.
The second main idea is that these particles are constantly changing</td>
  </tr>    
  <tr>
    <td>Intermediate</td>
    <td>How does the blockchain technology behind Bitcoin work?</td>
    <td>The blockchain is a distributed database that is used to record transactions. It is a public ledger that is shared by all users of the network.</td>
  </tr> 
  <tr>
    <td>Intermediate</td>
    <td>What's the recipe for making a classic French omelette?</td>
    <td>The classic French omelette is made with eggs, milk, salt and pepper.The classic French omelette is made with eggs, milk, salt and pepper.</td>
  </tr> 
  <tr>
    <td>Advance</td>
    <td>Discuss the socioeconomic and philosophical implications of AI becoming conscious.</td>
    <td>The implications of AI becoming conscious are many. The first and most obvious is that it will be able to think and reason. This will have a profound impact on the way that we live our lives. It will be able to make decisions for us, and it will be able to make decisions that we would not make.</td>
  </tr> 
  <tr>
    <td>Advance</td>
    <td>Describe how CRISPR-Cas9 technology is used for gene editing.</td>
    <td>CRISPR-Cas9 is a gene editing technology that is used to edit the DNA of an organism. It is a very powerful tool that can be used to edit the DNA of an organism in a very precise way.</td>
  </tr> 
</table>

## Dependencies

- [Hugging Face Transformers](https://github.com/huggingface/transformers)
- [PyTorch](https://pytorch.org/)
- [Qlora](https://github.com/qlora)


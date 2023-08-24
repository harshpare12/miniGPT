# miniGPT

miniGPT is a compact and simplified version of the renowned GPT-2 language model. 
This project aims to provide a clear and concise implementation of the GPT-2 model, making it easier for developers 
to understand the fundamental workings of transformer-based language models. Despite its size, miniGPT remains capable 
of generating coherent and contextually relevant text.

# Contents

This repository contains the following scripts:

1. encoder.py: This script is directly sourced from the OpenAI repository. It provides the implementation of the positional encoding used in transformer models.
2. gpt2.py: The core of the GPT-2 model resides in this script. It includes the GPT-2 architecture and the code for text generation. 
3. gpt2_mini.py: Building upon the principles in gpt2.py, this script offers an even more condensed version of the GPT-2 model. While simplified compared to the full GPT-2 implementation, it retains the essential components for generating text based on the given prompt. It's designed to showcase how a functional language model can be implemented with minimal lines of code, serving as a helpful educational resource.
4. utils.py: To aid in setting up the miniGPT model, utils.py contains functions for downloading and loading GPT-2 model weights, the tokenizer, and hyperparameters. This simplifies the process of getting started with miniGPT.

# Usage

To use miniGPT for text generation, follow these steps:

Install the required dependencies: tensorflow, fire, regex, numpy
Choose between gpt2.py for a more comprehensive model or gpt2_mini.py for an even more compact version.
Run the script and witness miniGPT generate text that follows the context of your prompt.

```python gpt2_mini.py "Arsenal played well in the Premier League last season. I think this season"```

You can also control the number of tokens to generate, the model size (one of ["124M", "355M", "774M", "1558M"]), and the directory to save the models:

```python gpt2_mini.py "Arsenal played well in the Premier League last season. I think this season" --n_tokens_to_generate 100 --model_size "774M" --models_dir "gpt_models"```

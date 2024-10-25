# Retrieval-Augmented Generation

This repository contains a notebook for the demonstration of Retrieval-Augmented Generation based on a ChromaDB Vector Database and an LLM. It demonstrates the basic workflow for both a local LLM (Llama 3.1) as well as a cloud-based LLM (OpenAI API).

To execute the code in the notebook, some preparatory steps are required:

## Llama 3.1 Setup

The notebook requires a configured PyTorch installation (including `torchvision` and `torchaudio`). Please follow one of the many publicly available manuals to set up PyTorch; ensure to pick the version matching your `CUDA` version. I am using `torch 2.4.1` for this notebook.

From the model perspective, you need to download `Llama 3.1` in a version of your choice depending on your available hardware. In the notebook, a quantized version of the 8B parameter model is applied; details on the different versions are reported here: https://huggingface.co/meta-llama/Llama-3.1-8B.

## Dependencies

All requirements apart from PyTorch can be installed via `pip install -r requirements.txt` in the same environment.

## OpenAI API Key Setup

The processing of prompts via the OpenAI API requires an OpenAI account. Additionally, you need to set up an API Key and charge the account to ensure a non-zero balance.

Store the API credentials in a `.env` file in a location of your choice in the following format:

```txt
OPENAI_API_KEY=sk-...
```

Then point the `load_dotenv` call in the notebook to this file.

# llms

Experiments with large language models — interpretability, steering, and concept inspection.

## Steerling-8B Exploration

`steerling_explore.ipynb` explores [Steerling-8B](https://huggingface.co/guidelabs/steerling-8b), an interpretable language model that decomposes its hidden state into ~33k known concept dimensions. The notebook covers:

1. **Basic generation** — simple text generation with the model
2. **Concept inspection** — identifying which concept dimensions activate for a given input
3. **Concept comparison** — finding shared vs. unique concepts between two texts
4. **Concept steering** — amplifying or suppressing specific concepts to influence generation
5. **Activation heatmap** — per-token concept activation visualization
6. **Sandbox** — open-ended steering experimentation

## Setup

```bash
python -m venv steerling-venv
source steerling-venv/bin/activate
pip install steerling torch
```

The notebook expects the Steerling-8B model weights cached locally via Hugging Face. It runs on Apple Silicon (MPS).

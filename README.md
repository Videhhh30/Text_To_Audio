# Text_To_Audio
Here's a clean and professional `README.md` for your GitHub repository, based on the provided code snippet using Hugging Face's `suno/bark-small` for text-to-speech:

---

# 🗣️ Text-to-Speech with `suno/bark-small`

This repository demonstrates a simple implementation of text-to-speech (TTS) using Hugging Face's `transformers` library and the `suno/bark-small` model.

## 🚀 Overview

Convert written text into natural-sounding speech using the `suno/bark-small` TTS model powered by Hugging Face Transformers. The output audio can be played directly in a Jupyter Notebook.

## 🛠️ Installation

Make sure you have Python 3.7+ and a CUDA-enabled GPU.

Install the required packages:

```bash
pip install transformers
```

> Note: `transformers` automatically installs `torch`, but make sure you have the appropriate CUDA version installed for GPU support.

## 🧪 Usage

Here's a quick example to run the text-to-speech pipeline:

```python
from transformers import pipeline
from IPython.display import Audio

# Define input text
text = "Python is a high-level, general-purpose programming language."

# Load TTS pipeline with the Bark-small model
pipe = pipeline("text-to-speech", model="suno/bark-small", device="cuda")

# Generate audio
output = pipe(text)

# Play audio in Jupyter Notebook
Audio(output["audio"], rate=output["sampling_rate"])
```

## 📦 Model

* **Model Used:** [`suno/bark-small`](https://huggingface.co/suno/bark-small)
* **Framework:** [Transformers by Hugging Face](https://huggingface.co/docs/transformers)

## ⚙️ Requirements

* `transformers >= 4.36`
* `torch >= 2.0`
* CUDA-compatible GPU (for optimal performance)

## 📋 Notes

* The `suno/bark-small` model is a compact version of Bark and provides reasonable speech quality with reduced computational load.
* Works well for short texts in English.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 🙌 Acknowledgments

* [Hugging Face](https://huggingface.co) for the Transformers library and pre-trained models.
* [Suno AI](https://suno.ai) for the Bark TTS model family.

---


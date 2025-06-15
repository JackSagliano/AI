# 🤖 Fine-tuning LLMs for Code Generation

This project provides a Google Colab notebook designed to fine-tune a language model (LLM) for code generation tasks. It leverages QLoRA for efficient training on low-resource GPUs and uses an instruction-tuned dataset containing Python code examples.

## 🎯 Objectives

- Fine-tune a pre-trained LLM using QLoRA
- Optimize the model for generating high-quality Python code
- Evaluate the model’s performance through advanced code quality metrics

## ⚙️ Base Model

- [`deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B`](https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B)

## 📚 Dataset

- [`bigcode/self-oss-instruct-sc2-exec-filter-50k`](https://huggingface.co/datasets/bigcode/self-oss-instruct-sc2-exec-filter-50k)
- Using a 4,000-sample subset for training

## 🧪 Techniques & Tools

- **QLoRA** for memory-efficient fine-tuning
- **BitsAndBytes** for 4-bit quantization
- **PEFT** (Parameter-Efficient Fine-Tuning)
- Code evaluation using code similarity (between our model's solution and the canonical one), `pylint`, and `radon` metrics

## 📦 Main Libraries

- `transformers`
- `peft`
- `trl`
- `bitsandbytes`
- `evaluate`, `radon`, `zss`

## 🚀 How to Use

1. Open the notebook `ProgettoAggiornato.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Run the cells in order: installations → setup → training → evaluation
3. Customize variables such as `model_name`, `dataset_range`, or LoRA parameters
4. Save the fine-tuned model or export results for further analysis

## 📊 Output

- A code-generation-optimized model
- `.json` files with generated outputs and evaluation scores
- Automatic quality reports on model generations


---

💡 *To better understand QLoRA and LLMs, check out the [Hugging Face PEFT documentation](https://github.com/huggingface/peft) and official model pages.*

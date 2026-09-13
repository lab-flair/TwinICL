# TwinICL

Resources for **TwinICL: Diagnosing Multimodal In-Context Learning through Paired Counterfactuals**.

**[🤗 Dataset on Hugging Face](https://huggingface.co/datasets/zihan-xue/twinicl-bench)**

## Overview

TwinICL is a benchmark for studying how input modality affects in-context learning—the ability to infer a task from demonstrations and apply it to a new input.

The benchmark pairs text and image versions of the same underlying shape tasks, enabling controlled comparisons across modalities. It includes **38 tasks** across four families: **selection, relation, aggregation, and transformation**.

This repository serves as the central resource page for the project.

## Dataset

The dataset is available on **[Hugging Face](https://huggingface.co/datasets/zihan-xue/twinicl-bench)**.

The current release contains:

- **38 tasks**, with 132 underlying examples per task.
- **Eight rendering variants** per example: four text styles and four image palettes.
- **40,128 rows** in total.

Each row contains the task name, rendering variant, text or image input, and expected text answer. Corresponding examples appear in the same row order within each task's variant files.

See the [dataset documentation](https://huggingface.co/datasets/zihan-xue/twinicl-bench/blob/main/README.md) for field descriptions, rendering details, and answer conventions.

### Load the dataset

Install the Hugging Face Datasets library:

```bash
pip install datasets
```

Load the dataset in Python:

```python
from datasets import load_dataset

data = load_dataset("zihan-xue/twinicl-bench", split="test")
```

The current release places all examples in a single split named `test`. These rows are individual examples; loading them does not construct the demonstration-and-query prompts used for in-context learning evaluation.

## Release Status

- **Dataset:** available on Hugging Face.
- **Evaluation and generation code:** not yet released.

Links to additional resources will be added here as they become available.

## Dataset License

The dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license, as specified on its [Hugging Face page](https://huggingface.co/datasets/zihan-xue/twinicl-bench).

## Contact

For questions or issues, please open an issue in this repository.

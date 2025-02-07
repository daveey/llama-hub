# Asana Loader

This loader loads documents from Asana. The user specifies an API token to initialize
the AsanaReader. They then specify a `workspace_id` to load in
the corresponding Document objects.

## Usage

Here's an example usage of the AsanaReader.

```python
from gpt_index import download_loader
import os

AsanaReader = download_loader('AsanaReader')

reader = AsanaReader("<ASANA_TOKEN">)
documents = reader.load_data(workspace_id="<WORKSPACE_ID">)

```

This loader is designed to be used as a way to load data into [GPT Index](https://github.com/jerryjliu/gpt_index/tree/main/gpt_index) and/or subsequently used as a Tool in a [LangChain](https://github.com/hwchase17/langchain) Agent. See [here](https://github.com/emptycrown/llama-hub/tree/main) for examples.

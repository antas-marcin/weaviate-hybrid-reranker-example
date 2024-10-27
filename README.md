# Weaviate Hybird, Reranker example

🎯 Overview
-----------

This is a simple demo of how one can run Weaviate vectorizer, reranker and generative Ollama modules and presents how one can perform meaningful searches.

📦 Requirements
----------------

In order to be able to create Weaviate one needs at least:

1. Docker
2. Python3

💡 Running
----------

In order to run the setup one needs to issue:

```sh
docker compose up -d
```

Please note that below operations take some time to succeed.

Pull [Aya-Expanse](https://huggingface.co/CohereForAI/aya-expanse-8b) model. It's an open source multi linugal large language model from Cohere. Please note that you need at least 5GB of free space on your disk.

```sh
docker exec -i generative_ollama ollama pull aya-expanse:8b
```

In order to run notebooks, it's advised to setup a venv for a project.

```sh
python3 -m venv .venv
source .venv/bin/activate
pip3 install -r requirements.txt
```

📖 How to use notebooks
----------

1. Import data: ([0-import.ipynb](./notebooks/0-import.ipynb))
2. Reranker example: ([1-reranker.ipynb](./notebooks/1-reranker.ipynb))
3. Hybrid example: ([2-hybrid.ipynb](./notebooks/2-hybrid.ipynb))

🔗 Useful links
----------

([Dataset used in notebooks](https://huggingface.co/datasets/neuralwork/arxiver))
([Vector similarity search](https://weaviate.io/developers/weaviate/search/similarity))
([Keyword search](https://weaviate.io/developers/weaviate/search/bm25))
([Hybrid search](https://weaviate.io/developers/weaviate/search/hybrid))
([Reranking](https://weaviate.io/developers/weaviate/search/rerank))

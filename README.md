# Projeto Oraculo

Use virtual env.

## Getting Started

Requirements:

- Python >=3.8
- Chroma
- Langchain

To get started with the LangChain library and this script, follow these steps:

1. Copy .env.copy to .env and populate the required api keys and notion database id

```shell
cp .env.copy .env
```

2. Install the required dependencies:

```shell
pip install -r requirements.txt
```

3. Set up your Notion API credentials. Follow the instructions in the [LangChain documentation](https://langchain-docs.com) to obtain the necessary credentials.

4. Update the script with your Notion database details. Replace the placeholders in the script with your own database URL, token, and other relevant information.

5. Run the script:

```shell
python oraculo.py
```

> The first time it will take a while to download and build your index. My notes took 5 minutes.

## Docker

6. Build the image

```shell
docker build --no-cache -t notionrag .
```

7. Run locally

```shell
docker run -rm --env-file .env -p 8501:8501 notionrag
```

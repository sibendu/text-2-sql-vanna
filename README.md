# Introducing Vanna AI
Text-To-SQL Playground

This GitHub repository is a companion resource to the Medium article [Text-to-SQL Just Got Easier: Meet Vanna AI, Your Text-to-SQL Assistant
](https://medium.com/mitb-for-all/text-to-sql-just-got-easier-meet-vanna-ai-your-rag-powered-sql-sidekick-e781c3ffb2c5)

[![Watch the video](https://raw.githubusercontent.com/tituslhy/glowing-engine/main/images/bullrun_thumbnail.png)](https://raw.githubusercontent.com/tituslhy/glowing-engine/main/media/bullrun_app.mp4)

## Setup
This repository uses the [uv package installer](https://docs.astral.sh/uv/pip/packages/). 

To create a virtual environment with the dependencies installed, simply type in your terminal:
```
uv sync
```

### Azure OpenAI Configuration
This application has been configured to use Azure OpenAI. You need to set up the following environment variables in a `.env` file:

```
AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com/
AZURE_OPENAI_GPT4O_DEPLOYMENT_NAME=gpt-4o
AZURE_OPENAI_API_KEY=your-api-key-here
AZURE_OPENAI_API_VERSION=2024-12-01-preview
```

**To get these values:**
1. Go to your Azure OpenAI resource in the Azure Portal
2. Navigate to **Keys and Endpoint**
3. Copy the endpoint URL and API key
4. Use your GPT-4o deployment name (created in Azure OpenAI Studio)

You can copy `.env.example` to `.env` and fill in your Azure OpenAI credentials.

You'll need to ingest the data into an SQLite database before you can interact with the app. Simply run the codes in `./notebooks/setup_db.ipynb` to ingest the ticker information from [Yahoo Finance](https://github.com/ranaroussi/yfinance).

## To run Chainlit app
This spins up your application on port 8000
```
chainlit run app.py
```

# Text-To-SQL with Vanna AI

## Setup

### Step 1: Setup environment

```
uv sync
```

### Step 2: Ingest data

To ingest the data into an SQLite database, run `./notebooks/setup_db.ipynb` 

### Step 3 Azure OpenAI Configuration

`.env` file:

```
AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com/
AZURE_OPENAI_GPT4O_DEPLOYMENT_NAME=gpt-4o
AZURE_OPENAI_API_KEY=your-api-key-here
AZURE_OPENAI_API_VERSION=2024-12-01-preview
```


## Run app

```
chainlit run app.py
```

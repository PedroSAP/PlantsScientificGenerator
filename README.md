# 🌿 PlantsScientificGenerator

This project is a FastAPI-based REST API powered by a public LLM (from Hugging Face) that allows users to input sentences with common plant names and receive their corresponding scientific names.

## 🚀 Features

- Natural language input
- Name extraction and classification using `flan-t5-xl`
- Easy deployment via Docker

## 📦 Setup

```bash
git clone https://github.com/yourusername/PlantsScientificGenerator.git
cd PlantsScientificGenerator
pip install -r requirements.txt
uvicorn app.main:app --reload
```

## 🐳 Docker Support

```bash
docker build -t plants-api 
docker run -p 8000:8000 plants-api
```

## 📬 Example Input

```json
{
  "user_sentence": "What is the scientific name of the monkey puzzle tree?"
}
```

## 📬 Example Output

```json
{
  "original_sentence": "...",
  "detected_common_name": "monkey puzzle tree",
  "scientific_name": "Araucaria araucana"
}
```

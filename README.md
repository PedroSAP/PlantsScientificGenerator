# 🌿 PlantsScientificGenerator

This project is a FastAPI-based REST API powered by a public LLM (from Hugging Face) that allows users to input the name of a common plant and receive its corresponding scientific name.

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
  "user_sentence": "Sunflower"
}
```

## 📬 Example Output

```json
{
  "original_input": "Sunflower",
  "scientific_name": "'Helianthus annuus'"
}
```

# Sentiment-Analysis-Gemini

## Overview
A FastAPI-based web service for sentiment analysis using Google's Gemini API. This project is built following the 12-Factor App methodology and demonstrates production-ready practices including Dockerization, CI/CD, and pre-commit hooks.


## Features

- Sentiment analysis using gemini 
- Modular, extensible Python codebase
- Docker containerization for consistent environments
- Easy setup and usage

## Installation

### Prerequisites

- Python 3.7 or higher
- [Docker](https://www.docker.com/) (optional, for containerized usage)
- git

### Clone the Repository

```bash
git clone https://github.com/BarshaRegmi/Sentiment-Analysis-Gemini
cd Sentiment-Analysis-Gemini


### Create virtual environment and activate it
```bash
python -m venv env
source env/bin/activate   # On Windows: env\Scripts\activate


### Install Python Dependencies
```bash
pip install -r requirements.txt

### Add your api key
Create a .env file in the root directory:
```bash
GEMINI_API_KEY=your_gemini_api_key_here



### Running the api
```bash
uvicorn app.main:app --reload


### Testing
```bash
pytest


### API Endpoint
POST /api/analyze

Request body


{
  "text": "I love this product!"
}


Response

{
  "sentiment": "positive"
}


### Docker Support
To build and run application with docker
```bash
docker build -t sentiment-api .
docker run -p 8000:8000 sentiment-api


### Precommit hooks
```bash
pre-commit install


### CI/CD
Includes a sample GitHub Actions workflow in .github/workflows/main.yml to:
Install dependencies and Run tests
# 🧠 MedAI-LLM-Chatbot

An AI-powered Medical Chatbot built using **LLMs, LangChain, Pinecone, Flask, and AWS**, designed to answer medical queries using Retrieval-Augmented Generation (RAG).

---

## Features

- AI Medical Chatbot (LLM-powered)
- Retrieval-Augmented Generation (RAG)
- Vector database using Pinecone
- LangChain integration
- Flask backend API
- OpenAI GPT integration
- AWS CI/CD deployment support
- Dockerized application
- Fast and scalable architecture

---

## 🛠️ Tech Stack

- Python 
- Flask 
- LangChain 
- OpenAI GPT 
- Pinecone Vector DB 
- AWS (EC2, ECR, IAM)
- Docker 
- GitHub Actions 

---

## Project Structure

```
MedAI-LLM-Chatbot/
│── app.py
│── store_index.py
│── requirements.txt
│── .env
│── Dockerfile
│── README.md
│
├── src/
│   ├── helper.py
│   ├── prompt.py
│   ├── utils.py
│
├── templates/
│   ├── index.html
│
├── static/
│   ├── style.css
│
└── data/
    ├── medical_docs/
```

---

##  Installation & Setup

###  Clone Repository

```bash
git clone https://github.com/SSea-man/MedAI-LLM-Chatbot.git
cd MedAI-LLM-Chatbot
```

---

###  Create Virtual Environment (No Conda Needed)

```bash
python3 -m venv medibot
source medibot/bin/activate
```

---

###  Install Dependencies

```bash
pip install -r requirements.txt
```

---

###  Setup Environment Variables

Create `.env` file:

```env
PINECONE_API_KEY=your_pinecone_api_key
OPENAI_API_KEY=your_openai_api_key
```

---

### Build Vector Database

```bash
python store_index.py
```

---

### Run Application

```bash
python app.py
```

Open browser:

```
http://localhost:8080
```

---

## How It Works

1. User enters medical query  
2. Query converted into embeddings  
3. Pinecone retrieves relevant context  
4. LangChain combines context + LLM  
5. OpenAI generates response  
6. Flask returns answer to UI  

---

## AWS CI/CD Deployment

### AWS Services Used

- EC2 (Virtual Machine)
- ECR (Docker Registry)
- IAM (Access Control)
- GitHub Actions (CI/CD Pipeline)

---

## 🚀 Deployment Flow

1. Build Docker image  
2. Push to AWS ECR  
3. Pull image on EC2  
4. Run container  

---

## EC2 Setup

```bash
sudo apt-get update -y
sudo apt-get upgrade -y

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

sudo usermod -aG docker ubuntu
newgrp docker
```

---

## GitHub Secrets

```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
PINECONE_API_KEY
OPENAI_API_KEY
```

---

## Docker Commands

### Build Image

```bash
docker build -t medai-chatbot .
```

### Run Container

```bash
docker run -p 8080:8080 medai-chatbot
```

---

## Future Improvements

- Voice assistant integration   
- Medical report summarizer   
- Multi-language support   
- Patient memory system   
- Mobile app 

---

## Disclaimer

This project is for **educational purposes only** and is not a replacement for professional medical advice.

---

## Author

Shah Mohammed Seaman

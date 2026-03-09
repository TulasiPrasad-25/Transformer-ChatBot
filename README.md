
#  Transformer-Based Conversational Chatbot

A conversational AI chatbot built using the **BlenderBot Transformer model from Hugging Face**.
The application provides a simple **web interface using Streamlit** where users can interact with the chatbot in real time.

The chatbot generates context-aware responses using a **pretrained transformer-based sequence-to-sequence model**.

---

#  Project Overview

This project demonstrates how to build and deploy a **Transformer-based chatbot** using modern NLP frameworks. The system leverages a pretrained model to generate human-like responses and deploys the application through a lightweight web interface.

The goal of this project is to showcase:

* Transformer-based conversational AI
* Integration of Hugging Face models
* Web deployment using Streamlit
* Public access using ngrok

---

#  Model Used

**BlenderBot 400M Distilled**

Model:
`facebook/blenderbot-400M-distill`

Features of this model:

* Pretrained on large conversational datasets
* Transformer-based encoder-decoder architecture
* Designed for open-domain dialogue generation
* Produces contextually relevant responses

Library used: **Hugging Face Transformers**

---

#  Technologies Used

* **Python**
* **PyTorch**
* **Hugging Face Transformers**
* **Streamlit**
* **pyngrok**

---

#  Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/transformer-chatbot.git
cd transformer-chatbot
```

---

### 2. Install Required Libraries

```bash
pip install datasets transformers accelerate streamlit pyngrok torch
```

---

#  Setup ngrok (Optional)

To expose the chatbot publicly, create a free account on:

[https://ngrok.com](https://ngrok.com)

Get your **authentication token** and run:

```python
from pyngrok import ngrok
ngrok.set_auth_token("YOUR_NGROK_TOKEN")
```

---

#  Running the Application

Run the Streamlit app:

```bash
streamlit run app.py
```

The chatbot interface will start at:

```
http://localhost:8501
```

---

#  Exposing the App Publicly

To make the chatbot accessible online:

```python
from pyngrok import ngrok
public_url = ngrok.connect(8501)
print(public_url)
```

This generates a **public URL** that others can use to access the chatbot.

---

#  Example Workflow

1. User enters a message in the Streamlit interface
2. Input is processed by the BlenderBot model
3. Model generates a response using the transformer architecture
4. Response is displayed in the chat interface

---

#  Project Structure

```
chatbot-project
│
├── app.py              # Streamlit chatbot application
├── chatbot.ipynb      # Development notebook
├── requirements.txt   # Required dependencies
└── README.md          # Project documentation
```

---

#  Future Improvements

Possible improvements for this project:

* Fine-tune BlenderBot on domain-specific datasets
* Add conversation history and memory
* Implement response filtering
* Deploy using Docker and FastAPI
* Host on cloud platforms (AWS, GCP, or Hugging Face Spaces)

* architecture diagram
* model explanation.

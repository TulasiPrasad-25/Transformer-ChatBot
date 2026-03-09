Running the Chatbot Locally
1️⃣ Clone the Repository
git clone https://github.com/yourusername/transformer-chatbot.git
cd transformer-chatbot

2️⃣ Install Dependencies
pip install datasets transformers accelerate streamlit pyngrok torch

3️⃣ Add Your ngrok Authentication Token
Create a free account at https://ngrok.com and get your auth token.
Then run the notebook or script and enter the token when prompted:
ngrok_key = getpass.getpass("Enter ngrok key")

4️⃣ Run the Streamlit Application
streamlit run app.py
The app will start on:
http://localhost:8501

5️⃣ Expose the App Using ngrok (Optional)
To make the chatbot publicly accessible:
from pyngrok import ngrok
ngrok.set_auth_token("YOUR_NGROK_TOKEN")
ngrok.connect(8501)
This will generate a public URL for the chatbot.

Model Used:-
This chatbot uses the Hugging Face transformer model:
facebook/blenderbot-400M-distill

Features:
Open-domain conversational AI
Seq2Seq transformer architecture
Pretrained on large dialogue datasets

Technologies Used:-
Python
Hugging Face Transformers
PyTorch
Streamlit
pyngrok

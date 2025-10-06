This project implements an AI Shopping Chat Agent that helps users discover, compare, and learn about mobile phones using natural language queries.

##LIVE DEMO :

IMP: Ollama runs locally so it needs to be installed on local machine.
If LLama not available then results provided by fallback mechanism. 

Deployed on streamlit cloud.

Link : https://aiphoneshoppingchatagent-fyckxr99ctjgdau2r8pedz.streamlit.app/

##SETUP INSTRUCTION

Requirements:

Ollama: for locally running any model.
Python 3.9+
Streamlit
LangChain Community

All requirements provided in requirements.txt

Steps for setup :

git clone https://github.com/AnishaCha/AI_Phone_Shopping_ChatAgent.git

cd AI_Phone_Shopping_ChatAgent

pip install -r requirements.txt

streamlit run AI_AGENT.py

Or Run locally as follows after downloading the code: 

1. Download Ollama.

	ollama run llama3.1:8b

2. Create python environment

	python3 -m venv chatbot

	source chatbot/bin/activate

3. Install packages

	pip install streamlit langchain langchain-community pydantic pandas python-dotenv

4. Run code locally

	streamlit run AI_AGENT.py

##TECH STACK AND ARCHITECTURE

Frontend  :  	Streamlit

AI Model  :  	llama3.1:8b (via Ollama, optional)

Framework  :  	LangChain (for ChatOllama and prompt templating)

Data Source  :  	Local JSON (phones.json) acts as database

Language  :  	Python 3.9.6

Query-> StreamlitUI -> LLAMA via OLLAMA (Generates natural expression) -> Fallback Heuristics (if llama not available) -> Results 

ChatOllama provides a simple interface for calling Llama models locally, instead of manually managing API calls.
ChatPromptTemplate helps you structure messages (system + user roles).

###PROMPT DESIGN AND SAFETY STRATEGY

Prompts are designed to be deterministic, safe, and minimal:
System prompts limit responses to factual, concise, and dataset-based answers.
Llama outputs are post-processed — unstructured responses are ignored.

"You are a shopping assistant. Write a short descriptive paragraph about this phone highlighting its strengths and weaknesses, using only provided specs."

"You are a phone shopping assistant. Write 2-3 sentences describing these phones, focusing on why someone might like them."

###LIMITATIONS

Ollama installation needed.
Text only and no product card.

Source Code : https://github.com/AnishaCha/AI_Phone_Shopping_ChatAgent









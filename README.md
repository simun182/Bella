# Bella

Bella is a custom chatbot that is built on top of llama3 model running locally through Ollama with a memory system through embeddings.
The chat with Bella is converted into a vector representation and stored in memory alongside the original text.
When you ask a new question, Bella calculates the similarity between your query's embedding and previous messages to give you the best response.
The approach is a small-scale version of Retrival-Augmented Generation (RAG), done entierly offline.

Requirements:
1. Ollama installed and running locally
2. Llama3 model installed in ollama
3. Nomic-embed-text embedding model also installed in ollama
4. Python packages: numpy and requests

Everything is open source and free !

How to use:
1. Start Ollama (ollama serve)
2. Run the llama3 model (optional, but might run into some errors if you don't run it before use)
3. Run the python code and it should work

Customizations:
You can change the llm that Bella runs on, you can change it for something less powerful (like tinyllama) or something more powerful (like deepseek) depending on your system specs. 
Just install that model, run it, change the llm_model variable in the code and its ready to use. 
You can change the prompt that is sent to Bella to change her personality, it is under function llm.
You can also change the variable most_similar in recall_context function to change how many past messages Bella recalls.

I am looking forward on working more on this project and adding new features and I hope you enjoy using Bella !




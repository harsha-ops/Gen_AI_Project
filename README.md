# Gen AI Project

## Overview
This project is a Dockerfile Generator AI that uses both local and hosted Large Language Models (LLMs) to generate Dockerfiles based on user input. It ensures adherence to security best practices while creating Dockerfiles.

## What is a Local LLM?
A Local LLM (Large Language Model) is a model that can be installed and run on local machines.

### Advantages:
- Ensures data security and privacy.
  
### Disadvantages:
- Requires infrastructure maintenance.

Ollama is one of the tools used to run LLMs locally on machines.

## What is a Hosted LLM?
A Hosted LLM is a model hosted on external servers, accessible via services like OpenAI.

### Advantages:
- No infrastructure maintenance is required.

### Disadvantages:
- Data security may be compromised as data is sent to external servers.

## Local LLM

### Prerequisites
1. **Download and Install Ollama**  
   For Linux:
   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ```

2. **Pull the Llama3 Model**  
   ```bash
   ollama pull llama3.2:1b
   ```

3. **Create a Virtual Environment**  
   ```bash
   python3 -m venv venv
   source venv/bin/activate 
   ```

### Run the Application
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/Gen_AI_Project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Gen_AI_Project/local-llms-ollama
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the application:
   ```bash
   python3 generate_dockerfile.py
   ```
5. Follow the prompts to interact with the Generative AI model.

### Example Usage
   ```bash
   python3 generate_dockerfile.py
   Enter programming language: python
   # The generated Dockerfile will be displayed...
   ```

## Hosted LLM

### Prerequisites
1. Create an API key using GoogleAI Studio.
2. Insert the API key into the `hosted-llms-gemini/generate_dockerfile_gemini.py` file.

### Run the Application
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/Gen_AI_Project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Gen_AI_Project/hosted-llms-gemini
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the application:
   ```bash
   python3 generate_dockerfile_gemini.py
   ```
5. Follow the prompts to interact with the Generative AI model.

### Example Usage
   ```bash
   python3 generate_dockerfile_gemini.py
   Enter programming language: python
   # The generated Dockerfile will be displayed...
   ```

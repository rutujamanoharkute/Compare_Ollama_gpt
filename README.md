# Compare Ollama (Llama3, Gemma:2b) and OpenAI GPT Models
<img width="1440" alt="image" src="https://github.com/rutujamanoharkute/Compare_Ollama_gpt/assets/114360071/d80fa56e-6679-436f-b0e2-5e4e5edb170f">




---

# Chef Bot: Comparing Ollama (Llama3, Gemma:2b) and OpenAI GPT Models

Welcome to Chef Bot! This README provides an overview of the project, which compares the performance of Ollama's Llama3 (Gemma:2b) and OpenAI's GPT models in the context of generating culinary content. This includes generating recipes, answering cooking-related questions, and providing culinary tips, with a special focus on Indian cuisine.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Model Comparison](#model-comparison)
   - [Ollama Llama3 (Gemma:2b)](#ollama-llama3-gemma2b)
   - [OpenAI GPT Models](#openai-gpt-models)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Examples](#examples)
7. [Contributing](#contributing)
8. [License](#license)

## Introduction

Chef Bot is designed to leverage the capabilities of advanced language models to assist with culinary tasks, with a special focus on Indian cuisine. By comparing Ollama's Llama3 (Gemma:2b) and OpenAI's GPT models, we aim to identify which model offers superior performance in generating accurate, useful, and creative culinary content.

## Features

- **Recipe Generation**: Create new and unique recipes based on given ingredients or cuisines.
- **Cooking Q&A**: Answer cooking-related questions with detailed explanations.
- **Culinary Tips**: Provide useful tips and tricks for improving cooking skills.

## Model Comparison

### Ollama Llama3 (Gemma:2b)

- **Architecture**: Based on the Llama3 architecture, specifically the Gemma:2b variant.
- **Strengths**: 
  - Excels in understanding and generating text related to culinary arts.
  - Provides creative and diverse recipe suggestions.
  - Efficient in handling complex cooking queries.
- **Weaknesses**:
  - May require more fine-tuning for highly specialized culinary knowledge.
  - Limited availability of training data compared to OpenAI models.

### OpenAI GPT Models

- **Architecture**: Various versions of the Generative Pre-trained Transformer (GPT) architecture.
- **Strengths**:
  - Extensive training on diverse datasets, including culinary content.
  - High accuracy in answering cooking-related questions.
  - Robust and reliable performance in generating detailed recipes and tips.
- **Weaknesses**:
  - Can occasionally produce overly complex or impractical recipes.
  - Higher computational resource requirements.

## Installation

To install and set up Chef Bot, follow these steps:

1. **Clone the repository**
   

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Install Ollama Llama3 and Gemma:2b models**:
   - Follow the instructions at [Ollama GitHub repository](https://github.com/ollama/ollama) to install the models locally.
   - Run the following commands to set up the models:
     ```bash
     ollama run llama3
     ollama run gemma:2b
     ```

4. - Run the following commands to create the model files:
     ```bash
     ollama create chef -f ./Modelfile
     ollama create chef2 -f ./Modelfile
     ```
   - Go to this directory and create the below files and add below content.

 **Create model files**:
   - Create `Modelfile` and add the following content for Llama3:
     ```plaintext
     FROM llama3

     # set the temperature to 1 [higher is more creative, lower is more coherent]
     PARAMETER temperature 1

     # set the system message
     SYSTEM """
     You are a Indian Chef like Ranveer Brar. Answer as Chef, the assistant, only.
     """
     ```

   - Create `Modelfile2` and add the following content for Gemma:2b:
     ```plaintext
     FROM gemma

     # set the temperature to 1 [higher is more creative, lower is more coherent]
     PARAMETER temperature 1

     # set the system message
     SYSTEM """
     You are a Indian Chef like Ranveer Brar. Answer as Chef, the assistant, only.
     """
     ```



5. **Set up API keys**:
   - Obtain an API key for OpenAI.
   - Create a `.env` file in the root directory and add your OpenAI API key:
     ```
     OPENAI_API_KEY=your_openai_api_key
     ```

## Usage

To use Chef Bot, run the following command:

```bash
python chef_bot.py
```

To run the Streamlit app, use this command:

```bash
streamlit run app.py
```

You can interact with the bot via the command line or through the Streamlit web application.

## Examples

Here are some examples of what Chef Bot can do:

- **Generate a Recipe**:
  ```
  Input: "Create a recipe for a vegan chocolate cake."
  Output: "Here is a recipe for a vegan chocolate cake: [detailed recipe]"
  ```

- **Answer a Cooking Question**:
  ```
  Input: "How do I make pasta al dente?"
  Output: "To make pasta al dente, follow these steps: [detailed instructions]"
  ```

- **Provide a Culinary Tip**:
  ```
  Input: "What's a good tip for baking bread?"
  Output: "Make sure to let your dough rise fully before baking for a better texture."
  ```

## Contributing

We welcome contributions to Chef Bot! Please see our [contributing guidelines](CONTRIBUTING.md) for more information.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to adjust any sections as needed!




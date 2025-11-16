## 1. LLM Sentiment Classification Example

This is a minimal Python example showing how to use OpenAI's ChatCompletion API to classify the sentiment of a restaurant review.

## Setup

1. Create and activate a virtual environment.
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Add your API key in a `.env` file:
    ```
    OPENAI_API_KEY=your_api_key_here
    ```
4. Run:
    ```bash
    python main.py
    ```

---

# Week 1: Introduction to AI & Generative AI

## 1. Different Types of AI Models

- **Supervised Learning**: The AI model learns from labeled data to make predictions.
- **Generative AI**: Produces well-made content (text, voice, images, videos, etc.) based on a prompt.
- **Unsupervised Learning**: The model finds hidden patterns in data without labels.

## 2. Applications of Generative AI

- **Text Generation**: Writing stories, articles, etc.
- **Reading**: Proofreading, summarizing, classification, etc.
- **Chatbots**: AI-powered systems designed for communication. They vary in functionality:
  - Some chatbots access databases and respond based on both pre-trained knowledge and real-time data.
  - Others rely solely on the training they've received.

## 3. Strengths of Generative AI

- **Supervised Learning**: Excels in predicting outcomes based on input data.
- **Generative AI**: Capable of producing creative outputs such as text, images, or videos based on specific prompts.

## 4. How to Prompt Generative AI (LLMs)

To get the best results from a large language model (LLM), follow these steps:

- **Provide Clear Inputs**: Be specific about the type of output you want.
- **Specify the Task**: Clearly define what you want the AI to do.
- **Categorize Output Fields**: If necessary, categorize the output based on your needs.
- **Iterate and Experiment**: Try different approaches to refine your prompts.

## 5. Limitations of Generative AI

- **Knowledge Cutoff**: AI models are trained on data up to a specific date and may not have knowledge of events or developments beyond that.
- **Hallucinations**: The AI can sometimes produce information that is incorrect or entirely fabricated.
- **Handling Structured/Tabular Data**: Supervised learning is better suited than generative AI for working with structured or tabular data.
- **Biases and Toxicity**: Generative AI can reflect societal biases and toxic language present in the data it was trained on.
- **Assumptions**: Without explicit instructions, treat an LLM as a "fresh college graduate" who needs guidance to provide accurate answers.

## 6. Best Practices for Prompting

- **Be Detailed and Specific**: The more precise you are, the better the AI's response will be.
- **Guide the AI**: Help the AI think through the problem and answer systematically.
- **Experiment and Iterate**: Refining the prompts through trial and error can improve the quality of the output.

## 7. Image Generation with Diffusion Models

- **Training of Diffusion Models**: These models start with a random image and progressively add noise over multiple iterations. The model then learns to reverse this process to generate new images.
- **Prompting Diffusion Models**:
  - **Inputs**: A noisy image and a prompt.
  - **Outputs**: The model generates an image that is less noisy and closer to the desired output.

## 8. Deployment of Generative AI Chatbots

Steps involved in deploying a generative AI chatbot:

1. **Development and Testing**: The developer tests the chatbot internally.
2. **Internal Deployment**: The bot is deployed for use within the company.
3. **External Deployment**: Once it proves to be robust, the bot is made available to customers.

## 9. Types of Human/Bot Interaction Ratios in Deployment

- **Full Human**: All tasks are handled by humans.
- **Human-in-the-Loop**: A human monitors and assists the bot, ensuring quality and accuracy.
- **Bot Triage**: The bot handles most tasks but escalates critical ones to humans.
- **Full Bot**: The bot handles all tasks independently.
## 2. LLM Sentiment Classification Counter Example

This is a minimal Python example showing how to use OpenAI's ChatCompletion API
to classify the sentiment of a restaurant review & then count and print the number of positive and negative sentiments.

## Setup

1. Create and activate a virtual environment.
2. Install dependencies:
pip install -r requirements.txt
3. Add your API key in a `.env` file:
OPENAI_API_KEY=your_api_key_here
4. Run:
python main.py
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

## 2. LLM Sentiment Classification Counter Example

This is a minimal Python example showing how to use OpenAI's ChatCompletion API
to classify the sentiment of a restaurant review & then count and print the number of positive and negative sentiments.

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

---

# Week 2: Deployment, Model Selection & Advanced Gen-AI Concepts

## 1. Deployment Steps

### 1.1 Supervised Learning Deployment
- Gather labeled data — ~1 month  
- Train the model — ~3 months  
- Deploy the model — ~1 month  

### 1.2 Prompt-Based AI Deployment
- Design the prompt — Minutes to hours  
- Deploy the system — Days to weeks  

## 2. Lifecycle of a Gen-AI Project (Experimental Process)

1. Define the scope of the project  
2. Build / Improve the system  
3. Test & evaluate internally (developer or internal company users)  
4. Iterate between steps (2) and (3) until robust  
5. Deploy & monitor performance  

## 3. Tools to Improve Gen-AI Performance

- Prompting  
- RAG (Retrieval-Augmented Generation)  
- Fine-Tune Models  
- Pre-Trained Models (training from scratch)  

## 4. Cost Intuition: Tokens

- Tokens are the units LLMs use to process text  
- Approximation: **Token count ≈ Word count × 1.33**  
- Costs scale with:
  - Input tokens  
  - Output tokens  
  - Model size  

## 5. RAG vs. General LLM Behaviour

### 5.1 General LLM Without RAG
- Example: When asked about parking, it may respond:  
  *"I need more information about what you're talking about."*

### 5.2 LLM With RAG
- Retrieves relevant information  
- Incorporates it into the prompt  
- Produces a more context-aware answer  

### 5.3 RAG Applications
- Chat with PDF  
- Answering questions using website content  
- Web search with AI mode  

**RAG transforms LLMs from knowledge sources into reasoning engines.**

## 6. Pre-Training & Fine-Tuning

### 6.1 Pre-Training
- Trained on hundreds of billions of words  
- Costs tens of millions of dollars  
- Takes months  
- Used for highly specialized domains or last-resort cases  

### 6.2 Fine-Tuning
- Further training on 1K–100K examples  
- Helps:
  - Imitate styles  
  - Learn domain-specific knowledge  
  - Improve small models for harder tasks  

**Rule of Thumb:**  
Start with a pre-trained model, then fine-tune for your specific business needs.

## 7. Choosing a Model

### 7.1 Model Size Guidelines
- **1B parameters** — Simple tasks (e.g., sentiment analysis)  
- **10B parameters** — Business chatbots, basic instructions  
- **100B+ parameters** — Deep knowledge, advanced reasoning  

### 7.2 Closed-Source Models
- Easy integration  
- Powerful and reliable  
- Cloud infrastructure  
- Relatively inexpensive  
- Lower vendor lock-in risk than before  

### 7.3 Open-Source Models
- Full control  
- Can run on your own hardware  
- Maximum privacy and data control  

## 8. Instruction Tuning & RLHF

### 8.1 Instruction Tuning
- Teaches LLMs to follow instructions  
- Uses (question → ideal answer) datasets  

### 8.2 RLHF (Reinforcement Learning from Human Feedback)
- Train a model to score answer quality  
- LLM generates responses  
- Model learns to prefer high-scoring answers  

## 9. Tool Use

### 9.1 Actions
(Enabled through fine-tuning)
- Process orders  
- Send user info/location to external software  
- Trigger workflows  

### 9.2 Reasoning Tools
- LLMs struggle with math  
- Require tools (like calculators) for accurate reasoning  

## 10. Agents

Agents use LLMs to perform multi-step, complex actions.

### Agents Can:
- Search  
- Visit and parse webpages  
- Summarize retrieved content  
- Plan and execute sequences of tasks  

Agents represent cutting-edge Gen-AI capability.

# Week 3: Gen-AI Impact, Jobs, Job Automation & Responsible AI

## 1. Day-to-Day Uses of Gen-AI
- **Writing Assistant**
- **Marketer** (Brainstorming)
- **Recruiter** (Summarizing reviews)
- **Programmer** (Coding)

---

## 2. Task Analysis of Jobs

### 2.1 Identifying Automation Opportunities
- Jobs are made of many mini-tasks.
- Some tasks can be automated even when the full job cannot.
- Example: **Customer service representatives**.

### 2.2 How to Assess Automation Potential
- Evaluate whether AI can perform each specific task.
- Test uncertain tasks with an LLM.
- Use partial automation to improve workflow.

---

## 3. Augmentation vs. Automation
- Companies usually begin with **augmentation** (AI assists workers).
- As models improve, they transition toward **automation** (AI performs tasks independently).

> _Waste — 15/11/2025, 23:24_

---

## 4. Evaluation of AI Potential

### 4.1 Technical Analysis
- Can the AI do X?
- Could a **fresh graduate** do it?
- If unsure, test with an LLM.
- Enhance capabilities using:
  - **RAG**
  - **Fine-tuning**

### 4.2 Business Analysis
- How much time does the task take?
- Does augmentation/automation yield ROI?
- Does improving this workflow increase business value?

### 4.3 Further Job Analysis
- Most jobs involve **many tasks**, not just one or two.
- Gen-AI can support multiple task categories, making it widely applicable.

> _Waste — 16/11/2025, 00:12_

---

## 5. Roles Needed to Build Gen-AI Software

### 5.1 Core Technical Roles
- **Software Engineer**  
  - Writes code  
  - Should understand prompting/LLMs  
- **Machine Learning Engineer**  
  - Implements AI systems  
  - Skilled in RAG, prompting, and fine-tuning  
- **Machine Learning Researcher**  
  - Conducts advanced research to improve AI models  

### 5.2 Data & Analytics Roles
- **Data Engineer**  
  - Ensures data structure and quality  
- **Data Scientist**  
  - Analyzes data to guide business decisions  

### 5.3 Product & Coordination Roles
- **Product Manager**  
  - Defines project scope and goals  
- **Project Engineer**  
  - Coordinates team efforts  
- **Prompt Engineer**  
  - Rarely a standalone role  

> _Waste — 16/11/2025, 00:43_

---

## 6. Automation Potential Across Sectors
- **Supervised learning** affects *lower-wage* jobs more.
- **Gen-AI & LLMs** impact *higher-wage* jobs significantly.
- **Knowledge workers** are more impacted than manual labor roles.

> _Waste — 16/11/2025, 01:00_

---

## 7. Concerns About AI
- Amplifying harmful human behaviors  
- Job displacement  
- Extreme-risk scenarios (e.g., extinction)  
- AI is still valuable even without perfect control  

### 7.1 Artificial General Intelligence (AGI)
- **Definition:** AI capable of performing *any* intellectual task a human can.

> _Waste — 16/11/2025, 01:10_

---

## 8. Responsible AI

### 8.1 Dimensions of Responsible AI
- **Fairness**  
- **Transparency**  
- **Privacy**  
- **Security**  
- **Ethical Use**  

### 8.2 Tips for Responsible AI
- Foster open discussion about ethical issues.
- Brainstorm how systems might fail or cause harm.
- Include diverse perspectives (cultural, ethnic, business).


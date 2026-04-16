# ☕ Coffee Shop Customer Service Chatbot 🚀

An **Agentic AI-powered chatbot system** designed to enhance customer experience in a coffee shop application. This project leverages **LLMs, RAG (Retrieval-Augmented Generation), and a recommendation engine** to handle real-time interactions such as ordering, answering queries, and suggesting products.

---

## 🎯 Project Overview

This project implements a **multi-agent architecture** where each agent is responsible for a specific task, enabling scalable and modular conversational AI.

### ✅ Key Capabilities:

* 🛒 **Order Management** – Handles multi-step order conversations with structured outputs
* 📚 **Menu Q&A (RAG)** – Answers questions about menu items, ingredients, allergens using vector search
* 🎯 **Personalized Recommendations** – Suggests products using Apriori + popularity-based methods
* 🛡️ **Query Filtering** – Blocks irrelevant or unsafe queries using a Guard Agent
* ⚡ **Real-time Chatbot Integration** – Works seamlessly with a React Native mobile app

---

## 🧠 System Architecture (Agentic AI)

The chatbot follows a **modular multi-agent pipeline**, improving control, scalability, and reliability.

### 🤖 Core Agents:

* **Guard Agent**

  * Filters unsafe or irrelevant queries
  * Ensures only valid requests are processed

* **Classification Agent**

  * Routes user queries to the appropriate agent
  * Handles intent detection

* **Details Agent (RAG)**

  * Uses **Pinecone vector database + embeddings**
  * Retrieves relevant knowledge and generates accurate responses

* **Order Taking Agent**

  * Manages multi-turn conversations
  * Maintains **conversation memory**
  * Validates menu items and calculates total order

* **Recommendation Agent**

  * Uses:

    * 📊 **Apriori Algorithm** (frequent itemsets)
    * 📈 **Popularity-based filtering**
  * Suggests complementary products

---

## 🔄 Workflow

```text
User Input
   ↓
Guard Agent (validation)
   ↓
Classification Agent (intent detection)
   ↓
Selected Agent:
   ├── OrderTakingAgent
   ├── DetailsAgent (RAG)
   └── RecommendationAgent
```

---

## 🛠️ Tech Stack

* **LLM Serving:** RunPod (OpenAI-compatible APIs)
* **Backend:** Python
* **Vector DB:** Pinecone
* **Frontend:** React Native
* **Recommendation Engine:** Apriori + Pandas
* **Monitoring (optional):** Grafana
* **Caching (optional):** Redis

---

## 📱 React Native App

The frontend provides a clean interface for users to:

* Browse menu items
* View product details
* Manage cart
* Interact with chatbot in real-time

---

## 📂 Project Structure

```
coffee_shop_customer_service_chatbot/
│
├── coffee_shop_app_folder/       # React Native frontend
├── python_code/
│   ├── API/                     # Backend APIs (Agent system)
│   ├── dataset/                 # Data for recommendation engine
│   ├── products/                # Product metadata
│   ├── build_vector_database.ipynb
│   ├── firebase_uploader.ipynb
│   ├── recommendation_engine_training.ipynb
```

---

## 🚀 Key Features & Highlights

* 🔹 Multi-agent orchestration (AgentController pattern)
* 🔹 Retrieval-Augmented Generation (RAG) for factual responses
* 🔹 Structured JSON outputs for reliable pipelines
* 🔹 Conversation memory handling
* 🔹 Hybrid recommendation system
* 🔹 Scalable and modular architecture

---

## ⚠️ Challenges & Learnings

* ❗ **Handling invalid JSON outputs from LLMs**

  * Fixed using a secondary validation layer

* ❗ **Maintaining conversation state**

  * Solved using structured memory in messages

* ❗ **Incorrect intent classification**

  * Improved with prompt tuning and context limiting

* ❗ **Balancing latency vs accuracy**

  * Optimized using limited context and efficient retrieval

---

## 🔗 References

* RunPod – Model deployment infrastructure
* Pinecone – Vector database for RAG
* Hugging Face – LLM models
* Firebase – App data management
* Kaggle – Dataset for recommendation system

---

## 🎯 Future Improvements

* Add **confidence scoring for classification**
* Implement **fallback/retry mechanisms**
* Integrate **LangGraph for better state management**
* Add **evaluation metrics (latency, accuracy, recall)**

---

## 🙌 Conclusion

This project demonstrates how to build a **production-style AI system** using:

* Agentic workflows
* Retrieval systems
* Recommendation engines

It goes beyond a simple chatbot and focuses on **scalability, modularity, and real-world usability**.

---

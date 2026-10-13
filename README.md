# Intelligent Customer Support Chatbot

**Building an AI-Powered Customer Support Chatbot Using DialoGPT, RoBERTa, and OPT**

## Project Overview

This project explores the development of an intelligent customer support chatbot using Natural Language Processing (NLP) and transformer-based models. The system aims to automate customer interactions by understanding user queries, analyzing sentiment, and generating relevant responses.

The project investigates three models—DialoGPT, RoBERTa, and OPT-125M—to explore different approaches to conversational response generation, query classification, and sentiment analysis.

## Project Objectives

- Automate responses to common customer support queries.
- Generate conversational responses that are relevant to user input.
- Classify customer queries by intent.
- Analyze customer sentiment to support context-aware interactions.
- Compare transformer-based models in terms of response quality and computational efficiency.

## Dataset

The project uses a customer support dataset containing question-and-answer pairs and conversational records.

| Attribute | Description |
|---|---|
| Original dataset size | 27,000 records |
| Sampled dataset | 5,000 records |
| Training split | 80% |
| Testing split | 20% |
| Domain | Customer support and e-commerce |

The dataset includes customer queries, corresponding support responses, query categories, sentiment labels, response times, and resolution statuses.

## Methodology

### 1. Data Preprocessing

The preprocessing pipeline includes:
- Removing missing values.
- Normalizing text and punctuation.
- Removing redundant spaces and unwanted characters.
- Tokenizing text into subword units.
- Applying padding to standardize input sequences.
- Splitting the dataset into training and testing subsets.

### 2. Transformer Models

**DialoGPT — Conversational Response Generation**

DialoGPT was used to generate conversational responses based on user queries. The report found that increasing the token sequence length from 100 to 150 improved the reported accuracy from 30% to 62%.

**RoBERTa — Query Classification and Sentiment Analysis**

RoBERTa was used to classify customer queries and analyze sentiment. The project explored its ability to identify user intent and sentiment categories, although its response-generation performance was limited.

**OPT-125M — Lightweight Response Generation**

OPT-125M was evaluated as a computationally efficient alternative for generating customer support responses. The report observed faster response generation but noted limitations in contextual understanding, fluency, and response coherence.

### 3. Training Configuration

The report describes the following experimental setup:
- **Programming language:** Python 3.9
- **Frameworks:** PyTorch and Hugging Face Transformers
- **NLP libraries:** NLTK and spaCy
- **Batch size:** 8
- **Learning rate:** 2e-5
- **Training epochs:** 3
- **Optimizer:** AdamW
- **Environment:** Google Colab

## Evaluation and Results

The models were evaluated using quantitative metrics and manual inspection of generated responses.

| Model | Reported Results | Main Observation |
|---|---|---|
| DialoGPT | 62% accuracy, 100% precision, 62% recall, 77% F1-score, 0.39 ROUGE-L | More complete and contextually relevant responses with a 150-token sequence |
| OPT-125M | 77% F1-score, 0.39 ROUGE-L | Computationally efficient, but sometimes repetitive and less coherent |
| RoBERTa | 32.7% reported response accuracy and 25% F1-score | More suitable for classification tasks than open-ended response generation |

*These are the results reported in the project paper. The metrics should be interpreted in the context of the experimental setup and the specific task evaluated.*

## Key Findings

- DialoGPT produced the strongest conversational responses among the evaluated approaches.
- Increasing the sequence length from 100 to 150 tokens improved DialoGPT's reported accuracy.
- OPT-125M offered a lighter-weight alternative but struggled with complex queries and response coherence.
- RoBERTa was more appropriate for query classification and sentiment analysis than free-form dialogue generation.
- Combining RoBERTa for classification with DialoGPT for response generation was identified as a potential improvement.

## Technology Stack

- **Programming:** Python
- **Natural Language Processing:** NLP
- **Conversational AI:** DialoGPT
- **Text Classification and Sentiment Analysis:** RoBERTa
- **Response Generation:** OPT-125M
- **Deep Learning:** PyTorch
- **Model Libraries:** Hugging Face Transformers
- **Text Processing:** NLTK, spaCy
- **Development Environment:** Google Colab

## Limitations and Future Work

The study used a sample of 5,000 records from a larger 27,000-record dataset. This reduced the training workload but also limited data diversity and potentially affected generalization.

Future improvements could include:
- Expanding the dataset with a more balanced range of customer queries.
- Fine-tuning models on domain-specific customer support conversations.
- Combining RoBERTa-based query classification with DialoGPT response generation.
- Improving response coherence through post-processing.
- Evaluating performance on a larger, independent test set.
- Further assessing response relevance and consistency across complex conversations.

## Academic Context

**Project:** Building an Intelligent Customer Support Chatbot

**Focus Areas:** Natural Language Processing, Conversational AI, Deep Learning, Text Classification, and Sentiment Analysis


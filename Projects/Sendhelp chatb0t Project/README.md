# Send Help chatbot

AWS Lex Chatbot Project

## 📌 Project Overview

I developed **SendHelp**, an interactive chatbot using Amazon Web Services **Lex** and **Lambda**
.This chatbot simulates a conversational AI assistant that helps users learn about Amazon S3 through both informative responses and an engaging quiz.Through this project, I demonstrated key concepts of chatbot development such as intents, utterances, and conversational flow using AWS services.

---

## 🎯 Project Objectives

* Build a functional chatbot using Amazon Lex
* Create intent-based responses for user interaction
* Design a quiz-based chatbot experience
* Implement branching logic for different user answers
* Demonstrate chatbot functionality through a live interaction


---

## 🧠 How the Chatbot Works

### 🔹 Part 1: Basic Chatbot

I first designed the chatbot with a simple intent to answer questions about Amazon S3.

* **Intent:** S3 Info

* **Example Utterances:**

  * "What is S3?"
  * "Tell me about Amazon S3"

* **Response:**

  * Amazon S3 is a cloud storage service that allows users to store and retrieve data from anywhere.

---

### 🔹 Part 2: Interactive Quiz (SendHelp Feature)

I then expanded the chatbot into a quiz-based learning assistant.

#### 📝 Quiz Flow

1. The user starts the quiz:

   * "Start quiz"
   * "Quiz me on S3"

2. The chatbot asks:

   * *"What does S3 stand for?"*

3. Multiple-choice answers:

   * A) Simple Storage Service
   * B) Secure Server Storage
   * C) Smart Storage System

4. Chatbot responses:

   * ✅ If the answer is correct, I programmed it to confirm and continue
   * ❌ If incorrect, it provides the correct answer and moves on

5. Follow-up question:

   * *"What is Amazon S3 mainly used for?"*

     * A) Cloud storage
     * B) Web hosting
     * C) Cloud computing

6. The chatbot then gives feedback and guides the user through the rest of the quiz.

---

## 🛠️ AWS Services Used

* **Amazon Lex** – used to build and manage the chatbot
* Natural Language Processing (NLP) – to interpret user input

* **Aws Lambda** -used to valid user input,hits API, queries databases

---

## ⚙️ Technical Implementation

* I created intents for both information retrieval and quiz interaction
* I defined utterances to reflect real user input
* I designed responses for correct and incorrect answers
* I implemented branching logic to control the conversation flow
* I tested the chatbot using the Amazon Lex test interface

---

## 💡 Key Learnings

* I learned how chatbots use intents and utterances to understand users
* I improved my ability to design conversational flows
* I implemented branching logic for interactive experiences
* I understood the importance of clear and user-friendly responses
* I explored how AI can support education and knowledge testing

---

## 🎥 Demo & Screenshots

I included screenshots of the chatbot and quiz interaction in the `screenshots` folder.

Examples include:

* Bot creation in Amazon Lex
* Intent and utterance setup
* Quiz interaction flow
* Correct vs incorrect responses

---

## ✅ Conclusion

Through the **SendHelp chatbot**, I demonstrated how Amazon Lex and lambda can be used together to build interactive and educational AI solutions.
This project showcases my ability to design conversational systems and apply cloud-based AI services to practical, real-world use cases.


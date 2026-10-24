# 🤖 Saint James Customer Service AI Agent (n8n + OpenAI)

A conversational AI agent that answers customer questions for **Saint James**, the French clothing brand from Normandy, in **French and English**, remembers the conversation, and **never invents answers**: anything outside company policy is handed over to a human.

Built with **n8n** (no-code workflow automation) and **OpenAI GPT-4o-mini**.

🎥 **Demo video:** [Watch here](ADD-YOUR-VIDEO-LINK)

---

## 📌 Problem
Fashion brands receive the same customer questions again and again: returns, delivery times, sizing, product care. Customers expect instant answers 24/7 and in their own language, while support teams lose hours on repetitive replies.

## 💡 Solution
An AI customer service agent that:
- ✅ Answers FAQs instantly using only official company information
- 🌍 Replies automatically in the customer's language (French / English)
- 🧠 Remembers context within the conversation
- 🛡️ Avoids hallucination: unknown questions are escalated to a human team member
- 📊 Logs every conversation in n8n for review

---

## 🔄 How it works

```
Customer message
      ↓
💬 Chat Trigger      → receives the message
      ↓
🤖 AI Agent          → decides how to respond
   ├── 🧠 OpenAI GPT-4o-mini → understands and writes the reply
   ├── 📝 Simple Memory      → keeps conversation context
   └── 📋 System Prompt      → Saint James policies (grounding)
      ↓
Reply to customer
```

## 🛠️ Tools used
| Tool | Purpose |
|---|---|
| n8n | Workflow automation & agent orchestration |
| OpenAI GPT-4o-mini | Language understanding and reply generation |
| n8n Simple Memory | Conversation context |
| System prompt | Grounding the agent in brand policies |

---

## 🧪 Test examples

| Customer input | Agent output | What it shows |
|---|---|---|
| What is your return policy? | Free returns within 30 days, unworn with tags | Grounded FAQ answer |
| Bonjour, la livraison prend combien de temps ? | Replies in French: 2–4 days in France | Multilingual |
| My name is Priya → What's my name? | "Your name is Priya" | Memory |
| Do you sell shoes? | A team member will reply within 24 hours | No hallucination / human handoff |

---

## 📸 Screenshots
![Workflow](screenshots/workflow.png)
![Chat demo](screenshots/chat-demo.png)

---

## 🚀 How to use
1. Create an n8n account (cloud or self-hosted)
2. Import `saint-james-chat-agent.json` (**⋯ → Import from file**)
3. Add your own OpenAI API credential to the OpenAI Chat Model node
4. Click **Open chat** and start testing

---

## 🎓 What I learned
- **Workflow vs Agent:** a fixed chain follows the same steps every time; an agent adapts its response to what the user asks.
- **Grounding with a system prompt** keeps answers accurate and on-brand, which reduces hallucination.
- **Memory** is essential for a natural conversation.
- **Human handoff** is a key part of responsible AI in customer service.

## 🔮 Next steps
- Add a Gmail tool so the agent can escalate complaints to the support team by itself
- Connect a Google Sheets order database for live order-status lookup
- Embed the chat widget on a website

---

👩‍💻 **Author:** Suganya, MSc Artificial Intelligence & Marketing Strategy, EPITA Paris
🔗 [LinkedIn](https://linkedin.com/in/suganyaraju10)

*This is a portfolio/demo project and is not affiliated with Saint James.*

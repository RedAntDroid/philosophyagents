# PhilosophyAgents 🧠

This is a deployment-ready fork and customization of the **PhiloAgents Course** project from the [DecodingML Substack](https://decodingml.substack.com/p/master-production-ai-with-our-end) by **Neural Maze**.

I built this as part of a hands-on learning process in agentic AI systems, integrating knowledge from the course with my own deployment, containerization, and frontend customization efforts.

---

## 📚 What I Learned

The original project helped me understand:

- 🔎 How **RAG (Retrieval-Augmented Generation)** works in practice
- 🤖 The architecture of **agentic AI systems**
- 🐳 How to use **Docker & Docker Compose** to manage production-ready stacks
- 🎮 How to run a **Phaser-based frontend UI** that interacts with a FastAPI + MongoDB backend

---

## 🛠️ Stack

- **Frontend**: Phaser 3 (served at port 8080)
- **Backend**: FastAPI (port 8000)
- **Database**: MongoDB Atlas Local (port 27017)
- **Deployment**: Docker Compose, Portainer, Netlify (for UI)

---

## 🚀 Running Locally

Clone and start the full infrastructure:

```bash
git clone https://github.com/RedAntDroid/philosophyagents.git
cd philosophyagents
make infrastructure-up

🙏 Acknowledgements
Big thanks to Neural Maze and the DecodingML Substack for the open-source PhiloAgents course.
This repo was adapted and deployed by me as part of my learning journey and portfolio.

🧑‍💻 Author
Maintained by Dharun




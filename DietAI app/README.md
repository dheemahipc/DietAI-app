# 🥗 Diet AI
Diet AI is a conversational AI agent designed to act as a personalized dietician and health coach. Accessible entirely via WhatsApp, it leverages Google's Agent Development Kit (ADK) and the Gemini 2.5 Flash model to provide scientifically accurate diet and exercise plans. 

This project goes beyond a simple LLM wrapper by integrating custom Python math tools for accurate macronutrient calculations and utilizing a robust, zero-downtime GitOps deployment pipeline.

## ✨ Key Features

* **Accessible via WhatsApp:** Users interact naturally via WhatsApp; no app downloads or web interfaces required.
* **Intelligent Middleware (n8n):** Handles webhooks, filters for text-only inputs to prevent crashes, and triggers parallel "typing..." indicators for a seamless user experience.
* **Agentic Precision:** The AI is strictly prompt-engineered to stay within health/fitness domains and relies on explicit Python functions to calculate exact BMI, BMR (Mifflin-St Jeor), and macro targets, eliminating LLM math hallucinations.
* **GitOps CI/CD:** Fully automated deployments. Code pushes trigger GitHub Actions to build and tag new Docker images, which are then synced and deployed via ArgoCD with zero downtime.
* **Kubernetes Ready:** Engineered to run smoothly on Kubernetes clusters with proper health checks and fast APIs.

# 📰 Unveiling Misinformation in Bangla Social Media
### A Multimodal Fake News Detection System

## 📌 Overview
Social media in Bangladesh often spreads **fake news** using both **text and images**.  
Most existing detection systems are **text-only** and designed for **English**, making them ineffective for Bangla.  

This project introduces a **multimodal ensemble-based system** for detecting **Bangla fake news** using:
- **Text Models:** BanglaBERT, XLM-RoBERTa, BanglaLM  
- **Image Models:** CNN, ResNet-50, EfficientNet, Vision Transformer (ViT), Swin Transformer  
- **Fusion:** Meta-classifier & ensemble strategies for robust multimodal detection  

---

## 🎯 Research Objectives
- Build a scalable **fake news detection system** for Bangla using **both text and images**.  
- Fine-tune **transformers** for textual misinformation.  
- Train **deep learning models** for manipulated images.  
- Design a **stacking ensemble** to combine outputs.  
- Develop a **demo interface** for real-time predictions.  

---

## ⚙️ Methodology
1. **Data Collection**  
   - Public Bangla fake news dataset with **7,680 labeled articles** (3,840 Fake + 3,840 Non-Fake).  
   - Images sorted into “Fake” and “Real” folders.  

2. **Preprocessing**  
   - Text cleaning (noise removal, casing fix, tokenization).  
   - Image resizing (224×224), normalization, and tensor conversion.  

3. **Model Training**  
   - **Text:** BanglaBERT (7 variants), XLM-R, BanglaLLM with LoRA.  
   - **Image:** ResNet50, ViT, Swin Transformer.  
   - **Training Setup:** lr=2e-5, batch=4/8, 3–5 epochs, fp16 mixed precision.  

4. **Ensemble & Fusion**  
   - Stacking meta-classifier with shallow MLP.  
   - Late, early, and intermediate fusion strategies.  
   - Ensemble improved F1 by **2–5%** over single models.  

5. **Deployment**  
   - Prototype built with **Gradio** (Python).  
   - Future plan: **Flask/FastAPI + React frontend**, deployable as web app or browser extension.  

---

## 📊 Results (Preliminary)
- **Text models** (BanglaBERT variants, XLM-R) achieved higher performance than classical baselines.  
- **Image models** (ViT, ResNet, Swin) captured visual misinformation with ~65% accuracy.  
- **BanglaLLM (LoRA fine-tuned)** achieved ~69% accuracy, showing promise for low-resource LLMs.  
- **Stacking ensembles** improved generalization compared to individual models.  

---

## 🚀 Future Work
- **Explainability:** Use SHAP/LIME for interpretability.  
- **Optimization:** Apply model compression for resource-limited devices.  
- **Advanced Fusion:** Explore CLIP/BLIP multimodal models.  
- **Deployment:** Build a real-time web app and browser extension for Bangla users.  


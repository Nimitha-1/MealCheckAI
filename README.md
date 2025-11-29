# MealCheckAI
AI-powered meal planner that generates doctor-approved, condition-specific meal suggestions based on your health profile and available pantry items. Supports nutrition tracking, prep time estimates, and a doctor-in-the-loop workflow for safe, practical meal planning.

## 🧩 Problem Statement

Diet plays a critical role in patient recovery. Whether dealing with digestive illnesses, metabolic disorders, or post-infection healing, the foods a patient consumes influence energy levels, recovery speed, and symptom stability.  

Patients often struggle with questions such as:

- “Can I eat this food right now?”  
- “Is this ingredient okay for my condition?”  
- “What can I cook with what I have at home?”  
- “How do I plan meals for the week safely?”  

This became personally relevant when I contracted hepatitis A. During recovery, I lacked a system that could consider my medical condition, pantry, and dietary restrictions to generate safe meal suggestions. Existing apps focus on fitness or lifestyle, not clinical recovery.

**Challenges for caregivers** include planning meals that are medically appropriate, quick to prepare, and feasible with available ingredients.

**Goal:** Create an AI agent that bridges medical dietary guidance and real-world meal planning, focusing on:

1. **Clinical relevance** — condition-specific dietary rules  
2. **Pantry awareness** — meals using available ingredients  
3. **Feasibility** — realistic preparation and cooking time  
4. **Doctor oversight** — clinician review and approval  

---

## 🤖 Why Agents?

Medical meal planning is complex:

- Requires **multi-step reasoning** (patient constraints → pantry → recipes → nutrition → prep time → validation)  
- Agents can **call tools dynamically**: nutrition databases, recipe filters, pantry scans, shopping lists  
- Supports **iterative refinement**: adjusting calories, swapping ingredients, following doctor feedback  
- **Human-in-the-loop compatible** for doctor approval  
- Provides **transparent reasoning** for trust in medical decisions  

---

## 🏗 What I Created — System Overview & Architecture

### 1. Patient Profile Module
Stores patient info:

- Demographics, medical conditions, allergies  
- Calorie needs, disliked ingredients  
- Maximum daily prep time, number of meals/day  

### 2. Pantry Awareness Engine
Patient inputs:

- Manual entry, barcode scanning, OCR, or fridge photo  
- Ensures recommendations are practical  

### 3. Recipe Knowledge Base
Each recipe includes:

- Ingredients, substitutions, nutrition, condition flags  
- Prep/cook time, difficulty level  
- Automatic filtering for incompatible foods  

### 4. Medical Constraint Checker
Rule engine enforces:

- No alcohol, raw seafood, limited fats  
- Easily digestible meals, moderated spices  
- High hydration foods  

### 5. Agent Orchestrator
Implements **Plan → Act → Reflect → Send for Approval**:

- **Plan:** Daily calorie targets, allocate meal slots, match recipes to condition & pantry  
- **Act:** Call nutrition/recipe tools, calculate nutrients, check prep times  
- **Reflect:** Adjust meals, swap ingredients, ensure rule compliance  
- **Send for Approval:** Doctor reviews flagged items and approves  

### 6. Doctor Review Workflow
Clinician checks:

- Meals and high-risk items  
- Nutrient summaries  
- Medical guideline adherence  
- Approve, reject, or modify meals  

### 7. Shopping List Generator
Generates weekly shopping list based on approved meals:

- Calculates missing ingredients  
- Aggregates quantities  
- Provides clean list  

---

## 🎬 Demo Flow

1. **Patient Setup:** Enter symptoms, restrictions, preferences, pantry items  
2. **Generate Plan:** 7-day meal plan with warnings and prep times  
3. **Doctor Review:** Flagged items, rationale, nutrient chart, approval  
4. **Final Output:** Approved meal plan, recipes, shopping list  

---

## 🛠 Tools & Technologies Used

- **Python** – Agent logic  
- **FastAPI** – Backend API  
- **SQLite/PostgreSQL** – Patient & recipe data  
- **USDA/Spoonacular** – Nutrition data  
- **OCR (Tesseract)** – Pantry scanning  
- **React/Blazor** – Frontend UI  
- **JWT Auth & Audit Logging** – Security  

**Agent Architecture:**

- Planner → Tool Executor → Reflector → Human Approver  

**Data Storage:**

- Recipes, pantry, patient profiles, approval logs  

---

## 🚀 Future Work

1. Evidence-based medical rules for more conditions  
2. Real-time pantry detection via image models  
3. Dietary Q&A assistant (doctor-approved answers)  
4. Optimization engine for cost, pantry usage, and balanced menus  
5. Patient education mode  
6. Mobile app for daily meal tracking  
7. Clinical trials with real patients and doctors  

---

## 🧡 Personal Motivation

Recovering from hepatitis A made me realize how stressful food choices can be. MealCheckAI aims to reduce patient stress, provide clarity, and ensure medical guidance is embedded in every meal decision.  

---

## 🔗 Links

- [GitHub Repository](https://github.com/Nimitha-1/MealCheckAI)  
- [Kaggle Notebook]((https://www.kaggle.com/code/nimitha123/mealcheckai))
---



# 🧠 YVEA — Plateforme IA pour la Certification & Supply Chain

YVEA est une application SaaS développée pour automatiser la génération, la validation et le suivi des certificats d’exportation, en intégrant des briques avancées d’intelligence artificielle (OCR, NLP, agents contextuels).

---

## 📚 Sommaire

- [🎯 Vision & Objectifs](#-vision--objectifs)
- [🚀 Fonctionnalités Clés](#-fonctionnalités-clés)
- [⚙️ Architecture Technique](#️-architecture-technique)
- [🤖 Intégration IA](#-intégration-ia)
- [🧭 Expérience Utilisateur](#-expérience-utilisateur)
- [📊 Résultats & Impact](#-résultats--impact)
- [📌 Roadmap & Évolutions](#-roadmap--évolutions)
- [🙌 Remerciements & Contact](#-remerciements--contact)

---

## 🎯 Vision & Objectifs

YVEA a pour ambition de **réinventer les processus de certification documentaire** pour l’export grâce à l’IA :

- Réduire les erreurs de conformité
- Accélérer les délais de traitement
- Améliorer l’autonomie des utilisateurs via un assistant IA
- Faciliter les interactions entre les entreprises et les autorités

---

## 🚀 Fonctionnalités Clés

| Fonction | Description |
|----------|-------------|
| ✅ Assistant IA intégré | Répond aux questions contextuelles et guide l’utilisateur |
| 📄 OCR avancé | Extraction automatique d’informations à partir de documents PDF, JPG, PNG |
| 🧠 Validation réglementaire IA | Vérifie la conformité documentaire selon le code HS |
| 📬 Messagerie intégrée | Canal sécurisé avec l’administration (WebSocket/HTTP fallback) |
| 📈 Dashboard de suivi | Historique, statuts, temps de traitement, précision IA |

---

## ⚙️ Architecture Technique

- **Frontend** : Next.js (TypeScript), Redux Toolkit, SWR
- **Backend** : NestJS, PostgreSQL, MinIO, Bull/Redis
- **DevOps** : Docker, GitHub Actions, AWS ECS, Terraform
- **Sécurité** : Authentification JWT, validation serveur, audit trail

graph TD
UI[Interface Utilisateur] -->|Formulaires, Assistant| Frontend
Frontend -->|API REST| Backend
Backend -->|Validation IA| AzureOpenAI
Backend -->|OCR| Tesseract
Backend -->|Docs| MinIO
Backend -->|Notifications| EmailService
Backend -->|Persistence| PostgreSQL

yaml
Copy
Edit

---

## 🤖 Intégration IA

### 🔍 OCR & Extraction Documentaire

- **Tesseract OCR** : pour les documents scannés
- **PDF.js** : pour les PDF textuels
- **Fallback intelligent** : choix dynamique selon le type de fichier

### 🧾 Validation de conformité IA

- Analyse réglementaire via GPT-4 sur des segments OCRisés
- Agrégation automatique des résultats
- Génération d’un rapport de conformité

### 💬 Assistant IA contextuel

- Basé sur Azure OpenAI GPT-4
- Fonctionne à chaque étape du processus
- Fournit des suggestions, réponses, liens utiles

---

## 🧭 Expérience Utilisateur

### Parcours principal

Tableau de bord → Nouveau certificat → Upload documents
→ Ajout produits → Vérification → Soumission → Validation → Suivi

yaml
Copy
Edit

### Frictions & Solutions

| Friction | Solution |
|----------|----------|
| Formulaire complexe | Multi-étapes, sauvegarde auto, feedback instantané |
| Upload hasardeux | Drag & drop, validation taille/format |
| Sélection HS délicate | Suggestions, recherche intelligente |
| Délais IA | Skeleton loaders, animations, estimations |

### Micro-interactions clés

- ✅ Coche verte animée lors de validation
- 🔄 Animation circulaire lors du traitement IA
- ⚠️ Modals pour les erreurs avec solution proposée

---

## 📊 Résultats & Impact

| Indicateur | Résultat |
|------------|----------|
| ⏱ Réduction du temps de traitement | ~80% |
| 🔍 Précision OCR (Tesseract + IA) | 98.5% |
| ✅ Fiabilité analyse IA (vs legacy) | 85%+ |
| 📉 Rejets de certificats | -65% |
| ⚡ Temps de réponse assistant IA | 2–4 secondes |

---

## 📌 Roadmap & Évolutions

- [ ] OCR sur documents manuscrits
- [ ] Modèles multimodaux (texte + image)
- [ ] Assistant IA capable d’actions automatiques
- [ ] Dashboard IA avec feedback utilisateurs
- [ ] Extension multilingue de l’interface

---

## 🙌 Remerciements & Contact

Projet piloté par **Moamen Elmasry**, dans un contexte de refonte post-départ CTO.  
Architecture reconstruite avec une approche IA-first, en développement assisté par LLMs.

📫 **Contact** : elmasrymoamen@hotmail.fr  
📅 **Calendly** : [https://calendly.com/elmasrymoamen/30min](https://calendly.com/elmasrymoamen/30min)

---

> *Ce projet démontre ma capacité à conduire un projet complexe, à intégrer des briques IA concrètes, et à livrer une expérience utilisateur robuste. Je recherche aujourd’hui une alternance ingénieur IA pour approfondir cette expertise aux côtés d’une équipe expérimentée.*

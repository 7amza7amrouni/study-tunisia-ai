# 📚 Study Tunisia AI - Plateforme Éducative Tunisienne Premium

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-blue)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5+-blue)](https://www.typescriptlang.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6+-green)](https://www.mongodb.com/)

## 🎯 Description

**Study Tunisia AI** est une plateforme éducative web et mobile complète destinée aux élèves du collège, lycée et baccalauréat tunisien. L'application offre une expérience d'apprentissage personnalisée, fluide et moderne avec intelligence artificielle intégrée.

### ✨ Caractéristiques Principales

- 📖 Bibliothèque complète de cours tunisiens (tous niveaux et sections)
- 🤖 Assistant IA éducatif intelligent (ChatGPT intégré)
- 📸 Scanner IA pour correction d'exercices (OCR + IA)
- 📊 Calculateur de moyenne avancé
- 🎮 Système de gamification (XP, Badges, Niveaux)
- 📅 Planning d'étude avec technique Pomodoro
- 👥 Communauté d'apprentissage par matière
- 💎 Abonnement Premium
- 📱 100% Responsive Mobile
- 🌍 Support FR/AR

## 🚀 Démarrage Rapide

### Prérequis
- Node.js 18+
- MongoDB Atlas (gratuit)
- Clé API OpenAI
- Docker (optionnel)

### Installation avec Docker (Recommandé)

```bash
# Cloner le repository
git clone https://github.com/7amza7amrouni/study-tunisia-ai.git
cd study-tunisia-ai

# Copier le fichier .env
cp .env.example .env

# Éditer .env avec vos clés API
nano .env

# Démarrer avec Docker
docker-compose up -d

# Frontend: http://localhost:3000
# Backend API: http://localhost:5000/api
# MongoDB: localhost:27017
```

### Installation Manuelle

#### Backend
```bash
cd backend
npm install
cp .env.example .env
npm run dev
# Écoute sur http://localhost:5000
```

#### Frontend
```bash
cd frontend
npm install
npm start
# Ouvre http://localhost:3000
```

## 📁 Structure du Projet

```
study-tunisia-ai/
├── frontend/                          # React + TypeScript
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.tsx
│   │   │   ├── Sidebar.tsx
│   │   │   ├── CourseCard.tsx
│   │   │   ├── ExerciseViewer.tsx
│   │   │   ├── AIAssistant.tsx
│   │   │   └── ...
│   │   ├── pages/
│   │   │   ├── Dashboard.tsx
│   │   │   ├── Courses.tsx
│   │   │   ├── Exercises.tsx
│   │   │   ├── AIChat.tsx
│   │   │   ├── Scanner.tsx
│   │   │   ├── GradeCalculator.tsx
│   │   │   ├── StudyPlan.tsx
│   │   │   ├── Community.tsx
│   │   │   ├── Profile.tsx
│   │   │   └── ...
│   │   ├── services/
│   │   │   ├── api.ts
│   │   │   ├── authService.ts
│   │   │   ├── courseService.ts
│   │   │   └── ...
│   │   ├── store/
│   │   │   ├── authSlice.ts
│   │   │   ├── userSlice.ts
│   │   │   └── store.ts
│   │   ├── types/
│   │   │   └── index.ts
│   │   ├── hooks/
│   │   │   ├── useAuth.ts
│   │   │   ├── useUser.ts
│   │   │   └── ...
│   │   ├── utils/
│   │   │   ├── validators.ts
│   │   │   ├── formatters.ts
│   │   │   └── ...
│   │   └── App.tsx
│   ├── public/
│   ├── package.json
│   ├── tsconfig.json
│   └── Dockerfile
│
├── backend/                           # Express + MongoDB
│   ├── src/
│   │   ├── models/
│   │   │   ├── User.ts
│   │   │   ├── Course.ts
│   │   │   ├── Exercise.ts
│   │   │   ├── Quiz.ts
│   │   │   ├── UserProgress.ts
│   │   │   ├── Scan.ts
│   │   │   ├── GradeCalculator.ts
│   │   │   ├── StudyPlan.ts
│   │   │   ├── CommunityPost.ts
│   │   │   └── Badge.ts
│   │   ├── routes/
│   │   │   ├── auth.ts
│   │   │   ├── courses.ts
│   │   │   ├── exercises.ts
│   │   │   ├── quizzes.ts
│   │   │   ├── scanner.ts
│   │   │   ├── grades.ts
│   │   │   ├── studyPlan.ts
│   │   │   ├── community.ts
│   │   │   ├── ai.ts
│   │   │   ├── user.ts
│   │   │   ├── payment.ts
│   │   │   └── admin.ts
│   │   ├── controllers/
│   │   │   └── (contrôleurs pour chaque route)
│   │   ├── middleware/
│   │   │   ├── auth.ts
│   │   │   ├── errorHandler.ts
│   │   │   ├── validation.ts
│   │   │   └── cors.ts
│   │   ├── services/
│   │   │   ├── aiService.ts
│   │   │   ├── scannerService.ts
│   │   │   ├── gamificationService.ts
│   │   │   ├── paymentService.ts
│   │   │   └── emailService.ts
│   │   ├── utils/
│   │   │   ├── constants.ts
│   │   │   ├── validators.ts
│   │   │   └── helpers.ts
│   │   ├── app.ts
│   │   └── server.ts
│   ├── data/
│   │   ├── courses.json
│   │   ├── exercises.json
│   │   ├── quizzes.json
│   │   └── init.js
│   ├── package.json
│   ├── tsconfig.json
│   └── Dockerfile
│
├── admin-panel/                       # Dashboard Admin
│   └── (structure similaire au frontend)
│
├── docs/
│   ├── API.md
│   ├── DATABASE.md
│   ├── INSTALLATION.md
│   └── CONTRIBUTION.md
│
├── docker-compose.yml
├── .env.example
├── LICENSE
└── README.md
```

## 🔧 Variables d'Environnement

Copier `.env.example` vers `.env` et configurer:

```bash
# Backend
PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb+srv://user:pass@cluster.mongodb.net/study-tunisia
JWT_SECRET=votre_cle_secrete
OPENAI_API_KEY=sk-...
STRIPE_SECRET_KEY=sk_test_...
FRONTEND_URL=http://localhost:3000
```

## 📚 Fonctionnalités Détaillées

### 1️⃣ Authentification & Onboarding
- Inscription avec email
- Onboarding intelligent (niveau, section, langue)
- JWT authentication sécurisé
- Récupération de mot de passe

### 2️⃣ Bibliothèque de Cours
**Matières couvertes:**
- Mathématiques (Limites, Dérivées, Suites, Probabilités, etc.)
- Physique (Mécanique, Électricité, Optique, etc.)
- Sciences (Chimie, Biologie, Géologie)
- Informatique (Algorithmes, Programmation, Bases de données)
- Français (Grammaire, Littérature, Conjugaison)
- Arabe (Grammaire arabe, Littérature, Récitation)
- Philosophie
- Économie-Gestion

**Chaque cours contient:**
- Chapitres structurés
- Leçons détaillées avec Markdown
- Formules mathématiques (LaTeX)
- Exemples corrigés avec explications
- Images explicatives
- PDF téléchargeables
- Fiches de révision
- Quiz associés

### 3️⃣ Exercices & Examens
- Exercices par chapitre et matière
- Séries complètes
- Devoirs et examens blancs
- Quiz interactifs
- Flashcards

**Chaque exercice inclut:**
- Correction détaillée
- Résolution étape par étape
- Niveau de difficulté (facile/moyen/difficile)
- Images et diagrammes
- Explications pédagogiques

### 4️⃣ Assistant IA Éducatif
- Chat en temps réel
- Réponse basée sur les cours de l'app
- Explications pédagogiques
- Résolution d'exercices
- Génération de résumés
- Création de quiz
- Support FR/AR

### 5️⃣ Scanner IA
- Scan d'exercices (image/PDF)
- OCR intégré (Tesseract.js)
- Correction automatique par IA
- Explication étape par étape
- Historique des scans
- Sauvegarde locale

### 6️⃣ Calculateur de Moyenne
- Configuration par niveau et section
- Affichage automatique des matières
- Saisie des notes (contrôle, synthèse, oral, TP)
- Calcul:
  - Moyenne par matière
  - Moyenne générale
  - Moyenne trimestrielle
  - Moyenne annuelle
- Objectif de moyenne
- Suggestions d'amélioration
- Identification des matières faibles
- Graphiques visuels

### 7️⃣ Gamification
**Système XP complet:**
- 100 XP = Cours complété
- 25 XP = Exercice complété
- 50 XP = Quiz complété
- 10 XP = Scanner utilisé
- 15 XP = Aide aux autres

**Niveaux:**
- 500 XP = Niveau 2
- 1000 XP = Niveau 3
- etc.

**Badges:**
- Premier Pas (1er cours)
- Maître Mathématique (tous cours math)
- Guerrier de l'Étude (10h d'étude)
- Score Parfait (20/20 quiz)
- Expert Communautaire
- etc.

**Classements:**
- Classement général
- Classement par section
- Classement entre amis

### 8️⃣ Planning d'Étude
- Planning hebdomadaire (lun-dim)
- Sessions d'étude configurables
- Technique Pomodoro (25min travail + 5min pause)
- Gestion des devoirs et examens
- Notifications intelligentes
- Statistiques de concentration
- Conseils de productivité

### 9️⃣ Communauté
**Groupes par:**
- Matière (Math, Physique, etc.)
- Niveau scolaire
- Section

**Fonctionnalités:**
- Posts/Questions entre élèves
- Réponses avec explications
- Partage d'exercices et séries
- Envoi d'images et documents
- Système de votes (utile/inutile)
- Badges pour meilleurs aidants
- XP pour aide aux autres
- Modération automatique
- IA répond dans le chat

### 🔟 Profil Étudiant
- Photo et informations personnelles
- Niveau et section
- Statistiques détaillées
- Progression par matière
- Historique complet
- Badges et achievements
- Préférences et paramètres
- Export des données

## 🎮 Accueil Intelligent

Le Dashboard personnalisé affiche:
- Cours recommandés (IA)
- Exercices recommandés
- Progression globale
- XP et niveau actuels
- Badges récemment débloqués
- Classement général
- Objectifs scolaires
- Planning de révision
- Dernières activités
- Résultats du scanner IA

## 💎 Abonnement Premium

**Tarifs:**
- 12 DT/mois
- 100 DT/an (2 mois gratuits)

**Avantages Premium:**
- IA avancée (réponses plus longues, détaillées)
- Scanner illimité
- Contenus exclusifs premium
- Statistiques avancées
- Révisions personnalisées
- Support prioritaire
- Export PDF des cours
- Offline mode

**Paiements:**
- Stripe (international)
- Konnect (Tunisie)
- D17 (Tunisie)

## 🔐 Admin Panel

Fonctionnalités administrateur:
- ➕ Ajouter/modifier/supprimer cours
- ➕ Ajouter exercices, PDF, images
- ➕ Gérer quiz et flashcards
- 👥 Gérer utilisateurs
- 💳 Gérer abonnements
- 📊 Statistiques globales
- 🔍 Modération communauté
- 📧 Envoi d'emails
- 📱 Gestion notifications

**Tout modifiable sans toucher au code!**

## 🔒 Sécurité

- ✅ JWT authentication
- ✅ Hachage des mots de passe (bcrypt)
- ✅ Validation des entrées
- ✅ Rate limiting
- ✅ CORS configuré
- ✅ Helmet.js (headers sécurisés)
- ✅ Environment variables
- ✅ Input sanitization
- ✅ HTTPS en production
- ✅ Audit logging

## 📱 Performance

- ⚡ Temps de chargement < 2s
- ⚡ Images optimisées
- ⚡ Code splitting React
- ⚡ Lazy loading des cours
- ⚡ CDN pour ressources statiques
- ⚡ Compression Gzip
- ⚡ Caching intelligente
- ⚡ PWA ready

## 🌐 Responsive Design

- 📱 Mobile First (< 640px)
- 📱 Tablet (640px - 1024px)
- 💻 Desktop (> 1024px)
- 🎯 Breakpoints Tailwind CSS
- 📐 Responsive images
- 🔄 Flexible layouts

## 📦 Tech Stack Complet

### Frontend
- React 18+
- TypeScript 5+
- Tailwind CSS 3+
- Redux Toolkit
- React Router v6
- Axios
- Framer Motion
- Recharts
- React Markdown
- React Icons
- Firebase Auth (optionnel)

### Backend
- Express.js 4+
- MongoDB 6+
- Mongoose 7+
- TypeScript 5+
- OpenAI API
- JWT
- bcryptjs
- Multer
- Tesseract.js (OCR)
- Stripe SDK
- Nodemailer
- Helmet
- CORS

### DevOps
- Docker
- Docker Compose
- GitHub Actions (CI/CD)
- Vercel (Frontend)
- Railway/Heroku (Backend)

## 📖 Documentation

- [API Documentation](./docs/API.md)
- [Database Schema](./docs/DATABASE.md)
- [Installation Complète](./docs/INSTALLATION.md)
- [Guide de Contribution](./docs/CONTRIBUTION.md)

## 🤝 Contribution

Les contributions sont bienvenues!

1. Fork le projet
2. Créer une branche (`git checkout -b feature/AmazingFeature`)
3. Commit (`git commit -m 'Add AmazingFeature'`)
4. Push (`git push origin feature/AmazingFeature`)
5. Ouvrir une Pull Request

Voir [CONTRIBUTION.md](./docs/CONTRIBUTION.md) pour plus de détails.

## 📄 License

MIT License - voir [LICENSE](./LICENSE)

## 👨‍💻 Auteur

**7amza7amrouni**
- GitHub: [@7amza7amrouni](https://github.com/7amza7amrouni)
- Email: amza7amrouni@gmail.com

## 📞 Support

- 🐛 Rapporter des bugs: [Issues](https://github.com/7amza7amrouni/study-tunisia-ai/issues)
- 💬 Questions: [Discussions](https://github.com/7amza7amrouni/study-tunisia-ai/discussions)
- 📧 Email: support@studytunisia.tn

## 🙏 Remerciements

- Merci à tous les contributeurs
- Merci aux étudiants tunisiens
- Merci aux enseignants qui ont fourni les contenus

---

**Fait avec ❤️ pour les étudiants tunisiens**

⭐ Si ce projet vous plaît, n'oubliez pas de mettre une étoile!

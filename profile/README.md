# 📄 **Générateur de CV**  

Bienvenue dans notre projet **Générateur de CV** ! Ce projet a été réalisé dans le cadre d'une évaluation pour mettre en pratique nos compétences en **Node.js**, **Express**, **MongoDB**, et **React**.

## 🚀 **Fonctionnalités principales**  

- **Authentification utilisateur :**  
  - Inscription et connexion sécurisées via JWT.  
  - Gestion des espaces personnels.  

- **Gestion des CV :**  
  - Création, modification, suppression de CV.  
  - Contrôle de la visibilité des CV.  

- **Consultation publique des CV :**  
  - Liste des CV visibles avec recherche par nom.  

- **Recommandations :**  
  - Ajout de recommandations sur les CV des utilisateurs.  
  - Gestion des recommandations reçues.  

## 🛠️ **Technologies utilisées**  

### **Backend :**  
- **Node.js**  
- **Express.js**  
- **MongoDB**  
- **JWT (JSON Web Token)**  

### **Frontend :**  
- **React**  
- **React Router**

## 📂 **Structure du projet**  

```plaintext
backend/
├── node_modules/          # Dépendances Node.js
├── src/                   # Source principale du backend
│   ├── controller/        # Contrôleurs (logique métier)
│   ├── middlewares/       # Middlewares (authentification, validation, etc.)
│   ├── models/            # Modèles de données (MongoDB)
│   ├── roles/             # Gestion des rôles et autorisations
│   ├── routes/            # Définition des routes de l'API
│   ├── Security/          # Gestion de la sécurité (hashing, JWT, etc.)
│   ├── validator/         # Validation des données entrantes
│   ├── app.http.js        # Gestion des tests HTTP locaux (Postman, etc.)
│   └── app.js             # Point d'entrée principal de l'application
├── .env                   # Variables d'environnement
├── .gitignore             # Fichiers à ignorer par Git
├── package-lock.json      # Verrouillage des versions des dépendances
├── package.json           # Gestion des dépendances et scripts
└── README.md              # Documentation du projet

frontend/
├── dist/                  # Fichiers générés après build
├── node_modules/          # Dépendances Node.js
├── public/                # Fichiers publics accessibles par l'utilisateur (favicon, index.html)
├── src/                   # Source principale du projet
│   ├── assets/            # Ressources statiques (images, icônes)
│   ├── components/        # Composants réutilisables
│   ├── Context/           # Gestion du contexte global de l'application
│   ├── Control/           # Logique et contrôle des formulaires ou autres modules
│   ├── Enum/              # Enums ou constantes utilisées dans l'application
│   ├── Navigation/        # Gestion de la navigation (barre de menu, routes, etc.)
│   ├── pages/             # Pages principales (Accueil, Connexion, CV, etc.)
│   ├── statutCV/          # Gestion des statuts des CV (visibilité, etc.)
│   ├── utils/             # Fonctions utilitaires
│   ├── App.jsx            # Composant racine de l'application
│   └── main.jsx           # Point d'entrée du projet React
├── .env                   # Variables d'environnement (config API, etc.)
├── .gitignore             # Fichiers à ignorer par Git
├── eslint.config.js       # Configuration ESLint pour le linting
├── index.html             # Fichier HTML principal
├── package-lock.json      # Verrouillage des versions des dépendances
├── package.json           # Gestion des dépendances et scripts du projet
├── README.md              # Documentation du projet
└── vite.config.js         # Configuration de Vite.js (outil de build)

```

## ⚙️ **Installation et Lancement en Local**  

### **Prérequis :**  
- Node.js installé.  
- MongoDB en cours d'exécution (localement ou via un service cloud).  

### **Backend :**  

1. Clonez le repository backend :  
   ```bash
   git clone https://github.com/Mathias002/cvGeneratorAPI.git
   cd cvGeneratorAPI
   ```
2. Installez les dépendances :  
   ```bash
   npm install
   ```
3. Configurez les variables d'environnement :  
   - Configurez les variables d'environnement dans le fichier `.env`.
   - (les valeurs à renseigner dans le .env sont disponible dans le readMe du repository cvGeneratorAPI)

4. Démarrez le serveur :  
   ```bash
   npm run start:dev app.js
   ```

### **Frontend :**  

1. Clonez le repository frontend :  
   ```bash
   git clone https://github.com/Mathias002/cvGeneratorFront.git
   cd cvGeneratorFront
   ```
2. Installez les dépendances :  
   ```bash
   npm install
   ```

3. Configurez les variables d'environnement :  
   - Configurez les variables d'environement dans le fichier `.env`.
   - (les valeurs à renseigner dans le .env sont disponibles dans le readMe du repository cvGeneratorFront)
   
3. Démarrez l'application React :  
   ```bash
   npm run start:dev app.jsx 
   ```

## 🌍 **Déploiement**  

### **Liens du projet en ligne :**  
- **Frontend déployé :** [https://cv-generator-front.netlify.app]
- **Backend & Documentation API déployé :** [https://cvgeneratorapi-production.up.railway.app]  

## 📜 **Endpoints principaux de l'API**  

### **Authentification :**  
- `POST /api/auth/register` : Inscription d'un utilisateur.  
- `POST /api/auth/login` : Connexion et récupération d'un token JWT.  

### **Gestion des CV :**  
- `POST /api/cv/createCv` : Créer un nouveau CV.  
- `GET /api/cv/getAllPubliccv` : Lister les CV publics.  
- `PATCH /api/cv/update/:id` : Modifier un CV.
- `GET /api/cv/:id` : Récupérer un cv par ID.  
- `DELETE /api/cv/:id` : Supprimer un CV.  

### **Avis :**  
- `POST /api/avis/:cvId` : Ajouter une recommandation à un CV.
- `PATCH /api/avis/:id` : Mise à jour d'un cv.  
- `DELETE /api/avis/:id` : Suppression d'un avis.

- ### **User :**  
- `GET /api/user/:id` : Afficher les infos d'un user.
- `PATCH /api/user/:id` : Mise à jour d'un user.  
- `DELETE /api/user/:id` : Suppression d'un user.  

## ✨ **Contributeurs**  
- **Mathias** : Backend - Deploiement 
- **Valérie** : Backend - Frontend
- **Ludovic** : Frontend - Deploiement

---

**💻 Happy coding, et bon courage pour la correction !** 😊

## **Comment intégrer des API REST dans React ?**

L'intégration des API REST dans un projet React repose principalement sur l'utilisation d'outils comme **`fetch`**, **`axios`**, et des hooks comme **`useEffect`** pour interagir avec le backend. Voici une démarche étape par étape.

---

### **1. Configurer un Service API dans React**

La meilleure pratique consiste à créer un fichier dédié pour centraliser les appels API, afin d'éviter les répétitions dans les composants.

#### **Créer un Service API avec `axios`**

1. **Installer `axios` :**

   ```bash
   npm install axios
   ```

2. **Créer un fichier `api.js`** dans le dossier `src/services`. 

#### Exemple : api.js

 
   - [Exemple de service API](https://github.com/MbayeSyAmar/Comment-integrer-des-API-REST-dans-React.git)



---

### **2. Appeler une API dans un Composant React**

Utilise `axios` pour appeler les API depuis React.

#### Exemple : Afficher la Liste des Posts

1. **Créer un composant `PostList.js` :**

   
  - [Exemple de composant](https://github.com/MbayeSyAmar/Comment-integrer-des-API-REST-dans-React.git)


---


### **3. Sécuriser les Requêtes avec JWT**

1. **Gérer l’Authentification** :

   - Lors de la connexion, récupère le **token JWT** depuis l’API NestJS et stocke-le dans le **localStorage**.

   
  - [Exemple de gestion de l'authentification](https://github.com/MbayeSyAmar/Comment-integrer-des-API-REST-dans-React.git)


1. **Vérifier les Permissions** dans les Composants :

   - Vérifie la présence du token pour afficher ou masquer certains éléments.

   
     - [Exemple de vérification de permissions](https://github.com/MbayeSyAmar/Comment-integrer-des-API-REST-dans-React.git)


---

### **4. Optimiser l’Intégration**

- **Mémoisation avec React Query** :
   - Remplace `useEffect` par [React Query](https://tanstack.com/query/latest) pour gérer les appels API avec cache et synchronisation automatique.

- **Gestion d’État Global avec Redux** :
   - Centralise les données des API REST dans un store Redux pour les partager entre plusieurs composants.
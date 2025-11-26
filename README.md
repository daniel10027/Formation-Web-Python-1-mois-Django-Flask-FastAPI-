# Formation Web Python – 1 mois (Django / Flask / FastAPI)

> Objectif : En 4 semaines  
> “Développer et déployer une vraie appli web/API en Django, Flask et FastAPI”.

---

## 0. Pré-requis recommandés

Avant d’attaquer le mois, il est recommandé de :

- Savoir écrire du Python de base (variables, fonctions, boucles, classes).
- Connaître un minimum la POO.
- Comprendre les bases du web : HTTP, requêtes, réponses, JSON, REST.
- Avoir déjà utilisé un terminal / Git de base.

Pour se mettre à niveau rapidement en Python :

- Parcours “Développeur d’application Python” – OpenClassrooms (parties Python de base)  
  PDF de syllabus :  
  https://static.oc-static.com/syllabus/518-developpeur-dapplication-python-1-fr-fr-standard.pdf  

---

## 1. Stack & outils à installer (Jour 0)

À faire AVANT de commencer le jour 1 :

- Python 3.10+
- pip + venv
- Git + compte GitHub / GitLab
- VS Code (extensions : Python, Pylance, GitLens, Django)
- PostgreSQL ou au minimum SQLite (intégré)
- Postman ou Insomnia pour tester les APIs
- Navigateur (Chrome / Firefox avec DevTools)

Docs officielles à garder dans les favoris :

- Django :  
  https://docs.djangoproject.com/fr/5.2/
- Flask :  
  https://flask.palletsprojects.com/
- FastAPI :  
  https://fastapi.tiangolo.com/

---

## 2. Vue d’ensemble du programme (4 semaines)

- **Semaine 1 :** Bases Web + Flask + HTML/CSS + Git
- **Semaine 2 :** Django complet (MVT, ORM, formulaires, auth)
- **Semaine 3 :** Django REST + bonnes pratiques + déploiement
- **Semaine 4 :** FastAPI + microservices + projet final orienté data

Chaque semaine :

- 5 jours “cours + exercices”
- 1 jour “mini-projet”
- 1 jour “révision / code review / refacto”

---

## 3. Semaine 1 – Fondations Web & Flask

### Objectif de la semaine

- Comprendre le fonctionnement du web (HTTP, requêtes, réponses, routes).
- Revoir Python adapté au web.
- Construire une première petite application Flask.

---

### Jour 1 – Rappels Web & Python

**Cours / Théorie**

- Python : revoir les bases dans le syllabus OC :  
  https://static.oc-static.com/syllabus/518-developpeur-dapplication-python-1-fr-fr-standard.pdf  
- HTTP, REST, JSON :  
  Introduction REST (MDN) :  
  https://developer.mozilla.org/fr/docs/Glossary/REST  

**Exercice**

- Écrire un script Python qui :
  - Consomme une API publique (exemple) :  
    https://jsonplaceholder.typicode.com/posts
  - Affiche les résultats en JSON formaté dans le terminal.

---

### Jour 2 – Introduction à Flask

**Cours**

- OpenClassrooms – “Concevez un site avec Flask”  
  https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask  

**Exercices**

- Créer une app Flask minimale :
  - `/` → renvoie “Hello Flask”
  - `/about` → renvoie une petite page HTML statique
- Ajouter un template Jinja2 avec une base HTML et un bloc de contenu.

---

### Jour 3 – Flask : Templates & Formulaires

**Cours**

- Continuer le cours Flask sur OpenClassrooms (chapitres sur templates & formulaires) :  
  https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask/4525912-ajoutez-une-nouvelle-table-dans-la-base-de-donnees  
  https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask/4526533-testez-le-parcours-utilisateur-avec-les-tests-fonctionnels  

**Exercices**

- Page `/contact` avec formulaire (nom, email, message) :
  - Validation côté serveur (champs obligatoires).
  - Affichage d’un message de succès après envoi.

---

### Jour 4 – Flask + Base de données

**Cours**

- Partie base de données du cours Flask :  
  https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask/4525912-ajoutez-une-nouvelle-table-dans-la-base-de-donnees  
- SQLAlchemy + Flask (modèle d’intégration proposé par la doc Flask) :  
  https://flask.palletsprojects.com/en/latest/patterns/sqlalchemy/

**Exercices**

- Créer un modèle `Article` (titre, contenu, date_creation).
- Routes :
  - `/articles` : liste des articles
  - `/articles/<id>` : détail d’un article
  - `/articles/new` : créer un article via formulaire.

---

### Jour 5 – Tests & Structuration d’un projet Flask

**Cours**

- Partie tests Flask sur OpenClassrooms (tests fonctionnels) :  
  https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask/4526533-testez-le-parcours-utilisateur-avec-les-tests-fonctionnels  

**Exercices**

- Écrire des tests unitaires / fonctionnels pour :
  - La route `/` (HTTP 200 + texte attendu).
  - La création d’un article.
- Réorganiser le projet Flask :
  - `app/__init__.py`
  - `app/routes.py`
  - `app/models.py`
  - `tests/`

---

### Jour 6 – Mini-projet Flask

**Mini-projet 1 : “Journal de bord”**

Fonctionnalités :

- CRUD complet sur des notes (titre, contenu, date).
- Templates propres (layout, navbar, footer).
- Liste paginée.
- Recherche par mot-clé dans le titre.

**Livrable :**

- Code + README expliquant comment lancer le projet.
- Screenshots de l’app.

---

### Jour 7 – Review & Git

- Mettre le projet Flask sur GitHub.
- Rédiger un `README.md` avec :
  - Description.
  - Installation.
  - Commandes pour démarrer.
- Relire le code, supprimer le code mort ou inutile, ajouter quelques commentaires.

---

## 4. Semaine 2 – Django (Site Web complet)

### Objectif de la semaine

- Comprendre l’architecture MVT de Django.
- Construire un site complet avec modèles, vues, templates et admin.
- Comprendre l’ORM, les migrations, les formulaires.

---

### Ressources principales

- OpenClassrooms – “Débutez avec le framework Django”  
  https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  
- Django – Tutoriel officiel “Écriture de votre première application Django”  
  https://docs.djangoproject.com/fr/5.2/intro/tutorial01/  
- Guide “Apprendre : Django (Guide A à Z + Ressources)”  
  https://www.learnthings.fr/apprendre/informatique/langages-de-programmation/python/django/

---

### Jour 8 – Installation & premier projet Django

**Cours**

- OpenClassrooms – chapitres 1–2 du cours Django :  
  https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  
- Tutoriel officiel Django, partie 1 :  
  https://docs.djangoproject.com/fr/5.2/intro/tutorial01/

**Exercices**

- Créer un projet `library`.
- Créer une app `books`.
- Modèle `Book` (titre, auteur, date_pub, résumé).
- Activer le modèle dans l’admin et tester la création de livres.
- Afficher une liste + page détail avec templates.

---

### Jour 9 – MVT, URL & Templates

**Cours**

- MVT, URLconf, templates dans le cours OC :  
  https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  
- Tutoriel Django, parties 2 et 3 :  
  https://docs.djangoproject.com/fr/5.2/intro/tutorial02/  
  https://docs.djangoproject.com/fr/5.2/intro/tutorial03/

**Exercices**

- Créer un `base.html` avec Bootstrap ou Tailwind (CDN).
- Liste de livres avec pagination.
- Page détail bien mise en forme.

---

### Jour 10 – ORM & Relations

**Cours**

- Relations dans le cours Django OC :  
  https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  

**Exercices**

- Modèle `Author` (nom, bio).
- Modèle `Category` (nom).
- Relations :
  - `Book` → `Author` (ForeignKey).
  - `Book` → `Category` (ManyToMany).
- Afficher pour chaque livre :
  - L’auteur.
  - La liste des catégories.

---

### Jour 11 – Formulaires & Authentification

**Cours**

- Formulaires et authentification dans le cours OC Django :  
  https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  

**Exercices**

- Créer un formulaire pour ajouter un livre (form classique ou `ModelForm`).
- Système d’inscription / connexion :
  - `/signup`, `/login`, `/logout`.
- Restreindre la création de livres aux utilisateurs connectés.

---

### Jour 12 – Django avancé : Class-Based Views, messages, etc.

**Cours**

- OpenClassrooms – “Allez plus loin avec le framework Django” :  
  https://openclassrooms.com/fr/courses/7192426-allez-plus-loin-avec-le-framework-django  

**Exercices**

- Transformer certaines vues en `ListView`, `DetailView`, `CreateView`.
- Utiliser le système de `messages` pour afficher les notifications.

---

### Jour 13 – Mini-projet Django (Blog / Catalogue)

**Mini-projet 2 : “Mini-blog Django”**

Fonctionnalités :

- Auth (signup/login/logout).
- CRUD posts (titre, contenu, image optionnelle).
- Modèle `Comment`.
- Pages :
  - Liste des articles.
  - Article détaillé.
  - Création / édition / suppression d’un article (auteur = user connecté).

---

### Jour 14 – Review & amélioration

- Refactor du code :
  - Déplacer les formulaires dans `forms.py`.
  - Structurer les `urls.py` par app.
- Publier le projet sur GitHub avec un bon README.

---

## 5. Semaine 3 – APIs, Django REST & Déploiement

### Objectif de la semaine

- Créer des APIs propres avec Django REST Framework (DRF).
- Gérer l’authentification (Token / JWT).
- Apprendre les tests d’API et le déploiement.

---

### Ressources principales

- OpenClassrooms – “Mettez en place une API avec Django REST Framework” :  
  https://openclassrooms.com/fr/courses/7192416-mettez-en-place-une-api-avec-django-rest-framework  
- Django REST Framework – Documentation officielle :  
  https://www.django-rest-framework.org/

---

### Jour 15 – Introduction à Django REST Framework

**Cours**

- Installation de DRF et première API (cours OC) :  
  https://openclassrooms.com/fr/courses/7192416-mettez-en-place-une-api-avec-django-rest-framework  

**Exercices**

- API `/api/books/` (GET/POST).
- API `/api/books/<id>/` (GET/PUT/DELETE).
- Créer un `BookSerializer`.

---

### Jour 16 – Authentification & Permissions dans DRF

**Cours**

- Sécurisation d’API dans le cours OC DRF (auth, permissions) :  
  https://openclassrooms.com/fr/courses/7192416-mettez-en-place-une-api-avec-django-rest-framework  

**Exercices**

- Installer `djangorestframework-simplejwt` :  
  https://github.com/jazzband/djangorestframework-simplejwt  
- Mettre en place :
  - Auth JWT.
  - Permissions :
    - Anonymes → lecture seule.
    - Authentifiés → CRUD sur leurs propres ressources.

---

### Jour 17 – Tests unitaires & intégration (APIs)

**Cours**

- Tests Django :  
  https://docs.djangoproject.com/fr/5.2/topics/testing/  
- Tests DRF :  
  https://www.django-rest-framework.org/api-guide/testing/

**Exercices**

- Tests :
  - Liste des livres renvoie 200.
  - Création d’un livre nécessite un token.
  - Un utilisateur ne peut pas modifier le livre d’un autre.

---

### Jour 18 – Déploiement d’une app Django

**Cours**

- Choisir un PaaS : Render / Railway / Heroku (si dispo).
  - Render :  
    https://render.com/docs/deploy-django  
  - Railway :  
    https://docs.railway.app/guides/django  

**Exercices**

- Déployer la mini-API (books ou blog) sur Render ou Railway.
- Configurer :
  - Variables d’environnement.
  - `DEBUG=False`.
  - Gestion des fichiers statiques (whitenoise ou équivalent).

---

### Jour 19 – API orientée Data

**Exercices**

- Créer un endpoint `/api/predictions/` dans DRF qui :
  - Reçoit des features en JSON (ex : `age`, `salary`, etc.).
  - Appelle une fonction Python (simulant un modèle ML) pour renvoyer une prédiction.
  - Retourne le résultat en JSON.

---

### Jour 20 – Mini-projet API Django

**Mini-projet 3 : “API de gestion de tâches + stats”**

Fonctionnalités :

- Modèle `Task` (titre, description, statut, date_due, owner).
- API DRF :
  - CRUD complet.
  - Filtre par statut / date / owner.
- Endpoint `/api/stats/` :
  - Nombre de tâches complétées / en cours / en retard.

---

### Jour 21 – Documentation & nettoyage

- Ajouter une doc API avec :
  - drf-yasg :  
    https://github.com/axnsan12/drf-yasg  
  - ou drf-spectacular :  
    https://drf-spectacular.readthedocs.io/  
- Documenter tous les endpoints dans un `README.md`.
- Exporter une collection Postman.

---

## 6. Semaine 4 – FastAPI & Projet final

### Objectif de la semaine

- Comprendre FastAPI (APIs modernes, typées, très rapides).
- Créer un microservice API en FastAPI.
- Faire un projet final qui combine Data + API + BDD.

---

### Ressources principales FastAPI

- Documentation officielle :  
  https://fastapi.tiangolo.com/  

- “FastAPI Tutorial for Beginners – Full Course (2025)” (EN) – YouTube :  
  https://www.youtube.com/watch?v=VirndPTeRaw  

- Playlist “FastAPI Tutorial for Beginners” :  
  https://www.youtube.com/playlist?list=PLS1QulWo1RIamDcSq3TvwMIrkIPdiTkxA  

- Autre crash course FastAPI (EN) :  
  https://www.youtube.com/watch?v=7t2alSnE2-I  
  Playlist complémentaire :  
  https://www.youtube.com/playlist?list=PL6xV3OpvkyrjKvi2YfQlba93WrGb38c5L  

---

### Jour 22 – Bases de FastAPI

**Cours**

- Doc FastAPI : tutoriel rapide :  
  https://fastapi.tiangolo.com/tutorial/  
- Première heure de la vidéo YouTube complète (VirndPTeRaw).

**Exercices**

- Projet FastAPI :
  - Endpoint `GET /` → “Hello FastAPI”.
  - Endpoint `GET /items/{id}` → retourne un item factice.
- Lancer avec :  
  `uvicorn main:app --reload`.

---

### Jour 23 – Pydantic, validation & modèles

**Cours**

- Modèles Pydantic dans la doc FastAPI :  
  https://fastapi.tiangolo.com/tutorial/body/

**Exercices**

- Modèle `User` (nom, email, is_active).
- Endpoint `POST /users/` :
  - Valide le JSON via un `UserCreate` (Pydantic).
  - Retourne l’utilisateur créé (stocké en mémoire pour l’instant).

---

### Jour 24 – FastAPI + DB (SQLAlchemy) & CRUD

**Cours**

- FastAPI + SQL DB :  
  https://fastapi.tiangolo.com/tutorial/sql-databases/

**Exercices**

- Lier FastAPI à une BDD SQLite ou Postgres.
- Créer les modèles SQLAlchemy nécessaires (ex : `PredictionRequest`, `PredictionResult`).
- CRUD simple pour stocker les historiques de prédictions.

---

### Jour 25 – Auth & CORS

**Cours**

- Sécurité / Auth dans FastAPI :  
  https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/  

**Exercices**

- Mettre en place une auth basique (JWT) :
  - `POST /login` → retourne un token.
  - `GET /me` → protégé, renvoie les infos de l’utilisateur.
- CORS (pour un futur front externe) :  
  https://fastapi.tiangolo.com/tutorial/cors/

---

### Jours 26–27 – Projet final

**Projet final : “Micro-plateforme Data API”**

Idée : une API qui expose un modèle de scoring / prédiction, avec historique.

**Architecture :**

- Backend principal : Django + DRF (gestion des utilisateurs, interface admin).
- Microservice de prédiction : FastAPI.
- BDD : Postgres (ou SQLite au début).

**Fonctionnalités Django :**

- Auth + Users.
- Modèles :
  - `Dataset` (optionnel).
  - `PredictionHistory` (features + résultat + date + user).
- Panel admin pour visualiser les prédictions.

**Fonctionnalités FastAPI :**

- Endpoint `/predict` qui :
  - Prend des features en JSON.
  - Appelle une fonction Python (ex : modèle ML, même simplifié).
  - Retourne la prédiction + métadonnées (score, label, etc.).

**Communication Django ↔ FastAPI :**

- Django :
  - Expose un endpoint `/api/predictions/`.
  - Quand une demande arrive :
    - Envoie les données au service FastAPI (HTTP, via `requests`).
    - Récupère la réponse.
    - Sauvegarde dans `PredictionHistory`.
    - Retourne la réponse au client.

**Livrables :**

- Soit 2 repos Git séparés : `django_backend/` et `fastapi_service/`.
- Soit un monorepo avec les 2 dossiers.
- Documentation :
  - README racine expliquant l’architecture globale.
  - README pour Django.
  - README pour FastAPI.
- Collection Postman avec :
  - Endpoints Django (auth, prédictions, historique).
  - Endpoint FastAPI (`/predict`).

---

### Jour 28 – Polish & Portfolio

- Nettoyage du code, refactor des noms de variables et fonctions.
- Ajout de tests sur les endpoints clés (Django + FastAPI).
- Ajout de captures d’écran et d’un petit diagramme d’architecture dans le README.
- Mettre tous les projets sur GitHub et les lier sur le CV / LinkedIn.

---

## 7. Ressources complémentaires

### Django

- OpenClassrooms – “Débutez avec le framework Django” :  
  https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  

- OpenClassrooms – “Allez plus loin avec le framework Django” :  
  https://openclassrooms.com/fr/courses/7192426-allez-plus-loin-avec-le-framework-django  

- MyMooc – “Développez votre site web avec le framework Django” :  
  https://www.my-mooc.com/fr/mooc/developpez-votre-site-web-avec-le-framework-django-c9c71957-c352-47bb-b06a-0e5d53d5f429  

- Tutoriel PDF – “Créer un site Web avec Django pour Python” :  
  https://www.labri.fr/perso/baudon/IremInfo/uploads/Main/HomePage/Django.pdf  

- Vidéo YouTube – “Python Django - Apprendre le Développement Web” (FR) :  
  https://www.youtube.com/watch?v=vN3_jywhg_E  

- Guide “Apprendre : Django (Guide A à Z + Ressources)” :  
  https://www.learnthings.fr/apprendre/informatique/langages-de-programmation/python/django/

---

### Flask

- OpenClassrooms – “Concevez un site avec Flask” :  
  https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask  

- MyMooc – Introduction à Flask (même formation OC, agrégée) :  
  https://www.my-mooc.com/fr/mooc/introduction-a-flask-6c0110d1-0f83-49a0-aafc-5c72976b5e0c  

---

### FastAPI

- Documentation officielle :  
  https://fastapi.tiangolo.com/  

- FastAPI Full Course – YouTube :  
  https://www.youtube.com/watch?v=VirndPTeRaw  

- Playlist “FastAPI Tutorial for Beginners” :  
  https://www.youtube.com/playlist?list=PLS1QulWo1RIamDcSq3TvwMIrkIPdiTkxA  

- Crash course FastAPI :  
  https://www.youtube.com/watch?v=7t2alSnE2-I  
  Playlist associée :  
  https://www.youtube.com/playlist?list=PL6xV3OpvkyrjKvi2YfQlba93WrGb38c5L  

---

### Plateformes / chaînes utiles

- OpenClassrooms (général) :  
  https://openclassrooms.com/  

- Grafikart (tutos FR, très bonne pédagogie même si pas toujours Python) :  
  Site : https://grafikart.fr/  
  YouTube : https://www.youtube.com/@grafikart  

---

## 8. Conseils pour suivre la formation

1. **Un repo par projet**  
   Chaque mini-projet = un dépôt Git → parfait pour le portfolio.

2. **Coder tous les jours**  
   Même si c’est 1h : corriger un bug, ajouter un test, améliorer une vue.

3. **Tenir un journal de progression**  
   Un fichier Markdown du type :
   - “Ce que j’ai appris aujourd’hui”
   - “Ce que je n’ai pas compris”

4. **Relier tout ça à la data**  
   À chaque fois que possible :
   - Exposer un petit modèle ML / script d’analyse via une API.
   - Garder des historiques dans la base pour pouvoir analyser plus tard.

---

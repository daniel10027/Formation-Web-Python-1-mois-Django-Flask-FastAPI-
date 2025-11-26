# Formation Web Python – 1 mois (Django / Flask / FastAPI)

> Objectif : En 4 semaines, développer et déployer une vraie appli web/API en Django, Flask et FastAPI”.

---

## 0. Pré-requis recommandés

Avant d’attaquer le mois, ton collègue doit idéalement :

- ✅ Savoir écrire du Python de base (variables, fonctions, boucles, classes).
- ✅ Connaître un minimum la POO.
- ✅ Comprendre les bases du web : HTTP, requêtes, réponses, JSON, REST.
- ✅ Avoir déjà utilisé un terminal / Git de base.

Pour se mettre à niveau rapidement en Python (facultatif mais conseillé) :  
- Parcours **“Développeur d’application Python”** – OpenClassrooms (chapitres sur Python de base) :contentReference[oaicite:0]{index=0}  
  👉 https://static.oc-static.com/syllabus/518-developpeur-dapplication-python-1-fr-fr-standard.pdf  

---

## 1. Stack & outils à installer (Jour 0)

À faire AVANT de commencer le jour 1 :

- **Python 3.10+**
- **pip** + **venv**
- **Git** + compte GitHub / GitLab
- Un IDE :
  - VS Code ( + extensions Python, Pylance, GitLens, Django)
- **PostgreSQL** ou **SQLite** pour commencer
- **Postman** / **Insomnia** pour tester les APIs
- **Navigateur** (Chrome / Firefox avec DevTools)

Docs officielles (à garder en favoris) :

- Django : https://docs.djangoproject.com/fr/5.2/ :contentReference[oaicite:1]{index=1}  
- Flask : https://flask.palletsprojects.com/  
- FastAPI : https://fastapi.tiangolo.com/  

---

## 2. Vue d’ensemble du programme (4 semaines)

- **Semaine 1 :** Bases Web + Flask + HTML/CSS + Git
- **Semaine 2 :** Django complet (MVT, ORM, formulaires, auth)
- **Semaine 3 :** Django REST + bonnes pratiques + déploiement
- **Semaine 4 :** FastAPI + microservices + projet final orienté data

Chaque semaine :
- 5 jours “cours + exos”
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

**Théorie / Cours**

- Revoir Python (fonctions, classes, modules, virtualenv) – via sections Python de ce syllabus OC :contentReference[oaicite:2]{index=2}  
  👉 https://static.oc-static.com/syllabus/518-developpeur-dapplication-python-1-fr-fr-standard.pdf  
- Comprendre HTTP, REST, JSON :
  - Article d’intro REST (au choix, par ex. MDN : https://developer.mozilla.org/fr/docs/Glossary/REST)

**Exercices**

- Écrire un script Python qui :
  - Consomme une API publique (ex. https://jsonplaceholder.typicode.com/posts)
  - Affiche les résultats au format JSON formaté.

---

### Jour 2 – Introduction à Flask

**Cours**

- OpenClassrooms – **“Concevez un site avec Flask”** :contentReference[oaicite:3]{index=3}  
  👉 https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask  
  (Objectif : suivre au moins les chapitres 1 et 2)

**Exos**

- Créer une app Flask minimale :
  - `/` → renvoie “Hello Flask”
  - `/about` → renvoie une petite page HTML statique
- Ajouter un template Jinja2 avec une base HTML et un bloc de contenu.

---

### Jour 3 – Flask : Templates & Formulaires

**Cours (OC + docs)**

- Chapitres d’OpenClassrooms sur les templates et formulaires :contentReference[oaicite:4]{index=4}  
  👉 https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask/4525912-ajoutez-une-nouvelle-table-dans-la-base-de-donnees  
  👉 https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask/4526533-testez-le-parcours-utilisateur-avec-les-tests-fonctionnels  

**Exos**

- Page `/contact` avec formulaire (nom, email, message) :
  - Validation simple côté serveur (champ obligatoire).
  - Afficher un message de succès après envoi.

---

### Jour 4 – Flask + Base de données

**Cours**

- Partie BDD du cours Flask OpenClassrooms :contentReference[oaicite:5]{index=5}  
- Lire la section sur l’ORM dans Flask (SQLAlchemy) dans la doc :  
  👉 https://flask.palletsprojects.com/en/latest/patterns/sqlalchemy/

**Exos**

- Créer un modèle `Article` (titre, contenu, date_creation).
- Routes :
  - `/articles` : lister les articles
  - `/articles/<id>` : détail d’un article
  - `/articles/new` : créer un article via formulaire

---

### Jour 5 – Tests & Structuration d’un projet Flask

**Cours**

- Partie tests Flask sur OpenClassrooms (pytest / flask-testing / Selenium) :contentReference[oaicite:6]{index=6}  

**Exos**

- Écrire des tests unitaires pour :
  - La route `/` (retourne HTTP 200)
  - La création d’un article
- Réorganiser le projet Flask :
  - `app/__init__.py`
  - `app/routes.py`
  - `app/models.py`
  - `tests/`

---

### Jour 6 – Mini-projet Flask

**Mini-projet 1 : “Journal de bord”**

Fonctionnalités :

- CRUD complet sur des notes (titre, contenu, date)
- Templates propres (layout, navbar, footer)
- Liste paginée
- Recherche par mot-clé dans le titre

**Livrable :**

- Code + README expliquant comment lancer le projet
- Screenshots de l’app

---

### Jour 7 – Review & Git

- Mettre le projet Flask sur GitHub.
- Faire un `README.md` simple :
  - Description
  - Installation
  - Commandes pour démarrer
- Relire le code, supprimer code mort / print, ajouter quelques commentaires.

---

## 4. Semaine 2 – Django (Site Web complet)

### Objectif de la semaine

- Comprendre l’architecture MVT de Django.
- Construire un site complet avec modèles, vues, templates, admin.
- Comprendre l’ORM, les migrations, les formulaires.

---

### Ressources principales

- OpenClassrooms – **“Débutez avec le framework Django”** :contentReference[oaicite:7]{index=7}  
  👉 https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  
- Django – Tutoriel officiel “Écriture de votre première application Django” :contentReference[oaicite:8]{index=8}  
  👉 https://docs.djangoproject.com/fr/5.2/intro/tutorial01/  
- Guide “Apprendre : Django” (parcours, ressources) :contentReference[oaicite:9]{index=9}  
  👉 https://www.learnthings.fr/apprendre/informatique/langages-de-programmation/python/django/

---

### Jour 8 – Installation & premier projet Django

**Cours**

- Chapitres 1–2 du cours OC Django (installation, création de projet) :contentReference[oaicite:10]{index=10}  
- Tutoriel officiel Django, part 1 (modèles, admin, premières vues) :contentReference[oaicite:11]{index=11}  

**Exos**

- Créer un projet `library` :
  - App `books`
  - Modèle `Book` (titre, auteur, date_pub, résumé)
  - Admin : pouvoir gérer les livres
  - Affichage liste + détail avec templates.

---

### Jour 9 – MVT, URL & Templates

**Cours**

- OC : sections sur MVT, URLconf, templates :contentReference[oaicite:12]{index=12}  
- Tutoriel Django part 2–3 (vues, templates, URL) :contentReference[oaicite:13]{index=13}  

**Exos**

- Ajouter des templates propres :
  - `base.html` avec Bootstrap ou Tailwind CDN
  - Liste de livres avec pagination
  - Page détail avec mise en forme propre

---

### Jour 10 – ORM & Relations

**Cours**

- OC Django : relations ManyToOne / ManyToMany :contentReference[oaicite:14]{index=14}  

**Exos**

- Ajouter modèles :
  - `Author` (nom, bio)
  - `Category` (nom)
- Relations :
  - `Book` → `Author` (ForeignKey)
  - `Book` → `Category` (ManyToMany)
- Template :
  - Afficher les catégories pour chaque livre.

---

### Jour 11 – Formulaires & Authentification

**Cours**

- OC Django : formulaires & auth (login/logout, gestion utilisateurs) :contentReference[oaicite:15]{index=15}  

**Exos**

- Créer un formulaire pour ajouter un livre (vue class-based ou fonction).
- Créer un système d’inscription simple :
  - `/signup`, `/login`, `/logout`
  - Restreindre l’ajout de livres aux utilisateurs connectés.

---

### Jour 12 – Django avancé (class-based views, messages, context processors)

**Cours**

- Continuer le cours OC “Débutez avec le framework Django” et commencer **“Allez plus loin avec le framework Django”** :contentReference[oaicite:16]{index=16}  
  👉 https://openclassrooms.com/fr/courses/7192426-allez-plus-loin-avec-le-framework-django  

**Exos**

- Convertir certaines vues en `ListView`, `DetailView`, `CreateView`.
- Utiliser le système de `messages` pour afficher les notifications (succès/erreurs).

---

### Jour 13 – Mini-projet Django (Blog / Catalogue)

**Mini-projet 2 : “Mini-blog Django”**

Fonctionnalités :

- Auth (signup/login/logout)
- CRUD posts (titre, contenu, image optionnelle)
- Commentaires simples (modèle `Comment`)
- Pages :
  - Liste des articles
  - Article détaillé
  - Création / édition / suppression d’un article (auteur = user connecté)

---

### Jour 14 – Review & amélioration

- Refacto du code :
  - Utiliser des `forms.py`
  - Mettre les URL dans `urls.py` d’app et les inclure dans `project/urls.py`
- Mettre le projet sur GitHub avec README.

---

## 5. Semaine 3 – APIs, Django REST & Déploiement

### Objectif de la semaine

- Créer des API propres avec Django REST Framework.
- Apprendre l’authentification (token/JWT).
- Voir les tests automatisés et le déploiement (Heroku/Railway/Render).

---

### Ressources principales

- OpenClassrooms – **“Mettez en place une API avec Django REST Framework”** :contentReference[oaicite:17]{index=17}  
  👉 https://openclassrooms.com/fr/courses/7192416-mettez-en-place-une-api-avec-django-rest-framework  
- Docs Django REST Framework : https://www.django-rest-framework.org/  

---

### Jour 15 – Introduction à Django REST Framework (DRF)

**Cours**

- Installer DRF, créer une API simple sur le modèle Book (liste/détail) :contentReference[oaicite:18]{index=18}  

**Exos**

- API `/api/books/` (GET/POST)
- API `/api/books/<id>/` (GET/PUT/DELETE)
- Serializer `BookSerializer`.

---

### Jour 16 – Authentification & permissions dans DRF

**Cours**

- Chapitres du cours OC sur la sécurisation d’API :contentReference[oaicite:19]{index=19}  

**Exos**

- Auth basée sur Token ou JWT (via `djangorestframework-simplejwt`).
- Protéger la création/modif/suppression de livres :
  - Anonyme → lecture seule
  - Utilisateur authentifié → CRUD sur ses propres ressources.

---

### Jour 17 – Tests unitaires & intégration

**Cours**

- Voir comment écrire des tests Django + DRF (tests API, clients de test)  
  (Tutoriel officiel Django, section tests, + doc DRF “Testing”)

**Exos**

- Test : liste des livres renvoie 200.
- Test : création de livre nécessite authentification.
- Test : utilisateur ne peut pas modifier le livre d’un autre.

---

### Jour 18 – Déploiement d’une app Django

**Cours**

- Choisir un PaaS : Render, Railway, ou autre (docs officielles).
- Lire une ressource sur le déploiement Django + Postgres (par ex. docs Render ou article blog).

**Exos**

- Déployer la mini-API ou le mini-blog de la semaine 2 sur un PaaS gratuit.
- Configurer :
  - Variables d’environnement
  - `DEBUG=False`
  - Static files (whitenoise ou stockage S3-like)

---

### Jour 19 – API orientée Data

**Objectif :** connecter la partie “Data” de ton collègue au web.

**Exos**

- Créer un endpoint `/api/predictions/` dans DRF qui :
  - Reçoit des features en JSON (ex: `age`, `salary`, etc.)
  - Appelle une fonction Python (mock d’un modèle ML) qui renvoie une prédiction.
  - Renvoie le résultat en JSON.

---

### Jour 20 – Mini-projet API Django

**Mini-projet 3 : “API de gestion de tâches / todo + stats”**

Fonctionnalités :

- Modèle `Task` (titre, description, statut, date_due, owner=user)
- API DRF complète :
  - CRUD
  - Filtre par statut / date / owner
- Endpoint `/api/stats/` :
  - Nombre de tâches complétées / en cours
  - Option : retourner un petit agrégat pour une visualisation future.

---

### Jour 21 – Review & documentation

- Ajouter une doc API simple (via `drf-yasg` ou `drf-spectacular`).
- Documenter tous les endpoints dans un `README.md`.
- Exporter une collection Postman de test.

---

## 6. Semaine 4 – FastAPI & Projet final

### Objectif de la semaine

- Comprendre FastAPI (framework moderne pour APIs performantes).
- Créer une API propre & typée.
- Construire un projet final combinant Data + API + base de données.

---

### Ressources principales FastAPI

- Doc officielle : https://fastapi.tiangolo.com/  
- YouTube – **“FastAPI Tutorial for Beginners – Full Course (2025)”** :contentReference[oaicite:20]{index=20}  
  👉 https://www.youtube.com/watch?v=VirndPTeRaw  
- Playlist “FastAPI Tutorial for Beginners” :contentReference[oaicite:21]{index=21}  
  👉 https://www.youtube.com/playlist?list=PLS1QulWo1RIamDcSq3TvwMIrkIPdiTkxA  
- Autre crash course complet :contentReference[oaicite:22]{index=22}  
  👉 https://www.youtube.com/watch?v=7t2alSnE2-I  
  👉 https://www.youtube.com/playlist?list=PL6xV3OpvkyrjKvi2YfQlba93WrGb38c5L  

---

### Jour 22 – Bases de FastAPI

**Cours**

- Premiers chapitres du cours vidéo complet (au moins la première heure) :contentReference[oaicite:23]{index=23}  

**Exos**

- Créer un projet FastAPI :
  - Endpoint `GET /` → “Hello FastAPI”
  - Endpoint `GET /items/{id}` → retourne un item factice
- Lancer avec `uvicorn main:app --reload`.

---

### Jour 23 – Pydantic, validation & modèles

**Cours**

- Sections de la doc sur Pydantic models (FastAPI docs).  

**Exos**

- Créer un modèle `User` (nom, email, is_active).
- Endpoint `POST /users/` :
  - Valide le JSON reçus via un `UserCreate` Pydantic model.
  - Retourne l’utilisateur créé (en mémoire pour l’instant).

---

### Jour 24 – FastAPI + DB (SQLAlchemy) & CRUD

**Cours**

- Chapitres sur FastAPI + BDD (SQLAlchemy) dans la doc.  

**Exos**

- Lier la FastAPI à une base SQLite / Postgres.
- Créer un modèle `PredictionRequest` et `PredictionResult`.
- CRUD simple pour stocker les historiques de prédictions.

---

### Jour 25 – Auth & CORS

**Cours**

- Sections doc FastAPI sur security (OAuth2, JWT).  

**Exos**

- Mettre en place une auth basique (JWT simple) :
  - `POST /login` → retourne un token
  - Protège un endpoint `/me` avec ce token.

---

### Jour 26–27 – Projet final

**Projet final : “Micro-plateforme Data API”**

Idée : une API qui expose un modèle de scoring / prédiction avec historique.

Stack :

- **Backend principal** : Django + DRF (gestion utilisateurs, interface admin).
- **Microservice prédiction** : FastAPI
- **BDD** : Postgres (ou SQLite pour démarrer)
- **Fonctionnalités :**
  - Django :
    - Auth + Users
    - Modèle `Dataset` + `PredictionHistory`
    - Panel admin pour voir les requêtes de prédiction
  - FastAPI :
    - Endpoint `/predict` qui prend des features en JSON
    - Appelle une fonction Python qui renvoie une prédiction (ex. modèle de régression linéaire simulé)
  - Communication :
    - Django envoie les données à FastAPI (requests HTTP)
    - FastAPI renvoie la prédiction
    - Django stocke la prédiction dans `PredictionHistory`

**Livrables :**

- 2 repos Git (ou un monorepo avec 2 dossiers : `django_backend/` et `fastapi_service/`)
- Documentation :
  - README racine expliquant l’architecture
  - README pour Django + README pour FastAPI
- Export Postman avec tous les endpoints.

---

### Jour 28 – Polish & Portfolio

- Nettoyage du code, refacto des noms, commentaires.
- Ajout de tests sur les endpoints clés.
- Ajout de captures d’écran + diagramme simple d’architecture dans le README.
- Mettre les projets sur GitHub (et les lier sur LinkedIn/portfolio).

---

## 7. Ressources complémentaires (à picorer pendant le mois)

### Django (FR + EN)

- OpenClassrooms – “Débutez avec le framework Django” :contentReference[oaicite:24]{index=24}  
  👉 https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django  
- OpenClassrooms – “Allez plus loin avec le framework Django” :contentReference[oaicite:25]{index=25}  
  👉 https://openclassrooms.com/fr/courses/7192426-allez-plus-loin-avec-le-framework-django  
- MyMooc – “Développez votre site web avec le framework Django” :contentReference[oaicite:26]{index=26}  
  👉 https://www.my-mooc.com/fr/mooc/developpez-votre-site-web-avec-le-framework-django-c9c71957-c352-47bb-b06a-0e5d53d5f429  
- Tutoriel PDF “Créer un site Web avec Django pour Python” :contentReference[oaicite:27]{index=27}  
  👉 https://www.labri.fr/perso/baudon/IremInfo/uploads/Main/HomePage/Django.pdf  

- Vidéo – “Python Django - Apprendre le Développement Web” (formation complète FR) :contentReference[oaicite:28]{index=28}  
  👉 https://www.youtube.com/watch?v=vN3_jywhg_E  

- Guide “Apprendre : Django (Guide A à Z + Ressources)” :contentReference[oaicite:29]{index=29}  
  👉 https://www.learnthings.fr/apprendre/informatique/langages-de-programmation/python/django/

---

### Flask

- OpenClassrooms – “Concevez un site avec Flask” :contentReference[oaicite:30]{index=30}  
  👉 https://openclassrooms.com/fr/courses/4425066-concevez-un-site-avec-flask  
- MyMooc – Introduction à Flask (même cours OC, agrégateur) :contentReference[oaicite:31]{index=31}  
  👉 https://www.my-mooc.com/fr/mooc/introduction-a-flask-6c0110d1-0f83-49a0-aafc-5c72976b5e0c  

---

### FastAPI

- Doc officielle :  
  👉 https://fastapi.tiangolo.com/  
- “FastAPI Tutorial for Beginners – Full Course (2025)” :contentReference[oaicite:32]{index=32}  
  👉 https://www.youtube.com/watch?v=VirndPTeRaw  
- Playlist “FastAPI Tutorial for Beginners” :contentReference[oaicite:33]{index=33}  
  👉 https://www.youtube.com/playlist?list=PLS1QulWo1RIamDcSq3TvwMIrkIPdiTkxA  
- Crash course complet :contentReference[oaicite:34]{index=34}  
  👉 https://www.youtube.com/watch?v=7t2alSnE2-I  
  👉 https://www.youtube.com/playlist?list=PL6xV3OpvkyrjKvi2YfQlba93WrGb38c5L  

---

### Plateformes & chaînes généralistes

- OpenClassrooms (général, Python, web) :contentReference[oaicite:35]{index=35}  
  👉 https://openclassrooms.com/  
- Grafikart (tutos FR, même si plutôt orienté JS/PHP, la méthodo est excellente) :contentReference[oaicite:36]{index=36}  
  👉 https://grafikart.fr/  
  👉 https://www.youtube.com/@grafikart  

---

## 8. Conseils pour tirer le maximum de cette formation

1. **Un repo par projet**  
   Chaque mini-projet a son propre repo Git → bon pour le portfolio.

2. **Écrire du code tous les jours**  
   Même 1h : corriger un bug, ajouter un test, refactoriser une vue.

3. **Noter les difficultés**  
   Tenir un petit journal (Markdown) : “ce que j’ai compris aujourd’hui / ce qui reste flou”.

4. **Rester proche de la data**  
   À chaque fois que possible :
   - Créer un endpoint API qui retourne un petit calcul statistique.
   - Exposer un mini-modèle ML ou un script d’analyse.

---

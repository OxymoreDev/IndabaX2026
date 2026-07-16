# Match Engine
### Système intelligent d'appariement entre demandeurs d'emploi et offres d'emploi
**Hackathon IndabaX Congo 2026**

---

## Présentation

Match Engine est un prototype d'intelligence artificielle développé dans le cadre du Hackathon IndabaX Congo 2026.

Le projet automatise la mise en relation entre les demandeurs d'emploi et les offres d'emploi en utilisant des techniques de traitement automatique du langage naturel (NLP) et de similarité vectorielle.

Le système aide les conseillers de l'ACPE à :

- recommander automatiquement les meilleures offres ;
- calculer un score de compatibilité ;
- expliquer les recommandations ;
- identifier les compétences manquantes (Skill Gap) ;
- produire des indicateurs décisionnels.

---

## Fonctionnalités

- Matching automatique Candidat ↔ Offre
- Score de compatibilité
- Recommandation Top-5 et Top-10
- Similarité TF-IDF
- Similarité Cosinus
- Skill Gap (explicabilité)
- Recherche intelligente
- Tableau de bord décisionnel
- Export officiel des recommandations

---

## Architecture

```
Frontend (Next.js)
        │
        ▼
ASP.NET Core Web API
        │
        ▼
ML.NET
        │
        ▼
TF-IDF + Cosine Similarity
        │
        ▼
Classement Top-K
```

---

## Technologies utilisées

### Backend

- ASP.NET Core
- C#
- ML.NET
- CsvHelper

### Frontend

- Next.js
- React
- TypeScript
- TailwindCSS

---

## Méthodologie

Le moteur d'appariement repose sur les étapes suivantes :

1. Chargement des données CSV
2. Nettoyage et normalisation des textes
3. Enrichissement via une base de connaissances métier
4. Vectorisation TF-IDF avec ML.NET
5. Calcul de la similarité cosinus
6. Génération du classement Top-K
7. Calcul des métriques Precision, Recall et NDCG

---

## Structure du projet

```
Backend/
Frontend/
Data/
soumission_matching.json
README.md
```

---

## API

### Résultats

GET

/api/Matching/results

---

### Recherche

GET

/api/Matching/search

---

### Evaluation

GET

/api/Matching/evaluate

---

### Export officiel

GET

/api/Matching/export-officiel

---

## Données

Le projet utilise :

- offres.csv
- candidats.csv
- Appariement_Demandeurs_Offres.csv

---

## Livrables

- Code source
- Backend ASP.NET Core
- Frontend Next.js
- Rapport technique
- soumission_matching.json

---

## Perspectives

Le moteur peut évoluer vers :

- Sentence Transformers
- Embeddings
- Base vectorielle
- Recherche sémantique avancée
- Apprentissage supervisé

---

## Équipe

Hackathon IndabaX Congo 2026

Projet développé par :

**Erasme Mayetela**

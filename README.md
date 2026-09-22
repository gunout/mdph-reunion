<div align="center">

# 🏥 MDPH La Réunion — Tableau de Bord

**Dashboard interactif d'analyse des données AAH, AEEH et indicateurs MDPH pour La Réunion**

[![Live Demo](https://img.shields.io/badge/🌐_Demo-Live-000091?style=for-the-badge)](https://gunout.github.io/mdph-reunion/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white)](https://www.chartjs.org/)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-000091?style=for-the-badge&logo=github)](https://gunout.github.io/mdph-reunion/)

[![Data: CAF](https://img.shields.io/badge/Source-data.caf.fr-000091?style=for-the-badge)](https://data.caf.fr/)
[![Data: data.gouv.fr](https://img.shields.io/badge/Source-data.gouv.fr-000091?style=for-the-badge)](https://www.data.gouv.fr/)
[![Data: DREES](https://img.shields.io/badge/Source-DREES-E1000F?style=for-the-badge)](https://drees.solidarites-sante.gouv.fr/)

🇫🇷 **Bleu · Blanc · Rouge — Une identité institutionnelle au service de l'analyse territoriale**

[**▶ Voir le dashboard en ligne**](https://gunout.github.io/mdph-reunion/)

</div>

---

## 🎯 À propos

Ce projet fournit un **tableau de bord interactif** pour l'analyse des données de la **Maison Départementale des Personnes Handicapées (MDPH) de La Réunion**.

Il exploite les **données publiques officielles** de la CNAF, DREES et INSEE pour produire une vision chiffrée, contextualisée et comparative de l'activité MDPH dans le département.

> **Objectif** : Fournir un outil d'analyse rigoureux, transparent et reproductible sur la réalité du handicap à La Réunion.

---

## ✨ Fonctionnalités

### 📊 Analyse descriptive
- **12 graphiques interactifs** (Chart.js)
- **8 KPIs dérivés** : taux de couverture, CAGR, moyenne mobile, pic historique
- **Filtres dynamiques** : période, granularité (mensuel/trimestriel/annuel)
- **Tableau de données brutes** triable et filtrable

### 🎯 Benchmarks nationaux
- **Taux AAH** : 43,4‰ (La Réunion) vs 33,0‰ (France) → **+32%**
- **Taux de pauvreté** : 32,8% vs 14,4% → **+128%**
- **Délais de traitement** adultes et enfants
- **Satisfaction usagers** (CNSA)

### 🔮 Analyse avancée
- **Projection linéaire à 24 mois**
- **Détection automatique d'anomalies** (écart > 2σ)
- **Annotations historiques** (COVID-19)
- **Analyse contextuelle** générée en langage naturel

### 📄 Export
- **Export PDF** (jsPDF + html2canvas)
- Aucune donnée envoyée à un serveur externe

---

## 🚀 Accès rapide

### En ligne

👉 **[https://gunout.github.io/mdph-reunion/](https://gunout.github.io/mdph-reunion/)**

### En local

```bash
# Cloner le dépôt
git clone https://github.com/gunout/mdph-reunion.git
cd mdph-reunion

# Lancer un serveur local (obligatoire pour charger les CSV)
python3 -m http.server 8010

# Ouvrir dans le navigateur
# → http://localhost:8010/
```

---

## 📡 Sources de données

| Source | Contenu | Fréquence |
|--------|---------|-----------|
| [**data.caf.fr**](https://data.caf.fr/) | Bénéficiaires AAH par département, âge, taux | Mensuelle |
| [**data.gouv.fr**](https://www.data.gouv.fr/) | Évolution AAH et AEEH 2012-2021 | Annuelle |
| [**DREES**](https://drees.solidarites-sante.gouv.fr/) | Benchmarks AAH | Annuelle |
| [**INSEE**](https://www.insee.fr/) | Population, pauvreté | Annuelle |
| [**CNSA**](https://www.cnsa.fr/) | Baromètre MDPH | Annuelle |

---

## 🏗️ Architecture

```
mdph-reunion/
├── index.html                    # Dashboard (page unique)
├── data/                         # Datasets CSV
│   ├── aah_reunion_evolution.csv
│   ├── aah_reunion_age.csv
│   ├── aah_reunion_aah_taux_incapacite.csv
│   ├── aah_reunion_aah_complement_age.csv
│   ├── aah_reunion_aah_taux_plein_partiel.csv
│   ├── aah_reunion_depuis_2012.csv
│   └── aeeh_reunion.csv
├── LICENSE                       # Licence MIT
└── README.md
```

### Stack technique

| Composant | Technologie |
|-----------|-------------|
| **Frontend** | HTML5 + CSS3 + JavaScript ES6 |
| **Graphiques** | Chart.js 4.x + chartjs-plugin-annotation |
| **Parsing CSV** | PapaParse 5.4 |
| **Export PDF** | jsPDF 2.5 + html2canvas 1.4 |
| **Hébergement** | GitHub Pages |

---

## 📊 Benchmarks nationaux

| Indicateur | La Réunion | France | Écart | Source |
|-----------|-----------|--------|-------|--------|
| **Taux AAH** (‰ hab. 20-64 ans) | **43,4** | 33,0 | **+32%** | DREES 2022 |
| **Taux de pauvreté** | **32,8%** | 14,4% | **+128%** | INSEE 2024 |
| **Bas revenus AAH** | **54,3%** | 34,8% | **+19 pts** | DREES 2022 |
| **Délai adultes** | 3,99 mois | 4,6 mois | **-13%** ✅ | MDPH 2024 |
| **Délai enfants** | **7,92 mois** | 4,0 mois | **+98%** ⚠️ | MDPH 2024 |

### Faits marquants

- 🔴 Prévalence du handicap **32% supérieure** à la moyenne nationale
- 🔴 Taux de pauvreté **2,3× plus élevé** qu'en France métropolitaine
- 🟢 Délais adultes **meilleurs** que la moyenne nationale
- 🔴 Délais enfants **2× plus longs** que la moyenne nationale

---

## 🤝 Contribution

Les contributions sont les bienvenues !

```bash
git checkout -b feature/ma-nouvelle-fonctionnalite
git commit -m "feat: ajout de la carte par commune"
git push origin feature/ma-nouvelle-fonctionnalite
```

**Convention de commit** : [Conventional Commits](https://www.conventionalcommits.org/)

---

## 📄 Licence

Distribué sous licence **MIT**. Voir [LICENSE](LICENSE) pour plus de détails.

---

<div align="center">

**🇫🇷 Liberté · Égalité · Fraternité**

Fait avec ❤️ à La Réunion

</div>

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>

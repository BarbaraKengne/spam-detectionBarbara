# 📧 Détection de Spam par Machine Learning

**Barbara KENGNE — Licence 3 Informatique, Aix-Marseille Université**

---

## 🎯 Objectif

Construire et comparer plusieurs modèles de classification pour détecter automatiquement les messages spam à partir d'un corpus de SMS réels.

---

## 📊 Résultats

| Modèle | Accuracy | Precision | Recall | F1-Score |
|--------|----------|-----------|--------|----------|
| Naive Bayes (MultinomialNB) | ~97% | ~100% | ~88% | ~94% |
| Régression Logistique | ~97% | ~97% | ~91% | ~94% |
| **SVM Linéaire** | **~98%** | **~98%** | **~93%** | **~96%** |

> ✅ Le SVM Linéaire est le meilleur modèle selon le F1-Score.

---

## 🗂️ Structure du projet

```
spam-detection/
│
├── spam_detection_barbara.ipynb   # Notebook principal
├── spam.csv                       # Dataset (5 572 SMS étiquetés)
├── README.md                      # Ce fichier
│
└── images/
    ├── distribution.png           # Répartition ham/spam
    ├── longueur_messages.png      # Analyse de la longueur
    ├── wordclouds.png             # Nuages de mots
    ├── comparaison_modeles.png    # Comparaison des 3 modèles
    └── confusion_matrix.png      # Matrice de confusion
```

---

## 🔬 Méthodologie

### 1. Exploration des données (EDA)
- Analyse de la distribution des classes (86.6% ham / 13.4% spam)
- Visualisation de la longueur des messages par catégorie
- Nuages de mots pour identifier les termes caractéristiques

### 2. Prétraitement
- Encodage des labels (ham = 0, spam = 1)
- Séparation train/test (80% / 20%) avec stratification
- Vectorisation **TF-IDF** avec unigrammes et bigrammes (5 000 features max)

### 3. Modèles entraînés
- **Naive Bayes (MultinomialNB)** — modèle probabiliste, interprétable
- **Régression Logistique** — modèle linéaire généralisé
- **SVM Linéaire (LinearSVC)** — meilleure performance sur texte

### 4. Évaluation
- Métriques : Accuracy, Precision, Recall, F1-Score
- Matrice de confusion
- Validation croisée 5 folds pour confirmer la robustesse

---

## 🛠️ Technologies utilisées

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-lightgrey?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-visualisation-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

- **Python 3.10**
- **Pandas / NumPy** — manipulation des données
- **Scikit-learn** — modèles ML et métriques
- **Matplotlib / Seaborn** — visualisations
- **WordCloud** — nuages de mots
- **TF-IDF** — vectorisation des textes

---

## 🚀 Lancer le projet

```bash
# Cloner le dépôt
git clone https://github.com/BarbaraKengne/spam-detection.git
cd spam-detection

# Installer les dépendances
pip install pandas numpy scikit-learn matplotlib seaborn wordcloud jupyter

# Lancer le notebook
jupyter notebook spam_detection_barbara.ipynb
```

---

## 📁 Dataset

Le dataset utilisé est le **SMS Spam Collection Dataset**, disponible sur [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset).  
Il contient 5 572 messages SMS en anglais, étiquetés **ham** (légitime) ou **spam**.

---

## 💡 Pistes d'amélioration

- [ ] Tester des modèles de deep learning (LSTM, BERT)
- [ ] Étendre à d'autres langues
- [ ] Déployer via une API Flask / FastAPI
- [ ] Ajouter une interface web simple

---

## 👩‍💻 Auteure

**Barbara KENGNE**  
Étudiante en Licence 3 Informatique — Aix-Marseille Université  
🔗 [LinkedIn](https://www.linkedin.com/in/barbara-nguimfack-kengne-343094303) | 🐙 [GitHub](https://github.com/BarbaraKengne) | 📊 [Kaggle](https://kaggle.com/barbarakengne)

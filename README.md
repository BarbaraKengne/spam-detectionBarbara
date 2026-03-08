# Détection de Spam par Machine Learning

Projet personnel réalisé en Licence 3 Informatique (Aix-Marseille Université).  
L'idée était de partir d'un dataset de SMS réels et de voir jusqu'où on peut aller avec des modèles classiques de ML.

---

## Ce que fait ce projet

À partir d'un corpus de 5 572 SMS étiquetés spam ou ham (légitime), j'ai :
- analysé les données (distribution, longueur des messages, mots fréquents)
- vectorisé le texte avec TF-IDF (unigrammes + bigrammes)
- entraîné et comparé 3 modèles : Naive Bayes, Régression Logistique, SVM Linéaire
- évalué les résultats avec accuracy, precision, recall, F1-score et une matrice de confusion

## Résultats

| Modèle | Accuracy | F1-Score |
|--------|----------|----------|
| Naive Bayes | ~97% | ~94% |
| Régression Logistique | ~97% | ~94% |
| SVM Linéaire | ~98% | ~96% |

Le SVM Linéaire donne les meilleurs résultats sur ce dataset.

---

## Fichiers

- `spam_detection_barbara.ipynb` — le notebook complet
- `spam.csv` — le dataset

---

## Lancer le projet

```bash
pip install pandas numpy scikit-learn matplotlib seaborn wordcloud jupyter
jupyter notebook spam_detection_barbara.ipynb
```

## Dataset

SMS Spam Collection Dataset — disponible sur [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset).

---

## Ce que j'aimerais faire ensuite

- tester avec BERT ou un modèle de transformers
- déployer via une petite API Flask
- tester sur des données en français

# td3_decentralisation

Code 1 : Logistic Regression (simple et rapide).

Code 2 : Random Forest (robuste pour des ensembles de données complexes).

Code 3 : SVM (idéal pour les frontières de décision claires).

Code 4 : KNN (basé sur la proximité des exemples).


## Résumé des performances des modèles

### **1. Évaluation des modèles**
Les 4 modèles ont été évalués sur le dataset Iris, en utilisant un ensemble de test composé de 30 échantillons. Voici les résultats pour chaque modèle :

| Modèle            | Précision globale | Matrice de confusion                          | F1-score moyen |
|--------------------|-------------------|-----------------------------------------------|----------------|
| Régression Logistique (Code_1.py) | 1.00             | `[[10, 0, 0], [0, 9, 0], [0, 0, 11]]`       | 1.00           |
| Random Forest (Code_2.py)         | 1.00             | `[[10, 0, 0], [0, 9, 0], [0, 0, 11]]`       | 1.00           |
| SVM (Code_3.py)                   | 1.00             | `[[10, 0, 0], [0, 9, 0], [0, 0, 11]]`       | 1.00           |
| KNN (Code_4.py)                   | 1.00             | `[[10, 0, 0], [0, 9, 0], [0, 0, 11]]`       | 1.00           |

---

### **2. Analyse détaillée**
#### Précision globale :
- Tous les modèles ont obtenu une précision globale de **100%**, ce qui signifie que chaque modèle a correctement classé les 30 échantillons de l'ensemble de test.

#### Matrice de confusion :
- La matrice de confusion montre que :
  - **Setosa** (10 échantillons), **Versicolor** (9 échantillons), et **Virginica** (11 échantillons) ont été correctement classifiés sans aucune erreur pour chaque modèle.

#### Rapport de classification :
- Chaque classe (`Setosa`, `Versicolor`, `Virginica`) a atteint une **précision**, un **rappel**, et un **F1-score** de **1.00**.
- Les moyennes macro et pondérées confirment également cette performance parfaite.

---

### **3. Explication des modèles**
1. **Régression Logistique (Code_1.py)** :
   - Modèle simple basé sur la séparation linéaire des classes.
   - Convient bien pour des datasets bien séparés comme Iris.

2. **Random Forest (Code_2.py)** :
   - Modèle basé sur des ensembles d'arbres de décision.
   - Robuste et performant, même sur des problèmes non linéaires.

3. **SVM (Code_3.py)** :
   - Modèle utilisant un noyau RBF pour séparer les classes.
   - Idéal pour des frontières de décision complexes.

4. **KNN (Code_4.py)** :
   - Modèle basé sur les plus proches voisins.
   - Performance dépendante du choix du nombre de voisins.

---

### **4. Conclusion**
- Tous les modèles se comportent parfaitement sur le dataset Iris en raison de la simplicité de ce dernier et de la séparation claire entre les classes.
- Dans des contextes plus complexes, les performances des modèles peuvent varier selon la nature des données. Par exemple :
  - La **Régression Logistique** pourrait échouer si les classes ne sont pas linéairement séparables.
  - Le **KNN** pourrait être sensible aux données bruitées.


# Question 2

Le modèle agrégé, basé sur un consensus des prédictions de 4 modèles distincts (Régression Logistique, Random Forest, SVM, et KNN), a obtenu une précision de 100% sur l'ensemble de test du dataset Iris.

## Points forts :
### Robustesse : 
En combinant plusieurs modèles, le consensus permet de corriger les erreurs potentielles de modèles individuels.
Performance : Le vote majoritaire est une méthode simple et efficace pour agréger les prédictions.
### Limites :
Le dataset Iris est relativement simple, ce qui explique les performances parfaites. Sur des datasets plus complexes, cette méthode devra être testée pour vérifier sa robustesse.

terminal : pip install flask scikit-learn

http://127.0.0.1:5000/predict?sepal_length=5.1&sepal_width=3.5&petal_length=1.4&petal_width=0.2

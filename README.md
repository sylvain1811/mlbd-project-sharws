# MLBD Project : Simplified Human Activity Recognition w/Smartphone

## Features

`list_indexes` est une liste qui contient des listes d'index, avec à la première case tous les index. Ensuite, les listes suivantes sont des listes contenant moins d'indices, car une méthode de feature selection a été appliquée.

## Models

On utilise différents models :

- MLP
- KNN
- SVM

## Conventions

- On stock les résultats dans un dictionnaire
  - Les clés sont les noms des classifiers
  - Les valeurs sont des dictionnaires
    - les clés sont les indices dans `list_indexes`, donc cela représentent quelles features sont utilisées
    - Les valeurs sont des dictionnaires
      - Les clés les nom des résultats (accuracy, confusion matrix, ...)
      - Les valeurs sont les valeurs effectives des résultats (double pour accuracy, liste de liste pour confusion matrix, ...)

Ci dessous un exemple de ce dictionnaire de résultats, avec des valeurs arbitraires.

```python
results = {"svm": {0: {"accuracy": 0.95, "conf_mat": [[...]]}, 1: {"accuracy": 0.91, "conf_mat": [[...]]}},
           "mlp": {0: {"accuracy": 0.98, "conf_mat": [[...]]}, 1: {"accuracy": 0.81, "conf_mat": [[...]]}}}
```

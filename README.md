# Projet-de-NLP
Projet de *Natural Language Processing* de 3ème année à l'Ensae Paris.

## Abstract

## Cloner le dépôt 

```
git clone https://github.com/averniere/Projet-de-NLP.git
```

## Installation des dépendances

Avant d'exécuter le code des différents notebooks : 
```
pip install -r requirements.txt
```
Ainsi que :
```
python -m spacy download fr_core_news_lg
```
Les professions de foi constituant un fichier trop volumineux, il est nécessaire de les télécharger au préalable en local. Le code du fichier `preprocess.py` charge des données sous la forme `legislatives.zip` dans le fichier `data/`.

## Organisation du dépôt

- `annotations/`: fichiers de phrases annotés.
- `data/`: fichier de métadonnées ARCHELEC.
- `outputs/`: fichiers de phrases avec les prédictions des labels par les deux modèles.
- `preprocess.py`: télécharge les données, les nettoie et les met sous la forme d'un dataframe *transcriptions*.
- `exploration.ipynb`: analyse des professions de foi grâce aux méthodes de *part of speech* et génération des phrases à annoter.
- `modeles.ipynb`: entraînement sur les annotations, permet de générer deux fichiers avec les phrases et leurs annotations (trop lourds pour le dépôt)
- `analyse.ipynb`: analyse des prédictions (seulement B-VERB) des modèles.


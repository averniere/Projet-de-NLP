# Projet-de-NLP
Projet de *Natural Language Processing* de 3ème année à l'Ensae Paris.

## Abstract
 L'étude des verbes dans une phrase, lorsqu'ils suivent un pronom personnel sujet, permet de répondre à la question de l'agence, ou du caractère actif, des locuteurs ou personnages des textes étudiés. Sous le prisme du genre, elle met en lumière les stéréotypes véhiculés par les auteurs, selon lesquels les femmes seraient moins actives que les hommes, ce qui se traduit lexicalement. Transposée à des textes politiques, ici les professions de foi de l'élection législative en France de 1993, cette étude vise à identifier si les candidats des différents bords politiques se présentent comme plus ou moins actifs. Le caractère actif est défini à la fois lexicalement parlant, en opposition aux verbes d'état, de cognition, de sentiment et par rapport au contexte de l'élection : est-ce qu'un candidat énonce des propositions concrètes ? En mobilisant des méthodes de *Natural Language Processing*, nous analysons les rôles et la fréquence des pronoms personnels dans les professions de foi par partis politiques et entraînons le modèle CamemBERT pour classifier les verbes comme actifs ou inactifs selon les deux définitions données. Les candidats d'extrême-droite et écologistes apparaissent comme les plus actifs selon les deux acceptions. Tous les candidats se positionnent le plus fréquemment comme lexicalement actifs, mais les partis traditionnels, de gauche et de droite parlent autant du contexte électoral que des actions qu'ils mèneraient en tant qu'élus. Ces résultats restent à nuancer, du fait du trop faible nombre de données annotées.
 
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
- `rapport.pdf`: texte du rapport


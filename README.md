# Jeu de cartes simple

Ce projet implémente un petit jeu de cartes en Python où plusieurs joueurs tirent chacun une carte et le joueur ayant la meilleure carte remporte la partie.

## Structure du projet

- `main.py` : point d'entrée de l'application.
- `controllers/base.py` : logique de contrôle du jeu, gestion des joueurs, distribution des cartes et détermination du gagnant.
- `models/card.py` : définition des cartes, des couleurs et des valeurs.
- `models/deck.py` : définition du paquet de cartes et de la pioche.
- `models/player.py` : définition du joueur et de sa main.
- `views/base.py` : interface utilisateur en ligne de commande.

## Prérequis

- Python 3.7+
- Un environnement virtuel recommandé

## Installation

1. Créez et activez un environnement virtuel :

```powershell
python -m venv venv
venv\Scripts\activate
```

2. Installez les dépendances :

```powershell
pip install -r requirements.txt
```

## Utilisation

Lancez le jeu avec :

```powershell
python main.py
```

### Déroulement

- Le jeu demande successivement les noms des joueurs (jusqu'à 5 joueurs maximum).
- Chaque joueur tire une carte.
- Les cartes sont ensuite retournées et le joueur avec la meilleure carte gagne.
- Vous pouvez choisir de recommencer une nouvelle partie.

## Personnalisation

- Ajoutez des règles supplémentaires dans `controllers/base.py`.
- Modifiez l'affichage de la vue dans `views/base.py`.
- Changez le comportement du paquet dans `models/deck.py`.

## Tests

Ce projet ne contient pas encore de tests automatisés, mais vous pouvez créer des tests unitaires pour :

- la comparaison des cartes dans `models/card.py`
- les méthodes du paquet dans `models/deck.py`
- la logique de distribution et de détermination du gagnant dans `controllers/base.py`

Une structure simple avec `pytest` pourrait ressembler à :

```powershell
pip install pytest
pytest
```

## Améliorations possibles

- Supporter un nombre de joueurs dynamique plus grand ou configurable.
- Ajouter des règles de jeu supplémentaires (par exemple, plusieurs tours, comparaison de mains complètes, ou un jeu de type bataille).
- Améliorer l'interface en ajoutant une interface graphique ou une interface web.
- Gérer la fin du paquet et la redistribution des cartes de façon plus robuste.

## Remarques

- Les cartes sont comparées d'abord par valeur, puis par couleur en cas d'égalité de rang.
- Le projet est conçu pour un usage en ligne de commande simple.

---
title: "Aller-Retour"
date: 2021-05-16T17:46:52-05:00
draft: false
cover:
    image: img/aller-retour_banner.png
tags: ["Unreal", "Game Jam", "Blueprint"]
---

# Présentation

Aller-Retour est un jeu réalisé lors de la 18e édition du Creative Jam organisé par PolyGames et l'école UQAC-NAD! J'étais accompagné d'un autre programmeur et de 5 artistes afin de réaliser ce jeu dans un délai de seulement 46h. Nous avons gagné le prix de la première place!

C'est un jeu avec une petite histoire où le joueur incarne une aventurière qui découvre un dispositif qui permet de voyager dans le temps. Le joueur est ainsi mené à traverser le niveau en en résolvant quelques puzzles afin d'arriver à la fin du jeu.

{{< youtube A6E1-JrCx7Q >}}

# Environnement adaptatif
Pour répondre à ce défi technique, nous avons créé une mécanique de voyage temporel. Ainsi, lorsque le joueur appuie sur "Q", un effet de transition d'époque a lieu et le joueur va être transporté dans le monde de l'année 2050. L'environnement peut ainsi être modifié dépendamment des actions produites dans le passé pour ensuite y voir les répercussions lorsqu'on revient en 2060.

![Video gameplay time travel](/img/aller-retour_timetravel.webp)

Puisque nous n'avions pas le temps de créer deux environnnements complètement différents pour les deux époques, nous avons alors utilisé trois "levels" dans unreal pour créer cet effet. Un level pour l'environnement qui ne change pas, puis un level par époque afin d'avoir des petits déplacements d'objets, un "PostProcessVolume" différent ainsi que les éléments de gameplay.

![Image du jeu](/img/aller-retour_levels.PNG)

# Programmation
Puisque le jeu a été fait lors d'un Game Jam, ce projet a été réalisé en Blueprints.

# Liens

[Page ITCH.IO du jeu](https://vincent-graciet.itch.io/aller-retourgj)

[Page du Creative Jam](https://itch.io/jam/18ime-creative-jam-virtuel)
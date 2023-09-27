---
title: "THAT GAME"
date: 2022-06-12T10:31:07-05:00
draft: false
cover:
    image: img/thatgame_banner.png
tags: ["Unreal", "Game Jam", "Blueprint"]
---

# Présentation

THAT GAME est un jeu réalisé lors du Game Jam Funni Jam #2 pendant 3 jours. J’étais le seul programmeur sur le projet accompagné de 4 artistes. Nous avons gagné le prix de la première place lors de ce Game Jam !

Le principle du jeu est simple, vous êtes le seul employé d'un magasin de jouets et la nouvelle sensation "THAT GAME" vient de sortir! Tout le monde en veut un. Les jouets de l'arrière-boutique n'en sont pas si contents et ne reculeront devant rien pour vous empêcher de vous procurer ces fichues boîtes. Le jeu comprend 5 niveaux se situant tous dans les mêmes pièces mais avec une difficulté croissante par rapport au nombre d'ennemis et de boîte que vous devez retrouver.

{{< youtube xYO-il5Mjw0 >}}

# Mécaniques

### Combat
Le jeu se joue à la première personne avec deux mécaniques de combat. Le joueur peut utiliser le pistolet coup-de-point afin de faire du dégât aux ennemies et le sablier magique afin de geler sur place ces derniers.

![Video gameplay combat](/img/thatgame_video.webp)

### Ennemis
Il y a plusieurs ennemis, certains utilisent le "pathfinding" simple d'Unreal afin de se déplacer dans l'environnement et d'autres sont statiques.

![Video ennemis](/img/thatgame_ennemies.webp)

### Interaction
Le système d'interaction est plutôt simple mais fonctionnel! Le jeu va trouver la meilleure interaction possible grâce à une série de paramètres. Ainsi, il n'est pas possible d'avoir deux interactions simultanément et ces derniers ne doivent pas être obstrués par d'autres éléments de l'environnement.

![Video interaction](/img/thatgame_interaction.webp)

# Programmation
Puisque le jeu a été fait lors d'un Game Jam et que j'étais le seul programmeur, ce projet a été réalisé en Blueprints.

# Liens

[Page ITCH.IO du jeu](https://lespaullord.itch.io/that-game)

[Page Funni Jam #2](https://itch.io/jam/funni-jam-2/results)
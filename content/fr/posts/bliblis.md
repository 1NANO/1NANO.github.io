---
title: "Blibli’s Playground of Ego Death"
date: 2022-01-23T17:17:46-05:00
draft: false
cover:
    image: img/bliblis_banner.jpg
tags: ["Unreal", "Game Jam", "Blueprint"]
---

# Présentation

Blibli's Playground of Ego Death est un jeu réalisé lors de la 19e édition du Creative Jam organisé par PolyGames et l'école UQAC-NAD! J'étais accompagné d'un autre programmeur et de 5 artistes afin de réaliser ce jeu dans un délai de seulement 48h. Nous avons gagné le prix artistique grâce à ce jeu.

Le but du jeu est de se promener dans l'imagination du personnage Blibli et de trouver le plus "d'Ego wizard" pour aider à rassembler son esprit fracturé et à recharger son "Ego power". Par contre, vous n'êtes pas seul dans ce monde. Un monstre tente sens cesse de vous attraper et votre seul moyen de le repousser est d'utiliser votre "Ego Power". Il s'agit d'un jeu à la première personne de type arcade où le but est d'atteindre le plus haut score sans mourir.

{{< youtube O6aqHrQpKok >}}

# Mécaniques

### Ego power
Le "Ego Power" permet d'échanger les rôles entre Blibli et le monstre. Ainsi, le monstre est repoussé et reçois des dégâts jusqu'à éventuellement disparaitre.

![Video gameplay combat](/img/bliblis_fight.webp)

### Effets visuels
Lorsque le joueur utilise le "Ego Power", plusieurs effets visuels ont lieu. Ci-dessous, le "material function" permet de créer un effet sinusoïdal au sol autour du joueur.

![Image material function](/img/bliblis_materialfunction.PNG)
![Video effet](/img/Bliblis_waves.webp)

### Monstre
Le monstre va constamment courir vers le joueur et va réapparaitre après un certain temps lorsqu'il est tué. Une musique stressante se met à jouer lorsque le monstre est dans les environs du joueur.

![Image monstre](/img/bliblis_monster.PNG)

# Programmation
Puisque le jeu a été fait lors d'un Game Jam, ce projet a été réalisé en Blueprints.

# Liens

[Page ITCH.IO du jeu](https://lespaullord.itch.io/bliblis-playoground-of-ego-death)

[Page du Creative Jam](https://itch.io/jam/19ieme-creative-jam-virtuel)
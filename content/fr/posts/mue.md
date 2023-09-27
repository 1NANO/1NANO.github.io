---
title: "Mue"
date: 2022-05-13T08:24:37-05:00
draft: false
cover:
    image: img/mue_banner.jpg
tags: ["Unreal", "C++"]
---

# Présentation

MUE est une courte expérience d'horreur à la première personne empreinte d'échos symboliques et d'une atmosphère à glacer le sang. Ce projet de synthèse universitaire a été réalisé en 4 mois avec l'aide de 2 autres programmeurs et 16 artistes.

En 1890, une jeune femme prénommée Alicia se réveille dans un bâtiment lugubre. Alors qu'elle plonge dans ce labyrinthe tortueux, des événements de plus en plus terrifiants se manifestent. Elle devra confronter sa peur de vieillir pour survivre en explorant cet environnement, reflet grotesque du fil de sa vie.

Aurez-vous le courage de surmonter vos peurs ? MUE vous invite dans un univers déphasé où nos plus profondes angoisses prennent vie. Ici, il n'y a qu'une chose qui peut vous sauver.

Memento Mori.

{{< youtube tacJPLp3VRM >}}

# Mécaniques

### Sanité
La sanité dans le jeu influence la visibilité ainsi que la vitesse de déplacement du joueur. On peut respirer en maintenant LT et RT ce qui enclenche le processus de respiration.

{{< youtube 3cl4_wY90Fw >}}

### Cinématique "seamless"
Ce système permet d'interpoller la caméra et les mouvements du joueur pendant des cinématiques afin qu'il n'y ait aucune coupure entre le début et la fin.

{{< youtube 63eZ3IRkozk >}}
-
{{< youtube YJWgF3jwUik >}}

### Ramper
À un certain moment, le joueur est mené à se pencher et entrer dans une cheminée. Puisque l'espace est donc restreinte, une mécanique spéciale a été conçu afin de pouvoir déplacer le joueur dans ce tunnel.

{{< youtube E3AzAcCjN3k >}}

### IA
À la fin du jeu, le joueur fait face avec la vieille grâce. Elle possède plusieurs chemins prédéfinis afin de ne pas toujours bouger de la même façon. Le joueur doit ainsi tenter de se faufiler sans se faire voir.

{{< youtube Xw6weU3JlZo >}}

# Programmation

Tout ce projet a été programmé en c++ avec une utilisation faible de Blueprints pour certains éléments de base.

# Lien

[Page ITCH.IO du jeu](https://uqac.itch.io/mue)

---
title: "Aller-Retour"
date: 2021-05-16T17:46:52-05:00
draft: false
cover:
    image: img/aller-retour_banner.png
tags: ["Unreal", "Game Jam", "Blueprint"]
---

# Presentation

Aller-Retour is a game made during the 18th edition of the Creative Jam organized by PolyGames and the UQAC-NAD school! I was accompanied by another programmer and 5 artists to create this game in just 46 hours. We won the first place prize!

It's a game with a short story where the player plays an adventurer who discovers a device that allows you to travel through time. The player is thus led to cross the level by solving a few puzzles in order to reach the end of the game.

{{< youtube A6E1-JrCx7Q >}}

# Adaptive environment
To address this technical challenge, we created a time travel mechanic. Thus, when the player presses "Q", an era transition effect takes place and the player will be transported to the world of the year 2050. The environment can thus be modified depending on the actions produced in the past to then see the repercussions when we return to 2060.

![Video gameplay time travel](/img/aller-retour_timetravel.webp)

Since we didn't have time to create two completely different environments for the two eras, we then used three levels in unreal to create this effect. A level for the environment which does not change, then a level per era in order to have small movements of objects, a different "PostProcessVolume" as well as the gameplay elements.

![Image of the game](/img/aller-retour_levels.PNG)

# Programming
Since the game was made during a Game Jam, this project was done in Blueprints.

# Links

[ITCH.IO game page](https://vincent-graciet.itch.io/aller-retourgj)

[Creative Jam page](https://itch.io/jam/18ime-creative-jam-virtuel)
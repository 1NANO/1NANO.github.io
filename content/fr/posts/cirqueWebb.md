---
title: "Le Cirque Webb"
date: 2021-12-13T09:28:14-05:00
draft: false
cover:
    image: img/cirquewebb_banner.jpg
tags: ["Unreal", "C++"]
---

# Présentation

Le cirque Webb est un jeu vidéo d’exploration linéaire rempli de mini-jeux de tir. Le joueur incarne Mousse la mouche qui visite le cirque des araignées. Il devra avancer dans les niveaux en collectionnant des étampes pour atteindre la magnifique grande roue.  À cet effet, le joueur devra utiliser la balle en sa possession pour gagner à des stands de tir, explorer pour trouver des jetons cachés ou vendre ses informations personnelles.

Ce jeu a été réalisé dans le cadre d'un cours à l'UQAC sur une durée de 4 mois avec l'aide de 2 autres programmeurs et 15 artistes. Je me suis principalement occupé du système de dialogue ainsi que la progression du "Game State". J’ai donc fait beaucoup de programmation UI et gameplay dans ce projet.

{{< youtube LBgsKHtbXMQ >}}

# Mécaniques

### Système de dialogue

#### Dialogue intelligent

Le Cirque Webb possède un système de dialogue complexe permettant de concevoir des arbres de dialogues intelligents. Il permet donc de faire des branchements conditionnels, lancer des éléments de gameplay, de recevoir les inputs du joueur et bien plus encore. Afin de pouvoir faire tout cela de manière visuelle et simple, j'ai utilisé le fonctionnement des "Behavior Trees" de Unreal. Normalement utilisé pour les intelligences artificielles, les "Behaviors Trees" permettent d'effectuer des tâches une après l'autre selon une hiérarchie précise de manière visuelle comme démontrée dans l'image ci-dessous.

![Image d'un arbre de dialogue](/img/cirquewebb_dialogueTree.PNG)

J'ai donc créé un total de 23 tâches afin de faire fonctionner notre jeu. Voici les plus importantes d'entre eux:
![Image environnement](/img/cirquewebb_dialogue_task.png)

- Speak task

Cette tâche permet simplement d'afficher du texte à l'écran, on peut également faire jouer une animation au personnage avec qui on discute et afficher son nom au besoin.
![Image speak task](/img/cirquewebb_dialogue_speaktask.png)

- Reply task

Cette tâche permet de poser une question au joueur et de lui afficher des choix de réponse. Grâce au champ "GI Variable Name", on peut sauvegarder la réponse dans une "map" du "Game Instance" ce qui va nous permettre de modifier certains éléments du jeu dépendamment des choix effectués par le joueur. Dans le cas de la photo suivante, la réponse à la question "Ça te va?" n'est pas sauvegardé mais plutôt directement utilisé pour la suite du dialogue. On peut voir qu'il y a ensuite un "Selector" qui nous permet de faire un branchement dans le dialogue suite à la réponse choisie.
![Image reply task](/img/cirquewebb_dialogue_replytask.png)

- Input task

La tâche "input" permet comme son nom le dit de recevoir une réponse du joueur. Lorsque cette tâche est exécutée, un clavier virtuel va apparaitre à l'écran afin de recevoir la réponse du joueur. On décide ici également de sauvegarder la réponse dans la variable $Nom du "Game Instance".
![Image input task](/img/cirquewebb_dialogue_inputtask.png)

- Selection task

Cette tâche permet d'effectuer un choix de réponse à nouveau mais cette fois si avec des images. Les éléments affichés sont obtenus à l'aide d'une "Data table".
![Image selection task](/img/cirquewebb_dialogue_selectiontask.png)
![Image data table](/img/cirquewebb_dialogue_datatable.png)

- Update Environment task

Puisqu'il y a plusieurs éléments qui changent dans l'environnement tout dépendant des choix effectués dans certain dialogue, cette tâche permet d'enclencher ce changement.
![Image update env task](/img/cirquewebb_dialogue_updateEnv.png)

- ChangeDialogTree task

Afin de pouvoir avoir différents dialogues pour le même NPC, cette tâche permet de modifier l'arbre qui va être utilisé la prochaine fois que le joueur interagi avec ce NPC. On va alors également mettre à jour une "Data table" possédant tous les dialogues actuels de tous les NPCs.
![Image change dialog task](/img/cirquewebb_dialogue_changetree.png)

- Exit task

Finalement, cette tâche permet tout simplement de terminer le dialogue et retourner le contrôle au joueur.
![Image exit task](/img/cirquewebb_dialogue_exit.png)

Voici ainsi un exemple de dialogue lorsqu'on utilise toutes ces tâches:
{{< youtube UY6WIkDE-PE >}}

#### Dialogue simple

Il y a également des dialogues simples qui permettent d'afficher ce qu'un NPC dit sans avoir à intéragir avec ce dernier. La boîte de dialogue va donc apparaitre automatiquement lorsque le joueur est proche et va disparaitre lorsqu'on s'éloigne.

![Video dialogue simple](/img/cirquewebb_dialogueSimple.webp)

### Changement dans l'environnement

Pendant le jeu, le joueur va être mené à faire des choix dans les différents dialogues. Certains de ces choix vont ainsi être représentés dans l'environnement comme ci-dessous.
![Image environnement](/img/cirquewebb_affiche.png)

### Lancer de balle

Le joueur peut à tout moment lancer des balles partout où il désire. Cela peut être utile pour détruire certaines boîtes cachées dans l'environnement comme ci-dessous. Il y a trois types de balles différents dans le jeu, la balle normale, la balle de métal et la balle dorée! Ces balles permettent de débloquer le prochain niveau et de finalement terminer le jeu.

![Video shooting ball](/img/cirquewebb_shoot.webp)


### Stands de tir

Afin de passer au prochain niveau, le joueur doit compléter les 3 stands de tir qui lui sont disponibles. La vidéo suivante démontre le "Gameplay" classique d'un stand de tir.
{{< youtube YLPek4A8sHQ >}}


### NPC

Il y a des dizaines de NPCs partout dans le jeu, certains sont "interactable" et permettent de déclencher un dialogue, d'autres ne font que se promener selon un chemin défini sur la "navmesh".

![Video npc walk](/img/cirquewebb_npcwalk.webp)


### Sauvegarde

Une classe héritant de "USaveGame" a été créée afin de sauvegarder notre game state. Ainsi, toutes les informations par rapport aux dialogues, la position du joueur, le nombre d'étampes/tokens et l'état des stands de tir sont sauvegardés.

# Programmation

Tout ce projet a été programmé en c++ avec une utilisation faible de Blueprints pour certains éléments de base. Un total de 88 classes et 14185 lignes de code ont été écrite pour ce jeu!

# Lien

[Page ITCH.IO du jeu](https://uqac.itch.io/le-cirque-webb)

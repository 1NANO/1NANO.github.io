---
title: "Le Cirque Webb"
date: 2021-12-13T09:28:14-05:00
draft: false
cover:
    image: img/cirquewebb_banner.jpg
tags: ["Unreal", "C++"]
---

# Presentation

Le Cirque Webb is a linear exploration video game filled with shooting mini-games. The player plays Mousse the fly who visits the spider circus. He will have to advance through the levels by collecting stamps to reach the magnificent Ferris wheel. To this end, the player will have to use the ball in his possession to win at shooting ranges, explore to find hidden tokens or sell his personal information.

This game was created as part of a course at UQAC over a period of 4 months with the help of 2 other programmers and 15 artists. I mainly took care of the dialogue system as well as the progression of the "Game State". So I did a lot of UI and gameplay programming in this project.

{{< youtube LBgsKHtbXMQ >}}

# Mechanics

### Dialogue system

#### Smart dialogue

Le Cirque Webb has a complex dialogue system allowing the design of smart dialogue trees. It therefore allows you to make conditional branching, launch gameplay elements, receive input from the player and much more. In order to be able to do all this in a visual and simple way, I used Unreal's "Behavior Trees". Normally used for artificial intelligence, “Behavior Trees” allow tasks to be performed one after the other according to a precise hierarchy in a visual manner as demonstrated in the image below.

![Dialogue Tree picture](/img/cirquewebb_dialogueTree.PNG)

So I created a total of 23 tasks in order to make our game work. Here are the most important of them:
![Image environnement](/img/cirquewebb_dialogue_task.png)

- Speak task

This task simply allows you to display text on the screen, you can also play an animation for the character you are chatting with and display their name if necessary.
![Image speak task](/img/cirquewebb_dialogue_speaktask.png)

- Reply task

This task allows you to ask the player a question and display multiple answer choices. Thanks to the "GI Variable Name" field, we can save the response in a "map" of the "Game Instance" which will allow us to modify certain elements of the game depending on the choices made by the player. In the case of the following picture, the answer to the question "Does it suit you?" is not saved but rather directly used for the rest of the dialogue. We can see that there is then a "Selector" which allows us to make a branch in the dialogue following the chosen response.
![Image reply task](/img/cirquewebb_dialogue_replytask.png)

- Input task

The "input" task allows, as its name suggests, to receive a response from the player. When this task is executed, a virtual keyboard will appear on the screen to receive the player's input. We also decide here to save the response in the variable $Nom of the “Game Instance”.
![Image input task](/img/cirquewebb_dialogue_inputtask.png)

- Selection task

This task allows you to make a multiple answer choices again but this time with images. The displayed elements are obtained using a "Data table".
![Image selection task](/img/cirquewebb_dialogue_selectiontask.png)
![Image data table](/img/cirquewebb_dialogue_datatable.png)

- Update Environment task

Since there are several elements that change in the environment depending on the choices made in a certain dialogue, this task allows you to initiate this change.
![Image update env task](/img/cirquewebb_dialogue_updateEnv.png)

- ChangeDialogTree task

In order to be able to have different dialogues for the same NPC, this task allows you to modify the tree that will be used the next time the player interacts with this NPC. We will then also update a "Data table" containing all the current dialogues of all the NPCs.
![Image change dialog task](/img/cirquewebb_dialogue_changetree.png)

- Exit task

Finally, this task simply allows you to end the dialogue and return control to the player.
![Image exit task](/img/cirquewebb_dialogue_exit.png)

Here is an example of dialogue when using all these tasks:
{{< youtube UY6WIkDE-PE >}}

#### Simple dialogue

There are also simple dialogues that allow you to display what an NPC says without having to interact with the latter. The dialog box will therefore appear automatically when the player is close and will disappear when the player moves away.

![Video dialogue simple](/img/cirquewebb_dialogueSimple.webp)

### Change in environment

During the game, the player will be required to make choices in the different dialogues. Some of these choices will thus be represented in the environment as below.
![Image environnement](/img/cirquewebb_affiche.png)


### Ball throw

The player can throw balls wherever he wants at any time. This can be useful for destroying some hidden boxes in the environment like below. There are three different types of balls in the game, normal ball, metal ball and golden ball! These balls allow you to unlock the next level and finally complete the game.

![Video shooting ball](/img/cirquewebb_shoot.webp)


### Shooting ranges

In order to advance to the next level, the player must complete the 3 shooting ranges available to him. The following video demonstrates the classic “Gameplay” of a shooting range.
{{< youtube YLPek4A8sHQ >}}


### NPC

There are dozens of NPCs throughout the game, some are interactable and allow you to trigger a dialogue, others just walk along a defined path on the "navmesh".

![Video npc walk](/img/cirquewebb_npcwalk.webp)


### Save

A class inheriting from "USaveGame" was created to save our game state. Thus, all information regarding dialogues, the player's position, the number of stamps/tokens and the state of the shooting ranges are saved.

# Programming

This entire project was programmed in C++ with little use of Blueprints for certain basic elements. A total of 88 classes and 14185 lines of code have been written for this game!

# Link

[ITCH.IO game page](https://uqac.itch.io/le-cirque-webb)

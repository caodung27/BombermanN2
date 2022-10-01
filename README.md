# BOMBERMAN GAME - PROJECT OOP N2

<!-- TABLE OF CONTENTS -->
# Table of contents :round_pushpin:
1. [Introduction](#Introduction)
2. [Game](#Game)
3. [UML-class-diagram](#UML-class-diagram)
4. [Features](#Features)
5. [Challenges](#Challenges)
6. [Acknowledgments](#Acknowledgments)
7. [References](#References)
<!-- <details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#Introduction">Introduction</a>
      <ul>
        <li><a href="#Team-members">Team Members</a></li>
	<li><a href="#installation">Installation</a></li>
	<li><a href="#motivation">Motivation</a></li>
	<li><a href="#task-allocation">Task Allocation</a></li>      
      </ul>
    </li>
    <li><a href="#technologies">Technologies</a></li>
    <li><a href="#uml-class-diagram">UML Class Diagram</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#challenges">Challenges</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
    <li><a href="#references">References</a></li>
  </ol>
</details> -->

<!-- ABOUT THE PROJECT -->

## Introduction <a name="Introduction"></a> :bricks:

<div align="center">
<img src="screenshots/Intro.gif" alt="">
</div>

<div style="text-align:justify">
This is our game project for our final lab in our Object-Oriented Programming course in semester 1 (2022 - 2023). Bomberman is an individual game that does not require players have excellent skills or advanced technology. It's a straightforward game that may be enjoyed by people of all ages. As a result of all of these factors, we developed a program that is user-friendly and assists users in having the greatest possible experiences. So, what are we waiting for? Let the story begin!
</div>

### Team Members :couplekiss_man_man:

| Order |         Name          |     ID      |            Email            |                       Github account                                                     |
| :---: | :-------------------: | :---------: | :-------------------------: | :---------------------------------------------------------: |
|   1   | Cao Xuan Dung(Leader) | 21020290    |   21020290@vnu.edu.vn       |          [cxddcx271](https://github.com/cxddcx271)          | 
|   2   | Tran Viet Dung(Base)  | 21020009    |   21020009@vnu.edu.vn       |          [SamoySamoy](https://github.com/SamoySamoy)        |
|   3   | Cong Nghia Hieu(Base) | 21020540    |   21020540@vnu.edu.vn       |          [congnghiahieu](https://github.com/congnghiahieu)  |      
### Installation :dart: 

1. Open the terminal on your IDE
2. Clone the repo
   ```sh
   git clone https://github.com/caodung27/BombermanN2
   ```
3. Check the file status
   ```sh
   git status
   ```
4. Change branch
   ```js
   git checkout 'branch_name'
   ```

### Motivation :mechanical_arm:

<div style="text-align:justify">
As a fresher developer, we assume that the Bomberman game is one of the most simple game which helps us in practicing coding with OOP also some significant aspects of the front-end such as: How to render the game? , How frame working in UX/UI? , ….
</div>

### Task Allocation :ok_man:

| Order | Task                                    |  Person   | Contribution |
| :---- | :-------------------------------------- | :-------: | :----------: |
| 1     | UI, Graphic, A* algorithm, Readme       |  Cao Dung |      34%     |
| 2     | Move, Enemy, Bomberman, Item            | Tran Dung |      33%     |
| 3     | Move, Enemy, Bomberman, Item            | Cong Hieu |      33%     |


<!-- Game -->
<br />

## Game <a name="Game"></a>:joystick:
### Technologies :globe_with_meridians:

- Language: [JAVA](https://www.java.com/en/)
- Framework: [IntelliJ](https://www.jetbrains.com/idea/), [Visual Studio Code](https://code.visualstudio.com)
- Intelligent: [A\* algorithms](https://www.geeksforgeeks.org/a-search-algorithm/)
- Library: [JavaFx](https://openjfx.io), [FXGL](https://github.com/AlmasB/FXGL)

## Description

- ![](readme/player.png) *Bomber* is the main character of the game. Bomber can move in 4 directions left / right / up / down according to the control of the player. 

- ![](readme/bomb.png) *Bomb* is the object that Bomber will place. Once placed, Bomber cannot move into Bomb position. However, as soon as the Bomber has placed and activated the Bomb at his position, the Bomber can once go from the location where the Bomb is placed to the next position. After activating for 2.5s, Bomb will explode by itself.

- ![](readme/wall.png) *Wall* is a fixed object, cannot be destroyed by Bomb and cannot be placed on Bomb, Bomber cannot move on this object

- ![](readme/brick.png) *Brick* is an object that does not allow Bomb to be placed but can be destroyed by Bombs placed nearby. Bomber cannot move into Brick until it is destroyed.

- ![](readme/portal.png) *Portal* is the object hidden behind a Brick object. When that Brick is destroyed, the Portal will appear and if all Enemys have been destroyed the player can move to another Level by moving into the Portal's location.

*Item* is also hidden behind the Brick and only shows up when the Brick is destroyed. Bomber can use Item by moving into Item's position. Information about the function of the Item is listed as follows:
- ![](readme/powerup_speed.png) *SpeedItem* This item will increase Bomber's movement speed.

- ![](readme/powerup_bombs.png) *BombItem* This item increases the number of Bombs that can be placed by one.

- ![](readme/powerup_flamepass.png) *FlamePassItem* When using this Item Bomber will be equipped with Gold armor and can pass through Flame without damage.

- ![](readme/powerup_flames.png) *FlameItem* This item increases the Bomb's range when it explodes.

- ![](readme/powerup_life.png) *LifeItem* When using this Item Bomber will gain 1 more life.

*Enemy* are the objects that the Bomber must destroy in order to pass the Level. Enemy can move randomly or chase Bomber on its own depending on the type of Enemy. Types of Enemy will be described in detail below:

- ![](readme/ballom.png) *Ballom* is the simplest Enemy, moving randomly at a slow speed.

- ![](readme/oneal.png) *Oneal* knows how to chase Bomber when approaching, has increased movement speed while chasing Bomber.

- ![](readme/pass.png) *Pass* moves randomly at pretty fast speed. When destroyed will spawn 2 more *Ballom*.

- ![](readme/dahl.png) *Dahl* has variable movement speed, sometimes fast, sometimes slow.

- ![](readme/doria.png) *Doria* knows how to chase Bomber when close but has a wider range than Oneal, has increased movement speed and can move through Brick while chasing Bomber.


## UML Class Diagram<a name="UML-class-diagram"></a>:clipboard:

<br/>
src/main/java/Bomberman
<br/>
├── Conllisions
<br/>
│   ├── FlameEnemy3Handler
<br/>
├── Components
<br/>
│   ├── Enemy
<br/>
│   │   ├── Enemy
<br/>
│   │   ├── Enemy1
<br/>
│   │   ├── Enemy2
<br/>
│   │   ├── Enemy3
<br/>
│   │   ├── Enemy4
<br/>
│   │   ├── Enemy5
<br/>
│   ├── BombComponent
<br/>
│   ├── BrickBreakComponent
<br/>
│   ├── FlameComponent
<br/>
│   └── PlayerComponent
<br/>
├── Constants
<br/>
│   └── Constant
<br/>
├── DynamicEntityState
<br/>
│   └── State
<br/>
├── Menu
<br/>
│   ├── GameMenu
<br/>
│   ├── MainMenu
<br/>
│   └── MenuButton
<br/>
├── Sounds
<br/>
│   └── SoundEffect
<br/>
├── UI
<br/>
│   ├── EndingScene
<br/>
│   ├── StageStartScene
<br/>
│   └── UIComponents
├── GameApp
<br/>
├── GameFactory
<br/>
└── GameType

<br/>


<!-- FEATURES -->
## Features<a name="Features"> :triangular_flag_on_post:
- Completed: UX/UI, sound of game, enhancing algorithms
- Incompleted: Minvo, 2 players, multiple characters for choosing, …
<br />

<!-- CHALLENGES -->
## Challenges<a name="Challenges">:bangbang:

- Task allocation for each team member
- Using platform for communication ([Trello](https://trello.com/b/Ac0ISkzt/bomber-game-oop-project-2022))
- Working environment (Github)
<br />
	
## Acknowledgments<a name="Acknowledgments">:brain:
<div style="text-align:justify">
We would want to express our gratitude to Tom for providing us with the chance to
participate in this project and apply what we learned in theory into practice. This project's
learning curve was steep, but it was well worth it for all of us. We have learned more about interface technologies to construct a functioning application
that interacts with our project. Tom, we want to thank you again for all the hard work and expertise that you have
put into your teaching. We'll make sure that all we've learned doesn't go to waste, and that
we can master them better from now on :heart:
</div>

<br />

## References<a name="References">  :eye::tongue::eye:
1. [bqcuong](https://github.com/bqcuong/bomberman-starter)
2. [minhnq410](https://github.com/minhnq410/Bomberman_Assignment_2/tree/master/src/uet/oop/bomberman)
3. [JavaFx Tutorial](https://openjfx.io/openjfx-docs/)
4. [A* Intelligent](https://www.simplilearn.com/tutorials/artificial-intelligence-tutorial/a-star-algorithm#:~:text=PythonExplore%20Course-,What%20is%20an%20A*%20Algorithm%3F,shortest%20path%20to%20be%20taken.)

<br />

<p align="right">(<a href="#top">Back to top</a>)</p>



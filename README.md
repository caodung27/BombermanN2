# BOMBERMAN GAME - BÀI TẬP LỚN OOP 

</div>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Nhathuy1305/OOP_BOMBERMAN_GAME.git">
    <img src="res/images/ttsalpha4.0@0.5x.png" alt="Logo" width="200" height="200">
  </a>

  <h3 align="center">OOP BOMBERMAN PROJECT</h3>
  <h4 align="center">Team Name: N2</h4>
</div>

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
|   1   |     Cao Xuan Dung     | 21020290    |   21020290@vnu.edu.vn       |          [cxddcx271](https://github.com/cxddcx271)          | 
|   2   |     Tran Viet Dung    | 21020009    |   21020009@vnu.edu.vn       |          [SamoySamoy](https://github.com/SamoySamoy)        |
|   3   |     Cong Nghia Hieu   | 21020540    |   21020540@vnu.edu.vn       |          [congnghiahieu](https://github.com/congnghiahieu)  |      
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

## Mô tả về các đối tượng trong trò chơi

- ![](readme/player.png) *Bomber* là nhân vật chính của trò chơi. Bomber có thể di chuyển theo 4 hướng trái/phải/lên/xuống theo sự điều khiển của người chơi. 

- ![](readme/bomb.png) *Bomb* là đối tượng mà Bomber sẽ đặt. Khi đã được đặt, Bomber không thể di chuyển vào vị trí Bomb. Tuy nhiên ngay khi Bomber vừa đặt và kích hoạt Bomb tại ví trí của mình, Bomber có một lần được đi từ vị trí đặt Bomb ra vị trí bên cạnh. Sau khi kích hoạt 2.5s, Bomb sẽ tự nổ.

- ![](readme/wall.png) *Wall* là đối tượng cố định, không thể phá hủy bằng Bomb cũng như không thể đặt Bomb lên được, Bomber không thể di chuyển vào đối tượng này

- ![](readme/brick.png) *Brick* là đối tượng không cho phép đặt Bomb lên nhưng có thể bị phá hủy bởi Bomb được đặt gần đó. Bomber không thể di chuyển vào vị trí Brick khi nó chưa bị phá hủy.

- ![](readme/portal.png) *Portal* là đối tượng được giấu phía sau một đối tượng Brick. Khi Brick đó bị phá hủy, Portal sẽ hiện ra và nếu tất cả Enemy đã bị tiêu diệt thì người chơi có thể qua Level khác bằng cách di chuyển vào vị trí của Portal.

*Item* cũng được giấu phía sau Brick và chỉ hiện ra khi Brick bị phá hủy. Bomber có thể sử dụng Item bằng cách di chuyển vào vị trí của Item. Thông tin về chức năng của các Item được liệt kê như sau:

- ![](readme/powerup_speed.png) *SpeedItem* Item này sẽ giúp Bomber được tăng tốc độ di chuyển.

- ![](readme/powerup_bombs.png) *BombItem* Item này giúp tăng số lượng Bomb có thể đặt thêm một.

- ![](readme/powerup_flamepass.png) *FlamePassItem* Khi sử dụng Item này Bomber sẽ được mặc giáp Vàng và có thể đi qua Flame mà không bị sao.

- ![](readme/powerup_flames.png) *FlameItem* Item này giúp tăng phạm vi ảnh hưởng của Bomb khi nổ.

- ![](readme/powerup_life.png) *LifeItem* Khi sử dụng Item này Bomber sẽ được tăng thêm 1 mạng nữa.

*Enemy* là các đối tượng mà Bomber phải tiêu diệt hết để có thể qua Level. Enemy có thể di chuyển ngẫu nhiên hoặc tự đuổi theo Bomber tùy theo loại Enemy. Các loại Enemy sẽ được mô tả cụ thể sau đây:

- ![](readme/ballom.png) *Ballom* là Enemy đơn giản nhất, di chuyển ngẫu nhiên với tốc độ chậm.

- ![](readme/oneal.png) *Oneal* biết đuổi Bomber khi lại gần, có tốc độ di chuyển tăng trong khi đuổi Bomber.

- ![](readme/pass.png) *Pass* di chuyển ngẫu nhiên với tốc độ khá nhanh. Khi bị tiêu diệt sẽ sinh ra thêm 2 *Ballom*.

- ![](readme/dahl.png) *Dahl* có tốc độ di chuyển thay đổi, lúc nhanh, lúc chậm.

- ![](readme/doria.png) *Doria* biết đuổi Bomber khi lại gần nhưng phạm vi rộng hơn Oneal, có tốc độ di chuyển tăng và có thể di chuyển xuyên Brick trong khi đuổi Bomber .

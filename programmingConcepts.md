1. Shape
 - The main character, Moon, is made by 2 arc.
 - The walls are made by round rectangle. And there is one more rect that has different color in big rect.
 - monsters have round body and 2 red horn.
 - The boss monster is not that different with normal monsters. But It has hands, feet, and body.
 - Portal is made by 2 ellipse. Like walls, there is ellpise that has different color in big ellipse.
 
 
2.Colors
 - The main character, Moons yellow. And Its outline is yellow too.
 - Wall: Big rect is LightSteelBlue. Small rect's rgb is (0,255,255).
 - Monsters: Body is PowderBlue. Their horns are red.
 - Boss: It is same with Monsters.
 - Portal: Big ellpise is DodgerBlue. Samll ellipse's rgb is (0,191,255).
 
 
3.Variables
-AttackChane: When player get A.C item, AttackChances increase by 1.
-Strength: It is used when player is on BOSS_STAGE. If player get item then strength increase
-And there is no specail variables.


4.Conditional Statements
- Scenevariables:
 : MAIN_MENU = 1;
 : How_to_play = 2;
 : CREDIT = 3;
 : STAGE1 = 4;
 : STAGE2 = 5;
 : STAGE3 = 6;
 : Pre_BOSS = 7
 : BOSS_STAGE = 8;
 : CLEAR = 9;
 : GAMEOVER = 10;
 
 
5.Loops
- loops are used When I make my world like this:

function createWorld(rows, columns) {
  let collection = []
  for (let i = 0; i < rows; ++i)
    collection.push(new Array(columns));
  return collection;
  
  
6.Functions
- Example:

function keyPressed() {
  if (currentScene>=3) {
     PLAY_GAME:
      GameScene.OnKeyPressed();
  }
}

function mousePressed()
{
  push();
  strokeWeight(7); stroke('yellow');
  fill(200,200,100,100);
  circle(mouseX, mouseY,60)
  pop();
}


7.Classes
- CreditScene,How_to_play, Main_menu, Monsters,Moon,Wall,Boss,Portal,Item and GameScene are made by class.
  then I can be able to distinguish and recognize these things easily.

8.Arrays
- Items are in one Array. So I can make Item_drop randomly.

1. Shape
 - The main character, Moon, is made by 2 arc.

push(); fill('yellow');
    stroke(250,250,this.outline,70);
    strokeWeight(8);
  arc(x,y,50,40,PI/2,3*PI/2);
  pop();
    
    
  push();
  fill(40);stroke(250,250,this.outline,70);
    strokeWeight(8);
  arc(x,y,17.5,40,PI/2,3*PI/2);
  pop();
    
    
  circle(x-13,y,7);circle(x-21,y,7);
  push(); fill(0);
  circle(x-13,y,3.5); circle(x-21,y,3.5);
  pop();
    
  push(); noFill()
  arc(x-14,y+10,7.5,5,0,PI);
  pop();

 - The walls are made by round rectangle. And there is one more rect that has different color in big rect.

push();
  rectMode(CENTER)
  fill(210,210,210); stroke('LightSteelBlue');
  rect(x,y,50,50,6);
  push(); noStroke();
  fill(0,255,255,20)
  rect(x,y,40,40,6);
  pop();


 - monsters have round body and 2 red horn.

push();
  push(); fill('PowderBlue');
  circle(x,y,40);
    pop();
  
  push();
  beginShape();fill('red');
  vertex(x-26,y)
  vertex(x-33,y-27)
  vertex(x-28,y-55)
  vertex(x-23,y-34)
  vertex(x-11,y-25)
  endShape(CLOSE); pop();
  
  push();
  beginShape();fill('red');
  vertex(x+26,y)
  vertex(x+33,y-27)
  vertex(x+28,y-55)
  vertex(x+23,y-38)
  vertex(x+11,y-25)
  endShape(CLOSE);pop();
  
  push(); fill(220,220,100);
  beginShape();
  vertex(x-15,y-8);
  vertex(x-7,y+3);
  vertex(x-3,y);
  endShape(CLOSE);
  pop();
  
  push();
  beginShape();fill(220,220,100);
  vertex(x+15,y-8);
  vertex(x+7,y+3);
  vertex(x+3,y);
  endShape(CLOSE);
  pop();
    pop();

 - The boss monster is not that different with normal monsters. But It has hands, feet, and body.

push();
    textSize(40); textAlign(CENTER,CENTER)
    text("Boss",width/2, height/4)
    pop();
    push();
    this.MOON.draw(mouseX+10,mouseY);
    pop();
    
    push(); fill(255,0,0,90); noStroke();
  ellipse(6*width/7, height/2 + 40*sin(millis()/500), 180,350);
  pop();
  
  push(); fill('PowderBlue');
  
  ellipse(6*width/7, height/2 + 40*sin(millis()/500),
          80 + 10*sin(millis()/500),170);
  
  ellipse(6*width/7- 30,height/2 + 90 + 40*sin(millis()/500), 30,20);
  ellipse(6*width/7+ 30,height/2 + 90 + 40*sin(millis()/500), 30,20);
  
  circle(6*width/7- 30,height/2 - 15 + 40*sin(millis()/500), 20);
  circle(6*width/7+ 30,height/2 - 15 + 40*sin(millis()/500), 20);
  
  circle(6*width/7, height/2- 90 + 40*sin(millis()/500), 50);
  
  push();
  beginShape();fill('red');
  vertex(6*width/7-26,height/2 - 90 + 40*sin(millis()/500) )
  vertex(6*width/7-33,height/2 - 90 + 40*sin(millis()/500) -27)
  vertex(6*width/7-28,height/2 - 90 + 40*sin(millis()/500) -55)
  vertex(6*width/7-23,height/2 - 90 + 40*sin(millis()/500) -34)
  vertex(6*width/7-11,height/2 - 90 + 40*sin(millis()/500) -25)
  endShape(CLOSE); pop();
  
  push();
  beginShape();fill('red');
  vertex(6*width/7+26,height/2 - 90 + 40*sin(millis()/500) )
  vertex(6*width/7+33,height/2 - 90 + 40*sin(millis()/500) -27)
  vertex(6*width/7+28,height/2 - 90 + 40*sin(millis()/500) -55)
  vertex(6*width/7+23,height/2 - 90 + 40*sin(millis()/500) -38)
  vertex(6*width/7+11,height/2 - 90 + 40*sin(millis()/500) -25)
  endShape(CLOSE);pop();
  
  push(); fill(220,220,100);
  beginShape();
  vertex(6*width/7-15,height/2 - 90 + 40*sin(millis()/500) -8);
  vertex(6*width/7-7,height/2 - 90 + 40*sin(millis()/500) +3);
  vertex(6*width/7-3,height/2 - 90 + 40*sin(millis()/500) );
  endShape(CLOSE);
  pop();
  
  push();
  beginShape();fill(220,220,100);
  vertex(6*width/7+15,height/2 - 90 + 40*sin(millis()/500) -8);
  vertex(6*width/7+7,height/2 - 90 + 40*sin(millis()/500) +3);
  vertex(6*width/7+3,height/2 - 90 + 40*sin(millis()/500) );
  endShape(CLOSE);
  pop();
  
  pop();

 - Portal is made by 2 ellipse. Like walls, there is ellpise that has different color in big ellipse.

    push(); fill('DodgerBlue');
    noStroke();
    ellipse(x,y,25,40);
    fill(0,191,255,40);
    ellipse(x,y,15,24);
    pop();
 
 
2.Colors
 - The main character, Moons yellow. And Its outline is yellow too.
 - Wall: Big rect is LightSteelBlue. Small rect's rgb is (0,255,255).
 - Monsters: Body is PowderBlue. Their horns are red.
 - Boss: It is same with Monsters.
 - Portal: Big ellpise is DodgerBlue. Samll ellipse's rgb is (0,191,255).
 
 
3.Variables
-AttackChane: When player get A.C item, AttackChances increase by 1.

let TILE = this.world[moveRow][moveColumn];
    if (TILE == Item1) {
      this.attackChance = this.attackChance +1
      this.world[moveRow][moveColumn] = FLOOR;
      console.log("Your attack chance is " + this.attackChance)

-Strength: It is used when player is on BOSS_STAGE. If player get item then strength increase

else if (TILE == Item2) {
      strength = strength+ 0.01
      this.world[moveRow][moveColumn] = FLOOR;
      console.log("Your strength is " + strength)
      
    } else if (TILE == Item3) {
      strength = strength+ 0.03
      this.world[moveRow][moveColumn] = FLOOR;
      console.log("Your strength is " + strength)
      
    }

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
  I created Item1, Item2, Item3 classes. And I did it like this.   

  let Items = [Item1, Item2, Item3]

else if (randomInt(20) == 0) {
          this.world[row][column] = random(Items);
        }

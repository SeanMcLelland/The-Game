The-Game
========

King Mulac!!



float x = 190;
float xt;
float yt, oldY;

float y = 270;
void setup() {
  size(400, 300);
}



void draw() {
  background(0, 0, 100);
  rect(x, y, 20, 20); // player

  pushMatrix();
  translate(xt, yt);
  rect(40, 260, 40, 40); //box
  rect(0, 290, width, 10); // platform
  ellipse(20, 70, 40, 20);
  ellipse(60, 60, 40, 20);
  ellipse(140, 10, 40, 20);
  ellipse(170, 60, 40, 20);
  ellipse(200, 20, 40, 20);
  ellipse(220, 20, 40, 20);
  ellipse(270, 90, 40, 20);
  ellipse(300, 40, 40, 20);
  ellipse(378, 70, 40, 20);
  ellipse(468, 50, 40, 20);
  ellipse(512, 40, 40, 20);
  popMatrix();


  if (keyPressed && (key == CODED)) {
    if (keyCode == LEFT && x > 104) {
      x--; 
      x--;
    } 
    else if (keyCode == RIGHT && x < 296) {
      x++;
      x++;
    }

    if (x < 105) {
      xt++;  
      xt++;
    }

    if (x > 295) {
      xt--; 
      xt--;
    }





    if (mousePressed) {
      jump=1;

      y--;  
      y--;  
      y--;
      if (jump==1) {
        y=oldY;
      }
    }
  }
}

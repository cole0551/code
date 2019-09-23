# code
float ballspeedx=7;
float ballspeedy=15;
float ballx = height/2;
float bally= width/2;

void setup() {

size(1000, 1000);
background(255, 255, 0);
}// end setup

void draw() {
background(255, 255, 0);
starts();
checkposition();
paddle();

ballx=ballx+ballspeedx; // moves the ball side to side
bally=bally+ballspeedy; // moves the ball up and down
}
void checkposition(){
  
  if (ballx > width){
    ballspeedx=ballspeedx * -1;
 }
 if (bally > height){
   ballspeedy=ballspeedy * -1;
 }
 if (bally < 0){
   ballspeedy=ballspeedy * -1;
 }
 
}
 void paddle(){
 rect(width/2,height/2,200,20);  
  
 }
 void starts(){
   fill(0, 0, 255);
rectMode(CENTER);
rect(width/2, height/2, width -50, height-50);
fill(255, 0, 0);
ellipse(ballx, bally, 40, 40); fill(0, 0, 255);}

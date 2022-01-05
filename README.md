[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-f059dc9a6f8d3a56e377f745f24479a46679e63a5d9fe6f495e02850cd0d8118.svg)](https://classroom.github.com/online_ide?assignment_repo_id=6638591&assignment_repo_type=AssignmentRepo)
# Processing Task 4 - Animation

## Learning Objectives
In this task, you will learn about:
* declaring global variables to initialize state values for animation
* modifying the draw() function to animate objects
* variable scope
* resetting state
* bouncing
* clearing old frames


Be sure to check out the `Sketch.java` code in this repository to see the basic arrangement of state variables for your animation.



## Step 1 - Lesson
Acquire the learning objectives by reviewing [this tutorial](https://happycoding.io/tutorials/processing/animation)

## Step 2 - Task
Demonstrate your learning objectives by doing one of the following animation sketches:

### Level 2
Add a rectangle to the bouncing ball program. The ball should bounce off the rectangle as well as the edges of the window.

### Level 3
Remember your drawing program from previous homeworks? Animate it by either bouncing it around the screen or by changing it over time.

### Level 4
Create an animation that shows a full day- start out with a sunrise, show the sun moving across the sky, then sunset, and finally the moon and stars. Change your background accordingly based on the position of the sun.


## Submission
1. Commit and push your code to this repository
2. Submit a **screen recording** of your work and upload it to the Google Classroom assignment post.



import processing.core.PApplet;

public class Sketch extends PApplet {
 
  float circleY = 50;
  float petal1Y = 0;
  float petal2Y = 0;
  float petal3Y = 100;
  float petal4Y = 100;
  float ySpeed = 2;
	

  public void settings() {
	
    size(500, 500);
 
  }
   
  public void setup() {
    background(194, 236, 255);
  }

 
  public void draw() {

    stroke(255, 209, 233);
    fill(255, 209, 233);
    
    background(194, 236, 255);
    ellipse(200, petal1Y, 100, 100);
    petal1Y = petal1Y + ySpeed;
    if(petal1Y > height) {
      ySpeed = ySpeed * -1;
    }
    
    ellipse(300, petal2Y, 100, 100);
    petal2Y = petal2Y + ySpeed;
    if(petal2Y > height) {
      ySpeed = ySpeed * -1;
    }

    ellipse(200, petal3Y, 100, 100);
    petal3Y = petal3Y + ySpeed;
    if(petal3Y > height) {
      ySpeed = ySpeed * -1;
    }

    ellipse(300, petal4Y, 100, 100);
    petal4Y = petal4Y + ySpeed;
    if(petal4Y > height) {
      ySpeed = ySpeed * -1;
    }

    
    stroke(255, 242, 158);
    fill(2255, 242, 158);
    ellipse(250, circleY, 100, 100);
    circleY = circleY + ySpeed;
    if(circleY < 0 || circleY > height) {
      ySpeed = ySpeed * -1;
    }

  }

}

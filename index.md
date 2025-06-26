# Robotic Arm/Claw Machine
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Coby L | Sage Creek | Engineering Design | Incoming Junior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

# First Milestone


[![Watch on YouTube](https://img.youtube.com/vi/QUYMb4puTQo/0.jpg)](https://www.youtube.com/watch?v=QUYMb4puTQo)


- Key components of my robot include the servos, joysticks, and shield/nano. The servo allows motion at each joint, the joysticks send signals to control the servos, and the shield pairs the Arduino code from my PC to the robot.
- For my first milestone, I completed the construction aspect of the robot, as well as the testing of the servos, joysticks, and shield/nano.
- A challenge I faced was that the designated shield was not compatible with the servos because it was too weak. I had to improvise and use an alternative shield, which could not attach to the robot as shown in the instructions. I altered the original build to successfully incorporate the new shield, allowing the servos to function.
- For milestone 2, I plan on having a working, running code that will allow me to control my robot using the joysticks.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
#include "CokoinoArm.h"

CokoinoArm arm;
int xL, yL, xR, yR;

void turnUD() {
  if (abs(xL - 512) > 20) {
    if (xL < 256) {arm.up(5); return;}
    if (xL > 768) {arm.down(5); return;}
    if (xL >= 256 && xL < 480) {arm.up(10); return;)
    if (xL > 540 && xL <= 768) {arm.down(10); return;}
  }
}

void turnLR() {
  if (abs(yL - 512) > 20) {
    if (yL < 256) {arm.right(5); return;}
    if (yL > 768) {arm.left(5); return;}
    if (yL >= 256 && yL < 480) {arm.right(10); return;}
    if (yL > 540 && yL <- 768) {arm.left(10); return;}
  }
}

void turnCO() {
  if (abs(xR - 512) > 20) {
    if (xR < 256) {arm.close(0); return;}
    if (xR > 768) {arm.open(0); return;}
    if (xR >= 256 && xR < 480) {arm.close(5); return;}
    if (xR > 540 && xR <= 768) {arm.open(5); return;}
  }
}

void setup() {
  arm.ServoAttach(4, 5, 6, 7);
  arm.JoyStickAttach(A0, A1, A2, A3);
}

void loop() {
  xL = arm.JoystickL.read_x();
  yL = arm.JoystickL.read_y();
  xR = arm.JoystickR.read_x();
  yR = arm.JoystickL.read_y();

  turnUD():
  turnLR();
  turnCO();
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.

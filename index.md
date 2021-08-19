# Ball Tracking Robot
I designed, programmed, and built a robot that will follow a ball as it rolls on the ground. It uses computer vision techniques to identify the ball. 

| **My name:** | **My School:** | **My Areas of Interest:** | **Grade:** |
|:--:|:--:|:--:|:--:|
| Alexander Chan | Regis High School | Mechanical Engineering/Computer Science | Rising Senior

![IMG_2244](https://user-images.githubusercontent.com/86970028/129973569-bb70e678-0fca-4174-ad06-08004da96ff6.jpg)
     

# Final Milestone

Three weeks after the start of my project, I reached my final milestone. The robot is now able to detect and follow the ball as it rolls on the floor.

Since my second milestone, I have implemented a circle detecting algorithm that I programmed called Hough Circle Transform.  The algorithm first detects object edges, or places with a substantial color change. For each pixel considered to be an edge, circles of a set radius range are drawn. If there is a circular object in the camera's view, the circles that are drawn will all intersect at the center of the circular object. In this way, the ball can be detected. I've also programmed the robot to travel towards the ball when it is detected.

I then made several modifications to the robot to prepare it to move about reliably. I constructed stronger mounts for the camera and ultrasonic sensor, added a portable charger to power the Raspberry Pi without an outlet, and mounted my Raspberry Pi on top of my broadboard to save space. I included a peice of cardboard between the Raspberry Pi and the breadboard to ensure neither the electric circuits on my breadboard nor the Raspberry Pi could interfere with each other.

Although this was my final milestone with Bluestamp that completed my robot's ball tracking capabilities, I will continue with the project in the future. I hope to add a servo motor to allow the camera to tilt upwards and track balls as they are picked up and thrown. In addition to other modification ideas, I will be adding solar panels so that the robot's batteries do not need to be recharged as often. 


<iframe width="560" height="315" src="https://www.youtube.com/embed/_SUSWzWiC0I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>                                                                                                       
<br>

# Presentation

Here's a video of the live presentation I gave right before completing my final milestone.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ml36HLql7Oo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> 
<br>

# Second Milestone

My second milestone focused on proccessing the video frames to isolate the ball. Every pixel in the frame is represented as a combination of 3 numbers, each of them values for red, green, and blue(RGB). Combinations of reds, greens and blues will make up any possible color. To isolate the red ball that I use, I wanted to first isolate the red colors in each frame.

I converted the RGB system to a similar but different system called HSV, which stands for hue, saturation, and value. Just like with RGB, HSV will make up any possible color.  I used HSV because it allowed me greater freedom to optimize the range of colors that I wanted to isolate. Additionally, if I wanted to use a different ball and isolate a different color, I would only have to adjust the hue value, whereas if I had used RGB I would have to adjust all there values.

Next, I specified a range of red HSV colors to be allowed through a filter. Any other colors would be filtered out and appear as black. By doing this, the Raspberry Pi only needed to process the red objects in the camera's view rather than all of the objects in the camera's view. The robot would also be able to tell the difference between different colored balls.
  
After filtering each video frame for red colors, I noticed that there was a lot of noise, or distortions, that looked like static in each camera frame. To solve this problem, I used an image processing technique called erosion. By eliminating some of the area around the edges of objects, the small dots that flickered on the screen were completedly eroded away, while larger objects like the ball only appeared slightly smaller. I then dilated each frame to return objects to their normal size, leaving the video feed without any distortions.

<iframe width="560" height="315" src="https://www.youtube.com/embed/SNreoi3gCcM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>


# First Milestone
  
I started my project by assembling the chassis of the car and wiring the ultrasonic sensor. However, connecting the ultrasonic sensor to the Raspberry Pi was challenging because a direct wire from the ultrasonic sensor to the Raspberry Pi sends 5V back to the Raspberry Pi, but the Raspberry Pi only takes 3.3V. I solved the problem with a voltage divider, which I found very interesting because it used math I had worked with in my Physics class. Once properly wired, the ultrasonic sensor emits ultrasonic waves that bounce off objects. My code calculates the distance from objects by using the amount of time it takes for the waves to bounce back to the sensor and the speed of those waves. 

I then wired and programmed the 2 motors. To control the motors, I used an L298N motor driver that allows me to control the exact speed and direction of the motor by modulating pulses of electricity. Shorter pulses allow less power to reach the motors and longer pulses allow more power to reach the motor. A seperate battery pack powers my motors.

<iframe width="560" height="315" src="https://www.youtube.com/embed/zY5fDYwYBLY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

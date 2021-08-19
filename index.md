# Ball Tracking Robot 
I designed, programmed and built a robot that will identify, locate and follow a ball. My project uses a rasberry pi to process images from the camera in order to detect and locate balls. The robot has an ultrasonic sensor that measures distances to ensure the robot does not hit the ball or any other obstacles that might be in its way. 

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Alexander Chan | Regis High School | Mechanical Engineering/Computer Science Engineering | Rising Senior

![IMG_2244](https://user-images.githubusercontent.com/86970028/129973569-bb70e678-0fca-4174-ad06-08004da96ff6.jpg)
     

  
 
# Final Milestone

My final milestone implemented the circle detected algorithm that I programmed called Hough Circle Transform. To detect circles, object edges, or places with a substantial color change, are first detected. For each pixel considered to be an edge, a circles of a set radius range are drawn. If there is a circular object in the camera's view, the circles that are drawn will all intersect at the center of the circular object. In this way, the ball can be detected. Different colored balls can be detected using the color filter I had programmed. 

After completing the image processing needed to find red balls in the camera's view, I then compiled the seperate coding projects for the ultrasonic sensor, motor, and camera image processing into one project. I also made several modifications to the robot to prepare it to move about reliably. I constructed stronger mounts for the camera and ultrasonic sensor, added a portable charger to power the rasberry pi without an outlet, and mounted my rasberry pi on top of my broadboard to save space. I included a peice of cardboard between the rasberry pi and the breadboard to ensure neither the electric circuits on my breadboard nor the rasberry pi could interfere with each other.

<iframe width="560" height="315" src="https://www.youtube.com/embed/_SUSWzWiC0I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>                                                                                                                                                                                                                                                                                                  

# Final Presentation

Here's a video of the live presentation I gave.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ml36HLql7Oo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> 

# Second Milestone

My second milestone focused on proccessing the video frames to isolate the ball. I first filtered each frame from the camera for red colors because I use a red ball. Each pixel in the frame is represented as a combination of 3 numbers, each of them values for red, green, and blue(RGB). Combinations of reds, greens and blues will make up any possible color. I converted the RGB system to a similar but different system called HSV, which stands for hue, saturation, and value. Just like with RGB, HSV will make up any possible color. I then specified a range of HSV colors to be allowed through a filter. Any other colors would be filtered out and appear as black. I used HSV because it allowed me greater freedom to optimize the range of colors for the ball that I use. Additionally, if I wanted to switch my ball to a different color, all I would have to do is adjust teh hue value to filter for a different color, whereas if I had used RGB I would have to optimize and adjust all theree values. 
  
After filtering each video frame for red colors, I noticed that there was a lot of noise, or distortions that looked like static in each camera frame. tolve this problem, I used an image processing technique called erosion. By eliminating some of the area around the edges of objects, the small dots that flickered on the screen were completedly eroded away, while larger objects like the ball only appeared slightly smaller. I then dilated each frame to return objects to their normal size, leaving the video feed without any distortions. I also set and optimized camera settings for saturation, contrast, and brightness to accentuate colors in the video feed and help the computer filter out the best range of colors. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/SNreoi3gCcM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# First Milestone
  
For my first milestone, I assembled the chassis of the car, wired the ultrasonic sensor and the 4 motors, and wrote a baseline program to control the sensors and the motors. Connecting the ultrasonic sensor to the Raspberry Pi was challenging because a direct wire from the ultrasonic sensor to the Rasberry Pi sends 5V back to the Raspberry Pi, but the Raspberry Pi only takes 3.3V. I solved the problem with a voltage divider, which I found very interesting because it used math I had worked with in my Physics class. Once properly wired, the ultrasonic sensor emits ultrasonic waves that bounce off objects. My code calculates the distance from objects by using the amount of time it takes for the waves to bounce back to the sensor and the speed of those waves. To control the motors, I used an L298N motor driver that allows me to control the exact speed and direction of the motor by modulating pulses of electricity. Shorter pulses allow less power to reach the motors and longer pulses allow more power to reach the motor.

<iframe width="560" height="315" src="https://www.youtube.com/embed/zY5fDYwYBLY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

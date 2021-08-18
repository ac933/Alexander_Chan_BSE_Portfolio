# Ball Tracking Robot 
I designed, programmed and built a robot that will identify, locate and follow a ball. My project uses a rasberry pi, a small computer, to process images from the camera in order to detect and locate balls. The robot has an ultrasonic sensor that measures distances to ensure the robot does not hit the ball or any other obstacles that might be in its way. 
| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Alexander Chan | Regis High School | Mechanical Engineering/Computer Science Engineering | Incoming Senior

![IMG_2244](https://user-images.githubusercontent.com/86970028/129973569-bb70e678-0fca-4174-ad06-08004da96ff6.jpg)


  
 
# Final Milestone

My final milestone is the increased reliability and accuracy of my robot. I ameliorated the sagging and fixed the reliability of the finger. As discussed in my second milestone, the arm sags because of weight. I put in a block of wood at the base to hold up the upper arm; this has reverberating positive effects throughout the arm. I also realized that the forearm was getting disconnected from the elbow servo’s horn because of the weight stress on the joint. Now, I make sure to constantly tighten the screws at that joint. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/_SUSWzWiC0I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Final Presentation

Here's a video of the live presentation I gave.
  
<iframe width="560" height="315" src="https://www.youtube.com/embed/ml36HLql7Oo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> 

# Second Milestone

My second milestone focused on proccessing the video frames to isolate the ball. Because I use a red ball, I filtered the video to display only red colors. Then, I removed distortions from it. I also optimized camera settings to improve accuracy.

<iframe width="560" height="315" src="https://www.youtube.com/embed/SNreoi3gCcM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# First Milestone
  
For my first milestone, I assembled the chassis of the car, wired the ultrasonic sensor and the 4 motors, and wrote a baseline program to control the sensors and the motors. Connecting the ultrasonic sensor to the Raspberry Pi was a little challenging because a direct wire from the ultrasonic sensor to the Rasberry Pi sends 5V back to the Raspberry Pi, but the Raspberry Pi only takes 3.3V. The ultrasonic sensor emits ultrasonic waves that bounce off objects. My code calculates the distance from objects by using the amount of time it takes for the waves to bounce back to the sensor and the speed of those waves. To control the motors, I used an L298N motor driver that allows me to control the exact speed and direction of the motor by modulating pulses of electricity. Shorter pulses allow less power to reach the motors and longer pulses allow more power to reach the motor.

<iframe width="560" height="315" src="https://www.youtube.com/embed/zY5fDYwYBLY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

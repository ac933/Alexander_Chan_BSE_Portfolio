# Ball Tracking Robot 
Using a Raspberry Pi, an ultrasonic sensor, a camera, and motors, the robot detects, tracks, and follows a ball. It uses blah.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Alexander Chan | Regis High School | Electrical/Mechanical Engineering | Incoming Senior

![Headstone Image]![IMG_2244](https://user-images.githubusercontent.com/86970028/129963346-977ceb3f-8fe1-4264-bfc8-6393480dba99.jpg)

  
  
  
<iframe width="560" height="315" src="https://www.youtube.com/embed/ml36HLql7Oo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  
  
# Final Milestone
My final milestone is the increased reliability and accuracy of my robot. I ameliorated the sagging and fixed the reliability of the finger. As discussed in my second milestone, the arm sags because of weight. I put in a block of wood at the base to hold up the upper arm; this has reverberating positive effects throughout the arm. I also realized that the forearm was getting disconnected from the elbow servo’s horn because of the weight stress on the joint. Now, I make sure to constantly tighten the screws at that joint. 

[![Final Milestone](https://res.cloudinary.com/marcomontalbano/image/upload/v1612573869/video_to_markdown/images/youtube--F7M7imOVGug-c05b58ac6eb4c4700831b2b3070cd403.jpg )](https://www.youtube.com/watch?v=_SUSWzWiC0I "Final Milestone"){:target="_blank" rel="noopeneror"}

# Second Milestone
My second milestone focused on proccessing the video frames to isolate the ball. Because I use a red ball, I filtered the video to display only red colors. Then, I removed distortions from it. I also optimized camera settings to improve accuracy.

[![Third Milestone](https://user-images.githubusercontent.com/86970028/126401793-34afdde5-babf-4a68-b608-46b652aa0ae0.png)](https://www.youtube.com/watch?v=SNreoi3gCcM "Second Milestone")
# First Milestone
  
For my first milestone, I assembled the chassis of the car, wired the ultrasonic sensor and the 4 motors, and wrote a baseline program to control the sensors and the motors. Connecting the ultrasonic sensor to the Raspberry Pi was a little challenging because a direct wire from the ultrasonic sensor to the Rasberry Pi sends 5V back to the Raspberry Pi, but the Raspberry Pi only takes 3.3V. The ultrasonic sensor emits ultrasonic waves that bounce off objects. My code calculates the distance from objects by using the amount of time it takes for the waves to bounce back to the sensor and the speed of those waves. To control the motors, I used an L298N motor driver that allows me to control the exact speed and direction of the motor by modulating pulses of electricity. Shorter pulses allow less power to reach the motors and longer pulses allow more power to reach the motor.

[![First Milestone](https://user-images.githubusercontent.com/86970028/126401936-94c9b1cf-0935-4364-8f62-71c1e7594c53.png)](https://www.youtube.com/watch?v=zY5fDYwYBLY&t=1s "Second Milestone")

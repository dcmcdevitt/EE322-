# EE322

## General Info

**In order of professional importance**
1. Electrical Enginnering Major
2. Mechatronics Minor
3. Class of 2025

---

*Bonus Info*
* I play video games in my free time
* I enjoy going to the gym
* I always try to improve my cooking and learn new cuisine
---
Some music from a video game I've played recently Lethal Compony can be found here: [Lethal Copany Soundtrack](https://www.youtube.com/watch?v=S8V5fySc_6o)

After accidently clicking the above link and not saving and then explaing to a friend that this was a learning moment he said
> The L is for learning not for losing - Nathan Taco-Bravo

Here is a photo I took on my recent trip to Iceland it's the Barnafoss also know as Children's Falls. 
![Barnafoss, Children's Falls](https://github.com/dcmcdevitt/EE322/assets/116912016/9ed50239-5ddd-4c5f-ba80-3f9bb00e49bb)


It's important to me to keep my code and digital notebooks orginized.
So here's a snipit of code from ENGR 122's Left Hand Test!
```
void setup() {
    Serial.begin(115200);
    motor1.attach(motor1pin);   //motor1 is attached using the motor1pin
    motor2.attach(motor2pin);   //motor2 is attached using the motor2pin
  
}
void loop() {
    motor1.write(180);   // Request to generate the PWM signal
    motor2.write(M2S);
    f_dist = ultrasonic_front.read(CM) * 10;
    l_dist = ultrasonic_left.read(CM) * 10;
    r_dist = ultrasonic_right.read(CM) * 10;

    //Printing all sensors
    sprintf(buffer, "Forward: %d Left: %d Right: %d", f_dist, l_dist, r_dist);
    Serial.println(buffer);
    
    if (f_dist < 120) {
      D90_left();
    }
    if (r_dist < 200 && M2S != 121) {
      M2S += 1;
    }
    if (l_dist < 200 && M2S != 118) {
      M2S -= 1;
    }
}
```

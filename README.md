# Automatic Solar Panel Cleaner Using Tinkercad

###### Developed and simulated an Automatic Solar Panel Cleaner using Arduino UNO in Tinkercad. The system integrates an LDR sensor to monitor Day or Night and a servo motor mechanism to perform automatic cleaning when dust or dirt accumulation is detected. An LCD display is used to show real-time status, ensuring efficient solar energy generation through automated maintenance.
---
## Here is the references...

Circuit Connections in TINKERCAD :-

<img src=https://github.com/lingeshkumarkamaraj/Auto-Solar-Panel-Cleaner/blob/main/1.png> 
<img src=https://github.com/lingeshkumarkamaraj/Auto-Solar-Panel-Cleaner/blob/main/2.png>
<img src=https://github.com/lingeshkumarkamaraj/Auto-Solar-Panel-Cleaner/blob/main/3.png>
<img src=https://github.com/lingeshkumarkamaraj/Auto-Solar-Panel-Cleaner/blob/main/4.png>
<img src=https://github.com/lingeshkumarkamaraj/Auto-Solar-Panel-Cleaner/blob/main/6.png>
<img src=https://github.com/lingeshkumarkamaraj/Auto-Solar-Panel-Cleaner/blob/main/5.png>

Working :- 

[<img width="300" height="300" src="https://img.icons8.com/color/96/start.png" alt="video"/>](https://youtu.be/OrODncMhrcE)


---
Code :-
```

#include<Servo.h>
Servo clnup;
Servo clndn;
int pr, sp;

void setup(){
  clnup.attach(7);
  clndn.attach(6);
  pinMode(A1,INPUT);
  pinMode(A0,INPUT);
  
  clnup.write(0);
  clndn.write(0);
  
  if(pr>100){
    clnup.write(90);
    delay(500);
    clndn.write(90);
    delay(1000);
    clnup.write(0);
    delay(500);
    clndn.write(0);
    delay(1000);
  }
}
void loop(){
  pr = analogRead(A0);
  sp = analogRead(A1);
  
  if(sp<820 && sp>100){
    clnup.write(90);
    delay(500);
    clndn.write(90);
    delay(1000);
    clnup.write(0);
    delay(500);
    clndn.write(0);
    delay(1000);
  }
  
  if(pr<800 && pr>100){
    clnup.write(90);
    delay(500);
    clndn.write(90);
    delay(1000);
    clnup.write(0);
    delay(500);
    clndn.write(0);
    delay(1000);
  }
  delay(2000);
}


```
---
[TINKERCAD LINK](https://www.tinkercad.com/things/lRvBoGBZoyM-panel-clean?sharecode=exMkYOFheM__0TgxbhVHY7pibX1ZsfoSd3sjNemLcS4)
---

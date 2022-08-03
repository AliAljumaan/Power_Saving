# Power_Saving
Transistors can be used in servo motors to reduce power consumption when there is no signal going to the servos.This circuit shows that when servo motor moves the circuit will have aroud 90mA and when it is stationary the circuit will have around 3mA.

![PowerSavingServo](https://user-images.githubusercontent.com/108624020/182668691-243a8802-be03-4a9d-8878-68a19004abd0.png)

The link of the circuit is [here](https://www.tinkercad.com/things/bz5nrGm1nhk-powersavingservo/editel).

the code used to run the circut.
```
#include <Servo.h>

Servo myservo;
int i;

void setup() {
  // put your setup code here, to run once:
  myservo.attach(7);
}

void loop() {
  // put your main code here, to run repeatedly:
  myservo.write(45);
  delay(1000);
  myservo.write(90);
  delay(1000);
  myservo.write(135);
  delay(1000);
  for(i=135;i>45;i-=2){
    myservo.write(i);
    delay(100);
  }
}
```


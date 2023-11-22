## Controling a RS2205 FPV Drone Motor with a adruino and a resistor
  This github base provide code for the topic (Which Harumi will forgot)
```C#
#include <Servo.h>

Servo esc;
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  pinMode(A0,INPUT);
  esc.attach(9, 0, 2000);
}
int inohm;
void loop() {
  // put your main code here, to run repeatedly:
  inohm = map(analogRead(A0),0,1023,900,2000);
  Serial.println(inohm);
  esc.writeMicroseconds(inohm);
  delay(100);
}

```

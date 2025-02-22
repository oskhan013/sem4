## Practical 1.
#### Aim: Introduction to Arduino circuits and breadboarding Blinking of LEDs
```
void setup()
{
 pinMode(13, OUTPUT);
 pinMode(8, OUTPUT);
 pinMode(4, OUTPUT);
}
void loop()
{
 digitalWrite(13, HIGH);
 delay(200);
 digitalWrite(8, HIGH);
 delay(200);
 digitalWrite(4,HIGH);
 delay(500);
 digitalWrite(13, LOW);
 delay(200);
 digitalWrite(8, LOW);
 delay(200);
 digitalWrite(4,LOW);
 delay(500);
}
```
[Circuit1](emb1.png)

## Practical 2
#### Aim: Program using Light Sensitive Sensors.
```
int sensorValue=0;
void setup(){
 pinMode(A0,INPUT);
 pinMode(13,OUTPUT);
 Serial.begin(9600);
}
void loop(){
 sensorValue=analogRead(A0);
 Serial.println(sensorValue);
 int fade=map(sensorValue,54,974,255,0);
 Serial.println(fade);
 analogWrite(13,fade);
 delay(1000);
}
```
[CIRCUIT2](emb2.PNG)

## Practical 3.
#### Aim: Program using temperature sensors.
```
int celsius = 0;
int fahrenheit = 0;
void setup()
{
 pinMode(A0,INPUT);
 Serial.begin(9600);
}
void loop()
{
 celsius = map(((analogRead(A0)-20)+3.04),0,1023,-40,-125);
 fahrenheit = ((celsius*9)/5+32);
 Serial.print(celsius);
 Serial.print("C\n");
 Serial.print(fahrenheit);
 Serial.print("F\n");
 delay(2500);
}
```
[CIRCUIT2](emb3.png)

## Practical 4.
### Aim: Program using Ultrasonic sensors.
``` 
const int echo = 6;
const int trig = 7;
long period;
float distance;
void setup()
{
 pinMode(trig, OUTPUT);
 pinMode(echo, INPUT);
 Serial.begin(9600);
}
void loop()
{
 digitalWrite(trig,LOW);
 delayMicroseconds(2);
 digitalWrite(trig,HIGH);
 delayMicroseconds(10);
 digitalWrite(trig,LOW);
 period = pulseIn(echo,HIGH);
 distance = period*0.034/2;
 Serial.print("Distance:");
 Serial.print(distance);
 Serial.print("cm\n.");
 delay(2500);
}
```
[CIRCUIT4](emb4.png)

## Practical 5.
#### Aim: Programs using digital infrared motion sensors.
```
int LED = 0;
int PIR = 2;
int val= 0;
void setup(){
 pinMode(LED,OUTPUT);
 pinMode(PIR,INPUT);
}
void loop(){
 val = digitalRead(PIR);
 if(val == HIGH){
 digitalWrite(LED,HIGH);
 }
 else{
 digitalWrite(LED,LOW);
 }
 delay(1000);
}
```
[CIRCUIT5](emb5.png)

## Practical 6.
#### Aim: Programs using gas sensors.
```
int LED = 13;
int MQ2pin = A0;
void setup()
{
 pinMode(LED,OUTPUT);
 pinMode(MQ2pin,INPUT);
 Serial.begin(9600);
}
void loop()
{
 float sensorValue;
 sensorValue = analogRead(MQ2pin);
 if(sensorValue >=250)
 {
 digitalWrite(LED,HIGH);
 Serial.print(sensorValue);
 Serial.println("GAS DETECTED");
 }
 else
 {
 digitalWrite(LED,LOW);
 Serial.println(sensorValue);
 Serial.print(sensorValue);
 }
 delay(1000);
}
```
[CIRCUIT6](emb6.png)

## Practical 7.
#### Aim: Programs using servo motors.
```
#include<Servo.h>
int pos = 0;
Servo servo_9;
void setup(){
 servo_9.attach(9);
}
void loop(){
 for(pos=0;pos<=180;pos+=1){
 servo_9.write(pos);
 delay(10);
 }
 for(pos=180;pos>=180;pos-=1){
 servo_9.write(pos);
 delay(10);
 }
}
```
[CIRCUIT7](emb7.png)

## Practical 8.
#### Aim: Programs making Tilt Sensor with Arduino.
```
int LED = 13;
int inpin = 7;
void setup()
{
 pinMode(LED,OUTPUT);
 pinMode(inpin,INPUT);
 Serial.begin(9600);
}
void loop()
{
 int value = digitalRead(inpin);
 if(value==0)
 {
 digitalWrite(LED,HIGH);
 }
 else{
 digitalWrite(LED,LOW);
 }}
 ```
[CIRCUIT8](emb8.png)

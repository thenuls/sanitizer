# sanitizer
Hand sanitizer doesn't replace soap and water if your hands are dirty, but along with regular hand washing, it definitely helps fight many important germs. How does it work? It works by killing cells—not human cells. It kills microbial cells.
codes
#include<Servo.h>
#define echoPin 4
#define trigPin 5
Servo Myservo;

int long duration;
int distance;
void setup(){ 
Myservo.attach(3);
pinMode(echoPin,INPUT);
pinMode(trigPin,OUTPUT);

}

void loop()
{
digitalWrite(trigPin,LOW);
delayMicroseconds(2); 
digitalWrite(trigPin,HIGH);
delayMicroseconds(10); 
digitalWrite(trigPin,LOW);
duration=pulseIn(echoPin,HIGH);
distance=(duration*0.034/2);
  
  if(distance<=5){
Myservo.write(180);
}
else {
Myservo.write(0);


}

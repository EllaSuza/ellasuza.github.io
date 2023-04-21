---
layout: default
---

[BACK TO HOME]({{ '../index.html' |relative_url }})

[Part of Hormao Machine]({{ '../index.html' |relative_url }})

On this page, I document my process of and research on controlling the movement of motors with light sensors.

# COMPONENTS I CAN USE

### Servo motors


analog clock making with servo motors: https://electronics-project-hub.com/analog-clock-using-arduino/


###### NOTES ON SERVO MOTORS

- Can only rotate 180 degrees
- Controlled by a PWM signal
- Consists of a complex gear mechanism, a DC motor and a controller with feedback system
  - gears will educe the speed of rotation t the output but it increases the torque which we want from a servo monitor

- has 3 pins:
  - red is +5V
  - brown is -Ve
  - orange is PWM input

previous work with it documented:
https://app.archbee.com/docs/hac8usg8LteFu7mWCOJMo/3i1QbF-wiJoXSA8UivstD

### Stepper motors

Stepper motor basics: https://forum.arduino.cc/t/stepper-motor-basics/275223 (not applied to unipolar steppers)


#### JK42HS40-1704-83AF
Data sheet : https://datasheetspdf.com/pdf/1380131/ETC/JK42HS/1

Someone working with the same and trying to find driver : https://forum.arduino.cc/t/stepper-driver-to-this-stepper-motor/299923

- bipolar
- 200 steps per revolution
- 1700 m/A per coil
- 2.7 v

possible drivers: 
- A4988
- DRV8825
- DRV8824



#### 28BYJ-48
Data sheet : https://www.digikey.nl/en/datasheets/mikroelektronika/mikroelektronika-step-motor-5v-28byj48-datasheet

- unipolar (6 wires)
- compatible with driver ULN2003
- 32 steps per revolution

###### NOTES ON STEPPER MOTORS

- Broadly speaking there are two types of stepper motors: UNIPOLAR AND BIPOLAR

Unipolar:
- four wires connecting to the two separate coils inside the motor (one pair to each coil)

Bipolar:
- Two types; with 5 wires and with 6 (hybrid) wires



### Light sensor

#### Light sensor LM393 9AM 
- same as : https://www.reichelt.nl/nl/nl/ontwikkelaarspanelen-lichtsensor-met-hoog-laag-rendement-lm39-debo-light-sens-p224222.html?PROVID=2809&gclid=Cj0KCQjw8qmhBhClARIsANAtbod-Ijv9C5QOjDjeGF2yvb9s8kTvQ6j2YI7AcJXzKBBsFdreawby7PgaAqCsEALw_wcB

https://www.instructables.com/LDR-Sensor-Module-Users-Manual-V10/


#### Light sensor TEMT 60000
- same as : https://www.tinytronics.nl/shop/en/sensors/optical/light-and-color/temt6000-light-sensor-module






# Stepper motor to Arduino
connecting Stepper motor 28BYJ-48 and driver ULN2003 to Arduino UNO


code: https://soldered.com/learn/how-to-use-stepper-motor-and-uln2003-driver/
```
/*
*  BYJ48 Stepper motor with the ULN breakout board
*  Connect :
*  IN1 - D8
*  IN2 - D9
*  IN3 - D10
*  IN4 - D11
*  VCC - 5V
*  Gnd - gnd
* 
*  e-radionica.com
*/
#define IN1  8
#define IN2  9
#define IN3  10
#define IN4  11
int koraci = 0;
boolean smjer = true;
unsigned long vrijemeZadnje = 0;    // we will note the time
unsigned long vrijemeTrenutno = 0;  // needed to
unsigned long vrijeme = 0;          // execute the given angle
int koraciPreostalo = 4095; //this stepper has 4095 steps in total
void setup()
{
    Serial.begin(115200);
    pinMode(IN1, OUTPUT);
    pinMode(IN2, OUTPUT);
    pinMode(IN3, OUTPUT);
    pinMode(IN4, OUTPUT);
}
void loop()
{
  while(koraciPreostalo > 0) // steps remaining until the full circle
  {
    vrijemeTrenutno = micros(); //write down the current time in microseconds
    if(vrijemeTrenutno - vrijemeZadnje >= 1000)
    {
      stepper(1); //call the stepper function (check void stepper below)
      vrijeme = vrijeme + micros() - vrijemeZadnje;
      vrijemeZadnje = micros();
      koraciPreostalo--;
    }
   }
   
   Serial.println(vrijeme);
   Serial.println("Wait..!");
   delay(2000);
   smjer = !smjer; // opposite direction
   koraciPreostalo = 4095;  // reset the number of steps
}
void stepper(int brojKoraka)
{
  for (int x=0; x < brojKoraka; x++) { switch(koraci) { case 0: digitalWrite(IN1, LOW); digitalWrite(IN2, LOW); digitalWrite(IN3, LOW); digitalWrite(IN4, HIGH); break; case 1: digitalWrite(IN1, LOW); digitalWrite(IN2, LOW); digitalWrite(IN3, HIGH); digitalWrite(IN4, HIGH); break; case 2: digitalWrite(IN1, LOW); digitalWrite(IN2, LOW); digitalWrite(IN3, HIGH); digitalWrite(IN4, LOW); break; case 3: digitalWrite(IN1, LOW); digitalWrite(IN2, HIGH); digitalWrite(IN3, HIGH); digitalWrite(IN4, LOW); break; case 4: digitalWrite(IN1, LOW); digitalWrite(IN2, HIGH); digitalWrite(IN3, LOW); digitalWrite(IN4, LOW); break; case 5: digitalWrite(IN1, HIGH); digitalWrite(IN2, HIGH); digitalWrite(IN3, LOW); digitalWrite(IN4, LOW); break; case 6: digitalWrite(IN1, HIGH); digitalWrite(IN2, LOW); digitalWrite(IN3, LOW); digitalWrite(IN4, LOW); break; case 7: digitalWrite(IN1, HIGH); digitalWrite(IN2, LOW); digitalWrite(IN3, LOW); digitalWrite(IN4, HIGH); break; default: digitalWrite(IN1, LOW); digitalWrite(IN2, LOW); digitalWrite(IN3, LOW); digitalWrite(IN4, LOW); break; } postaviSmjer(); } } void postaviSmjer() { if(smjer==1){ koraci++; } if(smjer==0){ koraci--; } if(koraci>7){ koraci=0; }
    if(koraci<0){ koraci=7; }
}
```



![1 tooth gear](/assets/images/motorlightsensor/gearmotor.mov)
(video of code running with 1 tooth gear)

[On how I made this gear, see my gear production page]({{ '/documentationella/hormaomachine/gear_production' | relative_url }})


#### Light sensor reading serial monitor

https://www.hackster.io/kiranpaul/light-magic-using-lm393-and-arduino-uno-14eadc

giving digital input

```
void setup() {
  pinMode(7,INPUT);
  /*pinMode(9,OUTPUT); */
  Serial.begin(9600); //initialise serial monitor

}

void loop() {
  int temp=digitalRead(8);      //assign value of LDR sensor to a temporary variable
  Serial.println("Intensity="); //print on serial monitor using ""
  Serial.println(temp);         //display output on serial monitor
  delay(300);
  if(temp==HIGH)               //HIGH means,light got blocked
  digitalWrite(9,HIGH);        //if light is not present,LED on
  else
  digitalWrite(9,LOW);         //if light is present,LED off
}
```

#### Light sensor and stepper motor

```
// Arduino stepper motor and LDR
// based on https://www.instructables.com/Light-Sensor-Stepper-Motor-Arduino/ but with some modifications
#include <Stepper.h>

// Include the header file

// change this to the number of steps on your motor

#define STEPS 32

// create an instance of the stepper class using the steps and pins

Stepper stepper(STEPS, 8, 10, 9, 11);

int val = 0;

int LDR = 7;

void setup()

{

Serial.begin(9600);

stepper.setSpeed(200);



pinMode(LDR, INPUT);

}

void loop()

{

int LDRValue = digitalRead(LDR);

Serial.print("sensor = ");

if (LDRValue ==LOW)

{


val = Serial.parseInt();

stepper.step(512);

Serial.println(val);

//for debugging

}

else

{

//digitalWrite(LED, LOW);


}

}

```


![1 tooth gear with light sensor](/assets/images/motorlightsensor/gearlightsens.mov)
(video of gear running when light is detected, and stops once all light is blocked)

[On how I made this gear, see my gear production page]({{ '/documentationella/hormaomachine/gear_production' | relative_url }})

## ASSEMBLY:

#### Stepper 28YJ-48 5 wires to Driver ULN2003

#### Driver ULN2003 to Arduino UNO
Int1 to pin D8

Int2 to pin D9

Int3 to pin D10

Int4 to pin D11

Ground to pin Ground

Power to pin 5V

#### LM393 9AM sensor to Arduino UNO
VCC to pin 5V

GROUND to pin Ground

DO to D7

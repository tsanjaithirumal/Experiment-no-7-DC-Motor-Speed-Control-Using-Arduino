## Exp-6 DC Motor Speed Control Using Arduino
### Date:05/04/2024
### Name:SANJAI T
### Rollnumber:212222040145
### Department:B.E CSE
### AIM : To control the speed and the direction of a DC motor using L293D driver ic( H- bridge)
### Components Required:
•	Arduino UNO board
•	L293D driver
•	12V DC motor
•	10K ohm potentiometer
•	Pushbutton
•	12V source
•	Breadboard
•	Jumper wires
### THEORY 
The L293D quadruple half-H drivers chip allows us to drive 2 motors in both directions, with two PWM outputs from the Arduino we can easily control the speed as well as the direction of rotation of one DC motor. (PWM: Pulse Width Modulation).
Arduino DC motor control circuit:
Project circuit schematic diagram is the one below.
## H BRIDGE CIRUCIT INTERFACE
![image](https://user-images.githubusercontent.com/36288975/167763051-b230c183-afc5-46f2-ba95-0f95e10dd6c9.png)
  
The speed of the DC motor (both directions) is controlled with the 10k potentiometer which is connected to analog channel 0 (A0) and the direction of rotation is controlled with the push button which is connected to pin 8 of the Arduino UNO board. If the button is pressed the motor will change its direction directly.
The L293D driver has 2 VCCs: VCC1 is +5V and VCC2 is +12V (same as motor nominal voltage). Pins IN1 and IN2 are the control pins where:

As shown in the circuit diagram we need only 3 Arduino terminal pins, pin 8 is for the push button which toggles the motor direction of rotation. Pins 9 and 10 are PWM signal outputs, at any time there is only 1 active PWM, this allows us to control the direction as well as the speed by varying the duty cycle of the PWM signal. The active PWM pin decides the motor direction of rotation (one at a time, the other output is logic 0).

### PROGRAM 
```
int in1=5;
int in2=6;
int en=3;

void setup()
{
  pinMode(in1,OUTPUT);
  pinMode(in2,OUTPUT);
  pinMode(en,OUTPUT);
}

void loop()
{
  analogWrite(en,255);
  digitalWrite(in1,LOW);
  digitalWrite(in2,HIGH);
  delay(500);
}
```
### Output:
![Screenshot 2024-04-05 160041](https://github.com/balar2004/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/118791778/ecb51a89-1c14-4adc-9af6-d42219723a98)

## Sematic Diagram:
![image](https://github.com/tsanjaithirumal/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119393916/92494652-4c15-4e6b-84be-402bb86c0c5d)

## Table:
![Screenshot 2024-04-05 161555](https://github.com/balar2004/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/118791778/c6778051-9d30-4847-9dfe-d1d27c0b665b)

## Graph:
![Screenshot 2024-04-05 161538](https://github.com/balar2004/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/118791778/770bb7a7-a822-4a68-b025-2c82a24b6a3a)

### RESULTS: 
Arduino uno interfacing DC motor using L293D driver ic H- bridge is learned and executed

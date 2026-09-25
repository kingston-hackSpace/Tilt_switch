# Tilt switch

A tilt switch is a simple component that acts like a switch controlled by orientation instead of a button press. Inside, a small metal ball (or a mercury bead in older versions) rolls freely inside a cavity with two contacts. When the switch is tilted past a certain angle, the ball rolls onto the contacts and closes the circuit; when it's tilted back, the ball rolls away and the circuit opens.

At hackSpace we have two module types:

- 3-pin module (no LED)

- [4-pin module (with LED)](https://arduinomodules.info/ky-027-magic-light-cup-module/)

---
## HARDWARE

- Arduino UNO

- Tilt switch (any)

- LED

- 220ohms resistor

---
## WIRING

<img src="Tilt_3and4pin_bb.jpg" width="800"> 

*Click on the image to expand diagram

---
## CODE and INSTRUCTIONS

### 3-PIN Tilt Switch

- Upload this code to your Arduino Board.

```
int LED = 2; 
int tiltPin = 3;  
int tilt; 

void setup(){
  Serial.begin(9600);
  pinMode(LED,OUTPUT); 
  pinMode(tiltPin,INPUT); 
}

void loop(){
  tilt = digitalRead(tiltPin); 
  Serial.println(tilt);

  if(tilt == HIGH) {
    digitalWrite(LED,HIGH);
  } else {
  digitalWrite(LED,LOW);
  }
}

```

- Flip your bradboard + tilt switch upside down, the LED should turn on!

### 4-PIN Tilt Switch

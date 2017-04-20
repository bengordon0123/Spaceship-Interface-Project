
int  switchstate = digitalRead(2);

void setup() {
  
    // declare the LED pins as outputs using the pinMode() function
 //set the LEDs as OUTPUT on pins: 3,4, and 5 and the button as input on pin 2 
 pinMode(3, OUTPUT);
 pinMode(6, OUTPUT);
 pinMode(7, OUTPUT);
 pinMode(2, OUTPUT);


  
}
void loop(){


 switchstate = digitalRead(2);


  // if the button is not pressed
  // turn on the green LED and off the red LEDs  
  if (switchstate == LOW) {

    digitalWrite(3, HIGH); // turn on the green LED on pin 3 
    digitalWrite(6, LOW);  // turn off the red LED on pin 4
    digitalWrite(7, LOW);  // turn off the red LED on pin 5

    
 }

  else {
    digitalWrite(3, LOW);  // turn off the green LED on pin 3
    digitalWrite(6, LOW);  // turn off the red LED on pin 4
    digitalWrite(7, HIGH); // turn on  the red LED on pin 5 

    // wait for a quarter second before changing the light

    delay(250);
    digitalWrite(3, HIGH); // turn on the red LED on pin 4 
    digitalWrite(6, LOW);  // turn off the red LED on pin 5

    // wait for a quarter second before changing the light
    delay(250);
  }
}


          

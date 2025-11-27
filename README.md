# nodemcu-01
# Microprocessor
NodeMCU använder ESP8266

# Två bassfunktioner i Ardunio
För att få NodeMCU(ESP8266) inbyggda LED lampan att blinka måste Ardunios två basfunktioner användas. 
* Setup ()
  Vilka portar som ska användas och hur

/ the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
  
* Loop ()
Instruktioner som upprepas om och om

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}


## Steg för steg 
* Installera **Ardunio IDE**
* ´File´ --> ´Exempels´ - ´0.1 Basics´ - ´Blink´
  
* Koppla med USB-kabel
* ´Tools´ - ´Board´ - ´Generic ESP8266 Module´
* Välj **Port** i ´Tools´ --> ´Port´
* Tryck ´Upplod´

![Dator](Dator.jpeg) 



  


# introduktion 
I denna redovisning ska jag presentera NodeMCU-01 som bygger på ESP8266 om vad en mikroprocessor är, hur man programmerar den i Arduino IDE och hur den kan styra exempelvis LED-lampor och sensorer.

# Microprocessor
NodeMCU bygger på ESP8266. En mikroprocessor (minidator) som kan programmeras genom programmet Ardunio IDE för att styra exempelvis lampor och sensorer. 


[
](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.amazon.se%2FAZDelivery-NodeMCU-Amica-V2-USB-C-anslutning%2Fdp%2FB0D8WCJH9B&psig=AOvVaw3CJ9W0DqJqUukIOYp1eyD7&ust=1764678455613000&source=images&cd=vfe&opi=89978449&ved=0CBUQjRxqFwoTCNj30dexnJEDFQAAAAAdAAAAABAM)<img width="1000" height="793" alt="image" src="https://github.com/user-attachments/assets/f2af3925-0320-4b1e-9bd2-f68ac328f4bb" />

# Portinitialisering 
Innebär att man förbreder en port på en mikroprocessor genom att bestäma om den ska fungera som ingån eller utgång. ställa in innan porten används. 

# Två bassfunktioner i Ardunio
För att få NodeMCU(ESP8266) inbyggda LED lampan att blinka måste Ardunios två basfunktioner användas. 
```cpp
setup()
```
Vid start eller reset av programmet körs denna kod
  ```cpp
Loop()
```
Instruktioner som upprepas om och om igen



![Code](https://github.com/user-attachments/assets/bbb809b4-ac21-4b59-8145-5178c8310077)

```c
/*
  ESP8266 Blink by Simon Peter
  Blink the blue LED on the ESP-01 module
  This example code is in the public domain

  The blue LED on the ESP-01 module is connected to GPIO1
  (which is also the TXD pin; so we cannot use Serial.print() at the same time)

  Note that this sketch uses LED_BUILTIN to find the pin with the internal LED
*/

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);  // Initialize the LED_BUILTIN pin as an output
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, LOW);  // Turn the LED on (Note that LOW is the voltage level
  // but actually the LED is on; this is because
  // it is active low on the ESP-01)
  delay(1000);                      // Wait for a second
  digitalWrite(LED_BUILTIN, HIGH);  // Turn the LED off by making the voltage HIGH
  delay(2000);                      // Wait for two seconds (to demonstrate the active low LED)
} 
```

## Steg för steg 
Installera **Ardunio IDE**
 `File` -> `Exempels` -> `0.1 Basics` -> `Blink`
  
Koppla med USB-kabel
`Tools` -> `Board` -> `Generic ESP8266 Module`
Välj **Port** i `Tools` -> `Port`
Tryck `Upplod`

![Dator](https://github.com/user-attachments/assets/22bb3cde-475b-47a8-ab35-a5594d6aaac8)



  

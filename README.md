# Arduino - 3 Buttons and 3 LEDs Project

This Arduino Uno project demonstrates how to use **3 digital push-buttons (inputs)** to control **3 individual LEDs (outputs)** using simple `if-else` conditions.

---

##  Components Used

- 1 Arduino Uno
- 3 Push Buttons
- 3 LEDs (Blue, Yellow, White)
- 3xResistors (220Ω for LEDs)
- Jumper Wires
- Breadboard

---

##  Pin Connections

| Button Color | Arduino Pin (Input) | LED Color | Arduino Pin (Output) |
|--------------|---------------------|-----------|-----------------------|
| Blue         | D2                  | Blue      | D8                    |
| Yellow       | D3                  | Yellow    | D9                    |
| White        | D4                  | White     | D10                   |

---

##  Code

void setup()
{
  pinMode(2, INPUT); // Blue_button
  pinMode(8, OUTPUT); // Blue_LED
  
  pinMode(3, INPUT); // Yellow_button
  pinMode(9, OUTPUT); // Yellow_LED
  
  pinMode(4, INPUT); // White_button
  pinMode(10, OUTPUT);// White_LED
}

//if-else
void loop()
{
  if (digitalRead(2) == HIGH) {
    digitalWrite(8, HIGH);
  } else {
    digitalWrite(8, LOW);
  }
  if (digitalRead(3) == HIGH) {
    digitalWrite(9, HIGH);
  } else {
    digitalWrite(9, LOW);
  }
  if (digitalRead(4) == HIGH) {
    digitalWrite(10, HIGH);
  } else {
    digitalWrite(10, LOW);
  }
  delay(10); }

  ##  How the Code Works
  The program checks the state of each button continuously.

If a button is pressed (HIGH), the corresponding LED turns on.

If the button is not pressed (LOW), the LED turns off.

This is handled using digitalRead() for inputs and digitalWrite() for outputs.

The delay(10); at the end is used to slightly reduce CPU usage.


 ## Circuit Diagram
![image](https://github.com/user-attachments/assets/057b77f1-e55a-4f6c-a828-f718ccc3e386)

##  Project Simulation (Tinkercad)

You can try the project online here:  
[🔌 Open Circuit in Tinkercad](https://www.tinkercad.com/things/8p3npzXqyf5/editel?returnTo=%2Fdashboard&sharecode=LOvpPSiPSGPG99b-QPpwyGpYYRiP3yF6LJ3nv2PXYIA)

---

 ## Author: Eman Alnahdiز


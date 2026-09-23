# XR2206 Function Generator & Arduino Visualizer

DIY XR2206 function generator PCB assembly and practical electronics project, successfully integrated with an Arduino Uno to plot live waveforms.

This project is part of my practical electronics work to strengthen my knowledge of circuit analysis, PCB assembly, and microcontroller programming.

## Project Status: Completed & Tested!
The PCB has been fully assembled, soldered, cleaned, and successfully powered using a 12V AC/DC adapter. It is connected to an Arduino Uno to read and visualize the generated wave signals in real-time.

## Work Completed
- **Component Placement:** Identified and placed all through-hole electronic components.
- **Soldering:** Successfully soldered the IC socket, resistors, switches, and capacitors (ensuring correct electrolytic polarity).
- **Board Maintenance:** Cleaned the PCB to remove residual flux after soldering.
- **Power Integration:** Obtained a suitable 12V 5.5x2.1mm DC barrel connector and safely powered the generator.
- **Arduino Integration:** Wired the generator to an Arduino Uno and programmed it to read the live wave output safely.
- **Testing:** Verified stable waveform creation and plotted the graphs on a PC.

## Hardware Wiring
To safely read the signals, the generator was configured with the following connections:
- **GND (Generator)** -> **GND (Arduino)**
- **SIN/TRI (Generator)** -> **Analog Pin A0 (Arduino)**
- *Note: The Amplitude potentiometer on the generator was dialed toward minimum to keep the output voltage safely within the Arduino's 5V limit.*

## Software (Arduino Code)
The following code was uploaded to the Arduino Uno to read the signal at 115200 baud:

```cpp
const int signalPin = A0; 

void setup() {
  Serial.begin(115200); 
}

void loop() {
  int sensorValue = analogRead(signalPin);
  Serial.println(sensorValue);
  delay(10); 
}
```

## Photos and Results

### Full Hardware Setup
![Hardware Setup](image_CaoN-J.png)

### Live Waveform Output (Serial Plotter)
![Live Waveform](image_fTBy1e.png)

---
*Proudly assembled, soldered, and programmed independently!*

# ESP32 LED Controller with Bluetooth

## Project Overview
A button-controlled LED system using ESP32 that:
- Cycles through Red ON → Blue ON → OFF states
- Sends Bluetooth notifications for each state change

Note on Simulation:  
Due to overload in rendering of simulation at WOKWI, it was not possible to do it there with ESP32. Instead, TinkerCAD's Arduino was used. Except for the Bluetooth functionality (which requires an additional library module), all other circuit logic remains identical.

##How It Works
1. Button Control:
   - Single button cycles through 3 states:
     - 1st press: Red LED ON
     - 2nd press: Blue LED ON
     - 3rd press: Both LEDs OFF
   - Uses internal pull-up resistor (no external resistor needed)

2. Bluetooth Messaging:
   - After each state change, sends:
     - "LED: RED"
     - "LED: BLUE"
     - "LED: OFF"
   - Device name: "ESP32_LED_Controller"

3. Circuit Logic:
   - Debouncing prevents multiple state changes per press
   - Efficient state machine implementation

## How To Run
### Hardware Setup

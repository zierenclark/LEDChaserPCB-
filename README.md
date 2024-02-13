# LEDChaserPCB-
Goal: Build LED chaser circuit PCB from online LEDchaser Schamtic on circuitdigest.com

Schematic from: https://circuitdigest.com/electronic-circuits/led-chaser-circuit

The circuit is designed to Power 10 LEDs in an on-and-off sequence similar to decorative lights. This circuit uses a 555 IC timer to generate a high and low signal at different frequencies according to the resistance of a potentiometer. This signal is then inputted into a 4017IC that changes in stage with each cycle of the 555 IC timer. This circuit uses another LED just to determine the frequency of the cycles that the 555 IC is outputting. 

<img width="488" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/ed24e489-bbc7-46ae-b605-7891f44ab7d8">

Equations for the 555 Timer:

High Output Signal: T1 = 0.693(R1+VR)C1  -----> VR = Variable Resistor(Potentiometer)

Low Output Signal: T2 = 0.693(R2)C1

Total Period: T = T1 + T2 = 0.693(R1+2VR)C1

Frequency Oscicillation: F = 1/T, F = 1.44/(R1+2VR)C1

Equations are from the online schematic.

Started by initially building the circuit on the breadboard to ensure all components worked properly and the schematic was correctly designed for the initial purpose.  Had to change all 150 Ohm resistors to 220 Ohm due to component availability. 

<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/33ba5d09-85c2-4c11-8ab1-14cdb58a3cc9">
<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/0713545d-f0be-4e3b-b8f6-b2ffd08ee32b">

<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/cd4fca27-2059-4de6-a919-c64a0a3bb1a9">

Once I confirmed the schematic was working properly, I began building it in Eagle PCB software. Going from schematic to PCB was particularly difficult since the stages of the 4017IC were not in order by the next stage due to the necessary design of the integrated circuit.

<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/87195a9a-81f9-4231-80df-6eb880cdf387">
<img width="681" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/46137701-32f0-4807-9220-04ba9692d602">


After printing the PCB on the LPKF S104 CNC mill, I assembled and soldered the circuit using the components from the breadboard prototype. 


<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/d76ad26e-21c5-4dc7-985b-0974270fe06d">
<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/8d38cb68-825f-4009-b934-e4cae80c6951">

Initially, the circuit was not receiving power due to a faulty positive wire I had soldered originally. After replacing the wire, the circuit nearly worked correctly except for an LED not flashing during the fifth stage which was due to a faulty connection during soldering. 

<img width="500" alt="image" src="https://github.com/zierenclark/LEDChaserPCB-/assets/155485134/cfd504cf-8b16-42b7-8939-43ca11ad3858">

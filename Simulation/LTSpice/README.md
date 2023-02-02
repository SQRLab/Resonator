# LTSpice
These are the circuit simulations I did in LTSpice for the capacitive divider and rectifier
portions of the feedback circuit for the resonator. I have also provided a standard diode library
file that can be used if you would like to run the simulations with the diodes I created

### SQRL_Resonator_Capacitive_Divider.asc
This simulation uses ideal capacitors to create a capacitive divider to simulate the capacitor pick-off of the resonator. It is connected to an inductor and capacitor in parallel to model the receiving coil of the resonator and the trap capacitance. 

### SQRL_Resonator_Full_Wave_Bridge_Rectifier_RF_Diode.asc
This simulation uses the HMPS-2822 RF Diodes in a full wave bridge rectifier to convert AC to DC power

### SQRL_Resonator_HALF_Wave_Bridge_Rectifier_RF_Diode.asc
This simulation uses the HMPS-2822 RF Diodes in a half wave bridge rectifier to convert AC to DC power

### standard.dio.txt
This is a list of diode models used to simulate real diode components. The HMPS-2822 is not in the standard library, so I added a model of the HMPS-2822 based on the SPICE parameters in this datasheet (https://media.digikey.com/pdf/Data%20Sheets/Avago%20PDFs/HMPS-282x.pdf). These are the steps to add the diode model:

1. Navigate to the location LTSPICE is stored on your computer. For me it is located in "C:/Program Files x86/LTspiceXVII" on Windows
2. In this folder, navigate to "/LTspiceXVII/lib/cmp" . This is where all the component libraries are stored
3. Double-click on the "standard.dio" file. This will open a text editor in LTSpice containing the diode models
4. Open the "standard.dio.txt file" from this repo, copy the text from this file, and paste the text into "standard.dio", replacing the old text . Additionally, you could copy this line of code and paste it on a new line in the standard.dio file: ".MODEL HMPS-2822 D(IS=2.2E-28 RS=8 N=1.08 TT=100p CJO=0.7p VJ=15 M=0.5 BV=15 IBV=1E-4 Iave=5m Vpk=15 mfg=Broadcom type=Schottky)"
5. Save "standard.dio", exit out of all open LTSpice applications, and relaunch LTSpice
6. Now, all of the simulations in this repo will work with the HMPS-2822 diode! If you would like to design your own simulations using this component, simply place down a diode symbol, right click on the diode, click on "Pick a New Diode", scroll down to the bottom of the diode models list, click on "HMPS-2822" under "Part No." and click "OK". 

### Download LTSPICE
https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html

### Results running full wave and half wave rectifiers side by side 
These are generally the types of waveforms outputed from AC-DC rectifiers. (I used an RF diode here used in another paul trap but is obsolete on Digikey as of now :joy:)


### Running Simulations and Displaying Waveforms
To run a simulation click the run button in the top bar (symbol is a running stick figure), click anywhere on the circuit to probe the voltage at that location and a waveform viewer should appear


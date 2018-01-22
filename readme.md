

MagLock Smart Deadbolt Project
==========================

Projects website: http://think430.github.io/MagLock

Table of Contents
=================

1.  [Bill of Materials](#bill-of-materials)

2.  [Skills Required](#skills-required)

3.  [Build Instructions](#build-instructions)


Bill of Materials (in CAD Funds)
---------

Raspberry Pi Model 3 B (https://www.amazon.ca/LANDZO-Raspberry-Completed-Kits/dp/B01IOVOQ38/ref=sr_1_8?s=electronics&ie=UTF8&qid=1516578546&sr=1-8&keywords=raspberry+pi+3)  - $73.88

Adafruit 12V Lock Solenoid (https://www.adafruit.com/product/1512) - $17.00

9V Power Supply (https://www.digikey.ca/product-detail/en/triad-magnetics/WSU090-2000/237-1425-ND/3094951) - $16.73

ON Semiconductor 1N4004 Diode (https://www.digikey.ca/product-detail/en/on-semiconductor/1N4004G/1N4004GOS-ND/1485474) - $0.26

ON Semiconductor MJE3055T NPN BiPolar Junction Transistor (https://www.digikey.ca/product-detail/en/on-semiconductor/MJE3055TTU/MJE3055TTUFS-ND/1052512) - $0.96

Panasonic 1k Ω 1W Resistor (https://www.digikey.ca/product-detail/en/panasonic-electronic-components/ERG-1SJ102/P1.0KW-1BK-ND/35945) - $0.33

Printed Solenoid Driver Board (https://github.com/think430/MagLock/raw/master/MagLock%20Diagram.fzz) - $13.08 (MOQ of 3)

Fritzing PCB Software (http://fritzing.org/home/) $0.00


Skills Required
---------

Basic Electrical Circuit Theory

Basic Soldering Skills

Basic *nix OS Knowledge

Basic Programming Knowledge


Build Instructions
---------

1. Order all required parts/components. Download Fritzing.

2. Exercising caution, solder together PCB. (Review PCB diagram in Fritzing for component locations). To ensure that the board is soldered together correctly, connect the 9V adaptor (+) to the driver board 9V post and the (-) to the driver board GND post. Plug the power supply into the wall. Then, using a Digital Multimeter, measure the voltage between the "Pi In" and GND pins on the driver board, there should be no voltage passing.

3. Connect your Raspberry Pi to a monitor, keyboard and mouse. If this is your first time booting up the Raspberry Pi, select Raspbian as the OS from the NOOBS screen. Once the OS has booted, connect the Raspberry Pi to a WiFi network then open the Terminal and run the following command "$sudo apt-get install wiringPi"

4. Download the lockcontrol.py script from the repository.

5. Read the code to determine which GPIO pins are being used. 

6. Connect the GPIO pin to the "Pi In" terminal on your driver board.

7. Connect a ground pin on the Raspberry Pi to the ground pin on the driver board.

8. Connect the 9V Adaptor Negative to the ground pin on the driver board.

9. Connect the 9V Adaptor Positive to the 9V post on the driver board.

10. Connect the Lock solenoid positive and negative to the solenoid (+) and (-) on the driver board.

11. Plug the 9V Adaptor into the wall.

12. Run the Python script on the Raspberry Pi. Once the spacebar is pressed, the lock should cycle (1s unlocked, then re-locked).

13. If the lock does not cycle, please troubleshoot the PCB, but most likely, you overheated the BJT while soldering it into place.

14. If the lock cycles, congratulations!

**Prototyping notice- Do not leave and prototype device plugged in and unattended, this is how you burn down your house, or worse! I do not take any responsibility for any unintended outcomes, injuries, or damages incurred by undertaking this project.**


-------------------------------------------------

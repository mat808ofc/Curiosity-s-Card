Coil to LA/LB, GND to ground, FD left open or wired to an MCU/LED if the field-detect feature is wanted, and EP (exposed pad) left open/floating per the datasheet.



No pours, no wires, no NOTHING near the coil and chip.

The chip can be near the coil.

LA/LB can be wired freely to the chip.

nfc is interesting



**The basic LED resistor formula:**



R = (V\_supply - V\_LED) / I\_desired



Vf - The forward voltage is the voltage it needs for a given current.

If - The forward current is the current actually flowing through the LED. Controls brightness. This is the value you target. Everything else in the calculation exists to make sure this number ends up where you want it.

They are related to each other. When more current flows through, Vf goes up as well.



The current is the same in every part of the circuit.

The total available voltage HAS to be spent between the resistor and the LED.



Formula: R = (V\_supply − V\_LED) / I\_desired



V\_supply: the total voltage available from the source (VOUT, \~2V in this case)

V\_LED (Vf): the voltage the LED itself consumes at YOUR CHOSEN CURRENT!!

(V\_supply − V\_LED): whatever voltage is "left over" after the LED takes its share, **this is the voltage the resistor needs to drop**

I\_desired (If): the current you want flowing through the LED (and therefore through the resistor too, since they're in series)

R: the resistance needed so that this leftover voltage, divided by this resistance, produces exactly the target current, this comes directly from **Ohm's Law (V = I × R, rearranged to R = V / I)**



**Finished Formula: R = (2 − 1.7) / 0.002A = 150 ------> R = 150 Ohms**



"mA" MUST BE CONVERTED TO "A"



If Vf (toll) was 1.65: (LED needs 1.65V at 2mA)



**R = 175 Ohms**



If Vf was 1.75: (LED needs 1.75V at 2mA)



**R = 125 Ohms**



If Vf was 1.8: (LED needs 1.8V at 2mA)



**R = 100 Ohms**



If the LED consumes more voltage, the resistor needs a smaller value, and if the LED consumes less voltage, the resistor needs a higher value



PART THAT WILL BE USED::



TLMS1000



COLOR: RED

LOW CURRENT

Vf for 2mA = approx. 1.75, so **R = 125 Ohms**


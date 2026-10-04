# Curiosity's Card

### About
This is a custom business card with a nfc chip "NT3H2111W0FHKH", antenna "NXP's official Class 4 antenna" and a low-current 0603 package red LED, Vishay's "TLMS1000-GS15", which at 2mA (it's tested current for usage) only needs 1.75V (according to the Vf vs. If graphic in the datasheet). This is because the LED will work with the chip's energy harvesting feature, which will "harvest" energy from the nfc device (like a phone). The total voltage the chip can usually output with this technique is 2V, so the LED is inside the budget. I used the Ohm's Law to find the resistor value for the LED. 

R = (V_supply - V_LED) / I_desired

Vf - The forward voltage is the voltage it needs for a given current.
If - The forward current is the current actually flowing through the LED. Controls brightness. This is the value you target. Everything else in the calculation exists to make sure this number ends up where you want it.
They are related to each other. When more current flows through, Vf goes up as well.
V_supply: the total voltage available from the source (VOUT, ~2V in this case)
V_LED (Vf): the voltage the LED itself consumes at THE CHOSEN CURRENT!!


R = (2 − 1.75) / 0.002A = 125Ω, which is approx. 130Ω.

Aside from calculations, I also added personal branding, the Hack Club logo, some cool gradients, a qr code to my github repos and a section with most of the SMD package sizes (It's fun).


### INSPIRATION:
I haven't done projects for quite a long time because I was exhausted from it since the Flight controller (I was also working on my RC plane) so I decided to make a little weekend project, a custom business card, which is also I have honestly been wanting to make for quite a while now.

### CHALLENGES:
My biggest challenge was understanding the math and physics for the LED, it seemed super confusing at first but now I get it, and it makes a lot of sense. I also found it hard to understand the nfc chip and tag, but I ended up figuring it out.

### BOM:
| Part                              | MFR.Part #                  | Qty        | Total Cost (USD) |  Link to part (lcsc)                                                                | Distributor |
|-----------------------------------|-----------------------------|------------|------------------|-------------------------------------------------------------------------------------|-------------|
| C1 (200nf 0603 capacitor)         |  0603B204K160CT             |  20        |    $0.9140       |    https://www.lcsc.com/pt/product-detail/C3833176.html?s_z=n_q_0603B204K160CT      | JLCPCB      |
| D1 (TLMS1000 0603 LED)            |  TLMS1000-GS15              |  5         |    $0.8605       |    https://www.lcsc.com/pt/product-detail/C23070302.html?s_z=n_q_TLMS1000-GS15      | JLCPCB      |
| R1 (130Ω 0402 resistor)           |  RC0402FR-07130RL           |  20        |    $0.0800       |    https://www.lcsc.com/pt/product-detail/C477610.html?s_z=n_q_RC0402FR-07130RL     | JLCPCB      |
| U1 (NXP NT3H2111W0FHKH)           |  NT3H2111W0FHKH             |  2         |    $1.2324       |    https://www.lcsc.com/pt/product-detail/C710403.html?s_z=n_q_NT3H2111W0FHKH       | JLCPCB      |
| Total: $3,0869                    |

JLCPCB quote for assembly of 2 boards + shipping (Global Standard Direct Line: $8.48) with -$10 coupon: $26.76
<img width="1397" height="486" alt="{DEB36AE8-D00F-4259-A287-6ED29371B2AF}" src="https://github.com/user-attachments/assets/78debaf0-6e6f-4810-a422-83814d936cb9" />

(You can find the excel full BOM file in the project files)

# Grand Total: $26.76

### Extras:

This project does not need a case or anything 3D printed or designed, it is just a business card.
If you have any questions, DM me on slack: Mateus (mateus.flecha808)

## Schematic
<img width="847" height="611" alt="{6E333D57-6D36-4BEA-881A-1B5B8A142C3A}" src="https://github.com/user-attachments/assets/779c6c39-c254-4df5-aba1-c4a874873c76" />

## PCB
<img width="963" height="663" alt="{DF59C323-F329-4ACC-A75C-B1E4562BDE57}" src="https://github.com/user-attachments/assets/ad1a9c70-b6f5-4ad5-b79c-50ef9694420b" />

## Render
<img width="1026" height="663" alt="{6B454F27-4811-417E-BAE5-E6EDF0D340DB}" src="https://github.com/user-attachments/assets/4a2a6e91-fb11-4e4e-9815-c8533eb92650" />
The resistors on the SMD package sizing sections WILL NOT be assembled on the pcb! It will just be the footprints to display the different sizes.




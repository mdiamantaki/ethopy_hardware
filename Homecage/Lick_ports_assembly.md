# Lick ports

Lick Ports are used both for lick detection and reward delivery. Regarding the former, lick ports include a LED and a photo sensor positioned in parallel. Close vicinity of an object (e.g. the tongue of a mouse) reflects the infrared light and activates the photosensor. This signal is connected to the control circuit board that links them with the computational node (Raspberry Pi or PC). Regarding the latter, a tube for water delivery for correct responses is coupled to a computerized valve that controls the liquid delivery that can deliver liquid volumes with 1μL resolution. The water is channeled through a liquid delivery device when the correct electrical signal is transmitted from the port to the electric control panel leading to the opening of the respective valve. Both the LED and photo sensor wires and the reward tubes are enclosed and glued in a metal cylinder at their end point in order to prevent possible damages that could be caused by chewing or other mice activities.

<div align="center">
  <figure id="fig">
    <img src="Lick_ports_Figures/Fig.png" width="%" />
  </figure>
</div>

## Hardware Parts List

### Electronics

| # | Item                                                          | Qty       | Source                   | Identifier         | Notes                                                       |
|:-:|:-:                                                            |:-:        |:-:                       |:-:                 |:-:                                                          |
<a id="electro1"></a>
| 1 | Shielded cable                                                | 25–28 cm  | Belden                   | 1804A              | To protect the signal from electrical noise and interference |
<a id="electro2"></a>
| 2 | Optical switch (Phototransistor)                              | 1         | Onsemi                   | QRE1113            |                                                             |
<a id="electro3"></a>
| 3 | Wirewound Resistor - Through hole EP 2W (SS, 330Ω, 5%)        | 1         | TE Connectivity          | EP2WSS330RJ        | To control the current flow                                 |
<a id="electro4"></a>
| 4 | Metal Film Resistor - Through hole 0.6W 50ppm CECC (47kΩ, 1%) | 1         | Vishay / Beyschlag       | MBB0207VC4702FCT00 | To control the signal output voltage                        |

### Other Hardware

| # | Item                                                          | Qty       | Source             | Identifier  | Notes                                                                                                                         |
|:-:|:-:                                                            |:-:        |:-:                 |:-:          |:-:                                                                                                                            |
<a id="other1"></a>
| 1 | Heat shrink set                                               | 6         | Cyg, Grobotronics  | 05-00017098 | 4x1/16'' - for the individual wires 1x3/16'' - for the sensor's side 1x1/4'' or 1x3/8'' - for the phototransistor's side     |
<a id="other2"></a>
| 2 | Welded Stainless Steel Tubing 6 mm OD, 0.25 mm Wall Thickness | 3–4 cm    | McMaster-Carr      | 50415K25    |                                                                                                                               |
<a id="other3"></a>
| 3 | Unolok Disposable Needle (18G)                                | 1         | HMD                | 100445      | For reward delivery                                                                                                           |
<a id="other4"></a>
| 4 | Male Pin Header (1×40, 2.54mm)                                | 3 pins    | Grobotronics       | 19-00011916 |                                                                                                                               |
<a id="other5"></a>
| 5 | Soldering Wire Cynel 100g 0.5mm - Lead Free                   | —         | Grobotronics       | 05-00605630 |                                                                                                                               |
<a id="other6"></a>
| 6 | Bison 5 minutes epoxy glue                                    | —         | Bison              | 6305448     |                                                                                                                               |


## Step-by-Step Assembly Instructions

### Connecting the cable to the sensor

**Step 1**. Cut the ends of the phototransistor ([Electronics parts list, item #2](#electro2)). pin connectors to shorten them to a few millimeters.

**Step 2**. Strip the outer insulation from the cable ([Electronics parts list, item #1](#electro1)). to expose the individual wires, then strip each wire to reveal the inner conductors.

**Step 3**. Slide a small piece of heat shrink tube (1/16’’) onto each wire ([Other Hardware parts list, item #1](#other1)). Make sure it covers both the pins of the sensor and the exposed wire (do not heat the heat shrink tube yet, just move it to the base of each wire).

**Step 4**. Each of the 4 pins of the phototransistor corresponds to a specific wire. The pin positions start from the trimmed edge of the rectangle (Pin 1), and the rest follow in an anticlockwise direction ([Fig. 1](#fig1)).
- `Pin 1`: anode of the LED (connects to the power supply)
- `Pin 2`: cathode of the LED (connects to the ground)
- `Pin 3`: collector of the sensor (current flow after light reflection)
- `Pin 4`: emitter of the sensor (connects to the signal output)

<div align="center">
<figure id="fig1">
  <img src="Lick_ports_Figures/Fig1a.png" width="30%" />
  <img src="Lick_ports_Figures/Fig1b.png" width="24.5%" />
  <figcaption><b>Figure 1</b>: <i>Positions of the phototransistor’s pins and their corresponding wires.</i></figcaption>
</figure>
</div>

**Step 5**. Use the soldering station to connect the pins vertically to their corresponding wires as described below ([Fig. 2](#fig2)).

**Step 6**. Use a hot air gun to heat the heat shrink tubes you have added to each wire to cover the wire and the phototransistor’s pins.

<div align="center">
<figure id="fig2">
  <img src="Lick_ports_Figures/Fig2.png" width="30%" />
  <figcaption><b>Figure 2</b>: <i>Heat shrink tubes covering the exposed wires and the phototransistor’s pins.</i></figcaption>
</figure>
</div>

**Step 7**. Cut a piece of heat shrink tube (3/16’’) long enough to cover the exposed cable and the pins of the phototransistor, and pass it down the cable. Αpply the epoxy glue ([Other Hardware parts list, item #6](#other6)) to the exposed section of the cable and cover it up to the edge. Cover the exposed cable with the heat shrink tube and use the hot air gun to heat it. Ensure that the phototransistor’s pins and the wires are well covered.
Note: As the hot air gun shrinks the tube, ensure that the epoxy glue will not cover the phototransistor.

<div align="center">
<figure id="fig3">
  <img src="Lick_ports_Figures/Fig3.png" width="30%" />
  <figcaption><b>Figure 3</b>: <i>Heat shrink tube covering the phototransistor side of the lick port.</i></figcaption>
</figure>
</div>


**Step 8**. Cut a steel cylinder ([Other Hardware parts list, item #2](#other2)). long enough to cover the heat shrink tube that covers the exposed wires ([Fig. 4](#fig4)). Carefully smooth both edges of the cylinder with sandpaper to ensure the mouse is not injured while licking it.

**Step 9**. Cut the pointy edge of the 18G needle ([Other Hardware parts list, item #3](#other3)). and smooth it with sandpaper. Remove the plastic hub from the needle. Ensure that the needle is long enough to extend beyond the bottom end of the steel cylinder so that it can be properly connected to the water tube ([Fig. 4](#fig4)).

> **Note:** The needle is required only if you will use the lick port for reward delivery.

<div align="center">
<figure id="fig4">
  <img src="Lick_ports_Figures/Fig4.png" width="30%" />
  <figcaption><b>Figure 4</b>: <i>Indicative lengths of the steel cylinder and the needle relative to the lick port.</i></figcaption>
</figure>
</div>

**Step 10**. Pass the phototransistor cable and the needle through the steel cylinder. Apply epoxy glue around the heat shrink tube insulation of the phototransistor ([Fig. 5](#fig5)) and the needle, ensuring that the phototransistor’s and the needle’s tops are not covered with glue. Pull the cable and the needle so that they are on the same level and a few millimeters below the top of the steel cylinder to prevent possible damage. Fill all the empty spaces between the phototransistor and the cylinder with epoxy glue.

<div align="center">
<figure id="fig5">
  <img src="Lick_ports_Figures/Fig5.png" width="30%" />
  <figcaption><b>Figure 5</b>: <i>Phototransistor end of the lick port.</i></figcaption>
</figure>
</div>

### Connecting the cable to the resistors

You will need two resistors:
- `330Ω`: The anode of the LED is connected to the power through the 330Ω resistor to control the current flowing through the LED.
- `47kΩ`: The resistor is placed between the emitter of the phototransistor and the ground to help define the signal output voltage.

**Step 11**. Shorten the wire connected to the anode and expose the conductor. Cut both ends of the 330Ω resistor ([Electronics parts list, item #3](#electro3)) and use soldering to connect the 330Ω resistor to the wires connected to the anode and the collector. Solder the resistor horizontally across the cable, connecting the distal pin to the collector wire and the proximal pin to the anode wire ([Fig. 6](#fig6)).

<div align="center">
<figure id="fig6">
  <img src="Lick_ports_Figures/Fig6.png" width="30%" />
  <figcaption><b>Figure 6</b>: <i>Connections of the 330Ω resistor.</i></figcaption>
</figure>
</div>

**Step 12**. Shorten the wire connected to the emitter and expose the conductor. Βend one of the pins of the 47KΩ resistor ([Electronics parts list, item #4](#electro4)). Use soldering to connect the cathode wire to the straight pin and the emitter wire to the other pin ([Fig. 7](#fig7)).

<div align="center">
<figure id="fig7">
  <img src="Lick_ports_Figures/Fig7.png" width="30%" />
  <figcaption><b>Figure 7</b>: <i>Connections of the 47kΩ resistor.</i></figcaption>
</figure>
</div>

**Step 13**. Use a male pin header ([Other Hardware parts list, item #4](#other4)) with 3 pins and connect it to the cable ([Fig. 8](#fig8)). Mark the tip that is connected to the bent pin of the 47kΩ resistor so you can distinguish it (it corresponds to the signal).

<div align="center">
<figure id="fig8">
  <img src="Lick_ports_Figures/Fig8.png" width="30%" />
  <figcaption><b>Figure 8</b>: <i>Connections of the signal cable (<b>P</b>: power, <b>G</b>: ground, <b>S</b>: signal).</i></figcaption>
</figure>
</div>

**Step 14**. Cover the exposed cable and the proximal part of the male pin header with heat shrink tube (1/4’’ or 3/8’’), and heat it with the hot air gun.

### Testing the lick ports

**Step 15**. Provide a DC power supply (∼3.5V). Connect the positive terminal to the power input and the negative terminal to the ground in the pins shown in ([Fig. 8](#fig8)).

**Step 16**. Use an oscilloscope and connect it to the signal cable ([Fig. 8](#fig8)).

**Step 17**. Use your finger to simulate the lick of a mouse and observe the activation of the phototransistor ([Fig. 9](#fig9)).

<div align="center">
<figure id="fig9">
  <img src="Lick_ports_Figures/Fig9a.png" width="30%" />
  <img src="Lick_ports_Figures/Fig9b.png" width="35.5%" />
  <figcaption><b>Figure 9</b>: <i>Sensor voltage output (left: connections of the power supply and the oscilloscope, right: activation of the phototransistor).</i></figcaption>
</figure>
</div>
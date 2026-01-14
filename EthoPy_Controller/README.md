# EthoPy Controller Board and Arduino

Arduino is a microcontroller that converts the analog signal from the lick and proximity ports to digital, and a Controller Board ensures the communication between the Arduino and Raspberry Pi.
<div align="center">
<figure id="fig13">
  <img src="Controller_Figures/Fig13.png" width="%" />
</figure>
</div>

## Parts List

### Electronics

| # | Item                                      | Qty  | Source                       | Identifier              | Notes |
|:-:|:-:                                        |:-:   |:-:                           |:-:                      |:-:    |
<a id="electro1"></a>
| 1 | 40-pin Stackable Female Extra Tall Header | 1    | Grobotronics                 |                         |       |
<a id="electro2"></a>
| 2 | Arduino Nano Every                        | 1    | Arduino Store                |                         |       |
<a id="electro3"></a>
| 3 | 1x2 Female Pin Header Right Angle         | 2    | Grobotronics                 | 05-00011907             |       |
<a id="electro4"></a>
| 4 | 1x3 Female Pin Header Right Angle         | 3    | Grobotronics                 | 05-00011907             |       |
<a id="electro5"></a>
| 5 | 1x2 Male Pin Header                       | 5    | Grobotronics                 | 19-00011916             |       |
<a id="electro6"></a>
| 6 | 1x15 Female Pin Header                    | 2    | Grobotronics                 | 19-00011915             |       |
<a id="electro7"></a>
| 7 | 1x15 Male Pin Header                      | 2    | Included in Arduino kit      | —                       |       |
<a id="electro8"></a>
| 8 | Metal Film Resistor 100 Ω, 1/4W, 1%       | 4    | YAGEO                        | MFR25SFTF52-100R        |       |
<a id="electro9"></a>
| 9 | Metal Film Resistor 2.2 kΩ, 1/2W, 1%      | 3    | YAGEO                        | MFR25SFTF52-2K2         |       |
<a id="electro10"></a>
| 10 | Metal Film Resistor 1 kΩ, 1/2W, 1%       | 3    | YAGEO                        | CFR-25JB-1K0            |       |
<a id="electro11"></a>
| 11 | Metal Film Resistor 10 kΩ, 1/4W, 1%      | 3    | YAGEO                        | CFR25SJT-52-10K         |       |
<a id="electro12"></a>
| 12 | BC547B Transistor                        | 2    | onsemi / Fairchild           | BC547B                  |       |
<a id="electro13"></a>
| 13 | Aluminium Electrolytic Capacitor         | 1    | Rubycon                      | 35ZLR220MEFC8X11.5      |       |
<a id="electro14"></a>
| 14 | Tactile Push Button Switch (6×6×6)       | 2    | Same Sky                     | TS02-66-70-BK-160-SCR-D |       |
<a id="electro15"></a>
| 15 | Tactile Push Button Switch (6×6×9)       | 1    | —                            |                         | —     |
<a id="electro16"></a>
| 16 | Diode Rectifier                          | 2    | Vishay General Semiconductor | 1N4005-E3/73            |       |
<a id="electro17"></a>
| 17 | Printed Circuit Board (PCB)              | 1    | Custom                       | —                       |       |

<figure id="fig1">
  <img src="Controller_Figures/Fig1.png" width="30%" />
  <figcaption><b>Figure 1</b>: <i>EthoPy Controller Board and Arduino parts</i></figcaption>
</figure>

> **Note:** You will also need: a soldering iron, a wire cutter

## Step-by-Step Assembly Instructions

**Step 1**. Print the PCB board of the schematic ([Fig. 2](#fig2)). PCB and gerber files for JLPCB will be available in a future update.

<figure id="fig2">
  <img src="Controller_Figures/Fig2.png" width="30%" />
</figure>

**Step 2**. Solder the 1x15 female pin headers on each side of the Arduino Nano Every board ([Fig. 3](#fig3)).

<figure id="fig3">
  <img src="Controller_Figures/Fig3a.png" width="45.6%" />
  <img src="Controller_Figures/Fig3b.png" width="30%" />
</figure>

**Step 3**. Solder each resistor into its designated position on the PCB according to its resistance value ([Fig. 4](#fig4)).

<figure id="fig4">
  <img src="Controller_Figures/Fig4.png" width="30%" />
</figure>

**Step 4**. Solder the five 1x2 male pins headers into the corresponding ports on the PCB ([Fig. 5](#fig5)).

<figure id="fig5">
  <img src="Controller_Figures/Fig5.png" width="30%" />
</figure>

**Step 5**. Solder the transistors onto their correct positions on the board ([Fig. 6](#fig6)).

<figure id="fig6">
  <img src="Controller_Figures/Fig6.png" width="30%" />
</figure>

**Step 6**. Solder the diodes in the same way ([Fig. 7](#fig7)).

<figure id="fig7">
  <img src="Controller_Figures/Fig7.png" width="30%" />
</figure>

**Step 7**. Solder the tactile push button switch in the appropriate position on the board ([Fig. 8](#fig8)).

<figure id="fig8">
  <img src="Controller_Figures/Fig8.png" width="30%" />
</figure>

**Step 8**. Solder the capacitor, ensuring the longer positive lead goes into the right hole ([Fig. 9](#fig9)).

<figure id="fig9">
  <img src="Controller_Figures/Fig9.png" width="30%" />
</figure>

**Step 9**. Solder the right-angle female pin headers - two on the left side (1x2) for valves and three on the bottom (1x3) for ports and centerport ([Fig. 10](#fig10)).

<figure id="fig10">
  <img src="Controller_Figures/Fig10.png" width="30%" />
</figure>

**Step 10**. Solder the two 1x15 female pin headers for the Arduino board ([Fig. 11](#fig11)).

<figure id="fig11">
  <img src="Controller_Figures/Fig11.png" width="30%" />
</figure>

**Step 11**. Mount the Arduino board onto the previously mentioned female pin headers ([Fig. 12](#fig12)).

<figure id="fig12">
  <img src="Controller_Figures/Fig12a.png" width="37.5%" />
  <img src="Controller_Figures/Fig12b.png" width="30%" />
</figure>

**Step 12**. Solder the 40-pin extra-tall stackable female header to connect the PCB to the Raspberry Pi board ([Fig. 13](#fig13)).

<figure id="fig13">
  <img src="Controller_Figures/Fig13.png" width="30%" />
</figure>

**Step 13**. Set up the Arduino using the code that will be provided in a future update.

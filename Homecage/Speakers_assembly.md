# Speakers' Setup
Speakers are used to provide auditory cues during behavioral experiments. They can be embedded within experimental setups to deliver sound stimuli. Below are the step-by-step instructions for setting up the speakers.

<p align="center">
  <img src="Speakers_Figures/Fig.png" width="40%" />
</p>

## Hardware Parts List

### Electronics
| # | Item                           | Qty  | Source            | Identifier      | Notes                            |
|:-:|:-:                             |:-:   |:-:                |:-:              |:-:                               |
<a id="electro1"></a>
| 1 | Ultrasound Speakers 40kHz      | 2    | PUI Audio         | UT-1640K-TT-2-R | Transmitter                      |
<a id="electro2"></a>
| 2 | Speaker (Receiver)             | 1    | —                 | —               |                                  |
<a id="electro3"></a>
| 3 | Jumper wire (female-to-female) | 2    | GROBOTRONICS      | 05-00011907     |                                  |
<a id="electro4"></a>
| 4 | Heat shrink set                | 6    | Cyg, Grobotronics | 05-00017098     | Two 12cm and four 20cm Jumper wire |

### 3D Printed Parts
You will find the blueprints for the item you should 3D print [here](3d_designs/center_port_with_speakers.stl).

## Step-by-Step Assembly Instructions

**Step 1**. Select four long female-to-female jumper wires and connect one end of each to the pins of the speaker (Fig. 1). Repeat this step twice.

<p align="center">
  <img src="Speakers_Figures/Fig1.png" width="30%" />
  <br>
  <em>Figure 1: Speaker connected with female-to-female jumper wires</em>
</p>

**Step 2**. Remove the square female heads from the other ends of the wires.

**Step 3**. Solder the ends of two jumper wire (one from each speaker) together along with one small female-to-female jumper wire (after removing its square female head) (Fig. 2).

<p align="center">
  <img src="Speakers_Figures/Fig2.png" width="30%" />
  <br>
  <em>Figure 2: Soldering ends of two jumper wires</em>
</p>

**Step 4**. Cut a piece of heat shrink tube long enough to cover the exposed wires (Fig. 3).

<p align="center">
  <img src="Speakers_Figures/Fig3.png" width="30%" />
  <br>
  <em>Figure 3: Coverd part with heat shrink tube</em>
</p>

**Step 5**. Use the oscilloscope and connect one end (measuring clip) to one wire of the speaker and the grounding clip to the other wire (Fig. 5).

<p align="center">
  <img src="Speakers_Figures/Fig5.png" width="30%" />
  <br>
  <em>Figure 5: .....</em>
</p>

**Step 6**. Connect your speakers to your Raspberry Pi Pinout. First, go to the `EthoPy/Interfaces/RPPorts.py` and look at the `class RPPorts(Interface)`. Here, you see which channel corresponds to the RP GPIO pins based on what you want to connect. So for **sound** is channel `GPIO 13` (Fig. 6) that has been set in the local_conf.json, for more details check [here](https://ef-lab.github.io/ethopy_package/local_conf/#3-logging-settings-optional).

<p align="center">
  <img src="Speakers_Figures/Fig6.png" width="25%" />
  <br>
  <em>Figure 6: Hardware mapping of behavioral sensor ports to GPIO pins</em>
</p>

Connect one wire of your speaker to `GPIO13` and the other wire to `ground`(Fig. 7).

<p align="center">
  <img src="Speakers_Figures/Fig7.png" width="30%" />
  <br>
  <em>Figure 7: Rasberry Pi's GPIO pins</em>
</p>

**Step 7**. Open your RP and run a task with auditory stimuli.
# Open-field Behavioral Setup Instructions

In this protocol, the open-field behavioral setup is used to allow freely-moving mice to perform two-alternative forced choice tasks. Below, we describe the protocol to implement an open-field behavioral setup for  a visual discrimination task.

## Hardware Parts List

### Electronics

| # | Item                               | Qty | Source                                   | Identifier                                                   | Notes                                            |
|:-:|:-:                                 |:-:  |:-:                                       |:-:                                                           |:-:                                               |
<a id="electro1"></a>
| 1 | Arduino Nano Every Board           | 1   | Arduino Store                            | ABX00028                                                     |                                                  |
<a id="electro2"></a>
| 2 | PCB Controller Board               | 1   | JLCPCB (JiaLiChuang (HongKong) Co., LTD) | [custom](../EthoPy_Controller/README.md)|  |
<a id="electro3"></a>
| 3 | 13.3" Capacitive Touch Screen LCD  | 1   | Waveshare                                | HDMI LCD (H)                                                 | Presentation of stimuli, with Toughened Glass Cover, 1920×1080 |
<a id="electro4"></a>
| 4 | HDMI Cable (2m, 4K/60Hz)           | 1   | Ugreen                                   |     ED015                                                    |Connects the screen with the PC                    |

### Other Hardware

| # | Item                                      | Qty | Source       | Identifier                                                | Notes                                                |
|:-:|:-:                                        |:-:  |:-:           |:-:                                                        |:-:                                                   |
<a id="other1"></a>
| 1 | V-SLOT 2020 1500mm                        | 1   | Grobotronics | 27-99920208                                               | cut into 4 pieces of 31 cm length                    |
<a id="other2"></a>
| 2 | V-SLOT 2020 250mm                         | 4   | Grobotronics | 27-99920210                                               |                                                      |
<a id="other3"></a>
| 3 | V-SLOT 2020 500mm                         | 2   | Grobotronics | 27-99920209                                               |                                                      |
<a id="other4"></a>
| 4 | Inside Hidden Corner Bracket 3-Way        | 4   | Grobotronics | 14-00015421                                               |                                                      |
<a id="other5"></a>
| 5 | RatRig Cast - 90 Degree Corner Bracket    | 4   | Grobotronics | 27-22280012                                               |                                                      |
<a id="other6"></a>
| 6 | Plexiglass Plates                         | 7   | Local vendor | —                                                         | 2 33x33cm plates, 1 30x30cm plate, 4 35x30cm plates  |
<a id="other7"></a>
| 7 | V-Hive Enclosure Base Model               | 1   | RatRig       | HW3303GK                                                  | Insulation of light and sound                        |
<a id="other8"></a>
| 8 | ISOLFON Foam Plate                        | —   | Muziker      | —                                                         | Sound insulator                                      |
<a id="other9"></a>
| 9 | M4 Screws                                 | —   | M4X10        | —                                                         | 11x L10 & 16x L8                                     |
<a id="other10"></a>
| 10| M4 T-nuts 20x20                           | 9   | —            | 14-00085144                                               |                                                      |
<a id="other11"></a>
| 11| V-Slot Gantry Set 2020 with Three Wheels  | 2   | Grobotronics | 14-00020155                                               |                                                      |
<a id="other12"></a>
| 12| Lickport                                  | 1   | —            | [Custom](../Homecage/Lick_ports_assembly.md) | Delivers water                                       |
<a id="other13"></a>
| 13| LHD Series 3-Way Control Solenoid Valve   | 1   | Lee SLR      | LHDA0533415H                                              |                                                      |


### 3D Printed Parts

You will find the blueprints for the items you should 3D print [here](3d_designs).

| # | Item            | Qty | Filename                                                                                              | Notes |
|:-:|:-:              |:-:  |:-:                                                                                                    |:-:    |
| 1 | Lower Corners   | 4   | [open-field_bottom_corner.stl](3d_designs/open-field_bottom_corner.stl)    |       |
| 2 | Upper Corners   | 4   | [open-field_top_corner.stl](3d_designs/open-field_top_corner.stl)          |       |

## Step-by-step Assembly Instructions

The open-field behavioral setup is enclosed in the Rat-Rig V-Hive Enclosure Base Model ([Other Hardware list, item #7](#other7)). Assembly instructions can be found here.

### Enclosure & Sound Insulation

**Step 1**. To make the enclosure sound-proof, use sound insulation material (eg. ISOLFON foam plate, ([Other Hardware list, item #8](#other8))) to cover all sides of the enclosure, i.e. use 4 pieces with dimensions 50x50cm and 2 pieces with dimensions 50x43cm.

### Arena Construction

The interior of the enclosure consists of a plexiglass box (arena), where the mouse is placed during the experiment (base: 30x30cm, walls: 35x30 cm, ([Other Hardware list, item #6](#other6))).

**Step 2**. Glue (e.g. hot glue) each side of the arena and place 3D printed parts (3D printed parts list, items #1,2) on the upper and lower corners (Fig. 1).

<p align="center">
  <img src="Open-field_Figures/Fig1a.png" width="30%" />
  <img src="Open-field_Figures/Fig1b.png" width="24%" />
  <img src="Open-field_Figures/Fig1c.png" width="24%" />
  <br>
  <em>Figure 1: Open-field arena: the arena (left), the base of the arena (center) and the arena on top of its base and inside the enclosure (right) </em>
</p>

**Step 3**. Construct the following drawer to place the arena (Fig. 1).

- `Base`: 4 V-SLOT 2020 ([Other Hardware list, item #1](#other1)) with a length of 31 cm each. Connect the rails in the shape of a square and place a plexiglass (33x33cm, Other Hardware list, item #6) in the middle. When connecting the plexiglass to the square, you need to cut its corners at around 6.1 mm.

- `Columns`: 4 V-SLOT 2020 250 mm ([Other Hardware list, item #2](#other2)). Connect them on the base.

- For the `connections` of the base and columns, use Inside Hidden Corner Brackets and M4 (8mm) screws ([Other Hardware list, item #4,9](#other4,9)).

- `Rails`: 2 V-SLOT 2020 with a length of 50 cm each ([Other Hardware list, item #3](#other3)). Place the rails on the base of the box and screw them using 4 90-Degree Corner Brackets ([Other Hardware list, item #5](#other5)). To screw the brackets on the V-SLOTS, use M4 screws (10mm, ([Other Hardware list, item #9](#other9))) and M4 20x20 Tee Nuts (Other Hardware list, item #10).

- `Sliding`: Screw 2 V-Slot Gantry Sets 2020 with Three Wheels ([Other Hardware list, item #11](#other11)) on each side of the base with M4 (8mm, ([Other Hardware list, item #9](#other9))) screws and M4 20x20 Tee Nuts ([Other Hardware list, item #10](#other10)). Attach each V-Slot Gantry Set to the rails.

### Screen

**Step 4**. Place a screen ([Electronics list, item #3](#electro3)) on the one side of the box between the 2 V-slots (Fig. 2).

**Step 5**. Connect the cable for power (included in the 13.3inch Capacitive Touch Screen LCD, ([Electronics list, item #3](#electro3))) and the HDMI ([Electronics list, item #4](#electro4)) (Fig. 1).

<p align="center">
  <img src="Open-field_Figures/Fig2a.png" width="30%" />
  <img src="Open-field_Figures/Fig2b.png" width="31%" />
  <br>
  <em>Figure 2: Screen: front side of the screen (left) and back side of the screen and connections (right)</em>
</p>

### Arduino Board

**Step 6**. Follow instructions for [EthoPy Controller Board](../EthoPy_Controller/README.md)

### Lickport

**Step 7**. Follow instructions [here](../Homecage/Lick_ports_assembly.md) to make the lickport ([Other Hardware list, item #12](#other12)).

**Step 8**. Connect the lickport to the arduino board and a solenoid valve ([Other Hardware list, item #13](#other13)) in a pressurized tubing network (STAR methods, liquid delivery).

### Extra Parts

To record the experiment you need red LED lights and a camera.

> **Note:** We used Arducam 2.3MP AR0234 Color Global Shutter USB 3.0 Camera Module-With Enclosure. If you use a camera that records in darkness, lights might not be necessary.

### PC Requirements
For the Open-field setup in the EthoPy project, in addition to the standard installation, you will need to enable real-time pose estimation by installing `DeepLabCut-Live`, which provides a lightweight, low-latency inference pipeline for online tracking. To achieve frame rates greater than 30 FPS, we strongly recommend using a system running Ubuntu paired with a powerful NVIDIA GPU (minimum 8GB VRAM), as this ensures compatibility with TensorFlow and allows for GPU-accelerated inference. CPU-only systems or unsupported GPUs (e.g., Intel or AMD) will not meet the real-time demands.

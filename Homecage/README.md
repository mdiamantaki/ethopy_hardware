# Raspberry Pi Behavioral Setup
A key component of multiple Ethopy behavioral systems is the [Raspberry Pi](https://www.raspberrypi.com/), a small, affordable, single-board computer. It includes ports for HDMI, USB, Ethernet, audio, camera interface (CSI), display interface (DSI), and General Purpose Input/Output (GPIO) pins. It primarily runs on a Linux-based OS called Raspberry Pi OS, and also supports other operating systems. Below, we analytically describe the steps to implement a Raspberry Pi-based behavioral setup.

<div align="center">
  <figure id="fig1">
    <img src="RP_Figures/Fig1b.png" width="%" />
  </figure>
</div>


## Hardware Parts List

### Electronics

| # | Item                                          | Qty     | Source              | Identifier            | Notes                                                                                     |
|:-:|:-:                                            |:-:      |:-:                  |:-:                    |:-:                                                                                        |
<a id="electro1"></a>
| 1 | Raspberry Pi 4 Model B/4GB                    | 1       | Raspberry Pi             |SC0192-3|                                                                                           |
<a id="electro2"></a>
| 2 | Official Raspberry Pi 7 Touch Screen Display  | 1       | Raspberry Pi              |  2473872         |                                                                                           |
<a id="electro3"></a>
| 3 | Premium High Speed microSD Card               | 1       |  Integral  | INMSDH32G-100/70V30              |                                                                                           |
<a id="electro4"></a>
| 4 | EthoPy Controller Board                       | 1       | [Custom](../EthoPy_Controller/README.md)              |                       |                                                                                           |
<a id="electro5"></a>
| 5 | Lick Ports                                    | 2 or 3  | [Custom](Lick_ports_assembly.md)              |                       | 2 to detect licks and deliver water, 1 can be used as a proximity indicator (center port) |
<a id="electro6"></a>
| 6 | Beam Photoelectric Sensor                     | 1       | HAITRONIC               | HR0172          |Can be used as a proximity indicator (center port)                                         |
<a id="electro7"></a>
| 7 | Solenoid valves                               | 2       | LEE SLR         | LHDA0533415H               |                                                                                           |
<a id="electro8"></a>
| 8 | Ultrasound Speakers 40kHz                     | 2       | PUI Audio      | UT-1640K-TT-2-R    |For auditory experiments. See: [Speakers_assembly](Speakers_assembly.md)                                                                    |

### Other Hardware

| # | Item                                | Qty | Source      | Identifier    | Notes       |
|:-:|:-:                                  |:-:  |:-:          |:-:            |:-:          |
<a id="other1"></a>
| 1 | M3 screws                           | 6   | Grobotronics  | M3X12/D7985  |             |
<a id="other2"></a>
| 2 | Raspberry Pi 4 Heatsink (40x30x5mm) | 1   | Grobotronics  | 49-00012076  |             |

### 3D Printed Parts
You will find the blueprints for the items you should 3D print [here](3d_designs).
| # | Item                          | Qty | Filename                                                                                            | Notes                           |
|:-:|:-:                            |:-:  |:-:                                                                                                  |:-:                              |
| 1 | Base                          | 1   | [base.stl](3d_designs/base.stl)                                            | Includes the lick port holders  |
| 2 | Screen holder                 | 2   | [screen_holder.stl](3d_designs/screen_holder.stl)                          |                                 |
| 3 | Center port holder            | 1   | [center_port.stl](3d_designs/center_port.stl)                              |                                 |
| 4 | Center port & speaker holder  | 1   | [center_port_with_speakers.stl](3d_designs/center_port_with_speakers.stl)  | Includes speaker holders        |
| 5 | Pins                          | 1   | [pin.stl](3d_designs/pin.stl)                                              | For mounting the center port holder |


<figure id="fig1">
  <img src="RP_Figures/Fig1a.png" width="30%" />
  <img src="RP_Figures/Fig1b.png" width="38.7%" />
  <figcaption><b>Figure 1</b>: <i>RP setup (top: 3D printed parts of the RP’s base, bottom: assembled RP base).</i></figcaption>
</figure>


## Step-by-step Assembly Instructions

**Step 1**. Install the [operating system of the RPi](https://www.raspberrypi.com/documentation/computers/getting-started.html#installing-the-operating-system). In our experiments, we have used the [Bullseye Raspberry Pi OS](https://www.raspberrypi.com/news/raspberry-pi-os-debian-bullseye/).

**Step 2**. Mount the Raspberry Pi to the Raspberry Pi Touch Display and connect the Flat Flexible Cable and the power of the Touch Display to the Raspberry Pi [instructions](https://www.raspberrypi.com/documentation/accessories/display.html).

**Step 3**. Connect the Ethopy Controller Board to the RPi.

**Step 4**. Add a heatsink ([Other Hardware parts list, item #2](#other2)) on the back of the RP to avoid excessive warming.

**Step 5**. Plug in the side and the center ([lick](Lick_ports_assembly.md) or interruptor) ports, and the valves to the EthoPy Controller Board, to the positions indicated on the board.

**Step 6**. Connect the valves to the water supply. Each LEE valve ([Electronics parts list, item #7](#electro7)) has 3 pipe-edges (1) to be connected to the lick port tube, (2) to be connected with the water supply tube, and (3) to be connected with the other valve through a tube and 2 pins to be connected to the board ([Fig. 2, left](#fig1)).

In the RP setup, the upper valve corresponds to the left lick port, and the bottom valve corresponds to the right lick port ([Fig. 2, right](#fig1)).

<figure id="fig2">
  <img src="RP_Figures/Fig2a.png" width="30%" />
  <img src="RP_Figures/Fig2b.png" width="30%" />
  <figcaption><b>Figure 2</b>: <i>Connections of the solenoid valve (left: positions of the tubes, right: placement of the valves on the RP board).</i></figcaption>
</figure>

**Step 7**. Connect to the RPi and run a test task.

- ssh username@ip_address 

> For more information, visit their: [Rasberry Pi: Remote access](https://www.raspberrypi.com/documentation/computers/remote-access.html)

- Follow the instructions on how to [install/run EthoPy](https://ef-lab.github.io/ethopy_package/installation/)

> **Note (Optional):** Rename the RP and set a static IP address.

> **Tip:** When using multiple RPs, it is best to use unique names that follow a consistent structure and assign static IP addresses to each RP to facilitate identification and management. To do this, connect to the RP and change its default name following the [instructions](https://ef-lab.github.io/ethopy_package/raspberry_pi). It is recommended to use a fixed prefix followed by an incremental number for each RP added.

# mini-laser-printer
My store, http://www.makerstore.fun, offers both finished products and DIY kits. We help you save time and money by sourcing parts for you.
If you prefer to source them yourself, you can shop on platforms like AliExpress or Amazon, though the total cost may be higher. If you choose this option, please purchase the following items in order:
| Item Name | Specs/Parameters | Qty | Recommendations & Tips |
| :--- | :--- | :---: | :--- |
| Custom Motherboard (PCB) | Integrated Large & Small Board | 1 Set | Includes both boards. |
| NANO Development Board | - | 1 | Must select Mini USB interface version. |
| A4988 Stepper Driver | - | 2 | Recommended to keep one as a spare. |
| FPC Flexible Cable | 10cm, 1.0mm-4P | 1 | Critical Spec: Reverse/Flip connector. |
| Data Cable | Matching Interface | 1 | Must match the dev board (usually Mini USB). |
| Laser Head | 5V 250mW | 1 | For wood/leather/paper. Dark objects work best. Cannot engrave metal. |
| Case Printed Parts | PLA/PETG | 1 Set | - |
| Screws | M2.5 * 8 Countersunk | 17 | For fixing frame and circuit board. |
| Screws | M2 * 4 Countersunk | 8 | For fixing motor bracket and adapter board. |
| Micro Stepper Motor | 58mm screw rod, 3mm pitch | 3 | Recommend Samsung ODD salvage motors (longer stroke, cost-effective). |
| Cooling Fan | 5010 Blower, 5V | 1 | Check holes: Recommend 4-hole mount. Common 3-hole fans need modification. |
| Optical Shaft (Rod) | Diameter 3mm | 4 | Lengths: 100mm (2 pcs) and 82mm (2 pcs). Search "dowel pins" or custom. |
| Grease | - | 1 | Apply to optical rods and screw rods. |
| Power Supply | 12V/9V 2A | 1 | Interface DC5.5*2.1. Do not exceed 12V (On-board components rated 16V). |
| Light Shield | Green Translucent Plastic | 1 | Recommend Green Cellophane/PVC (not sticker). Filters red light. |
| Safety Goggles | Green | 1 | Must wear! Darker is better. Never look directly at the laser. |

Download the circuit files from the repository and choose a cost-effective PCB manufacturer to fabricate the board. Below is the list of required components:
| Item Name | Specs / Parameters | Qty |
| :--- | :--- | :---: |
| FPC Connector | 4P-1mm, Bottom-contact Flip-lock | 2 |
| | 4P-1mm, Top-contact Drawer | 3 |
| XH2.54 Terminal | 2P, Horizontal | 1 |
| PH2.0-2P | 2P, Horizontal | 1 |
| DC044 Power Jack | DC044 Plastic Shell | 1 |
| 2.54mm Single Row Female Header | 1*15P | 2 |
| | 1*8P | 4 |
| SMD Aluminum Electrolytic Capacitor | 16V 220UF, 6.3*7.7mm | 4 |
| 1206 SMD Capacitor | 0.1UF | 3 |
| 1206 SMD Resistor | 10Ω | 1 |
| | 10K | 4 |
| MOSFET | 30N3P | 1 |
| Power Regulator | XL1509-5.0 | 1 |
| Power Inductor | 68UH | 1 |
| Diode | SS34, SMA Package | 1 |





When using this printer, please pay attention to electrical safety and use the provided protective goggles!

If you purchase the finished product, no firmware flashing is required. For the DIY kit, please upload the program to the Nano board.To make changes, modify the code in the repository and re-flash the ATmega328 main controller. If you don't need to customize the firmware, simply ignore this notice.


#User Guide

1.If this is your first time using the device, please open the repository, access the motherboard driver folder, and install the CH341SER driver.

2.After installing the motherboard drivers, please run the host software installer. Once completed, select LaserGRBL to install the control software for this laser printer. Finally, select the COM port connected to your computer from the left panel and click Connect. All configuration is now complete.

Assembly Instructions: 
First, install the motor as shown in the figure and tighten the screws.
![image](images/1.png)

Take two short shafts and insert them halfway as shown in the figure. Install the laser head into the fixture, insert the short shafts, and finally push the shafts all the way into the bottom.
![image](images/2.png)

Assemble the two stepper motors as shown.
![image](images/3.png)

Assemble the turbofan as shown.
![image](images/4.png)

Take out the mainboard, use pliers to snap off the small board as shown, and then screw it onto the back of the laser slide rail.Warning: Please ensure the stepper motor driver board is oriented as shown in the figure. Incorrect installation may cause damage to the board.
![image](images/5.png)

Then, connect the stepper motor flat cable to the small board.
![image](images/6.png)

Secure the mainboard to the mounting holes.
![image](images/7.png)

Take out the long shaft and insert the laser slide rail into the main body.
![image](images/8.png)

Connect the laser power supply and the flat cable.
![image](images/9.png)

Finally, install the remaining parts and tighten the screws.


Note: For this drawer-style FPC connector, the metal contacts on the flat cable must face upwards when inserted.
![image](images/11.png)

For this clamshell FPC connector, the metal contacts on the flat cable must face downwards when inserted.
![image](images/12.png)

Debugging:
Connect the 12V power supply. Connect one probe of the multimeter to the metal shell of the USB port on the Nano board, and connect the other probe to the potentiometer of the stepper motor driver as shown in the figure.
Check the voltage and use a small flat-head screwdriver to adjust the left stepper motor driver to 0.28V and the right one to 0.5V.
![image](images/13.png)

If the sliding is not smooth, fine-tuning of the various structural components may be required.


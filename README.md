# BrodBoost-C2

BrødBoost-C2 is a project of Axiometa, it is available for sale at [axiometa.io](https://www.axiometa.io/products/axiometa-brodboost-c2-breadboard-power-supply)

BrødBoost-C2 is a USB-C breadboard power supply that delivers clean 5V and 3.3V power directly to your breadboard. It features short-circuit fuse protection, USB ESD protection, an ideal diode for reverse polarity safety, a load switch with soft startup, and ferrite bead filtering for low-noise operation. An on/off switch and power LED keep you in control, while USB data passthrough keeps your lines accessible.

<img width="3000" height="1688" alt="169_bbs0004" src="https://github.com/user-attachments/assets/2ba027ab-2758-4469-a374-c76857b5c18a" />

# Overview
<img width="2735" height="965" alt="Overview_BBS0004" src="https://github.com/user-attachments/assets/b8a81ff6-8352-46bb-aa7c-88f4a7971bf2" />


# Compatibility
<img width="2669" height="1160" alt="Dimensions_BBS0004" src="https://github.com/user-attachments/assets/5ea27d54-e684-4f5f-8c80-b289b487ce54" />


# Voltage Selection
Both voltage rails can be independently selected or simultaneously set to 5.0 V or 3.3 V by moving around the jumper cap. Although the jumper cap design has received mixed opinions, it is implemented here as a safety feature and to be cautios of BOM. The design requires deliberate jumper cap movement, which helps prevent accidental voltage changes from 3.3 V to 5.0 V that might occur if a switch were used.
<img width="2668" height="1102" alt="HOWto_BBS0004" src="https://github.com/user-attachments/assets/24b0b958-e7f3-4e33-aa41-fce7a5575a99" />


# Schematic
A USB-C receptacle accepts a standard USB-C cable. The CC1 and CC2 lines are pulled to ground through 5.1 kΩ resistors to negotiate 5 V from the host. Power flows through a ferrite bead for noise suppression, a 1 A polyfuse for short-circuit protection, and decoupling capacitors.
An ideal diode provides reverse polarity and overvoltage protection. A load switch with controlled soft startup prevents inrush current. The power switch and red power LED sit in series on the main rail. USB ESD protection is included on the data and power lines.
Step-down conversion from 5 V to 3.3 V is handled by the AP2114H-3.3TRG1 LDO regulator. Both voltage outputs are routed to 1×3 2.54 mm headers for rail selection. A separate header provides access to 5 V, 3.3 V, ground, and USB data lines.
<img width="2703" height="1862" alt="image" src="https://github.com/user-attachments/assets/b4928ede-d03d-4cc9-91f5-1c4b3497827b" />

# PCB Design
BrodBoost-C2 is a two-layer PCB measuring 12 mm by 54.0 mm, designed to maximize trace width and optimize the switching regulator's ground return path. This layout comfortably supports the nominal device current of approximately 1 A.

**Top**
<img width="3614" height="847" alt="T_BBS0004" src="https://github.com/user-attachments/assets/515c4f96-dcaa-44ca-9c97-efa0c467b682" />
**Bottom**
<img width="3614" height="847" alt="B_BBS0004" src="https://github.com/user-attachments/assets/f3780d17-396f-4bf6-b2b9-97f77a8f052f" />

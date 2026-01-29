# Hexapod PCB

![Preview](media/preview.png)

This repository contains all the files necessary to order the PCB for my hexapod robot.

For a complete overview of the project, refer to the [main Hexapod repository](https://github.com/ggldnl/Hexapod). Additionally, you may want to check out the repository containing the [Hardware](https://github.com/ggldnl/Hexapod-Hardware).

<table>
  <tr>
    <td><img src="media/render.png" alt="Render"></td>
    <td><img src="media/image_1.png" alt="PCB"></td>
  </tr>
</table>

## 🔧 Components

<div align="center>

| Component               | Quantity     | Notes                               | TH/SMD      | Optional     |
|-------------------------|--------------|-------------------------------------|-------------|--------------|
| 1x3 male header         | 24           | Connect the motors to the PCB       | TH          | No           |
| 1x3 female header       | 24           | Connect the motor headers on the Servo2040 to the PCB | TH | No  |
| 1x17 female header      | 1            | Connect the Servo2040 GPIOs to the PCB | TH       | No           |
| 2x20 female header      | 1            | Connect the Raspberry to the PCB    | TH          | No           |
| 0603 LED                | 1            | Signal 5V                           | SMD         | YES          |
| 100 ohm 0603 resistor   | 1            | LED                                 | SMD         | YES          |
| ITS4141NHUMA1           | 1            | Smart high-side power switch        | SMD         | NO           |

</div>

Approximate cost for PCB manufacturing: around 50€
Approximate cost for PCB assembly (only SMD components): around 30€
Approximate cost for sourcing TH components: around 10€ (assorted pack of headers on Amazon containing a lot more than what you will need for the build)

PCB manufacturing and assembly for this project are sponsored by [PCBWay](https://www.pcbway.com/). The boards came back perfect and I can’t recommend their service enough.

<p align="center">
  <img src="media/image_2.png" alt="Assembled PCB by PCBWay" width="600">
</p>

## 📝 Notes

1. Some ground connections are not enforced, a DRC check will fail. The problem lies on some ground pins on both the Raspberry and the Servo2040. These are internnally connected so it won't cause any issue.
2. The traces carrying current to the motors should be fine (1.524 mm wide, 1oz, top layer) for the load I expect, but I'll keep an eye on them to check if they overheat.
3. The traces carrying signals from the servo2040 to the pins at the bottom of the PCB are a bit long, but this shouldn't be a problem.

## 🤝 Contribution

Feel free to raise issues or contribute improvements to this repository. For further information about the project, check out the [main Hexapod repository](https://github.com/ggldnl/Hexapod). Give a ⭐️ to this project if you liked the content.

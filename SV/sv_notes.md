**Starting the SV with book/cadence**
SV is an extension of Verilog-2001

![](assets/20250204_170844_image.png)

---

Data Types:

---


| DataType | Description | Sign             | state        |
| :--------- | ------------- | ------------------ | -------------- |
| bit      | 1bit        | default unsigned | 2 state(0/1) |
| byte     | 8bit        | default signed   |              |
| shortint | 16bit       | default signed   |              |
| int      | 32bit       | default signed   |              |
| longint  | 64bit       | default signed   |              |
| integer  |             |                  |              |
| logic    |             |                  | 4 state      |

Verilog has Strict Data type rules:\
▪ Variables(registers)(integer, real, reg, time) are assigned values in procedural blocks.
▪ Netsare driven by continuous assignments, module inputs, module instance outputs, or primitive instances.

=>These lead to the following connectivity characteristics:
▪ Module inputs are always nets.
▪ Module outputs are variablesif driven by a procedural block, or netsin all other cases.
▪ Connections to the input ports of a module instance are variables if driven by a procedural block, or nets in all other cases.
▪ Connections to the output ports of a module instance are always nets.
▪ Connections to bidirectional inoutports are always nets.
This means that module input ports must connect internally to nets, module output ports must connect
externally to nets, and module inoutports must connect both internally and externally to nets. Only
module output ports can connect internally to variables.

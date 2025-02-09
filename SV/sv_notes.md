**Starting the SV with book/cadence**
SV is an extension of Verilog-2001

![](assets/20250204_170844_image.png)

---

==>&emsp;&emsp;&emsp;&emsp;&emsp;Data Types:

---


| DataType | Description                                 | Sign             | state        |
| :--------- | --------------------------------------------- | ------------------ | -------------- |
| bit      | 1bit                                        | default unsigned | 2 state(0/1) |
| byte     | 8bit                                        | default signed   | 2 state      |
| shortint | 16bit                                       | default signed   | 2 state      |
| int      | 32bit                                       | default signed   | 2 state      |
| longint  | 64bit                                       | default signed   | 2 state      |
| integer  | 32bit                                       | default signed   | 4 state      |
| logic    | 1bit                                        | default unsigned | 4 state      |
| reg      | 1bit                                        | default unsigned | 4 state      |
| wire     | 1bit                                        | default unsigned | 4 state      |
| time     | 64bit                                       | default unsigned | 4 state      |
| real     | double precision<br /><br /> floating point |                  | 2 state      |

Verilog has Strict Data type rules:<br>
▪ Variables(registers)(integer, real, reg, time) are assigned values in procedural blocks.<br>
▪ Netsare driven by continuous assignments, module inputs, module instance outputs, or primitive instances.<br>

=>These lead to the following connectivity characteristics:<br>
▪ Module inputs are always nets.<br>
▪ Module outputs are variablesif driven by a procedural block, or netsin all other cases.<br>
▪ Connections to the input ports of a module instance are variables if driven by a procedural block, or nets in all other cases.<br>
▪ Connections to the output ports of a module instance are always nets.<br>
▪ Connections to bidirectional inoutports are always nets.<br>

This means that module input ports must connect internally to nets, module output ports must connect
externally to nets, and module inoutports must connect both internally and externally to nets. Only
module output ports can connect internally to variables.<br>

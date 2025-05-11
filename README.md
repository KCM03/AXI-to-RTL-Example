# AXI-to-RTL-Example
Quick and Easy Reminder of how to interface a processing system (PS) to RTL programmable logic (PL) on an FPGA for hardware acceleration

## Hardware Basics
- To create an example project, choose the the "create and package new ip" from the "tools" dropdown menu in vivado.<br />
![image](https://github.com/user-attachments/assets/11a137b7-8d17-42aa-8a01-c656a2646d55)<br />
Create a New AXI4 Peripheral:<br />

![image](https://github.com/user-attachments/assets/06ef9ebc-9cba-47e1-a57a-565deb18e87d)<br />
The following menus displays the current state of the created peripheral (i.e, an axi-lite slave interface with 4 storage registers); leave these unaltered for now.<br />

<img width="698" alt="image" src="https://github.com/user-attachments/assets/bb3d6a6a-f466-4f7e-9b59-b722f15ca779" /><br />
On creation, select "Edit IP" to create a new project in while the IP block-desing HDL wrapper will be declared.<br /><br />

<img width="473" alt="image" src="https://github.com/user-attachments/assets/213c1b3a-3fac-45d0-aebc-2e209e614d70" /><br />
Now, Vivado will create a top-level wrapper HDL file (for this example slave_out, the name of the project) and a Sub-hierarchical axi-slave entity to faciliate the handshake protocol between the axi-master (the processor) and the created IP.<br />

<img width="898" alt="image" src="https://github.com/user-attachments/assets/8a7b50f5-93bf-4481-b289-b392027b8cdc" /><br />

The AXI controller entity contains the generic AXI-lite input and output ports This entity contains the registers "slv_regXX" which contain the data written by the master to this slave interface; the register being written to is chosen through the S_AXI_AWADDR port. This address input is buffered by the "mem_logic" signal.<br />

<img width="473" alt="image" src="https://github.com/user-attachments/assets/8d927e0a-c77d-4c2e-b6ea-c3dc55dd9c89" /><br />

<img width="423" alt="image" src="https://github.com/user-attachments/assets/73a44f3b-1207-45d0-83a4-fe22cf54aa6a" /><br />
<img width="460" alt="image" src="https://github.com/user-attachments/assets/8151f6a9-89c1-42ff-85d7-f77d45218968" /><br />







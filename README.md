# AXI-to-RTL-Example
Quick and Easy Reminder of how to interface a processing system (PS) to RTL programmable logic (PL) on an FPGA for hardware acceleration

# Hardware Basics
- To create an example project, choose the the "create and package new ip" from the "tools" dropdown menu in vivado.
![image](https://github.com/user-attachments/assets/11a137b7-8d17-42aa-8a01-c656a2646d55)
Create a New AXI4 Peripheral:
![image](https://github.com/user-attachments/assets/06ef9ebc-9cba-47e1-a57a-565deb18e87d)
The following menus displays the current state of the created peripheral (i.e, an axi-lite slave interface with 4 storage registers); leave these unaltered for now.
<img width="698" alt="image" src="https://github.com/user-attachments/assets/bb3d6a6a-f466-4f7e-9b59-b722f15ca779" />
On creation, select "Edit IP" to create a new project in while the IP block-desing HDL wrapper will be declared.
<img width="473" alt="image" src="https://github.com/user-attachments/assets/213c1b3a-3fac-45d0-aebc-2e209e614d70" />
Now, Vivado will create a top-level wrapper HDL file (for this example slave_out, the name of the project) and a Sub-hierarchical axi-slave entity to faciliate the handshake protocol between the axi-master (the processor) and the created IP.
<img width="898" alt="image" src="https://github.com/user-attachments/assets/8a7b50f5-93bf-4481-b289-b392027b8cdc" />





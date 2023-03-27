# Flood-Sensors-KiCad-Files

This repository contains KiCad files for my master's thesis IoT infrastructure, which includes water leak detection sensors. It does not include any source code as it is the intellectual property of the Nicolaus Copernicus University in Torun and cannot be published here. The infrastructure is divided into a web service made with Node.js and EJS, a PCB master board that communicates with the web service using TCP or UDP protocols, and a set of leak detection sensors that communicate with the master using the Modbus protocol and notify it when a leak is detected. The Master board sends a notification message to the web service about the leak.

### Folder Structure:

- Master - KiCad project of the Master PCB
- Slave - KiCad project of the Slave PCB
- Datasheet - datasheets of used chips/components
- KiCad_symbols - KiCad library files made by me
- Pictures - some pictures

### Master Board:

The Master board is responsible for managing communication between the web service and the Slave boards. It features an ATmega128 microcontroller, which has more RAM memory than the ATmega32 mentioned in the documentation. Communication with the web service is handled by the ENC28J60 chip, and to communicate with slaves, the MAX485 chip is used.

### Slave Board:

The Slave board detects water leaks and communicates with the Master board using the MAX485 chip. It features an LM393 chip for detecting the leak and is controlled by an ATmega32 microcontroller.

### Web Service:

The web service is built using Node.js and EJS and is responsible for receiving notification messages from the Master board about water leaks. It allows users to view the status of the system.

### License:

This project is licensed under the MIT License - see the LICENSE file for details.

### Working devices:
<img src="https://github.com/ernest-czachorowski/Flood-Sensors-KiCad-Files/blob/main/Pictures/Working.jpg" widht="500">

### Master board:
<img src="https://github.com/ernest-czachorowski/Flood-Sensors-KiCad-Files/blob/main/Pictures/Master.jpg" widht="500">

### Slave board:
<img src="https://github.com/ernest-czachorowski/Flood-Sensors-KiCad-Files/blob/main/Pictures/Slave.jpg" widht="500">

### Prototype board:
<img src="https://github.com/ernest-czachorowski/Flood-Sensors-KiCad-Files/blob/main/Pictures/Prototype_1.jpg" widht="500">

### Prototype board:
<img src="https://github.com/ernest-czachorowski/Flood-Sensors-KiCad-Files/blob/main/Pictures/Prototype_2.jpg" widht="500">

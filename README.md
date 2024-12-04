# Smart-Door-Locking-Security-System
# Project Overview
This project was created as part of an embedded systems diploma, designed to enhance security through a layered architecture approach. It utilizes two ATmega32 microcontrollers to implement a secure and adaptable door security system.

## **Key Features**

### **1. Human Machine Interface (HMI_ECU)**
- **User Interaction:** Manages all interactions via a keypad and LCD display.  
- **Password Setup:** Enables users to create a 5-digit password with confirmation.  
- **Main Menu:** Displays options for door control and password management.

### **2. Control ECU**
- **System Core:** This module processes user inputs and controls system operations.  
- **Password Verification:** Compares the entered password with the stored one in the EEPROM.  
- **Error Handling:** Provides multiple attempts to enter the correct password, activating a buzzer for incorrect entries.

### **3. Security Features**
- **Password Storage:** Securely stores the password in EEPROM and allows updates.  
- **Unlock Door:** When the correct password is entered, it activates a DC motor to unlock the door.  
- **Password Change:** Lets users change the password after verifying the current one.

## **Components Used**
- **GPIO:** Manages connections to peripherals.  
- **Keypad:** Used for password input.  
- **LCD:** Displays instructions, status, and menu options.  
- **Timer:** Manages operation timing and delays.  
- **UART:** Handles serial communication between microcontrollers.  
- **I2C:** Facilitates communication with the EEPROM.  
- **EEPROM:** Stores and retrieves the password securely.  
- **Buzzer:** Alerts users with sound when the wrong password is entered.  
- **DC-Motor:** Controls the locking mechanism of the door.

## **Microcontroller**
- **ATmega32:** Two ATmega32 microcontrollers are used—one for the HMI_ECU and another for the Control_ECU.

## **System Workflow**

### **1. Create System Password**
The system prompts the user to set and confirm a 5-digit password.

### **2. Main Menu Options**
The LCD displays the main menu, offering options to either open the door or change the password.

### **3. Open Door**
The user enters the password to unlock the door. If correct, the DC motor is activated to unlock the door.

### **4. Change Password**
Users can change the password by verifying the current password and setting a new one.

### **5. Password Validation**
The system ensures that the entered password matches the stored one. If incorrect, the user is allowed multiple attempts, with the buzzer sounding on each failed entry.
## Simulation Screenshots
![System 1](https://github.com/hassanowis/Smart-Door-Locking-Security-System/blob/main/imgs/Sytem%201.png?raw=true)  
*Figure 1: Enter the Password *

![System 4](https://github.com/hassanowis/Smart-Door-Locking-Security-System/blob/main/imgs/System%204.png?raw=true)  
*Figure 2: password is correct*

![System 3](https://github.com/hassanowis/Smart-Door-Locking-Security-System/blob/main/imgs/System%203.png?raw=true)  
*Figure 3: password is wrong*

## **Usage Instructions**

### **1. Initial Setup**
Power on the system and follow the prompts to configure the initial password.  

### **2. Operating the Door Lock**
To unlock the door, select the "Open Door" option in the main menu and input the password.  
To change the password, select "Change Password," enter the current password, and set a new one.

### **3. Error Handling**
If an incorrect password is entered, the buzzer will sound, and the user can attempt again. After several failed attempts, the system will temporarily lock out to prevent further attempts.

# **Barebones Digital Lock**  
A passcode-protected digital lock built entirely using basic logic circuits—no microcontrollers involved!  

## **Project Overview**  
The **Barebones Digital Lock** is a simple yet effective demonstration of how a secure passcode system can be implemented using combinational and sequential digital logic. This project showcases the power of flip-flops, logic gates, and counters to create a fully functional lock system, emphasizing simplicity and resourcefulness by avoiding microcontrollers or advanced processing units.

## **Key Features**  
- **4-Digit Passcode Security**: Securely stores a 4-digit passcode, with each digit ranging from 0–9.  
- **Mode Switching**: A `#` key is used to toggle between modes (e.g., passcode input and verification).  
- **Minimal Components**: Designed using only basic components like flip-flops, logic gates, and encoders.  
- **Efficient Design**: Combines combinational and sequential circuits for streamlined operation.  

## **How It Works**  
1. **Keypad Input**: A matrix keypad is used to enter digits of the passcode.  
2. **Encoder**: Converts each keypress into a unique 4-bit binary value.  
3. **Sequential Storage**: Flip-flops store the passcode digits sequentially, controlled by a counter and AND gates.  
4. **Mode Control**: A T flip-flop toggles between input and verification modes using the `#` key.  
5. **Validation Logic**: Logic circuits compare the entered code with the stored passcode to grant or deny access.

## **Components Used**  
- **Logic Gates**: AND, OR, NOT, and NAND gates.  
- **Flip-Flops**: D and T flip-flops for storage and mode switching.  
- **Keypad**: A standard matrix keypad for passcode input.  
- **Counter**: Sequentially enables flip-flops for digit-by-digit storage.  

## **Why "Barebones"?**  
This project eliminates the need for microcontrollers, making it a cost-effective and straightforward solution for basic access control. It’s ideal for understanding and demonstrating the fundamentals of digital logic design.


## **How to Replicate**  
1. **Build the Circuit**: Follow the circuit diagrams provided in the repository.  
2. **Gather Components**: A list of required components is available [here](#).  
3. **Simulate**: Use simulation software like Proteus or Logisim to test the design.  
4. **Assemble**: Assemble the hardware and test functionality.

## **Team**  
This project was collaboratively developed by:  
- [Liana Shams](#)  
- [Abdullah Salim](#)  
- [Mohammad Yasir](#)  
- [Afsana Umme Kulsum Eaty](#)

## **License**  
This project is licensed under the [MIT License](LICENSE).

---

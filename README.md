# **Barebones Digital Lock**  
A passcode-protected digital lock built entirely using basic logic circuits—no microcontrollers involved!  

## **Project Overview**

The **Barebones Digital Lock** is a simple yet effective demonstration of how a secure passcode system can be implemented using combinational and sequential digital logic. This project showcases the power of flip-flops, logic gates, and counters to create a fully functional lock system, emphasizing simplicity and resourcefulness by avoiding microcontrollers or advanced processing units.

This project was developed as part of the **CSE231 - Digital Logic Design** course at **North South University** during the **Spring 2024 Semester**. The course was instructed by **Dr. Khaleda Akter**, who encouraged projects that were not overly simplistic and avoided microcontroller usage. The system was independently designed and implemented by the team members.

## **Key Features**

- **4-Digit Passcode Security**: Securely stores a 4-digit passcode, with each digit ranging from 0–9 and extended inputs A, B, C, and D.  
- **Control Characters**: The `*` key is used to reset the passcode, while the `#` key switches between authentication and registration modes.  
- **Conditional Access**: Switching to registration mode is only allowed if the stored authentication and registration passcodes match, ensuring security. However, switching back to authentication mode is always possible.  
- **Minimal Components**: Designed using only basic components like flip-flops, logic gates, and encoders.  
- **Efficient Design**: Combines combinational and sequential circuits for streamlined operation.  

## **How It Works**

1. **Keypad Input**: A matrix keypad is used to enter digits of the passcode, allowing inputs 0–9 and A–D.  
2. **Control Characters**:  
   - The `*` key resets the passcode.  
   - The `#` key toggles between authentication and registration modes.  
3. **Encoder**: Converts each keypress into a unique binary value.  
4. **Sequential Storage**: Flip-flops store the passcode digits sequentially, controlled by a counter and logic gates.  
5. **Mode Control Logic**:  
   - Switching to registration mode (`*`) is blocked if the stored digits in the authentication and registration flip-flops do not match, preventing unauthorized access.  
   - Switching to authentication mode (`#`) is always permitted.  
6. **Validation Logic**: Logic circuits compare the entered code with the stored passcode in authentication mode to grant or deny access.  

## **Implementation Challenges**

1. **Keypad Limitation**:  
   During the implementation, the team initially purchased a 4x4 matrix keypad for input purposes. However, it was discovered that using this keypad required an Arduino or similar microcontroller, which was not permitted for this project. To overcome this limitation, the team innovatively created a custom keypad using individual switches, ensuring compliance with the project’s constraints while maintaining full functionality.

2. **Clock Signal Instability**:  
   Giving the clock signal using a physical switch introduced unpredictability. This caused the counters used to control the cursor positions for the authentication and registration modes to behave erratically. The system would sometimes fail to register inputs, or worse, cause three digits to change to the same value at once, disrupting the passcode functionality.  
   To resolve this issue at the hardware level, a **555 timer** in monostable mode was used alongside a **capacitor** to stabilize the clock signal. This ensured that the counters received consistent and predictable pulses, eliminating the erratic behavior and improving overall reliability.

## **Why "Barebones"?**  
The name **"Barebones"** reflects the simplicity and fundamental nature of this project. It was designed to demonstrate the core principles of digital logic design using basic, easily available components—without relying on microcontrollers, advanced processors, or complex systems. By utilizing flip-flops, logic gates, and counters, this project showcases how secure systems can be built from the ground up using only the essential building blocks of digital electronics. The aim was to create a fully functional system with minimal resources, ensuring that the project was accessible and easy to understand for those learning the fundamentals of digital circuits.

## **How to Replicate**  
1. **Build the Circuit**: Follow the circuit diagrams provided in the repository.  
2. **Gather Components**: A list of required components is available [here](#component-list).  
3. **Simulate**: Use simulation software like Logisim to test the design.  
4. **Assemble**: Assemble the hardware and test functionality.

## **Component List**

|            | Component                             | Quantity |
|------------|---------------------------------------|----------|
| 1          | 9V Battery                            | 1        |
| 2          | Bread Board                           | 12       |
| 3          | Common Anode 7-segment display        | 10       |
| 4          | Common Cathode 7-segment display      | 8        |
| 5          | IC 7404 Hex Inverter                  | 2        |
| 6          | IC 7408 Quadruple 2-input AND gates   | 5        |
| 7          | IC 74148 8:3 Priority Encoder         | 2        |
| 8          | IC 7432 Quadruple 2-input OR gates    | 6        |
| 9          | IC 7447 Common Anode BCD Decoder      | 8        |
| 10         | IC 7473 Dual JK Flip-flops            | 2        |
| 11         | IC 7474 Dual D Flip-flops             | 16       |
| 12         | IC 7486 Quadruple 2-input XOR gates   | 4        |
| 13         | Push Switch                           | 16       |
| 14         | Set of Jumper Wires (40pcs)           | 5        |
| 15         | Wire Box                              | 3        |

## **Team**  
This project was collaboratively developed by:  
- [Liana Shams](#)  
- [Abdullah Salim](https://github.com/abdullahxsalim)  
- [Mohammad Yasir](#)  
- [Afsana Umme Kulsum Eaty](#)

## **License**  
This project is licensed under the [MIT License](LICENSE).

---

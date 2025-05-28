# One-Dimensional Ping-Pong Game

A hardware-only 1D "Ping-Pong" game implemented using the GreenPAK SLG46620V programmable logic device.

## 🎮 Game Description

This project implements a simple but engaging ping-pong game entirely in hardware - no microcontroller or software required! A single active bit (representing the ball) moves across a 6-LED array. When the ball reaches either edge, players must press a button within a brief time window to reflect it back.

### Gameplay Features
- **Ball Movement**: A shifting bit across 6 LEDs simulates ball movement
- **Player Input**: Button press required at edges (Q0 or Q5) to reflect the ball
- **Audio Feedback**: Buzzer sounds on successful hits
- **Progressive Difficulty**: Ball speed doubles every two successful reflections
- **Forgiving Design**: Missed balls restart from the opposite edge

## 🔧 Hardware Implementation

### Target Device
- **GreenPAK SLG46620V** - Dual-matrix programmable logic device

### Architecture Overview
The design utilizes both logic matrices of the SLG46620V:

- **Matrix0**: Handles user input, clock division, bounce detection logic, and buzzer control
- **Matrix1**: Contains the core 6-bit shift register for ball movement and directly drives LED outputs

### Key Components
- Clock divider for timing control
- 6-bit shift register for ball position tracking
- Direction control logic
- Input detection and timing windows
- Progressive speed control system
- Audio output control

## 🎯 Project Goals

This project demonstrates:
- **Pure Hardware Logic**: Implementation without microcontrollers or software
- **Interactive Real-time Behavior**: Responsive gameplay using only configurable logic blocks
- **GreenPAK Capabilities**: Showcasing the potential of configurable logic for low-power embedded designs
- **Educational Value**: Practical application of digital circuit design principles

## 📋 System Requirements

### Hardware
- GreenPAK SLG46620V programmable logic device
- 6 LEDs for ball visualization
- 2 push buttons for player input
- 1 buzzer for audio feedback
- Appropriate resistors and connections

### Tools
- GreenPAK Designer software for configuration
- Programming hardware for SLG46620V

## 🚀 Getting Started

1. **Design Configuration**: Load the GreenPAK configuration file into GreenPAK Designer
2. **Hardware Assembly**: Connect LEDs, buttons, and buzzer according to the pin configuration
3. **Programming**: Program the SLG46620V with the generated configuration
4. **Testing**: Power up and test all game functions

## ⚡ Technical Highlights

- **Zero Software Dependency**: Entire game logic implemented in configurable hardware
- **Low Power Design**: Leverages GreenPAK's efficient logic blocks
- **Real-time Response**: Hardware-based timing ensures consistent gameplay
- **Scalable Difficulty**: Dynamic speed adjustment based on player performance

## 📚 Educational Applications

This project serves as an excellent example for:
- Digital logic design courses
- Embedded systems education
- Hardware description and implementation
- Real-time system design principles

## 👨‍🎓 Author

**Mykola Balyk**  
First-year Computer Science Student  
Ukrainian Catholic University, Lviv, Ukraine  
📧 balyk.pn@ucu.edu.ua

## 📝 Academic Context

Completed as a semester project for Digital Circuit Design course, demonstrating practical application of configurable logic devices in interactive system design.

---

*This project demonstrates the potential of configurable logic for simple, low-power interactive systems without relying on traditional microcontroller-based approaches.*

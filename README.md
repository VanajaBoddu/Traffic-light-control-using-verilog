# Time-Based Traffic Lights Controller

## Objectives
- To build and understand finite state machines.
- To understand Moore finite state machine.
- Implementing a time-based traffic light controller using finite state machine.
- Integrating smaller modules.
- Working in teams.
- Develop problem solving skills.

## Project Breakdown

### State Table for Traffic Light Controller (Moore FSM)
| Current State | Input (Time) | Next State | Output  |
|---------------|--------------|------------|---------|
| STATE1        | 15, 10, 5, 5 | STATE1     | 0, 0, 0, 1 |
| STATE1        | 14, 9, 4, 4  | STATE1     | 0, 0, 0, 1 |
| STATE1        | 13, 8, 3, 3  | STATE1     | 0, 0, 0, 1 |
| STATE1        | 12, 7, 2, 2  | STATE1     | 0, 0, 0, 1 |
| STATE1        | 11, 6, 1, 1  | STATE1     | 0, 0, 0, 1 |
| STATE1        | 10, 5, 0, 0  | STATE2     | 0, 0, 0, 1 |
| STATE2        | 10, 5, 5, 15 | STATE2     | 0, 0, 1, 0 |
| STATE2        | 9, 4, 4, 14  | STATE2     | 0, 0, 1, 0 |
| STATE2        | 8, 3, 3, 13  | STATE2     | 0, 0, 1, 0 |
| STATE2        | 7, 2, 2, 12  | STATE2     | 0, 0, 1, 0 |
| STATE2        | 6, 1, 1, 11  | STATE2     | 0, 0, 1, 0 |
| STATE2        | 5, 0, 0, 10  | STATE3     | 0, 0, 1, 0 |
| STATE3        | 5, 5, 15, 10 | STATE3     | 0, 1, 0, 0 |
| STATE3        | 4, 4, 14, 9  | STATE3     | 0, 1, 0, 0 |
| STATE3        | 3, 3, 13, 8  | STATE3     | 0, 1, 0, 0 |
| STATE3        | 2, 2, 12, 7  | STATE3     | 0, 1, 0, 0 |
| STATE3        | 1, 1, 11, 6  | STATE3     | 0, 1, 0, 0 |
| STATE3        | 0, 0, 10, 5  | STATE4     | 0, 1, 0, 0 |
| STATE4        | 5, 15, 10, 5 | STATE4     | 1, 0, 0, 0 |
| STATE4        | 4, 14, 9, 4  | STATE4     | 1, 0, 0, 0 |
| STATE4        | 3, 13, 8, 3  | STATE4     | 1, 0, 0, 0 |
| STATE4        | 2, 12, 7, 2  | STATE4     | 1, 0, 0, 0 |
| STATE4        | 1, 11, 6, 1  | STATE4     | 1, 0, 0, 0 |
| STATE4        | 0, 10, 5, 0  | STATE1     | 1, 0, 0, 0 |

### Verilog Modules
#### Pulse Generator (One Hertz)

## Simulation
- Simulations for STATE 1 and STATE 2.
- Simulations for STATE 3 and STATE 4.
  
## Challenges Overcome
- Timing synchronization
- State transitions
- Reliability of simulated traffic flow
  
## Results and Achievements
The successful emulation of a traffic signal system on the FPGA showcased the efficient operation of the implemented Moore state machine. The controller accurately managed traffic light sequences, validating its reliability and functionality.

## Learnings and Future Developments
Insights into digital circuit design, Verilog programming, and finite state machines.

## Future developments could include:
Scalability for larger intersections
Integration of sensor inputs for adaptive signaling
Optimization for real-time applications

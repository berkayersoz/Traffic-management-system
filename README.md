# Smart Traffic Management System Using OMNeT++ and FLoRa

## 🚦 Overview
This project simulates a smart traffic management system designed to optimize traffic light control at a crossroad intersection using OMNeT++ and the FLoRa framework. The goal is to minimize vehicle wait times and congestion by dynamically adjusting traffic lights based on real-time sensor data.

Camera sensors placed at each road detect the number of waiting vehicles. This data is sent via LoRa (Long Range) communication to a central Control Unit (CU), which determines the optimal traffic light changes. The simulation models realistic vehicle behavior and network performance using stochastic processes such as Poisson distribution and Monte Carlo simulations.

---

## 📌 Objectives
- Dynamically control traffic lights based on vehicle density.
- Model real-time communication over LoRa between sensors and control unit.
- Evaluate network and system performance under varying traffic conditions.
- Simulate realistic vehicle arrivals using Poisson distribution.
- Analyze results for congestion control and communication efficiency.

---

## 🧠 Key Concepts

- **Poisson Distribution**: Simulates random vehicle arrivals over time.
- **Monte Carlo Simulation**: Models probabilistic scenarios for signal timing and traffic flow.
- **Event-Based Simulation**: OMNeT++ is used to simulate discrete events such as arrivals, message transmissions, and traffic light changes.
- **FLoRa Framework**: Used for implementing LoRa communication between devices in the network.

---

## 🏗️ System Architecture

- **Vehicles**: Random arrivals, tracked with speed, position, and wait time.
- **Camera Sensors**: Detect vehicle counts every 5 seconds and transmit data via LoRa.
- **Control Unit (CU)**: Determines optimal traffic light states based on sensor data.
- **Traffic Lights**: Change dynamically based on decisions from the CU.
- **LoRa Nodes**: Enable wireless communication with delays and queuing.

---

## 🧩 Simulation Components

### Entities
- Vehicles  
- Traffic Lights  
- Camera Sensors  
- Control Unit  
- LoRa Gateway & Nodes  

### Attributes
- `Vehicle`: Arrival time, speed, position, wait time  
- `Traffic Light`: Status (green/red), timer  
- `Sensor`: Road ID, detection interval, delay  
- `Control Unit`: Decision logic, timing  
- `LoRa`: Transmission rate, message queue  

### Events
- New vehicle arrival  
- Sensor captures vehicle count  
- Message transmission/reception  
- Traffic light change  
- Control Unit decision  

### Wait Types
- **Unconditional**: Traffic light duration (30s), sensor detection (5s)  
- **Conditional**: Vehicle waits for green, message queue waits, CU waits for all reports  

---

## 🧪 Tools and Technologies

| Tool/Library    | Purpose                                   |
|----------------|-------------------------------------------|
| **OMNeT++**     | Discrete event simulation framework       |
| **FLoRa**       | LoRa protocol modeling and simulation     |
| **INET Framework** | Optional, for network integration       |
| **C++ / NED**   | Model definitions and logic               |

---

## 🗓️ Project Timeline

### ✅ Completed Milestones
- Defined system entities and attributes
- Modeled events and traffic flow logic
- Established OMNeT++ simulation structure
- Designed message passing and delays via LoRa

### 🚧 Remaining Milestones
- [ ] Implement traffic light control algorithm in OMNeT++
- [ ] Integrate vehicle and sensor logic with LoRa communication
- [ ] Test simulation under various traffic conditions
- [ ] Finalize documentation and prepare simulation results

---

## 🏁 Running the Simulation

### Requirements
- OMNeT++ (v6.0 or compatible)
- FLoRa framework installed
- CMake, GCC, or Clang

### Steps
1. Clone this repository.
2. Open OMNeT++ IDE.
3. Import the project and build it.
4. Run the simulation using the provided `.ini` configuration files.
5. View output logs, network visuals, and performance metrics.

---

## 📊 Output and Results

Expected output includes:
- Vehicle queue lengths over time
- Traffic light state transitions
- LoRa communication delay analysis
- Graphs showing congestion levels under varying conditions

---

## 👥 Team Members

| Name       | Responsibilities                              |
|------------|-----------------------------------------------|
| **Berkay** | System architecture, OMNeT++ control logic, LoRa module integration |
| **Boğaçhan** | Vehicle and sensor modeling, event scheduling, FLoRa communication logic |

---

## 📄 License
This project is for academic use as part of **CNG 476 - System Simulation** at METU NCC. All rights reserved.

---

## 📬 Contact
For questions or collaboration, please contact:
- Berkay: [ersozberkay2003@gmail.com]
- Boğaçhan: [bogachanayar@gmail.com]

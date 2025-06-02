Overview
This project presents a smart traffic management system designed and simulated using OMNeT++ and the FLoRa framework. The system dynamically optimizes traffic light control at a four-way intersection by adjusting green light allocation based on real-time traffic queue data.

Vehicle arrivals are modeled using a Poisson process to realistically simulate traffic flow randomness. Camera sensors on each road segment monitor queue lengths and report this information every 5 seconds via low-power LoRa wireless communication to a centralized control unit. The control unit processes the incoming data and updates traffic light statuses every 10 seconds, prioritizing the road with the longest vehicle queue.

By incorporating probabilistic traffic models, Monte Carlo simulations, and stochastic processes, the system is able to adapt dynamically to changing traffic conditions, aiming to reduce congestion and improve overall traffic flow efficiency.

Features
Dynamic Traffic Light Control: Traffic light durations adjust in real time according to traffic density.

LoRa-based Communication: Lightweight, low-latency wireless communication between sensors and control unit.

Realistic Traffic Modeling: Vehicle arrivals follow a Poisson process for randomness and unpredictability.

Modular Design: Separate modules for TrafficNodes (road sensors) and a centralized ControlUnit.

Performance Metrics: The system tracks metrics such as average vehicle waiting time, queue lengths, and communication latency to evaluate effectiveness.

System Architecture
TrafficNode Modules: Simulate camera sensors that monitor vehicle queues on each road.

ControlUnit Module: Collects sensor data and makes traffic light control decisions.

LoRa Communication Channels: Simulate wireless communication between TrafficNodes and the ControlUnit.

Simulation Flow
TrafficNodes initialize with random queue lengths.

Every 5 seconds, each TrafficNode sends its current queue length to the ControlUnit.

The ControlUnit collects reports from all roads and every 10 seconds decides which road receives the green light.

TrafficNodes receive traffic light status updates and react accordingly.

Usage
The simulation is implemented using OMNeT++ with the FLoRa framework.

Network and module configurations are defined in .ned files.

Core logic is implemented in C++ within TrafficSimulation.cc and TrafficSimulation.h.

Repository
The full source code and simulation files are available at:

https://github.com/berkayersoz/Traffic-Management-System

Future Work
Integrate a more detailed Poisson-based vehicle arrival model.

Enhance communication delay modeling for LoRa transmissions.

Implement vehicle departure modeling based on green light duration.

Extend the system to multi-intersection traffic networks for broader smart city applications.

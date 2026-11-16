# Traffic Control System

A pedestrian-aware traffic signal controller for a four-way intersection, built on an Arduino Mega. Ultrasonic sensors detect pedestrians near each crossing and the controller adjusts the signal phases so vehicles and pedestrians never get conflicting green lights.

Built at **IIIT Bhagalpur** with the REC club, under the guidance of Mr. Kumar Ujjwal, from 14 June to 14 July 2023.

**Team:** Rahul Kumar · Shiv Shankar · Satwik Bhakta

## Problem statement

Design a system that detects pedestrians and changes the traffic signals accordingly, for smooth and safe traffic flow.

## Hardware

| Component | Role |
|-----------|------|
| Arduino Mega | Controller (chosen for its large number of I/O pins) |
| Ultrasonic sensors (×4) | Measure pedestrian distance at each approach |
| RGB LEDs | Traffic signal heads |
| Servo motor | Actuator |
| Breadboard and jumpers | Prototyping |

Software: Arduino IDE.

## How it works

1. Each ultrasonic sensor continuously measures the distance to the nearest pedestrian at its crossing.
2. The controller works through the possible vehicle and pedestrian movements at the four-way junction and picks a safe phase, so that no two conflicting flows are green together.
3. When a pedestrian is detected within range, their crossing is given priority and the conflicting vehicle signals turn red, with delays between phases.

A key takeaway was how many movement combinations even a simple four-way junction has, and how much care it takes to keep every combination safe.

## Simulation

The circuit and code can be run in Tinkercad:
[Tinkercad project](https://www.tinkercad.com/things/5hBu3TV0ZPS-ingenious-leelo/editel?sharecode=1sfsLds5MyPKpd0PBrmxLXJpCS1dG1OeNqn_4jiY2xo)

## Documentation

The full project report, including the circuit diagram, is in [`Doc4.docx`](Doc4.docx).

## Possible improvements

- LIDAR for more accurate, real-time detection
- Traffic-density input from mapping APIs
- Error checking and a feedback path for fail-safe operation
- Adaptive timing with ML or reinforcement learning

## Acknowledgements

Thanks to the REC club and our mentors at IIIT Bhagalpur.

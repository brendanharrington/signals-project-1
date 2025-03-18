# Moon Rover System Modeling

## Introduction

This project explores the modeling, analysis, and control of an autonomous lunar rover tasked with collecting moon rock specimens. The rover system consists of two primary components: a driving rover and an attached specimen trailer. The rover utilizes LIDAR sensors for navigation feedback and an electric motor driven by electronic signals for propulsion. To facilitate safe and efficient towing of the trailer, the vehicles are interconnected via elastic rods modeled as an elastic coupling.

The primary objective is to understand and characterize the rover's physical system using theoretical methods and numerical simulations. Initially, the rover system is mathematically modeled using differential equations derived from Newtonian mechanics and subsequently analyzed using Laplace transforms. Simulink simulations are performed to verify theoretical predictions and evaluate system responses to various inputs.

Following verification, the focus shifts toward optimization and control. Specifically, the goal is to develop an input voltage signal controlling the motor that maximizes the rover's efficiency in delivering moon rock samples to a designated destination. Constraints include limiting elastic rod stretching, avoiding saturation of the motor force, and minimizing the time required for completing the mission.

The project consists of theoretical analysis, simulation verification, and a practical optimization challenge, providing comprehensive experience in system modeling, simulation, and control system design.


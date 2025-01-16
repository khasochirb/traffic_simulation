# Traffic Simulation Using Network Graphs

This project models and analyzes traffic dynamics on urban road networks using Python and NetworkX. The simulation provides insights into traffic patterns, congestion, and road usage. It serves as an educational tool and theoretical exploration of traffic systems, rather than a real-world predictive model.

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Setup and Installation](#setup-and-installation)
4. [Usage](#usage)
5. [Simulation Details](#simulation-details)
6. [Limitations and Improvements](#limitations-and-improvements)
7. [Future Work](#future-work)
8. [Contributors](#contributors)

---

## Overview

This project simulates traffic on urban road networks using graph theory concepts:
- Roads are represented as edges.
- Intersections are represented as nodes.
- Traffic flow is simulated using cars moving along paths determined by shortest-path algorithms.

The road network is modeled using OpenStreetMap data for specific locations, such as Adalbertstraße 58 in Berlin and Esmeralda 920 in Buenos Aires.

GitHub Repository: [Traffic Simulation](https://github.com/khasochirb/traffic_simulation)

---

## Features

- **Dynamic Traffic Simulation**: Cars navigate from their current locations to destinations using shortest-path algorithms.
- **Congestion Modeling**: Simulates traffic jams when multiple cars attempt to use the same road segment.
- **Visualization**: Generates visual representations of road networks with traffic density data.
- **Statistical Analysis**: Evaluates network metrics (e.g., Betweenness Centrality) for their correlation with congestion.

---

## Setup and Installation

### Prerequisites
- Python 3.8 or higher
- Required libraries: `networkx`, `matplotlib`, `osmnx`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/khasochirb/traffic_simulation.git
   cd traffic-simulation
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### Running the Simulation
1. Load a road network:
   - Use OpenStreetMap data for a specific location.
2. Initialize simulation parameters:
   - Number of cars, simulation steps, etc.
3. Run the simulation:
   ```python
   python simulate_traffic.py
   ```

### Visualizing Results
- The `plot_network_with_traffic` function adjusts edge widths and colors based on traffic density.

---

## Simulation Details

### Classes
1. **Car**: Represents individual vehicles with attributes for location, destination, and path.
2. **TrafficSimulation**: Manages the simulation logic, including pathfinding and congestion modeling.

### Key Algorithms
- Shortest-path computation using Dijkstra’s algorithm.
- Traffic congestion is modeled with a threshold of 5 cars per road segment.

---

## Limitations and Improvements

### Current Limitations
- Static road networks: No dynamic updates for road closures or construction.
- Basic congestion model: Traffic jams based on a fixed threshold.
- Uniform vehicle behavior: Ignores differences in vehicle types and driver behaviors.

### Proposed Improvements
- Dynamic congestion thresholds based on road attributes.
- Integration of real-time traffic data.
- Advanced models for driver behavior and environmental factors.

---

## Future Work

- Enhance visualization with interactive dashboards.
- Expand simulation to include other modes of transportation (e.g., buses, bicycles).
- Improve statistical analysis of network metrics for congestion prediction.

---

## Contributors

- **Khas Bayar**


Feel free to contribute by opening an issue or submitting a pull request!

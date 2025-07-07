# Dynamic Parking Pricing System  
Capstone Project – Summer Analytics 2025
---
## Overview
Urban parking lots often suffer from inefficient pricing — leading to either overcrowding or underutilization.  
This project implements a real-time dynamic pricing engine for urban parking spaces using Pathway for data streaming and Bokeh for real-time visualization.
Built as part of the Summer Analytics 2025 Capstone hosted by the Consulting & Analytics Club.
---
##  Model Implemented
### Model 1: Baseline Linear Pricing
A simple model where prices increase linearly with occupancy:
Price = 10 + 10 × (Occupancy / Capacity)
✔Smooth and explainable price changes  
✔Real-time updates with a 2-hour tumbling window  
✔Pricing varies from $10 to $20 based on demand
---
## Tech Stack
| Layer             | Technology         |
|------------------|--------------------|
| Data Streaming    | Pathway            |
| Data Processing   | Pandas, NumPy      |
| Visualization     | Bokeh, Panel       |
| Platform          | Google Colab       |
| Dataset Format    | CSV                |
---
## Architecture Diagram
```mermaid
graph TD
  A[CSV Dataset (73 days)] --> B[Replay Stream with Pathway]
  B --> C[Real-time Windowing (2hr Tumbling)]
  C --> D[Model 1 Pricing Logic]
  D --> E[Live Price Output Table]
  E --> F[Visualization via Bokeh + Panel]


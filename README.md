# 3D Palletization - Thesis

Code developed as part of my Master's thesis on 3D palletization.

## About the Project

The project addresses the 3D Bin Packing Problem (3D-BPP) in the context of
warehouse shipments. The proposed approach uses the Extreme Point Heuristic (EPH)
to determine feasible positions for placing boxes on pallets (120×80 cm, max. 1500 kg).

The algorithm considers:

- Box and pallet dimensions
- Box weight and maximum pallet weight
- Box orientation
- Collision and overlap constraints
- Minimum base support (70%) for stable placement

## Implementation

- Python
- Apache Spark (PySpark)
- Microsoft Fabric

The repository contains a single notebook with the full pipeline: data preparation,
packing sequence, box selection, 3D packing, container recommendation, validation
against historical data, and 3D visualization.

> **Note:** the data comes from a company's ERP system and is confidential, so it is
> not included. The notebook is provided for reference and cannot be run as-is.

## Results

On a sample of 825 units across 63 shipments, the algorithm generated
132 pallets.

Validated against historical shipments with full dimensional coverage
(146 shipments), the estimated number of pallets matched the real number
in 77.4% of cases (MAE = 0.67 pallets).

Performance depends heavily on dimensional data availability: only 47.5% of historical
content lines had dimensions. See the thesis for the full analysis.

## Thesis

**3D Palletization using the Extreme Point Heuristic**
Author: Maria Inês Veiga Cardoso · Year: 2026

# Geometric-Packing-Kaggle
A Kaggle optimization project that uses simulated annealing and computational geometry to pack rotated polygonal objects into minimal square containers without overlap.


🎄 Santa 2025 – Christmas Tree Packing Challenge

This repository contains my solution to the Kaggle competition
Santa 2025 – Christmas Tree Packing Challenge, a computational geometry and optimization problem.

📌 Problem Overview

Santa needs to pack shipments of 1 to 200 identical Christmas tree toys into the smallest possible square box.
Each tree may be translated and rotated, but no overlaps are allowed.

The goal is to minimize the size of the square that contains all trees for each configuration.

🧠 Solution Approach

The problem is solved using a geometry-driven optimization pipeline:

1️⃣ Tree Modeling

The Christmas tree is modeled as a fixed polygon using Shapely

All trees share the same geometry and differ only in position and rotation

2️⃣ Initialization

Initial placements are generated using grid-based (hexagonal) layouts

For some cases, Kaggle’s sample layouts are used as a starting point

3️⃣ Optimization

Simulated Annealing is applied to minimize the bounding square size

Random translations and rotations are explored while respecting constraints

4️⃣ Overlap Resolution

A repulsive cleanup strategy pushes overlapping trees apart

Final safety checks guarantee overlap-free placements

5️⃣ Full Coverage

The process is repeated independently for all configurations from n = 1 to 200

A Kaggle-compliant submission file is generated automatically

🛠️ Technologies Used

Python

Shapely (computational geometry)

NumPy

Pandas

Matplotlib

Kaggle Notebooks

📊 Results

Successfully generated placements for all 200 configurations

Guaranteed no overlapping trees

Produced a valid Kaggle submission file

Submission evaluated on the Kaggle leaderboard

📁 Repository Structure
├── santa-project.ipynb     # Main Kaggle notebook
├── README.md               # Project documentation


⚠️ Competition datasets and submission files are not included in this repository,
in accordance with Kaggle’s data usage rules.


📌 Notes

The notebook is designed to be executed inside Kaggle

Runtime is higher due to geometric optimization and safety checks

Focus is on correctness and optimization quality, not inference speed

👤 Author

Samiksha Chandawar

🏁 Acknowledgments

Kaggle for hosting the competition

Shapely library for geometric operations

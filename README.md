# Fulgurite

Fulgurite will be a real-time 3D electromagnetism simulation engine written in C++. It will model electric and magnetic fields, charged particle dynamics, and field interactions using numerical methods.

The goal of the project is to build a physically grounded computational environment for visualizing and experimenting with classical electromagnetism.


## What it does

Fulgurite simulates classical electromagnetism in a discrete 3D space using numerical methods. It is designed to evolve from simple electrostatics into full electromagnetic field simulation.

Current and planned capabilities include:

- Simulation of point charges in 3D space
- Electric field computation using Coulomb’s law and superposition
- Particle motion under electric forces
- Numerical integration of motion over time
- Visualization of vector fields and particle trajectories
- Future support for magnetic fields, induction, and Maxwell-based field propagation

At its core, Fulgurite treats space as a computational field where physical laws are evaluated numerically at each time step.


## Physics model

The initial implementation is based on classical electrostatics.

Coulomb’s law:

```
F = k * (q1 * q2) / r^2 * r_hat
```

Electric field definition:

```
E = F / q
```

Superposition principle:

```
E_total = sum(E_i)
```

## Architecture overview

The engine is divided into three main layers:

Core physics layer

Responsible for:
- charge representation
- force computation
- field evaluation
- numerical integration

Simulation layer

Responsible for:
- time stepping
- world state management
- physics updates

Rendering layer

Responsible for:
- visualization of particles
- vector field rendering
- debug overlays

## Installation

## Requirements

- C++17 or later
- CMake (recommended)
- A C++ compiler (GCC, Clang, or MSVC)
- OpenGL-compatible system (for rendering layer, once implemented)

Optional dependencies:
- GLFW
- GLM
- ImGui

## Build instructions

Clone the repository:

```
git clone https://github.com/ecgo3/fulgurite.git
cd fulgurite
```

Create build directory:

```
mkdir build
cd build
```

Generate build files:

```
cmake ..
```

Compile:

```
cmake --build .
```
You can run it by typing
```
./Fulgurite
```

## Current status

The project is in early development.

Initial focus:

- Point charge simulation
- Electric field computation
- Numerical integration
- Basic rendering pipeline

---

## Roadmap

### v0.1 – Static electric fields
- Point charge system
- Coulomb interaction
- Electric field computation
- Basic visualization

### v0.2 – Dynamic charges
- Moving particles
- Improved integration
- Particle trails

### v0.3 – Magnetism
- Lorentz force
- Magnetic field generation
- Particle spirals

### v0.4 – Current systems
- Wire modeling
- Biot–Savart approximation
- Electromagnets

### v0.5 – Induction
- Faraday’s law approximation
- Time-varying fields
- Generators and transformers

### v1.0 – Full field solver
- Discrete Maxwell equations
- FDTD simulation
- Electromagnetic waves
```

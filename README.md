# Solving ODEs Numerically

This repository provides implementations of various numerical methods to solve ordinary differential equations (ODEs). Two distinct ODEs are considered, and different methods are applied to approximate their solutions. The first ODE describes the motion of a pendulum, while the second represents a logistic growth model.

## Pendulum ODE

### Euler Methods
1. `euler_method`: Basic Euler method for solving ODEs.
2. `euler_explicit`: Explicit Euler method for solving the pendulum ODE.
3. `trapezoidal`: Trapezoidal method for solving the pendulum ODE.

#### Usage
```python
import numpy as np
import matplotlib.pyplot as plt

# Define the pendulum ODE
def f(t, theta, omega):
    # ODE definition here

# Set initial conditions
theta0 = np.pi/4
omega0 = 0.0
num_steps = 800
dt = 0.01
t0 = 0.0

# Apply Euler methods
theta_euler_explicit, t_euler_explicit = euler_explicit(f, theta0, omega0, t0, dt, num_steps)
theta_trapezoidal, t_trapezoidal = trapezoidal(f, theta0, omega0, t0, dt, num_steps)
t_euler, theta_euler = euler_method(f, theta0, omega0, t0, dt, num_steps)

# Plot the results
# ...
```

### Graphs of Accuracy
```python
import numpy as np
import matplotlib.pyplot as plt

# Define logistic growth ODE
# ...

# Set parameters
K = 2
r = 10
step_size = 0.1
num_steps = 100

# Apply Euler methods for logistic growth ODE
x1, y1 = euler_method_1(dydt, 1, step_size, num_steps)
x2, y2 = euler_method_2(dydt, 1, step_size, num_steps)
x3, y3 = euler_method_3(dydt, 1, step_size, num_steps)

# Plot the results
# ...

# Analytical solution using sympy
# ...

# Display the analytical solution
# ...
```

## Dependencies
- NumPy
- Matplotlib
- SciPy

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Getting Started

To get started with this project, clone the repository and install the required dependencies.

### Prerequisites

- Python 3.x
- NumPy
- Matplotlib
- SciPy

### Installation

```bash
git clone https://github.com/yourusername/yourproject.git
cd yourproject
pip install -r requirements.txt
```

## Usage

Run the provided examples to see the numerical solutions of ODEs and their accuracy graphs.

```bash
python pendulum_ode.py
python logistic_growth_ode.py
```

## Contributing

If you would like to contribute to this project, please follow the guidelines in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Special thanks to contributors and libraries used in this project.

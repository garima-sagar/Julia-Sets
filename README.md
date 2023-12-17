# Julia-Sets
Plotting julia sets for different values of complex constant

# Julia Set Generator

## Overview
This Python script generates and visualizes Julia sets, which are fascinating fractal patterns in complex dynamics. The Julia set is constructed by iterating a complex function on a grid of complex numbers. The code utilizes NumPy for numerical operations and Matplotlib for plotting.

## How it Works
The Julia set is generated by iterating the function \(Z = Z^2 + c\), where \(Z\) is a complex number, and \(c\) is a constant complex number. The algorithm explores how the initial complex numbers evolve over iterations, and the resulting pattern is visualized.

### Mathematical Explanation
- The script defines a grid of complex numbers based on specified width, height, and ranges for \(x\) and \(y\).
- The complex constant \(c\) is initialized, and you can experiment with different values to observe diverse Julia set patterns.
- The iterative process begins, updating each complex number in the grid using \(Z = Z^2 + c\).
- A mask is created based on the condition that the absolute value of each complex number is less than 1000.
- The mask is accumulated over iterations, creating an image representing the Julia set.

## Code Structure
### `generate_julia_set` Function
```python
def generate_julia_set(width, height, xmin, xmax, ymin, ymax, c, max_iter):
    # ... (explained in code comments)
    return img
```
This function generates the Julia set image based on the specified parameters.

### `plot_julia_set` Function
```python
def plot_julia_set(julia_set):
    # ... (explained in code comments)
```
This function plots the generated Julia set using Matplotlib.

### Setting Parameters and Visualization
```python
width, height = 800, 800
xmin, xmax = -2, 2
ymin, ymax = -2, 2
c = complex(-0.8, 0.156)  # Experiment with different values of 'c'
max_iter = 100

julia_set = generate_julia_set(width, height, xmin, xmax, ymin, ymax, c, max_iter)
plot_julia_set(julia_set)
```


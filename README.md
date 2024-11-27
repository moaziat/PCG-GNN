# JIT compiled preconditioned conjugate gradient (PCG)

### Overview: 
1 -  There are many ways to solve PDEs. In this repository we are implementing the PCG, an iterative solver. 

For example here we are trying to solve 2D poisson ![equation](https://latex.codecogs.com/svg.latex?-\nabla^2%20u%20=%20b%20\quad%20\text{in}%20\quad%20\Omega%20\subset%20\mathbb{R}^2)

With centered finite difference method we discretize the equation into a sparse matrix problem, which is solved iteratively.

2- We use a JIT compiled PCG using Numba to accelerate computations on CPU. (may extend it to GPU acceleration in the near future).

To clone this repository: 
```bash
clone https://github.com/moaziat/JIT-PCG-Solver.git
```
### Dependencies
```bash
pip install requirements.txt

```
## Execution 
```
cd JIT parallelized solver/ 
python poisson2D_parallel.py 
```
### Grid Parameters
`nx`, `ny`: Grid points in x/y dimensions (default: 500, 500)

`xmin`, `xmax`: Domain boundaries in x direction
`ymin`, `ymax`: Domain boundaries in y direction

`dx`, `dy`: Computed step sizes

## Example of the problem


The default problem simulates two point sources in the domain:
- Positive source at (1/4, 1/4)
- Negative source at (3/4, 3/4)

The potential field is generated by these sources.

## Reference 
The implementation follows ideas from the 12 Steps to Navier-Stokes course by Lorena A. Barba: https://lorenabarba.com/blog/cfd-python-12-steps-to-navier-stokes/.

## Contact
For issues or suggestions, feel free to reach out to the repository owner @moaziat.







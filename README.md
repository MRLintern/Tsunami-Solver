
## Tsunami-Solver: Tsunami Modeling with the 2D Shallow Water Equations

* A __C++17 Finite Element Solver__ for modeling __Tsunami__ generation and propagation using the __Nonlinear 2D Shallow Water Equations__. 
---
### Overview

* __Tsunamis__ are __Long-Wavelength__, __High-Energy Waves__ caused by __underwater disturbances__ such as __Earthquakes__, __Landslides__, or __Volcanic Eruptions__.
* This project simulates __Tsunami Wave propagation__ in __coastal__ and __open-ocean__ settings using the __2D Nonlinear Shallow Water Equations__.




---
### Governing Equations
* The __Shallow Water Equations (SWEs)__ are a set of __Hyperbolic Partial Differential Equations__ that describe the __flow__ below a __pressure surface__ in a fluid (typically the ocean) when the __horizontal length scale__ is much __greater__ than the __vertical depth__.
* They model __depth-averaged__, __incompressible__, __inviscid flow__, assuming the __vertical acceleration__ is __negligible__.
* Components of the SWEs:
    * `h(x,y,t)`: __fluid depth__
    * `u(x,y,t)`,`v(x,y,t)`: __horizontal velocities__ in `x-` and `y-directions` respectively.
    * `g`: __gravitational acceleration__.
    * `n = h+b`: __free surface elevation__.
    * `b(x,y)`: __ocean bottom topography__.
* The __2D conservative form__ is:
    * `dh/dt + d(hu)/dx + d(hv)/dy = 0`; __mass conservation__.
    * `d(hu)/dt + d(hu^2 + 1/2gh^2)/dx + d(huv)/dy = -ghdb/dx`: __momentum x-direction__.
    * `d(hv)/dt + d(huv)/dx + d(hv^2 + 1/2gh^2)dy = -ghdb/dy`: __momentum y-direction__.
    * Note: `d` representes `partial differential operator`.
* Application to Tsunami Modeling:
    * The __initial disturbance__ (e.g., from a __submarine earthquake__) displaces water.
    * __SWEs__ simulate the __wave propagation__ over __varying bathymetry__.
    * Can simulate __inundation__ by extending the domain with moving wet/dry boundaries.
---
### Requirements
* __Compiler__: `g++ 13.1.0`. Your compiler needs to be able to make use of `C++17` features.
* __OS__: `Ubuntu 20.04`.
* [CMake 4.0.2](https://cmake.org/).
* [Eigen Library - 3.4.0](https://eigen.tuxfamily.org/index.php?title=Main_Page).

---
### Instructions: Getting and Using the Software

### References & Resources
* ___Modern Fortran: Building Efficient Parallel Applications___ by __Milan Curcic__. This wonderful book shows how to develop a parallel solver for solving the __Shallow Water Equations, modelling __Tsunamis__ using __Fortran__ and __Coarrays__. 

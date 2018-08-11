---
layout: page
title: Mathematical Modeling
---

### The KdV equation: finite difference methods for nonlinear PDEs
#### (2018)

The Korteweg-de Vries equation is the poster child for solvable non-linear PDEs. It models the behavior of shallow-water waves [first observed]("http://www.macs.hw.ac.uk/~chris/scott_russell.html") by John Russel in the mid-19th century, in which any given initial condition devolves into collections of solitons - solitary waves traveling at constant speed. 

As part of the final project for my Numerical Methods for PDEs course at Columbia University, I implemented several finite difference methods for solving the KdV equation and compared their convergence and stability properties (you can find part of the analysis [this](https://github.com/TiagoJCor/Numerical-Methods-KDV/blob/master/numerical_KDV.ipynb) Jupyter Notebook).

<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/kdveq/kdvsolitons.png" width="310" height="210"> <figcaption><font size="3">Caption1</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/kdveq/kdvsolitons2.png" width="310" height="210"> <figcaption><font size="3">Caption2</font></figcaption> </figure></div>
</div>

Finite difference methods are easy to understand and implement, but are often superseeded in efficiency by other (faster) approaches. For the KdV equation with periodic boundary conditions one can take advantage of the Fast Fourier Transform to compute the spatial derivatives. This version of a **spectral method** boasts higher convergence properties are produces more stable simulations. Below are a series of videos of the time-dependent solution to the KdV equation, given different initial conditions:

* [Single soliton](https://drive.google.com/file/d/1FZuBoY9WnwVYD6kC2p0drA1o4exNobN-/view?usp=sharing);

* [Two solitons](https://drive.google.com/open?id=1NGMIAR_1-p6ydgFwgCZ2gWCRSyBRf03q) traveling at different speeds;

* [Single soliton plus cosine wave](https://drive.google.com/open?id=1G1bRAdLtqmr8X_CXkWoM5FxkfRUxoXxC), quickly devolving into a train of solitons traveling at different speeds.


### Ising model: studying phase transitions with Monte Carlo methods
#### (2016)

<p> </p>

As part of a class on Monte Carlo (MC) methods at Bates College, I simulated the behavior of a two-dimensional **Ising model** - a mathematical description of ferromagnets - using the **Metropolis-Hastings** algorithm. This model depicts a lattice of up/down spin particles whose natural tendency is to align themselves with their neighbors, thus lowering the overall energy of the system. An MC simulation allows us to identify the temperature at which a phase transition occurs, which would otherwise be a difficult analytical problem.

We proceeded in the following way: first the state of each particle in the lattice is initialized randomly. In any given iteration of the algorithm, a random particle is chosen. If inversing its spin produces a lower energy (*e.g.* a spin down particle conforming to its spin up neighbors), the spin flip is accepted. Otherwise, we essentially flip a biased coin to determine whether the system is altered. The degree to which the proposed change is favored is proportional to the the background **temperature** (hotter systems are more susceptible to random fluctuations) and inversely proportional to the hypothetical energy increase.

As an example, check out a [video](https://drive.google.com/open?id=1PCurBmP5v0ob1E0UodKkJlWlzoWzD15q "Video of 2D Ising Model simulation")  of 100-by-100 lattice simulation. You can find the code used on my [GitHub](https://github.com/TiagoJCor/Monte-Carlo-Simulations) page.


<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/isingmodel/isingbefore.png" width="300" height="200"> <figcaption><font size="3">Two-dimensional lattices are initialized at random. Black dots represent <i>down</i> spins, red crosses <i>up</i> spins.</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/isingmodel/isingafter.png" width="300" height="200"> <figcaption><font size="3">State of the system after a million steps of the algorithm. The lumping together of spins reflects a state of lower energy.</font></figcaption> </figure></div>
</div>

For very low temperatures all spins will rapidly align themselves with those of their neighbors in an orderly fashion. High temperatures produce unordered systems that do not necessarily converge to a steady state solution. Identifying the **critical temperature** below which large conglomerates of like spins appear was one of the goals of this project.

<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/isingmodel/isingenergy.png" width="290" height="200"> <figcaption><font size="3">System energy at the end of each simulation. Colder temperatures lead to more ordered systems with lower energy.</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/isingmodel/isingmagn.png" width="300" height="200"> <figcaption><font size="3">Average magnetization of the system (+1 for <i>up</i> spin, -1 for <i>down</i> spin). As the temperature decreases, most simulations end with either all <i>up</i> or all <i>down</i> spins.</font></figcaption> </figure></div>
</div>

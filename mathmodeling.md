---
layout: page
title: Mathematical Modeling
---

### Ising model: studying phase transitions with Monte Carlo methods
#### (2016)

<p> </p>

As part of a class on Monte Carlo methods at Bates College, I simulated the behavior of a two-dimensional **Ising model** - a mathematical description of ferromagnets - using the **Metropolis-Hastings** algorithm. This model depicts a lattice of up/down spin particles whose natural tendency is to align themselves with their neighbors, thus lowering the overall energy of the system. The key insight here is identifying the temperature at which a phase transition occurs.

The state of each particle in the lattice is initialized randomly. In any given iteration of the algorithm, a random particle is chosen. If flipping its spin produces a lower energy (*e.g.* a spin down particle surrounded by spin up particles), the spin flip is accepted. Otherwise, the probability of this particle maintaining its current state is proportional to the hypothetical energy increase, and inversely proportional to the background temperature. 

<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/isingmodel/isingbefore.png" width="300" height="200"> <figcaption><font size="3">Two-dimensional lattices are initialized at random. Black dots represent <i>down</i> spins, red crosses <i>up</i> spins.</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/isingmodel/isingafter.png" width="300" height="200"> <figcaption><font size="3">State of the system after a million steps of the algorithm. The lumping together of spins reflects a state of lower energy.</font></figcaption> </figure></div>
</div>

For very low temperatures, the spins will all rapidly align themselves with those of their neighbors in an orderly fashion. High temperatures produce unordered systems that do not necessarily converge to a steady state solution. Identifying the **critical temperature** below which large conglomerates of like spins appear was one of the goals of this project.

<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/isingmodel/isingenergy.png" width="290" height="200"> <figcaption><font size="3">System energy at the end of each simulation. Colder temperatures lead to more ordered systems with lower energy.</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/isingmodel/isingmagn.png" width="300" height="200"> <figcaption><font size="3">Average magnetization of the system (+1 for up spin, -1 for down spin). As the temperature decreases, most simulations end with either all up or all down spins.</font></figcaption> </figure></div>
</div>

[animation](https://drive.google.com/open?id=1PCurBmP5v0ob1E0UodKkJlWlzoWzD15q "Video of 2D Ising Model simulation")



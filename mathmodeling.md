---
layout: page
title: Mathematical Modeling
---

### Ising model: studying phase transitions with Monte Carlo methods
#### (2016)

<p> </p>

As part of a class on Monte Carlo methods at Bates College, I simulated the behavior of a two-dimensional **Ising model** - a mathematical description of ferromagnets - using the **Metropolis-Hastings** algorithm. This model depicts a lattice of up/down spin particles whose natural tendency is to align themselves with their neighbors, thus lowering the overall energy of the system. 

In each iteration of the algorithm, a random particle is chosen. If flipping its spin produces a lower energy (*e.g.* a spin down particle surrounded by spin up particles), the spin flip is accepted. If not, the probability of this particle maintaining its current state is proportional to 

<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/isingmodel/isingbefore.png" width="300" height="200"> <figcaption><font size="3">caption1</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/isingmodel/isingafter.png" width="300" height="200"> <figcaption><font size="3">caption2</font></figcaption> </figure></div>
</div>

<div style="width: 100%; overflow: hidden;">
    <div style="width: 45%; margin-left: 5%; float: left;"> <figure><img src="/img/isingmodel/isingenergy.png" width="290" height="200"> <figcaption><font size="3">caption1</font></figcaption> </figure>  </div>
    <div style="width: 45%; margin-right: 5%; float: right;"> <figure><img src="/img/isingmodel/isingmagn.png" width="300" height="200"> <figcaption><font size="3">caption2</font></figcaption> </figure></div>
</div>

[animation](https://drive.google.com/open?id=1PCurBmP5v0ob1E0UodKkJlWlzoWzD15q "Video of 2D Ising Model simulation")



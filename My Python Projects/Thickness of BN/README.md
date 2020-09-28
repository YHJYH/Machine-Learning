# Introduction 
This is the second assignment of three assignments of the course PHYS20161 Introduction to Programming for Physicists.<br>
<br>
BN is  a  crystalline  compound  that  is  composed  of  2D  layers  of  boron  and  nitrogen  in  a hexagonal lattice.  
It is often used as an electrical insulator or as a substrate for graphene.
In this project you will measure the thickness of a sample of BN by analysing the fraction of electrons that tunnel through. 
You will do this using an approach that is very similar to what is implemented at research level.<br>
## Background Theory
Quantum  tunnelling  allows  a  particle  to  pass  through  a  potential  at  energies  that  classicallywould be forbidden. The fraction of projectiles that tunnel through the barrier are given by the transmission coefficient,_T_:<br>
_T=e^−βd_,(Eq.1)<br>
where _d_ is the thickness of the material and<br>
_β= 2√\[2m/h^2 \* (V0−E)]_,(Eq.2)<br>
where the particle has mass _m_ and energy _E_. _V0_is the height of the potential.  this is illustrated in figure 1.  Last year you explored QM tunnelling across a square barrier using equation 2 in vibrations and waves (PHYS10302)<br>
In a more realistic scenario, we would expect the barrier to have rounded edges.  Therefore the height of the potential varies with distance.  This means we instead must integrate over thethickness of the material,<br>
_T= exp\[−2∫√2m/h^2 \* (V(x)−E)dx_ integrate from _d1_ to _d2_(Eq.3)<br>
where _d2_ and _d1_ represent the edges of the barrier.  For a square well we would find _d2−d1=d_ from before.<br>
We use the following form for the potential\[1]<br>
_V(x) =V0 − 1.15λd^2/x(d−x)_(Eq.4)<br>
where<br>
_λ=e^2\*ln2/8π\*sigma\_r\*sigma\_0\*d_ (Eq.5)<br>

\[1]We use the same approach as described by Simmons, J. G. (1963).Generalized formula for the electric tunnel effect between similar electrodes separated by a thin insulating film. Journal of applied physics, 34(6), 1793-1803.

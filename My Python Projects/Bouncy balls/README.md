# Introduction
This is the firstassignment of three assignments of the course PHYS20161 Introduction to Programming for Physicists.<br>

## Analytical approach
We can calculate  the number  of bounces analytically using conservation of energy.  <br>
At height _h_ the ball will have a potential energy of _mgh_, where the symbols have their usual meanings.<br>
After one bounce the ball reaches a height _hη_ (0< _η_ <1) where _η_ takes into account energy lost during the bounce (an efficiency if you will). <br>
After a second bounce the ball will reach a height _hη^2_, and so on.<br>
<br>
We can find the number of bounces above some minimum height,_h\_min_,  by examining the energy loss: _mgh\_min_ = _mghη^n_,<br>
where _n_ represents the number of bounces.<br>

## Expectations
Given user input for the initial height, minimum height of interest, and _η_; we expect your codeto be able to calculate the following:<br>
1. The number of bounces over _h\_min_, _n_.<br>
2. How many seconds it takes to complete these bounces.<br>
We will also be marking you on programme style and expect your code to contain:<br>
1. A clear header with the author, date and purpose of the code.<br>
2. Reasonable assumptions for any constants that should be clearly named.<br>
3. Useful functions that break up the calculations.<br>
4. Unambiguous variable and function names.<br>
5. Results outputted clearly.<br>
We will award additional marks based on how well written the submission is and if it can provide any additional information.  For instance,  does it validate any of the input variables? Does it validate them well?  Can it calculate anything else?  Can the user decide this?<br>
Good luck!

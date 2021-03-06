# Newman_BAND
MATLAB code for John Newman's BAND numerical method. 

Modified from original FORTRAN code in Appendix C of "Electrochemical Systems" 3rd ed. by John Newman and Karen Thomas-Alyea.

Original publication for BAND method:
Newman, John. Numerical Solution of Coupled, Ordinary Differential Equations. I&EC Fundamentals. 7:3, 1968. pp. 514-517

Test problem is a ternary diffusion problem using Stefan-Maxwell equations and two Dirichlet boundary conditions, from Chapter 2 in "Multicomponent Mass Transfer" by Ross Taylor & R. Krishna (example 2.1.1). 

This program includes 5 files:

autoband_test: run this file. 
defines operating conditions, number of variables, initial guess, intializes variables

autoband: calculates derivatives of each governing equation by each variable, at mesh points j-2, j-1,j,j+1,j+2

band: solves for and returns change variables

eqn: includes governing equations (must sum to zero)

matinv: inverts banded matrix in band algorithm

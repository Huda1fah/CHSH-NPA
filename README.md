# CHSH-NPA
This Repo will contain codes for NPA and CHSH Inequality which are almost constructed for any generalized use.
The code for CHSH is still under development therefore, if you come up with something better, you will be good to go.

######
HOW THE CODE WORKS
#####

For CHSH, we take 2 observers, Alice and Bob and they share a state Psi. The value of the observables lies between -1 and 1.
The technique we have implemented is an optimization technique called See-Saw.
We initialize a random state, but any state depending upon the use can be used.
Then we iterate for Bob's observable using CVX , and by keeping the other variables constant, 
we get B1, B2. Then we optimize the Alice variables and similarly the optimized A1, and A2.
So before the final iteration, we get optimal A1, A2, B1, and B2 then we optimize rho using these variables 
we get an optimized rho. We put this rho again in the starting loop till the specified iterations.

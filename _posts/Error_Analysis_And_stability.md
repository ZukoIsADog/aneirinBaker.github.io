## Error Analysis 

Now that we have discussed several methods and shown that some are better than others it would be wise to begin discussing how exactly to determine which algorithm/method is better than the otheres. Scientists and Mathematicians have work out ways to determin properties of these algoirhtms to quantify how good (or bad) an algorithm is. 

### Stability 

The solutions to our systems may be a little inaccurate however it would be goof to know when our solutions are going to beocome innacurate and spiral out of control. If we can predict this before hand this will be ery useful .
The ideal of stability is that some small perturbations in the initial conditions will magnify erros ehilst some will be dampened out (If anyone has heard of Chaos thoery then these ideas will be familiar). A stability analysis will show which one of these proosibilities will occur, ideally we want our system to dampen out the errors.

In it's most simple form it is very easy to undersatdn what is going on. We first take a solution to the ODE 

\\[ y'(x,t) = f(y,t)\\] 

We require that a solution that is perturbed by a small factor $ \epislon $ we shall require that the solution not change by a factor c which is sufficently small , in maths terms

\\[ | Y_e - Y| \leq c | e| \\]

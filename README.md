Download Link: https://assignmentchef.com/product/solved-math565-homework-3
<br>
1.      Suppose the sequence {xn} converges linearly to the limit x with asymptotic error constant λ. Further, suppose that xn+1 − x, xn − x and xn−1 − x are all the same sign. Show that

(1)

2.    A sequence {xn} converges superlinearly to x provided

= 0                                                     (2)

Show that if xn → x with order of convergence α &gt; 1, then {xn} convergences superlinearly.

3.    Suppose that {xn} converges superlinearly to x. Show that

= 1                                                    (3)

Why might this be useful when developing root-finding schemes?

4.   Use the Bisection method to find the root of the equation f(x) = x2 − 1051. Estimate the number of iterations required to reach a tolerance of τ = 10−10. Can you actually achieve this tolerance? Why or why not? How would you choose a more appropriate tolerance?

5.   For the ”Depth of submersion” problem, we derived the model

(4)

where 0 ≤ β ≤ 1 and 0 ≤ x ≤ 2. Solve f(x) = 0 using a Fixed Point iteration scheme. Find at least three different functions g(x) you can use and decide which ones converge to the fixed point. Solve the problem for β = 0.1 and β = 0.95.

6.   Use the ”Depth of submersion” problem we developed in class to determine the depth to which a glassmarble of radius 2 cm and density 0.040 gcm−3 sinks in the water of density 0.998 gcm−3. You may use any method discussed in class, but you must use your own code.

7.   In the lecture notes for the Method of False Position, we derived an expression for the asymptotic errorconstant for the method, given by

(5)

Show that this satisfies |λ| &lt; 1. Use the notes to consider four possible cases.

1

8.   (Math 565.) The Lambert W function L(x) is defined implicitly by the equation x = yey. In Matlab, for example, this function is implemented lambertw.

To evaluate L(x), we have to solve x = yey for y. The strategy is to use Newton’s Method, and argue that the method converges for every value of x in the domain of the function L(x).

The goal for this problem is to code a Lambert-W function using Newton’s Method.

(a)   Show that the domain for L(x) is [−1/e,∞).

(b)   Write a function L(x) that you can call for any value of x in the domain of the function. In this function, you will call Newton’s Method to determine the appropriate value of y for the input argument x.

(c)    Argue graphically that Newton’s Method will converge for any input value of x in the domain. Hint: Interpret Newton’s Method as a fixed point iteration for the function

(6)

and show that as a fixed point iteration x = g(x) converges. You are not expected to write a formal proof, but instead provide convincing graphical evidence that Newton’s Method will converge for this problem.

(d)   Provide convincing evidence that you are accurately computing L(x). For example, you can check that L(xex) = x for a range of given values x, e.g. x = 3,10,101.

(e)   Plot L(x) over the range [−1/e,10]. On the same graph, plot y = xex and show graphically, that the two functions are inverses of each other.

9.   (Math 565.) The equation h(t) = −33t + 784(1 − e−0.3t)

models the height of a rocket in the air at time t, subject to air resistance. The goal of this problem is to find the time tg at which the rocket hits the ground. With some algebra, this problem can be converted to one for which the Lambert-W function created in problem Problem 8 can be used.

Assuming the ground is at height 0, we need to solve h(t) = 0. To do this, we first convert the model to the general form

At + eBt = 1                                                             (7)

for constants A and B that depend on problem parameters. To solve this general problem for t, we use the transformation

(8)

Substituting this expression for t into (7), we get an equation in u that we can solve using the LambertW function. Then, using (8), we can solve for t to get the time the rocket hits the ground.

(a)    Carry out the steps above to solve the air-resistance model to find the time tg the rocket hits the ground. Report this value to 8 digits of accuracy.

(b)   Create a plot of the rocket trajectory, and provide convincing evidence that your value tg is correct.

(c)    Argue why is it is better to convert the problem to one which we can use L(x) for rather than solving the air-resistance model directly.
# Finding prime numbers with python

### Main objective:
Creating a program that finds all the prime numbers up to a given value **as fast as possible**.
Iterative improvements of this algorithm is shown through 3 functions that are improved versions of the previous. 

### Sub-tasks
There are three main ways of solving this problem, all methods having different levels of efficiency. These three methods are outlined below and includes code snippets with explanations.


## Method 1: Bruteforcing the prime
Bruteforcing the prime numbers includes checking **all** possible factors of a number, and seeing if any give a remainder of 0 when dividing the number being checked. If the condition inside the for-loop below is true, it is evident that the number being checked, `x`, is NOT a prime. See code below for how to do this:

```.py
for i in range(2, x):
  if x % i == 0:
    return False
```

If no factors are found, the function returns `True`, meaning `x` is a prime number.


## Method 2: Testing only integers up to square root of `x`
This method significantly reduces the amount of numbers required to test if the number `x` is a prime. This is done by Only testing the integers up until the square root of `x`.

The reason this is possible, can be illuminated when looking at the example of 36. The factors of 36 are as follows:
* 1 x 36
* 2 x 23
* 3 x 12
* 4 x 9
* **6 x 6**
* *9 x 4*
* *12 x 3*
* *23 x 2*
* *36 x 1*

The key values here are **6 x 6**. This is the square root of 36, and after this the factors highlighted in *cursive* are merely a repeat of the factors before **6 x 6**. 











### Breaking the objective into smaller sub-tasks
The objective outlined above can easily be broken down into smaller sub-problems, that can more easily be thought through and developed, and thereafter be combined to form the larger program. An example of how I would break this task into smaller tasks is shown through the following list:

* Bruteforcing the prime number
* 
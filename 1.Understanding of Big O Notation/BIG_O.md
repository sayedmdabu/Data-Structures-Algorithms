Understanding of Big O Notation


https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/big_O.jpg

the time complexity for selection sort can be defined by the function f(n) = n²/2-n/2


https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Selection%20Sort%20Loops%20Illustrated.png


3. Big O, Little O, Omega & Theta
Big O: “f(n) is O(g(n))” iff for some constants c and N₀, f(N) ≤ cg(N) for all N > N₀

Omega: “f(n) is Ω(g(n))” iff for some constants c and N₀, f(N) ≥ cg(N) for all N > N₀

Theta: “f(n) is Θ(g(n))” iff f(n) is O(g(n)) and f(n) is Ω(g(n))

Little O: “f(n) is o(g(n))” iff f(n) is O(g(n)) and f(n) is not Θ(g(n))

—Formal Definition of Big O, Omega, Theta and Little O


In plain words:

Big O (O()) describes the upper bound of the complexity.
Omega (Ω()) describes the lower bound of the complexity.
Theta (Θ()) describes the exact bound of the complexity.
Little O (o()) describes the upper bound excluding the exact bound.


https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Relationships%20between%20Big%20O,%20Little%20O,%20Omega%20&%20Theta%20Illustrated.png

For example, the function g(n) = n² + 3n is O(n³), o(n⁴), Θ(n²) and Ω(n). But you would still be right if you say it is Ω(n²) or O(n²).



4. Complexity Comparison Between Typical Big Os
When we are trying to figure out the Big O for a particular function g(n), we only care about the dominant term of the function. The dominant term is the term that grows the fastest.

For example, n² grows faster than n, so if we have something like g(n) = n² + 5n + 6, it will be big O(n²). If you have taken some calculus before, this is very similar to the shortcut of finding limits for fractional polynomials, where you only care about the dominant term for numerators and denominators in the end.

https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Another%20way%20to%20look%20at%20Big%20O,%20Image.png

https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Complexity%20Growth%20Illustration.jpeg


1. O(1) has the least complexity
Often called “constant time”, if you can create an algorithm to solve the problem in O(1), you are probably at your best. In some scenarios, the complexity may go beyond O(1), then we can analyze them by finding its O(1/g(n)) counterpart. For example, O(1/n) is more complex than O(1/n²).

2. O(log(n)) is more complex than O(1), but less complex than polynomials
As complexity is often related to divide and conquer algorithms, O(log(n)) is generally a good complexity you can reach for sorting algorithms. O(log(n)) is less complex than O(√n), because the square root function can be considered a polynomial, where the exponent is 0.5.

3. Complexity of polynomials increases as the exponent increases
For example, O(n⁵) is more complex than O(n⁴). Due to the simplicity of it, we actually went over quite many examples of polynomials in the previous sections.

4. Exponentials have greater complexity than polynomials as long as the coefficients are positive multiples of n
O(2ⁿ) is more complex than O(n⁹⁹), but O(2ⁿ) is actually less complex than O(1). We generally take 2 as base for exponentials and logarithms because things tends to be binary in Computer Science, but exponents can be changed by changing the coefficients. If not specified, the base for logarithms is assumed to be 2.

5. Factorials have greater complexity than exponentials
If you are interested in the reasoning, look up the Gamma function, it is an analytic continuation of a factorial. A short proof is that both factorials and exponentials have the same number of multiplications, but the numbers that get multiplied grow for factorials, while remaining constant for exponentials.

6. Multiplying terms
When multiplying, the complexity will be greater than the original, but no more than the equivalence of multiplying something that is more complex. For example, O(n * log(n)) is more complex than O(n) but less complex than O(n²), because O(n²) = O(n * n) and n is more complex than log(n).


Question 2: Rank following functions from the most complex to the least complex.

https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Rank%20following%20functions%20from%20the%20most%20complex%20to%20the%20least%20complex..png

Solution to Section 2 Question:
It was actually meant to be a trick question to test your understanding. The question tries to make you answer O(n²) because there is a nested for loop. However, n is supposed to be the input size. Since the image array is the input, and every pixel was iterated through only once, the answer is actually O(n). The next section will go over more examples like this one.


5. Time & Space Complexity
So far, we have only been discussing the time complexity of the algorithms. That is, we only care about how much time it takes for the program to complete the task. What also matters is the space the program takes to complete the task. The space complexity is related to how much memory the program will use, and therefore is also an important factor to analyze.

The space complexity works similarly to time complexity. For example, selection sort has a space complexity of O(1), because it only stores one minimum value and its index for comparison, the maximum space used does not increase with the input size.

Some algorithms, such as bucket sort, have a space complexity of O(n), but are able to chop down the time complexity to O(1). Bucket sort sorts the array by creating a sorted list of all the possible elements in the array, then increments the count whenever the element is encountered. In the end the sorted array will be the sorted list elements repeated by their counts.

https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Bucket%20Sort%20Visualization.png


6. Best, Average, Worst, Expected Complexity
The complexity can also be analyzed as best case, worst case, average case and expected case.

Let’s take insertion sort, for example. Insertion sort iterates through all the elements in the list. If the element is smaller than its previous element, it inserts the element backwards until it is larger than the previous element.

https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Insertion%20Sort%20Illustrated,%20Image.gif



https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Big%20O%20Cheatsheet%20for%20Common%20Algorithms.png



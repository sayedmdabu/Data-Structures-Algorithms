Understanding of Big O Notation


https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/big_O.jpg

the time complexity for selection sort can be defined by the function f(n) = n²/2-n/2


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


https://github.com/sayedmdabu/Data-Structures-Algorithms/blob/main/1.Understanding%20of%20Big%20O%20Notation/Rank%20following%20functions%20from%20the%20most%20complex%20to%20the%20least%20complex..png



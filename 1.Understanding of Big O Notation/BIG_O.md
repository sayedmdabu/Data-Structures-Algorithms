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
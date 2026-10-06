**Order of complexity or O(n)** measures performance and scale, and it calculates how much execution time or memory usage explodes as data input **n** grows.  


**Cyclomatic complexity** measures code structure and testability, and it counts the number of linearly independent paths thru your code, driven by if, loop, and switch logic. It shows how hard it is for you to understand the code, and how many unit tests you will need to cover every scenario.



### Order of complexity O(n)

| Complexity | Description | Example code |
|-|-|-|
|**O(1)** Constant 🔆 **Excellent**|• Always does the same amount of work. <br />• No matter how large the input grows, does the execution time stay exactly the same?|var item = items\[0]|
|**O(log n)** Logarithmic ✅ **Very good**|• Keeps throwing away half the remaining work. <br />• Am I cutting the remaining search space or workload roughly in half each iteration?|while (count > 1) <br />  count /= 2|
|**O(√n)** Square Root ☑️ **Good**|• Only checks up to the mathematical square root of the boundary. <br />• Do I only need to test factors or values up to √n?|for (int i = 0; i \* i < n; i++)|
|**O(n)** Linear ☁️ **Average**|• Visits every single item in the collection once. <br />• Do I need to touch or process every individual item exactly once?|foreach (var item in items)|
|**O(n log n)** Linearithmic 🪫 **Below average**|• Sorts data or repeatedly splits data efficiently. <br />• Am I sorting a collection or repeatedly splitting and merging data?|for (int size = n; size > 1; size /= 2)<br />  for (int i = 0; i < n; i++)|
|**O(n²)** Quadratic ❌ **Bad**|• Every item checks every other item in the dataset. <br />• For each item, do I scan all items (or the remaining items) again?|foreach (var a in items) <br />  foreach (var b in items)|
|**O(n³)** Cubic 📉 **Very bad**|• Every item checks every possible pair of items. <br />• Do I have three deeply nested loops iterating over the dataset?|foreach (var a in items) <br />  foreach (var b in items) <br />   foreach (var c in items)|
|**O(2ⁿ)** Exponential 💥 **Disastrous**|• Each increase in input size doubles the total work. <br />• Does each function step branch recursively into two or more independent paths?  <br />**Visualisation (n=3):** DoThing(3) <br />➡️ DoThing(2) ➡️ DoThing(1) and DoThing(1)<br />➡️ DoThing(2) ➡️ DoThing(1) and DoThing(1)|DoThing(int n) { <br />  DoThing(n - 1)<br />  DoThing(n - 1)<br /> }|
|**O(n!)** Factorial ☢️ **Nuclear**|• Tries every possible arrangement, order, or permutation.<br />• Am I loop-branching through a shrinking list of choices until no options are left?  <br />**Visualisation (n=3): <br />• 1 ➡️ 2 ➡️ 3 (123)<br />  ➡️ 3 ➡️ 2 (132)<br />• 2 ➡️ 1 ➡️ 3 (213)<br />  ➡️ 3 ➡️ 1 (231)<br />• 3 ➡️ 1 ➡️ 2 (312)<br />  ➡️ 2 ➡️ 1 (321)**|for (int first = 0; first < 3; first++)<br />  for (int next = 0; next < 2; next++)<br />    for (int last = 0; last < 1; last++)|




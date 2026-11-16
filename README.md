## 📲 Code maintainability   
A smartphone is an example of code maintainability.  
  
The touchscreen is a simple interface to use the complexity of the apps, as per John Ousterhout's Philosophy of Software Design.  
The apps are the code that is neatly organised to minimise my thinking for future changes, as per Robert Martin's Clean Code.  

I create highly maintainable code by having a simple interface and neatly organised apps.  
  
**References**  
[John Ousterhout - The Philosophy of Software Design](https://www.amazon.co.uk/Philosophy-Software-Design-John-Ousterhout/dp/1732102201)  
[Robert Martin - Clean Code](https://www.amazon.co.uk/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)  
[Microsoft best practice on code metrics such as maintainability and cyclomatic complexity.](https://learn.microsoft.com/en-us/visualstudio/code-quality/code-metrics-values)  
[Reddit community discussion about best code maintainability.](https://www.reddit.com/r/softwarearchitecture/comments/1l01moi/clean_code_vs_philosophy_of_software_design_deep)  

  
## 🔄 Code complexity  

**Order of complexity or O(n)** measures performance and scale.  
As data (n) increases, then run time and memory usage increases.  

**Cyclomatic complexity** measures code structure and testability.  
The number of code paths, from If conditions and For loops, for understanding code and creating tests.  

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
  
  
**References**  
[Wikipedia on Big O Notation.](https://en.wikipedia.org/wiki/Big_O_notation)  
[What is cyclomatic complexity and how to reduce it?](https://sourcegraph.com/blog/cyclomatic-complexity-what-it-is-and-how-to-reduce-it)  
[A philosophy of software design versus clean code.](https://github.com/johnousterhout/aposd-vs-clean-code)  
[IMB: what is cyclomatic complexity and best practices.](https://www.ibm.com/think/topics/cyclomatic-complexity)  
  

## Chapter 2 - Implementing a Parser and AST

1. The Abstract Syntax Tree (AST)
2. Parser Basics
3. Basic Expression Parsing
4. Binary Expression Parsing 
5. Parsing the Rest
6. The Driver
7. Conclusion


- Let's break each thing 

We will build full [parser](https://en.wikipedia.org/wiki/Parsing) for our langauge. The parser we will build uses a combination of [Recursive Descent Parsing](https://en.wikipedia.org/wiki/Recursive_descent_parser) and [Operator-Precendence Parsing](https://en.wikipedia.org/wiki/Operator-precedence_parser) to parse parse the "K" langauge (the latter for binary expressions and the former for everything else).


### The Abstract Syntax Tree (AST)
The AST for a program captures its behavior in such a way that it is easy for later stages of the compiler (e.g code generation) to interpret. We basically want one object for each construct in the language, and the AST should closely model the langauge. 


`Parser, syntax analysis or syntactic analysis` --> is the process of analyzing a string of symbols, either natural languagem computer languages or data structures, conforming to the rules of a formal grammer.


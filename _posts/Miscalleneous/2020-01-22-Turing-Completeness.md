---
layout: post
category: Miscellaneous
tags: cs
---


Today I learnt about turing completeness, what it means to call a machine or a programming language turing complete. 

The idea of turing completeness stems from automata theory. A formal definition of turing complete would be as follows: 
>A computer or a programming language is said to be Turing complete if it can implement a Turing machine or if any system is Turing Equivalent. A Turing machine is a mathematical model of computation that can, in principle, perform any calculation that any other programmable computer can.  

But in practicality, modern computation machines/programming languages, are called turing complete if they can emulate a turing machine. 

## A halting problem interpretation of Turing Machines
The halting problem is a problem from computability theory. The problem itself is as follows: 
> Given any arbitrary program and an input to the program, determine if the program halts or not

An example of an arbitrary program, which doesnt halt would be as follows: 
```c++
while(1){
    ...
}
```
In the abstract framework, there are no resource constraints i.e no constraints on amount of time or storage. In turing machines the halting problem is undecidable. That is given an arbitrary program and its input, its not possible to determine if it halts or not in a turing machine. So inversely, we can think of machines on which the halting problem is undecidable to be turing complete.

Most modern programming languages are turing complete. That is you can write any arbitrary program f in them, but there is no program which given the program f and its input determine if it halts or not. Conversely, turing incompleteness in programming languages often comes from the weaker argument that, you can't write any arbitrary program in the given language. Hence the halting problem just wouldn't come into existence. 


In a more practical sense, 
```c++
int add(int i){
    return i + add(i +1)
}
int main()
{
  int x = add(1);
  return 0;
}
```
While practically when you try to run this program, the program would crash due to memory issues, given infinite storage this would just make the compiler hang. The compiler would be unable to decide the "halt-ness" of this program and since that would be undecidable you could call the language turing complete.



## The proof of halting problem being undecidable - Proof by Contradiction
Consider the existence of a machine `P` which can decide if a program halts or not. When the input and the program, `(f,i)` is inputted into the program `P`, it can mention if its halts or not. 
Consider another program `X` which takes some program `g` as some input, The pseudo-code for this is as follows:
```c++
void P(program f, input i){
  if (...){
    return halts
  }
  else {
    return doesn't halt
  }
}

void X(g){
  if(P(g, g) == halts) {
    loop forever;
    }
  else {
    return;
  }
}
```
Although this program would work for most programs, lets consider the case of when the program `X` runs `X` itself.
```c++
X(X){
  if(P(X,X) == halts){
    loop forever;
  }
  else {
    return;
  }
}
```
The issue here is, if the function P can successfully predict that the program `X` won't halt then, the program X(X) will never halt, then the program will run infinitely long and it has failed to do what it was tasked for. and if the program does say that this program will successfully halt, then due to condition, the if struct will trigger and it will loop forever. Since, for both cases, it turns out that it can't successfully decide on the halting issue, the existence of such a machine `P` which decides on haltability is imposssible to have and hence the halting problem is undecidable.


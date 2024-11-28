---
marp : true
theme: default
class: default
math: mathjx
footer: "Ajeet Kumar | ajeetskbp9843@gmail.com | [Linkdin Profile]()"

---
# <!--fit -->Computation Theory


---
## Table of Contents
| [0. Preliminaries](#ch-0--preliminaries) | [1. Introduction](#ch-1--introduction) | [2.Deterministic Finite Automata(DFA)](#ch-2-deterministic-finite-automata) |[3. Non-determistic Finita Automata(NFA)](#ch-3--non-deterministic) | [4.$\epsilon$-Non-determinstic Finite Automata($\epsilon$-NFA)](#ch-4---non-determinstic) | [5. Finite Automata : Equivalance and Minimization](#ch-5--finite-automata) | [6. Grammer of a Language](#ch-6--grammer-of-a) |[7.0 Regular Expression of a Lanugage](#ch-7--regular-expression-of) |


---
## <!--fit--> Ch-0 : Preliminaries


---
## <!--fit--> Ch-1 : Introduction

---
1. What is the **need** to study **theory of computation** ?
> *There are certain questions like
>   1. What are mathematical properties of the computer hardware and software ?
>   2. What is a computation and algorithm ? Can we formally define them ?
>   3. What are the limitations of computers(computing machine) ? Can we compute anything ?

2. What is the main aim and purpose to study theory of computation ?
> Able to develop the formal mathematical models of computation like deterministic finite automata, non-deterministic finite automata and turing machine(it can model real world classical computers)

<!--footer: ""-->
---

3. Can any mathematical problem be solved systematically ?
> In search of the answer to this question, mathematician and others started to understand the meaning of computation since 1930, which led to the development of the following fields in computation
> 1. Complexity Theory
> 2. Computability Theory
> 3. Automata Theory

---
## Complexity Theory
4. What makes problems computationally difficult(hard) and easy(soft) ? 
5. What is computationally easy and hard problems ? 
> Those problems which are efficiently solvable are computationaly easy problem while problems we don't know whether they can be efficiently solved or if we can't solve them efficiently are called as hard problems.

6. What is the soul purpose of complexity theory ?
> Able to classify the computational problems according to their degree of difficulty and prove the problems which seems hard are really hard and vica versa.

---

## Computability Theory
7. What are the fundamental mathematical problems that are not solvable by computers?
> Let's a mathematical problem like Is an arbitary mathematical statement is true or false ? So, it can't be solved without formal definition as we know from logics. Thus, there is a need arise for formal notion of the  computer, algorithm and computation to build a theoretical model shows that a problem is solvable or unsolvable which led to the developement of the real classical computers today.

8. What is soul purpose and aim of computability theory ?
> Able to Classify problems as solvable or unsolvable.

---
## Automata Theory
9. What is Automata Theory ?
> We define the definitions and properties of computation models like 
>  1. Finite Automata used in text processing, compiler design and hardware design.
>  2. Context-Free Grammer used to define programming languages and Artificial Intelligence.
>  3. Turing machine used as abstract model of the real classical computers like Personal Computers at our Home i.e Laptop or Desktop.

10. What is the soul purpose and aim of the Automata Theory ?
> Able to identify do These models have same powers or can one model solve more problems than the other ?

---
**Analysing Fundamental Capabilities and limitation of Systems**
- fundamental capabilities and limitations
of computers. 
- mathematical properties of computer hardware and software.
- Theory in practice like the design of
new programming languages, compilers, string searching, pattern
matching, computer security, artificial intelligence, etc.
- Problem solving skills. Theory
teaches you how to think, prove, argue, solve problems, express,
and abstract.
- To better understand the complex computers in an abstract and
simple mathematical model.

---
## <!--fit--> Ch-2: Deterministic Finite Automata

---
### Deterministic Finite Automata
> A finite automaton is a 5-tuple $D = (Q, \Sigma, \delta, q_0, F)$ where
> 1. Q is the finite set of all states
> 2. $\Sigma$ is the finite set of input alphabets
> 3. $\delta : Q \times \Sigma \to Q$ is a transition function defined as $\delta(q, a) = p$
> where $q, p \in Q$ and $a \in \Sigma$.
> 4. $q_0 \in Q$ is initial/starting state
> 5. $F \subseteq Q$ is the set of all final/accepting states where $F = \{q_1, q_2, \dots, q_k. \}$

Transition function is the program of DFA machine which tells us what $D$ can do in each step.

---
Consider a switch in an electric board for controlling the light bulb/fan etc. Now, Modeling this ON/OFF Switch problem with DFA is $D = (Q, \Sigma, \delta, q_0, F)$
1. $Q = \{ON, OFF \}$
2. $\Sigma = \{Push\}$
3. $\delta(ON, Push) = OFF$ and $\delta(OFF, Push) = ON$
4. $q_0 = OFF$
5. $F = \{ON\}$

Transition Table of DFA
|$\delta$ | Push |
|---------|------|
|  ON     | OFF  |
| OFF     | ON   |

State Diagram of DFA

---
Consider problem of controlling highway's toll gate i.e designing a computing machine that controls the highway's toll gate
1. When a car, trucks and heavy machinaries arrives at the toll gate, gate is get closed.
2. Toll gate gets open when driver paid the amounts 25, 50, 100 Rs for car, truck and heavy machinary.

In order to modeling this problem, we have to decides the process of the machine
1. States $Q = \{q_0, q_1, q_2, q_3\}$
2. Alphabet $\Sigma = \{25, 50, 100\}$
3. Transition Function $\delta(q_i, a) = q_j$ where $0 \le i, j \le 3$
4. Starting state $q_0$
5. Final State $F = \{q_3\}$

---
Transition Table for the DFA of the Cotrolling toll gate is
|$\delta$ | 25 | 50 | 100 |
|---------|----|----|-----|
|$q_0$      |
|$q_1$      |
|$q_2$      |
|$q_3$     |

State Transition Diagram for DFA of Controlling gate

The main focus of designing DFA is what types of string input are accepted by DFA.

---
0. Concatenation Operation of finite sequence of input alphabets
1. Kleene Star/Closure Operation of string of any length
 - $\Sigma^0 = \epsilon$
 - $\Sigma^1 = \Sigma = \{a, b, c, \dots\}$
 - $\Sigma^2 = \Sigma . \Sigma = \{ab, ba, ac, ca, bc, cb, \dots, \}$
 - $\dots$
 - $\Sigma^* = \{\epsilon, a, b, c, ab, ac, bc, ca, ba, cb, \dots\}$
 - $\Sigma^* = \Sigma^0 \bigcup \Sigma^1 \bigcup \Sigma^2 \dots \bigcup \Sigma^k, \dots$

Hence $\Sigma^*$ is the set of all possible string using input alphabet $\Sigma$ of any length  including zero legth string.


---
## <!--fit-->Ch-3 : Non-deterministic
## <!--fit-->Finite Automata (NFA)

---
### Non-deterministic Finite Automata
> A finite non-deterministic automaton is a 5-tuple $N = (Q, \Sigma, \delta, S, F)$ where
> 1. Q is the finite set of all states
> 2. $\Sigma$ is the finite set of input alphabets
> 3. $\delta : Q \times \Sigma \to P(Q)$ is a transition function defined as $\delta(q_j, a) = \{q_i\}$ where $ \forall i$.
> where $q, p \in Q$ and $a \in \Sigma$.
> 4. $S \subseteq Q$ is finite set of inital/starting state
> 5. $F \subseteq Q$ is the set of all final/accepting states where $F = \{q_1, q_2, \dots, q_k. \}$

---

---
## <!--fit-->Ch-4 : $\epsilon$-Non-determinstic
## <!--fit-->Finite Automata($\epsilon$-NFA)

---
## <!--fit-->Ch-5 : Finite Automata
## <!--fit-->Equivalance and Minimization

---
## <!--fit-->Ch-6 : Grammer of a 
## <!--fit-->Language of a Finite Automata

---
## <!--fit-->Ch-7 : Regular Expression of
## <!--fit-->a Language of a Finite Automata
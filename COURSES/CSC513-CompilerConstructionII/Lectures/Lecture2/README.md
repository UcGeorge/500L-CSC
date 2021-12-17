[COURSES](../../README.md) > [CSC 513 - COMPILER CONSTRUCTION II](../../README.md) > LECTURE 2

# CSC 513 - COMPILER CONSTRUCTION II: LECTURE 2

### RECORDING: [https://drive.google.com](https://drive.google.com/file/d/1OzFAehHP6v5_7qZge0fSr0uhUUvs3W-Y/view?usp=sharing)

## Overview of the Lecture

- Context Free Grammar (CFG)
  - Issues Surrounding Grammar
- How to write a Grammar
- BASIC BLOCK AND FLOW GRAPH

---

Context Free Languages consist of:

- Context Free Grammars (CFGs)
- Pushdown Automata (PA)

---

Formal Definition of Grammar : `G = (V,T,S,P)`

- `V` : Set of variables
- `T` : Set of terminal symbols
- `S` : Start variable
- `P` : Set of production rules

---

Production rules (`P`) can be in the forms:

- `A → xB`
- `A → Bx`
- `C → x`
  > Where `x` is a string of terminals.

---

## Derivations

- Grammar rules determine the legal strings of token symbols by means of derivation.
- Derivation is a sequence of replacements of structure names by choices on the right-hand sides if grammar rules.
- A derivation begins with a single structure name and ends with a string of token symbols
- At each step in a derivation, a single replacement is made using one choice from a grammar production rule.

---

## Symbols in Rules

- Start symbol
  - The most general structure that is listed first in the grammar production rules.
- Non-terminals
  - Structure names are also called non-terminals since they always must be replaced further on in a derivation.
- Terminals
  - Symbols in the alphabeth are called terminals since they terminate the derivation.
  - Terminals are usually tokens in compiler applications.

---

## Regular vs. Context-free Grammar

A regular grammar is either right or left linear, whereas context free grammar is any combination of terminals and non-terminals.

Hence regular grammars are a subset of context-free grammars. Grammar generating pilandromes is not regular:

- `S → ABA`
- `A → something`
- `B → something`
  > The name context-free grammar is explained by property of productions that are independent of the surrounding symbols. There are also context-sensitive grammars where productions depend on the context (symbols that surround variables)

---

## Advantages of context free grammar

- A grammar give a precise, yet easy to understand, syntactic specification of a programming language.
- An efficient parser can be constructed automatically from a property designed grammar.
- A gram imparts a structure to a program that is useful for its translation into object code for the detection of errors.

---

## Definition: Context-Free Languages

A language `L` is context-free if and only if there is a grammar `G` with<br>
`L = L(G)`

---

## Ambiguity

A context-free grammar `G` is ambigous if some string `w ∈ L(G)` has two or more derivation trees (two or more leftmost/rightmost derivations)

# AI Knowledge - Knights and Knaves Logic Puzzle 

## Introduction

In 1978, logician Raymond Smullyan published “What is the name of this book?”, a book of logical puzzles. Among the puzzles in the book were a class of puzzles that Smullyan called “Knights and Knaves” puzzles.

In a Knights and Knaves puzzle, the following information is given: Each character is either a knight or a knave. A knight will always tell the truth: if knight states a sentence, then that sentence is true. Conversely, a knave will always lie: if a knave states a sentence, then that sentence is false.

The objective of the puzzle is, given a set of sentences spoken by each of the characters, determine, for each character, whether that character is a knight or a knave.

## Example Puzzle

Let's consider a simple example to illustrate how these puzzles work:

**Character A says:** "I am both a knight and a knave."

Here's the logical reasoning:
- If A were a knight, the statement would have to be true, as knights always tell the truth.
- However, the statement cannot be true because a character cannot be both a knight and a knave simultaneously.
- Therefore, we conclude that A must be a knave.

More complex puzzles involve multiple characters and statements, making them challenging to solve.

## Solving with Propositional Logic

To automate the solution to Knights and Knaves puzzles, we can represent the problem using propositional logic. Each character's identity (knight or knave) and their statements can be translated into logical expressions. An AI running a model-checking algorithm can then deduce the correct identities of the characters based on the logic and constraints provided.

In the context of this project, there is a Python script (`logic.py`) that defines various classes for different types of logical connectives, such as And, Or, Not, and more. These classes can be composed within each other to create complex logical sentences, representing the statements made by different characters. 

The `model_check` function in `logic.py` takes a knowledge base and a query. The knowledge base is a single logical sentence, and if multiple logical sentences are known, they can be joined together using the And expression. The `model_check` function recursively considers all possible models and returns `True` if the knowledge base entails the query, and `False` otherwise.

The main function of `puzzle.py` loops over all puzzles, and uses model checking to compute, given the knowledge for that puzzle, whether each character is a knight or a knave, printing out any conclusions that the model-checking algorithm is able to make.

Feel free to explore the provided code and add your own logical statements to the knowledge bases to solve the Knights and Knaves puzzles.



------------

<sup>This repo is part of Harvard's CS50 AI studies.</sup>

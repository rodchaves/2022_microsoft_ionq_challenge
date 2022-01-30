# iQuHACK 2022 Microsoft + ionQ challenge
Authors: Bárbara Andrade, Braulio Antonio, Roberto Arevalo, and Rodrigo Chaves

# Amaze Maze 

A quantum program was written to create the Quantum Amaze Maze. The game was created as part of the IonQ + Microsoft Joint Challenge @ MIT iQuHACK 2022. The Quantum Amaze Maze contains quantum computing aspects. The game consists of the user choosing gates which will result in realization of a specific state. After the decisions are made entanglement can be calculated. The decision to use a switchgate was done for simplicity. The use of Microsoft Azure with Qiskit and IonQ was used in the creation of the game. Qiskit and IonQ allow for programming in Python.

## Brief description
We propose a quantum maze: the user is given a 4-qubit product state $|{0000}\rangle$, and the goal is to choose a sequence of gates (we regard this as a quantum path) which produces a maximally mixed state in the end (shows all possible outputs with same probability).

## Motivation
Quantum mechanics is a fascinating theory that features some counter-intuitive phenomena. In this project, we give the user the opportunity to experience the manifestation of a key aspect of the quantum theory: the non-commutativity of physical observables. In the game, the player uses such ingredient to create a maximally mixed state.

## Physics
The game allows the following 1-qubit, and 2-qubit gates: X,Y,Z, Hadamard, CNOT, SWAP, CHadamard, CX, CY, and CZ. Some of these operators do not commute, and this creates quantum superpositions.

Although we know entangled states are created through the game, it is not straightforward to quantify entanglement since we are dealing with a real quantum computing experiment, and its outputs are probabilities associated to product 4-qubit states. For this reason, in the game we propose that the user creates a maximally mixed state, which is a state we know how to identify: it has probability equals $\frac{1}{16}$ for all possible modes.

Given a set of output probabilities $\{p_j\}$, we associate a score to it, defined as how much it deviates from the maximally mixed probability distribution. $s(dP) = \frac{1-dP}{1-dE}$, where $dP$ and $dE$ are Manhattan distances between a point, corresponding to a probability distribution, and the origin in a $2^4$ real space. The maximally mixed state is the one that minimizes this distance. With this definition, the score ranges from 0 to 1.

## Game mechanics
The game is in the file "the amaze maze.ipynb" and you need to run all the cells before playing. 

The games mechanics is the following:

- Every round the player starts in the 4-qubit state $|{0000}\rangle$;
- Every round has 5 stages (this can be modified in a later version);
- In each stage the player can choose between two different gates to apply (by inputing a or b) to some of their qubits (so far we have included only 1 and 2 qubit gates);
- At the end the player will receive a score that is calculated as defined above. We cannot directly measure how entangled this state is, but maximally mixed states are always maximally entangled;
- The maximum score and name of the player who scored is saved for subsequent rounds.

The "1 round of the game on the quantum hardware.png" includes a screenshot of the game.

## What's next
There are two things that could be easly implemented to make the game more fun! 

The first one is to connect our quantum backend with a real maze game like the one in maze.py (the code is from Keno Leon: https://k3no.medium.com/build-a-maze-with-python-920ac2266fe7 ). 

The second is to add more qubit gates!
There are more than 70 gates available on qiskit and it is just a matter of some more lines of code to have them in our game.

## Team's experience
It has been a positive experience for all of us being able to collaborate and learn from the scholars from MIT and other institutions. Being able to listen and participate in the tutorials and talks from professors of different universities has also been very insightful. Gaining experience with Microsoft's quantum hardwares that are used in the field of quantum computing has been invaluable. This was the first hackathon for most of us, and there were several new things, such as taking initiative, brainstorming, and having to work with very limited time. It feels refreshing to participate in a project just for fun and not for work.

## Link to presentation!
https://docs.google.com/presentation/d/1Yoxlu7wUPkGhHYH9V8vZ1PizcXqinkEVudkeapg6W7c/edit?usp=sharing 

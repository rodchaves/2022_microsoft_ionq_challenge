### The Amaze Maze

This game's purpose is to show how qubits can get entangled by applying different gates on them.

## The mechanics

The games mechanics is the following:
- Every round the player with starts with a qubit in the |0000> state
- Every round has 5 stages (this can be modified in a later version)
- In each stage the player can choose between two different gates to apply to some of their qubits (so far we have included only 1 and 2 qubit gates)
- At the end the player will receive a score that is calculated as indicated below and which serves as a proxy to emasure entanglement. We cannot measure entanglement properly since we do not have access to the full qubit states.

- The maximum score and name of the player who scored is saved for subsequent rounds.

## The context
    
Entanglement and entangle states is a concept that is already tricky to grasp for a 2 qubit system. 
With a higher number of qubits it just becomes harder and harder to anticipate how much entanglement we will have from applying quantum gates.

After a few rounds player will realize that entanglement is not so easy to get from control gates if we start in a |0000> state and that the best startegy is to apply Hadamard gates or convert any of the |0> to |1> and then apply control gates. 

## What's next

There are two things that could be easly added to make the game more fun!

The first one is to connect our quantum backend with a real maze game like the one in maze.py (the code is from Keno Leon: https://k3no.medium.com/build-a-maze-with-python-920ac2266fe7 )

The second is to add more qubit gates! 
There are more than 70 gates available on qiskit and it is just a matter of some more lines of code to have them in our game
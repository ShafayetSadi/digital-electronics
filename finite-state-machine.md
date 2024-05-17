# Finite State Machine

A finite state machine (FSM) is a mathematical model of computation. It is an abstract machine that can be in one of a finite number of states at any given time. The FSM can change from one state to another in response to some inputs; the change from one state to another is called a transition. An FSM is defined by a list of its states, its initial state, and the conditions for each transition. The FSM can be represented by a state transition diagram, a state table, or state equations. FSMs are used in various applications, such as digital systems, control systems, and software engineering.

All the synchronous sequential circuits are finite state machines. The state of the machine is represented by the values of the flip-flops in the circuit. The output of the machine is determined by the current state of the machine and the input to the machine.


## Types of Finite State Machine

There are two types of finite state machines:

1. **Moore Machine**: In a Moore machine, the output depends only on the current state of the machine. The output is associated with each state of the machine. The output is produced after the transition from one state to another.

2. **Mealy Machine**: In a Mealy machine, the output depends on the current state of the machine and the input. The output is associated with each transition of the machine. The output is produced during the transition from one state to another.

In the Moore Machine, the output is associated with the clock signal. Because, the state of the machine is determined by the clock signal. In the Mealy Machine, the output is associated with the input signal and the clock signal. Because, the state of the machine is determined by the input signal and the clock signal.

## State Transition Diagram

A state transition diagram is a graphical representation of a finite state machine. It consists of a set of states, a set of transitions between the states, and a set of inputs and outputs. The states are represented by circles, the transitions are represented by arrows, and the inputs and outputs are represented by labels on the transitions. The state transition diagram shows the sequence of states and transitions that the machine goes through in response to a sequence of inputs. The state transition diagram is used to design, analyze, and implement the finite state machine.

## State Table

A state table is a tabular representation of a finite state machine. It consists of a set of states, a set of inputs, a set of outputs, and a set of next states. The states are represented by rows, the inputs are represented by columns, the outputs are represented by columns, and the next states are represented by cells. The state table shows the sequence of states and transitions that the machine goes through in response to a sequence of inputs. The state table is used to design, analyze, and implement the finite state machine.

The state table for the above state transition diagram is:
TODO

## State Equations



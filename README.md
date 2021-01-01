# Turing-Machine-TM-that-simulates-DFA

Standard Turing Machine (TM) that simulates DFA. The result TM can decide whether the DFA accept or rejects a string.
The input includes an encoded DFA and an encoded string that needs to be input into the DFA. The TM will be running under transducer mode and output is based on whether the DFA accepts the string or not.
![TM](https://github.com/HaiTrieuNg/Turing-Machine-TM-that-simulates-DFA/blob/main/Images/TM.png)

INPUT ENCODING

![Input](https://github.com/HaiTrieuNg/Turing-Machine-TM-that-simulates-DFA/blob/main/Images/Input.png)

The input has 3 parts:

• The input string w for the DFA

Each symbol is encoded into a unary number and separated by a 0 (zero).

In this project, the input symbol will be English lowercase letters. 1 is a, 11 is b, 111 is c, etc.

For example, 10111011 means acb. Note that the input string for the DFA can be λ (this part is empty).

• Transition function δ of the DFA

Each state is encoded into a unary number, so that q0 is 1, q1 is 11, q2 is 111, etc.

Each transition starts with D. And each transition has 3 parts, separated by a 0 (zero):

o Current state: 1, 11, 111, etc. Only one current state per transition;

o Read condition: same as the encoding for the input: 1 is a, 11 is b, etc. Only one symbol per transition;

o Next state: 1, 11, 111, etc. Only one next state per transition.

For example, D11010111 means if the current state is q1, and the current symbol is a, transit to q2.

Note that the transitions are NOT ordered.

• All accepting states of the DFA

This part starts with an F. States are separated by a 0 (zero)

For example, F1011 means q0 and q1 are the accepting states of the DFA.

Note that there may be no final states. But the F will still be there.



OUTPUT

![Output](https://github.com/HaiTrieuNg/Turing-Machine-TM-that-simulates-DFA/blob/main/Images/Output.png)

The TM will be running under transducer mode and accept the input, and output a capital letter (A or R):

• If the DFA accept the string w, the output of your TM should be A;

• If the DFA reject the string w, the output of your TM should be R.

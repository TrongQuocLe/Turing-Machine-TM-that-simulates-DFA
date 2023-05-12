# Turing-Machine-TM-that-simulates-DFA

Standard Turing Machine (TM) that simulates DFA. The result TM can decide whether the DFA accept or rejects a string.
The input includes an encoded DFA and an encoded string that needs to be input into the DFA. The TM will be running under transducer mode and output is based on whether the DFA accepts the string or not.

HaiTrieuNg Ver
![TM from HaiTrieuNg](https://github.com/TrongQuocLe/Turing-Machine-TM-that-simulates-DFA/blob/main/Images/TM%20simulates%20DFA.png)

The Ol'School Ver
![TM from The Ol'School Ver](https://github.com/TrongQuocLe/Turing-Machine-TM-that-simulates-DFA/blob/main/Images/DFA_Accepter_2.png)

## INPUT ENCODING

The input has 3 parts:

• The input string w for the DFA

Each symbol is encoded into a unary number and separated by a 0 (zero).

In this project, the input symbol will be English lowercase letters. 1 is a, 11 is b, 111 is c, etc.

For example, 10111011 means acb. Note that the input string for the DFA can be λ (this part is empty).

• Transition function δ of the DFA

Each state is encoded into a unary number, so that q0 is 1, q1 is 11, q2 is 111, etc.

Each transition starts with T. And each transition has 3 parts, separated by a 0 (zero):

o Current state: 1, 11, 111, etc. Only one current state per transition;

o Read condition: same as the encoding for the input: 1 is a, 11 is b, etc. Only one symbol per transition;

o Next state: 1, 11, 111, etc. Only one next state per transition.

For example, D11010111 means if the current state is q1, and the current symbol is a, transit to q2.

Note that the transitions are NOT ordered.

• All accepting states of the DFA

This part starts with an F. States are separated by a 0 (zero)

For example, F1011 means q0 and q1 are the accepting states of the DFA.

Note that there may be no final states. But the F will still be there.

## OUTPUT

The TM will be running under transducer mode and accept the input, and output a capital letter (A or R):

• If the DFA accept the string w, the output of your TM should be A;

• If the DFA reject the string w, the output of your TM should be R.

## TECHNICAL NOTES

• We assume that the input string of TM is 100% correct. Therefore, your TM is NOT supposed to have any
error detection and/or error reporting.

• Understanding the problem then coming up with more test cases is a part of the project. That is, no other test
cases will be provided other than the example given above.

• You can use "Turing Machine With Building Blocks" in JFLAP. Follow the same procedure as showed in class:

o First, design each block (TM), then insert them as blocks into the .jff for the main design.

o If you want to edit any block, first edit the original file for that block and save it, then in the .jff for the
main design, delete and insert the block again.

o Always have a backup of your current work before modifying it.

o When naming your .jff files, please follow Java’s naming rules as JFLAP is a Java program!

• You can use the Stay option, ! and ~ symbol if needed. For more information, please refer to the lecture notes
as well as JFLAP's documentations and tutorials.

• Because of the complexity of the problem, accepting a string may go through many configurations. In this case,
JFLAP will give you a warning "xxxx configurations have been generated. Should we continue?". If you see this
warning, click yes, until you feel it seems to go forever, then click cancel or no, and manually "debug" the cause
by stepping through the input

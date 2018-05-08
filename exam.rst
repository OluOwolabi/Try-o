..  _cs-lab-procedures:

:Author: Olu Owolabi

..  include::   /references.inc

Introduction
*******************

Is an arrangement of guidelines executed straightforwardly by a PC's focal handling unit (CPU). Every direction plays out a certain assignment, for example, a heap, a hop, or an ALU activity on a unit of information in a CPU enlist or memory. Each program straightforwardly executed by a CPU is comprised of a progression of such guidelines. A substantially more meaningful version of machine dialect, called low level computing construct, utilizes mental helper codes to allude to machine code guidelines, instead of utilizing the directions' numeric qualities specifically. For instance, on the Zilog Z80 processor, the machine code 00000101, which makes the CPU decrement the B processor enroll, would be spoken to in low level computing construct as DEC B.




Purpose of the Code
********************
The program is to be used to count the digits up and down. The code is written in C++ programming language for its translation from the initial assembly language programming.
For the implementation of the program, the use of array was implemented the code to store integers before execution.

..  code-block:: text
  vector <int> integerToArray(int x)
        {
           vector <int> resultArray;
         while (true)
         {
          resultArray.insert(resultArray.begin(), x%10);
         x /= 10;
         if(x == 0)
            return resultArray;
         }
         
..  code-block:: text

    $ cd /HDrive


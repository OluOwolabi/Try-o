
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

    vector <int> integerToArray(int x){
          vector <int> resultArray;
        while (true){
             resultArray.insert(resultArray.begin(), x%10);
               x /= 10;
              if(x == 0)
       return resultArray;
    }


 
The above code snippet is represents the array code for the program. The array lists and stores the integers in the code before it is finally executed through the command line.
The program conversion was to process the code in accordance with the assembly code in the Tom program.


..  code-block:: text

         struct compute: std::ctype<char> {
         compute(): std::ctype<char>(get_table()) {}
          static std::ctype_base::mask const* get_table() {
           static std::vector<std::ctype_base::mask>
                  rc(table_size, std::ctype_base::mask());
                  rc['/'] = std::ctype_base::space;
                   rc['-'] = std::ctype_base::space;
        return &rc[0];
    }
};

..  image:: https://github.com/OluOwolabi/Try-o/blob/master/2.png
    :align: center
    :width: 600
    
    
The above code is the main operation of the program, the code allows the program to enter only numbers and not letters since the processing are only supposed to be numbers only. The program, just like the Tom program, will request the user to enter the exact path for the Tom then it will execute the total value after the processing is done.
This is shown in the above diagram, as the displays after each digit processing.


The Use
*******

The program is a conversion program from the Tom program which was implemented in assembly to C++. The program is used to fetch the path of the Tom and then processes the values as shown in the above diagram. The Path of the Tom in this case is +1+5+7-2 and when it is entered to the program, the program will be executing the by processing each path and displaying the results. The below code is a snippet of the fetcher in C++ 
void printDirectory(File dir, int numTabs) {

..  code-block:: c
		
	#include <bits/stdc++.h>
	#include <string>
	#include <vector>
	#include <algorithm>
	#include<stdio.h>
	#include<stdlib.h>
	#include <sstream>



	using namespace std;

	struct compute: std::ctype<char> {

		compute(): std::ctype<char>(get_table()) {}

		static std::ctype_base::mask const* get_table() {
			static std::vector<std::ctype_base::mask>
				rc(table_size, std::ctype_base::mask());

			rc['/'] = std::ctype_base::space;
			rc['-'] = std::ctype_base::space;

			return &rc[0];
		}
	};
	typedef std::vector< int > ints_t;

	struct veryfyDigit
	{
		int operator()( const char chr ) const
		{
			const int result = chr - '0';
			return result;
		}
	};
	void calc()
	{
		 int number;
		  ints_t* result;
		std::ostringstream os;
		os << number;
		const std::string& numberStr = os.str();
		std::transform(
			numberStr.begin(),
			numberStr.end(),
			std::back_inserter( *result ),
			veryfyDigit() );
	}

	 void mainCalculation(){

	int total=0;
		string key2;
		char factor;
		char key=0;
		cout<<"Enter Major Tom Path : "<<endl;
		cin>>key2;

		int n = key2.length();


		char value[n+1];


		strcpy(value, key2.c_str());

		for (int i=0; i<n; i++){


		  if(value[i]=='+'){

		  factor='+';

		  }else
		   if(value[i]=='-'){

					  factor='-';

		  } else
				if(isdigit(value[i])){
		  if(factor=='+'){

					int z=(int)value[i] - '0';
				   total+=z;
				   factor='0';
		  }else

		  if(factor=='-'){
					  int z=value[i] - '0';
					  total=total-z;
					  factor='0';
		  }else{}

		  } else { }

		}
	 cout<<"Total Value = "<<total<<endl;
	 //+1+5+7-2
	}

	int main()
	{
		mainCalculation();
		veryfyDigit();
	   compute();
		calc();

		return 0;
	}



The code fetches the path which has been entered into the system or program , it then display it on the program ready for the processing.



..  image:: https://github.com/OluOwolabi/Try-o/blob/master/Untitled2.png
    :align: center
    :width: 600





Testing of the Code in C++
************************

This a C++ converted version of Major Toms' Code.

..	code-block:: c
	
	
	#include <bits/stdc++.h>
	#include <string>
	#include <vector>
	#include <algorithm>
	#include<stdio.h>
	#include<stdlib.h>
	#include <sstream>



	using namespace std;

	struct compute: std::ctype<char> {

		compute(): std::ctype<char>(get_table()) {}

		static std::ctype_base::mask const* get_table() {
			static std::vector<std::ctype_base::mask>
				rc(table_size, std::ctype_base::mask());

			rc['/'] = std::ctype_base::space;
			rc['-'] = std::ctype_base::space;

			return &rc[0];
		}
	};
	typedef std::vector< int > ints_t;

	struct veryfyDigit
	{
		int operator()( const char chr ) const
		{
			const int result = chr - '0';
			return result;
		}
	};
	void calc()
	{
		 int number;
		  ints_t* result;
		std::ostringstream os;
		os << number;
		const std::string& numberStr = os.str();
		std::transform(
			numberStr.begin(),
			numberStr.end(),
			std::back_inserter( *result ),
			veryfyDigit() );
	}

	 void mainCalculation(){

	int total=0;
		string key2;
		char factor;
		char key=0;
		cout<<"Enter Major Tom Path : "<<endl;
		cin>>key2;

		int n = key2.length();


		char value[n+1];


		strcpy(value, key2.c_str());

		for (int i=0; i<n; i++){


		  if(value[i]=='+'){

		  factor='+';

		  }else
		   if(value[i]=='-'){

					  factor='-';

		  } else
				if(isdigit(value[i])){
		  if(factor=='+'){

					int z=(int)value[i] - '0';
				   total+=z;
				   factor='0';
		  }else

		  if(factor=='-'){
					  int z=value[i] - '0';
					  total=total-z;
					  factor='0';
		  }else{}

		  } else { }

		}
	 cout<<"Total Value = "<<total<<endl;
	 //+1+5+7-2
	}

	int main()
	{
		mainCalculation();
		veryfyDigit();
	   compute();
		calc();

		return 0;
	}

..  image:: https://github.com/OluOwolabi/Try-o/blob/master/Untitled.png
    :align: center
    :width: 600
         
 

 Fetch, Execute, Decode and Store Unit
 *************************************
	..  image:: https://github.com/OluOwolabi/Try-o/blob/master/Untitled3.png
    :align: center
    :width: 600
         


	




Conclusion
**********

The conversion of  the program to C++ programming language is possible and the results can be displayed with the exactness as the initial Tom program which was in assembly language programming.



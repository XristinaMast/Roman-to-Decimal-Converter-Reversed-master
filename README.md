# Roman-to-Decimal-Converter-Reversed-master



##Purpose##
The purpose of the above code is to convert a number, either an integer or a Roman numeral, to a
to a Roman or integer number respectively. In other words, the user enters a number,
if it is an integer and will convert it to a Roman number, corresponding procedure if
Roman number is entered. My work is therefore divided into three parts: the
the correct data assignment, the conversion
the conversion of an integer number to a Roman number and the conversion of a Roman number
to an integer.




##Code explanation##
First, we reset a flag variable to zero and ask the user to enter
a number, which we do not know either if it is correct (i.e. if it is e.g. "jsiXkm" or "95dk5"), or if it is less than 4000
nor whether it is Roman or integer. Therefore we read an element from the
from the keyboard and store it in a variable x. We move x to a temporary file (temp.file, which we first delete in
in case it already exists) and then using "sed -i" 
we remove as many numbers as the temporary file contains and
store them in a variable a.
Using the same procedure, remove all Roman symbols from the temporary file
and store it in a variable b. We do all the above procedure to
understand what situation we are in and change the value of the flag accordingly, i.e. whether the user i.e.
entered: integer-where we figure out if the variable a equals the blank and is
less than 4000; so the flag variable takes the value 1, Roman numeral-where
we understand it if the variable b equals the blank; so the flag variable takes the value 2 or wrong data where
the flag variable
remains with the value 0. The above process is repeated until the data
entered by the user is correct. Once we are sure that the data
is correct we delete the temporary file we created at the beginning (temp.file) if we are not using it
below and continue the normal flow of the program.


In case the flag variable has the value 1 then, as
mentioned above, the user has entered an integer. However, to show
the correct Roman symbols, we start by comparing the number with 1000 for
we display "M"
and then subtract 1000, this process is done until the
number becomes less than 1000. Then we calculate how many
hundreds the integer contains (with the variable s) while subtracting within a
iteration which terminates as soon as the integer is less than 100 and
depending on the value of s
the corresponding Roman symbol is displayed. The same procedure is used for
of tens. Then, to display the correct units, we compare the
number x
(after subtracting all the thousands, hundreds, etc.) from 1 to
9 and display the appropriate symbol. Note that we display the message
"Your number
is: " before the program starts subtracting units from x, using the echo -n command (also used in
display of symbols) so that the message appears on the same line as the
corresponding Roman symbols.


In the case where the flag variable has the value 2 then, as
mentioned above, the user has entered a Roman numeral. In principle,
we reset a variable ar
which will be incremented in subsequent option structures, in another variable em we store the string size which is decremented by one at each
selection structure, and immediately afterwards in the variable th where we store the last letter of the string (essentially parsing the string from left to right).
So depending on the last character of the string it enters the corresponding structures
option structures (that's why we only use if and not elif, to access each structure)
and changes the variable ar
accordingly. For example, if the last character is I, then the variable ar is added to 1. But suppose
however, the last character is V and then followed by I (i.e. "IV" has been inserted which is 4) then 5 is added to the variable ar and then a
unit and at the end it is displayed. Similarly if "IX" is inserted, first add 10 to the variable ar and then subtract one unit to
display 9. In other words, we add and subtract in the variable ar depending on the character that
we find and display.

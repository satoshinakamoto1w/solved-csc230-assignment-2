Download Link: https://assignmentchef.com/product/solved-csc230-assignment-2
<br>
Upon successful completion of this assignment, you should be able to write C programs that:

<ul>

 <li>Use various C data types</li>

 <li>Create, store data in and read from C arrays.</li>

 <li>Write and call C functions that receive input parameters and return values.</li>

 <li>Use the C bitwise and shift operators</li>

</ul>

The problem to be solved by this program is to input an integer, calculate the factorial of that integer and output the result in decimal and binary.  There is a qualifier, the individual bits of the binary form must be each stored into a separate element of an array.

A sample execution of a program that follows the specifications is:

<table width="610">

 <tbody>

  <tr>

   <td width="610"><strong>FACTORIAL &amp; BIT TESTER </strong><strong> </strong><strong>Input a positive integer value between 0 and 65535 ==&gt; 7  </strong><strong>  7     Factorial =  5040 or 0x13b0     or      0b0001001110110000  </strong><strong>Do another (y/n)? y </strong><strong> </strong><strong>Input a positive integer value between 0 and 65535 ==&gt; 12  </strong><strong>  12    Factorial = 64512 or 0xfc00     or      0b1111110000000000 </strong><strong> </strong></td>

  </tr>

 </tbody>

</table>

Notice that the hexadecimal output is optional and not described in the specifications below.

Since the integers used throughout this assignment are unsigned short, which are 16 bits wide, it will be convenient to have the following constant defined using the pre-processor:

<strong># define SIZE_INT 16 </strong>

Here are the specifications of the functions to be used:  <strong> </strong>

<ul>

 <li>Write a function that accepts an array of <strong>unsigned char</strong> sized integers describing an integer in binary format (each item in the array corresponds to a single bit of the integer) and prints each element of the array as a decimal number. The function prototype (or signature) is:</li>

</ul>

<strong>void printBitArray(unsigned char theBits[SIZE_INT]);  </strong>

<ul>

 <li>Write a function accepts an <strong>unsigned short</strong> sized integer value and an array of <strong>unsigned char</strong> sized integer values. The function places each of the 16 bits of unsigned short integer into different array elements, in the least significant bit location.  If, for example, the input integer was 25 ( = 0x0019 = 0b0000000000011001 ) then the array would need to contain:</li>

</ul>

<table width="355">

 <tbody>

  <tr>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>1 </strong></td>

   <td width="23"><strong>1 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>0 </strong></td>

   <td width="22"><strong>1 </strong></td>

  </tr>

 </tbody>

</table>




The function prototype (or signature) is:

<strong>void toBits(unsigned short value,unsigned char inBits[SIZE_INT]);  </strong>

<table width="582">

 <tbody>

  <tr>

   <td colspan="2" width="582"><strong>NOTE:  While this can be completed using the integer modulus and division </strong></td>

  </tr>

  <tr>

   <td colspan="2" width="582"><strong>operators, more grades will be awarded to code that uses at least 1 bitwise </strong></td>

  </tr>

  <tr>

   <td width="286"><strong>operator and a mask and bit shifting.</strong></td>

   <td width="296"><strong>   </strong></td>

  </tr>

 </tbody>

</table>




<ul>

 <li>Write a <em>recursive</em> function that accepts an <strong>unsigned short</strong> sized integer parameter, calculates and returns the factorial of that value. The return value should also be an unsigned short  The function prototype (or signature) is:  <strong>unsigned short factorial(unsigned short num); </strong><strong> </strong></li>

 <li>Write a <strong>main</strong> function that, inputs an integer number (of size <strong>unsigned short</strong>), calculates the factorial of that number, uses <strong>toBits</strong> to place the 16 bits of the result into 16 separate locations of a byte sized integer array, and then uses <strong>printBits</strong> to output the contents of that array. Finally, the program should give the user the option of re-running with different input.</li>

</ul>

For C programs written in CSc 230, we will choose to follow a previously defined style guideline:  <a href="https://users.ece.cmu.edu/~eno/coding/CCodingStandard.html">https://users.ece.cmu.edu/~eno/coding/CCodingStandard.html</a><a href="https://users.ece.cmu.edu/~eno/coding/CCodingStandard.html">.</a>  Review the guideline and ensure your code follows the recommendations of the authors.



Download Link: https://assignmentchef.com/product/solved-cs590-homework-2-recurrences-and-sorting
<br>
<h1>Part 2: Radix-sort on strings</h1>

The class random generator has been updated (<em>random_generator.h</em> and <em>random generator.cpp</em>) by a member function which generates random strings of up to a given length with characters between “a” and “z”.

<ul>

 <li><em>char* random_string(int max, int&amp; m) </em></li>

</ul>

The function picks a string length <em>m</em> at random in between 1 and <em>max</em> (<em>1&lt;=m&lt;= max</em>). The length <em>m</em> of the random string is stored in the second parameter. The function then allocates <em>m + 1 </em>characters. The first <em>m </em>characters (<em>0……m-1</em>) are chosen at random in between the characters “a” and “z”. The <em>m</em>-th character is set to 0 in order to mark the end of the string.

A string in C is represented by an array of characters (e.g. <em>char *st</em>). Each character is an ASCII representation of a specific integer value. The character “a” is a representation of the value 97 according to the ASCII table. The individual characters of the array/string can therefore be viewed as a digit.

<ol>

 <li>Implement an insertion sort algorithm for strings that sorts a given array of strings according to the character at position <em>d</em>. It is necessary to include the length of each string (<em>array A len</em>) as it is unclear whether or not the digit<em> d</em> exists. A non-existing digit <em>d</em> is interpreted as a 0 in the sorting process. Add a parameter <em>int d </em>and <em>int* A_len</em> to the algorithm arguments and modify the given insertion sort algorithm accordingly. This algorithm should be implemented in the method below:</li>

</ol>

void insertion_sort_digit(char** A, int* A_len, int l, int r, int d)

Notes:

<ul>

 <li>Do not copy the characters itself, but only the pointer to the string/array of characters instead.</li>

 <li>Do not fill the strings with 0’s to make them of equal size.</li>

 <li>Do not compute the length of a string with <em>strlen</em>. Use the int array <em>A_len</em></li>

 <li>If you move a string within the array of strings then you must update the array containing the length of the strings accordingly.</li>

</ul>

<ol start="2">

 <li>Use this modified insertion sort algorithm to implement radix sort for an array of strings. Measure the runtime performance for arrays of random strings 10 times for every combination of array size n = 10000; 25000; 50000; 75000; 100000 and length of the random strings m = 25; 50; 75. Discuss your results. (You might have to adjust the value for <em>n</em> dependent on your computers speed, but allow each test to take up to a couple of minutes). This algorithm should be implemented in the method below:</li>

</ol>

void radix_sort_is(char** A, int* A_len, int n, int m)

<ol start="3">

 <li>Develop a counting sort algorithm for strings that sorts a given array of strings according to the character at position<em> d</em>. As for the insertion sort on digit <em>d</em>, a non-existing digit <em>d</em> is treated as a 0 throughout the counting sort. This algorithm should be implemented in the method below:</li>

</ol>

void counting_sort_digit(char** A, int* A_len, char** B, int* B_len, int n, int d)

Notes:

<ul>

 <li>Do not copy the characters itself, but only the pointer to the string/array of characters, instead.</li>

 <li>Do not fill the strings with 0’s to make them of equal size.</li>

 <li>Do not compute the length of a string with <em>strlen</em>. Use the int array <em>A_len</em></li>

 <li>When moving the string into its correct position you also have to move the length of the string into its correct position.</li>

 <li>You can use <em>int C[256]</em> to store the counters/positions.</li>

</ul>

<ol start="4">

 <li>Use this new counting sort algorithm to implement radix sort for an array of strings. Measure the runtime performance for arrays of random strings 10 times for every combination of array size n = 100000; 250000; 500000; 750000; 1000000 and length of the random strings m = 25; 50; 75. Discuss your results. (You might have to adjust the value for <em>n</em> dependent on your computers speed, but allow each test to take up to a couple of minutes). This algorithm should be implemented in the method below:</li>

</ol>

void radix_sort_cs(char** A, int* A_len, int n, int m)




<strong>Remarks: </strong>

<ul>

 <li>You are not allowed to use code from online resources. Your submission will be tested against that, and will receive a 0, and a report to the Graduate Academic Integrity Board if it is detected.</li>

 <li>Your report has to be typed, and submitted in a pdf file. You should provide figures that plot the running times in relation to the input size parameters.</li>

 <li>You might have to adjust the value for n depending on your computers speed, but allow each test to take up to a couple of minutes.</li>

 <li>Start with smaller values of n and m and stop if one instance of the algorithm takes more than 5 min to complete (the insertion sort implementations will hit that limit early on).</li>

 <li>Discuss your results means that in your report you have to present the results in a table, and analyze and interpret your findings properly. What do the experiments tell you?</li>

 <li>The programming, testing and the experimentation will take some time. Start early.</li>

 <li>Feel free to use the provided source code for your implementation. You have to document your code.</li>

 <li>A Makefile is provided to build the code in the Virtual Box provided.</li>

 <li>Your code has to compile, and run at the Virtual box shared with you in order to be graded.</li>

 <li>Your methods should be added in the sort.h/sort.cpp files. You must keep the same file structure, makefile that is provided in the skeleton code.</li>

</ul>









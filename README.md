Download Link: https://assignmentchef.com/product/solved-cs204-homework1-matrix-operations
<br>
The aim of this homework is to recall CS201 material and practice on matrices (two dimensional arrays/vectors) and file input/output. You are asked to implement a program which finds counts of words(strings) with given N characters in a 2D matrix. The details of the homework will be explained in the following sections of the document.

2.     Input

The program prompts for the input file name. Then, it reads the file name from the standard input. The first line of the input file contains <strong>a single integer</strong> stating the <strong>number of rows in the matrix (M)</strong>, which is equal to the <strong>number of columns </strong>because matrices will be <strong>square matrix</strong> (M x M matrix with M rows and M columns).

The following lines will be the rows of matrix. All elements in the cells of matrix <strong>must be</strong> uppercase letters (A-Z) – your program must check this. You also need to check if there are indeed M rows and M columns. There is an empty line after matrix rows. At the following line of empty line, there is a single integer (<strong>N</strong>) for the length of strings you will be searching in the matrix. A sample input file can be as follows:

4 ABCD

BCDA

CDAB

DABC

3




<strong> </strong>

<h1>Program Flow</h1>

What your program needs to do is find and list strings with given length <strong>N</strong> and the number of their appearances in the (<strong>M x M)</strong> matrix.

<ul>

 <li>The strings can start from any cell in the matrix.</li>

 <li>Once you are in a cell, you can go any of the four directions: left, right, up and down.</li>

 <li>You must <strong><u>NOT</u></strong> visit the same cell while generating a string.</li>

 <li>You will stop once you have <strong>N</strong> letters in your string (i.e., once you visit <strong>N</strong> cells).</li>

</ul>

Boundaries of variables are as follows: <strong>0 &lt; N &lt; 20</strong> and <strong>0 &lt; M &lt; 20</strong>. With that in mind, the flow of the program will be as following:

<ul>

 <li>Prompt for the input file name and perform an input check. If an invalid file name is entered, ask again until a correct file name is entered.</li>

 <li>Read the value of <strong>M </strong>from the file. Store the matrix in the given input file. If the size of matrix does not satisfy the given row (equal to column) value <strong>M</strong>, print an error message and end the execution.</li>

 <li>Read <strong>N </strong>from input file.</li>

 <li>Find all the strings of length <strong>N</strong> in the matrix. Do not forget: while generating strings, the directions to move are left, right, up, down.</li>

 <li>Store the strings you have found and the number of times they exist in the matrix.</li>

 <li>Print out the strings and the number of their appearances. For the output format check sample runs.</li>

</ul>

Sample output for the sample input given above is as following:

<em>The given matrix includes: </em>

<em>[+] ABC exists 8 many times. </em>

<em>[+] BCD exists 8 many times. [+] BAB exists 4 many times. </em>

<em>[+] BCB exists 4 many times. </em>

<em>[+] CDA exists 10 many times. </em>

<em>[+] CBC exists 4 many times. </em>

<em>[+] CDC exists 4 many times. [+] CBA exists 8 many times. </em>

<em>[+] DAB exists 8 many times. [+] DCD exists 6 many times. </em>

<em>[+] DAD exists 6 many times. </em>

<em>[+] DCB exists 8 many times. </em>

<em>[+] ADA exists 4 many times. </em>

<em>[+] ABA exists 4 many times. </em>

<em>[+] ADC exists 10 many times. </em>

<em>[+] BAD exists 8 many times.</em>

<strong><u>Note:</u></strong>

Reuse of same cell is not allowed while generating strings. The following image is an example to the rule where the size of the strings <strong>N</strong> is set to 6.

It is not allowed to generate <strong>“KQCDCQ” as in the figure </strong>since Q at (2,3) is visited twice. However the string <strong>“KQCDCQ” is in the matrix: </strong>the last Q can come from (4,3). So your program must report only this.







<h1>3.     Sample Runs</h1>

Below you can find sample outputs for the program:

<strong>input.txt </strong>

4

ABC

BCDDF

CDAB

DABC




3







<strong>Case 1: </strong>

<em>Please enter the input file name: <strong>input1.txt</strong> Couldn’t open file. Please enter again: <strong>input.txt</strong> </em>

<em>Input file is not as expected. </em>

<em>Press any key to continue . . . </em>

<strong> </strong>

<strong> </strong>

<strong>input2.txt </strong>

<strong> </strong>

4

ABCD

BCDA

CDAB




3

<strong> </strong>

<strong> </strong>

<strong>Case 2:</strong>

<em>Please enter the input file name: <strong>input.txt</strong> </em>

<em>Input file is not as expected. </em>

<em>Press any key to continue . . . </em>

<em> </em>

<strong>Input3.txt </strong>

<strong> </strong>

3

AB*

BCD

CDA




3

<strong> </strong>

<strong> </strong>

<strong>Case 3:</strong>

<em>Please enter the input file name: <strong>input3.txt</strong> </em>

<em>Input file is not as expected. </em>

<em>Press any key to continue . . . </em>

<strong> </strong>

<strong>Input4.txt </strong>

<strong> </strong>

3

555

BCD

CDA




3

<strong> </strong>

<strong> </strong>

<strong>Case 4:</strong>

<em>Please enter the input file name: <strong>input4.txt</strong> </em>

<em>Input file is not as expected. </em>

<em>Press any key to continue . . . </em>

<strong> </strong>

<strong>Input5.txt </strong>

<strong> </strong>

4

ABCD

BCDA

CDAB

DABC




3

<strong> </strong>

<strong> </strong>

<strong>Case 5:</strong>

<em>Please enter the input file name: <strong>input5.txt</strong> </em>

<em>Given matrix includes: </em>

<em>[+] ABC exists 8 many times. [+] BCD exists 8 many times. [+] BAB exists 4 many times. [+] BCB exists 4 many times. </em>

<em>[+] CDA exists 10 many times. </em>

<em>[+] CBC exists 4 many times. </em>

<em>[+] CDC exists 4 many times. [+] CBA exists 8 many times. </em>

<em>[+] DAB exists 8 many times. [+] DCD exists 6 many times. [+] DAD exists 6 many times. </em>

<em>[+] DCB exists 8 many times. </em>

<em>[+] ADA exists 4 many times. </em>

<em>[+] ABA exists 4 many times. </em>

<em>[+] ADC exists 10 many times. </em>

<em>[+] BAD exists 8 many times. </em>

<em>Press any key to continue . . . </em>

<em> </em>

<strong> </strong>

<strong>Some Important Rules:  </strong>

In order to get a full credit, your programs must be efficient and well presented, presence of any redundant computation or bad indentation, or missing, irrelevant comments are going to decrease your grades. You also have to use understandable identifier names, informative introduction and prompts. Modularity is also important; you have to use functions wherever needed and appropriate.

When we grade your homeworks we pay attention to these issues. Moreover, in order to observe the real performance of your codes, we may run your programs in <em>Release</em> mode and <strong>we may test your programs with very large test cases</strong>.

<strong> </strong>

<strong>What and where to submit (PLEASE READ, IMPORTANT): </strong>You should prepare (or at least test) your program using MS Visual Studio 2012 C++. We will use the standard C++ compiler and libraries of the abovementioned platform while testing your homework. It’d be a good idea to write your name and last name in the program (as a comment line of course). <strong> </strong>




Submissions guidelines are below. Some parts of the grading process are automatic. Students are expected to strictly follow these guidelines in order to have a smooth grading process. If you do not follow these guidelines, depending on the severity of the problem created during the grading process, 5 or more penalty points are to be deducted from the grade.

Name your cpp file that contains your program as follows:




<strong><em>“SUCourseUserName_YourLastname_YourName_HWnumber.cpp” </em></strong>




Your SUCourse user name is actually your SUNet username that is used for checking sabanciuniv e-mails. Do NOT use any spaces, non-ASCII and Turkish characters in the file name. For example, if your SUCourse user name is valent, name is Valentina, and last name is Tereşkova, then the file name must be:




<h2>Valent_Tereskova_Valentina_hw1.cpp</h2>




Do not add any other character or phrase to the file name. Make sure that this file is the latest version of your homework program. Compress this cpp file using WINZIP or WINRAR programs. Please use “zip” compression. “rar” or another compression mechanism is NOT allowed. Our homework processing system works only with zip files. Therefore, make sure that the resulting compressed file has a zip extension. Check that your compressed file opens up correctly and it contains your cpp file.




You will receive no credits if your compressed zip file does not expand or it does not contain the correct file. The naming convention of the zip file is the same as the cpp file (except the extension of the file of course). The name of the zip file should be as follows:




<h2>SUCourseUserName_YourLastname_YourName_HWnumber.zip</h2>




For example <strong>zubzipler_Zipleroglu_Zubeyir_hw1.zip</strong> is a valid name, but   <strong><em>hw1_hoz_HasanOz.zip, HasanOzHoz.zip </em></strong>




are <strong>NOT</strong> valid names.
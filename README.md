Download Link: https://assignmentchef.com/product/solved-comp2560-lab-4-process-control-and-file-i-o
<br>
Read the following programs and write down the expected results. Then run the programs to check the results. Make sure you understand why. To pass the lab test, you may be asked for the results of similar programs. For this exercise, it is assumed that all <em>fork()</em> function calls are successful, and the part of code for checking whether a <em>fork()</em> call is successful or not is omitted.




#include &lt;unistd.h&gt;

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;




int main() {




fork();                                                            fork();                                                  fork();

printf(“%d
”, getpid());

}




———————————————




#include &lt;unistd.h&gt;

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;




int main() {




if (fork() == 0)                                                                           fork();                                                   else {

fork();                                                               fork();

printf(“%d
”, getpid());                                                          }

}




———————————————




#include &lt;unistd.h&gt;                                         #include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;




int main() {




if (fork() == 0)                                                                           fork();                                                   else {

fork();                                                               fork();                                                  }                                                                          printf(“%d
”, getpid());

}

———————————————

#include &lt;unistd.h&gt;

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;

int main() {

if (fork() == 0)

fork();                                                   else {

fork();                                                               fork();                                                              exit(0);                                                           }                                                                       printf(“%d
”, getpid());

}

Part II

Use <em>fork()</em> to create a child process.

<ul>

 <li>The parent process checks the first command line argument. If it is not an integer number between 1 and 10 (inclusive), the parent process will print out an error message; otherwise, it will write the number into a file called <em>dat</em>.</li>

 <li>The child process reads the number from the file and prints out its factorial number. You need to make sure that the child process will read the file only after the parent has finished writing into it.</li>

</ul>

You can use library functions to convert a string into an integer. You can use library I/O call to print error message. With file <em>data.dat</em>, you must use system call I/O (no library I/O call allowed).
















2
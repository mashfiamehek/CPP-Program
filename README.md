# CPP-Program
This C++ project is aimed at  calculates CGPA (Cumulative Grade Point Average) based on user inputs for grades. The program assumes a typical grading system where each course has a specific number of credit hours, and the user enters their grades (on a scale of 0-10)..  It is implemented with standard C++ features and can be compiled and run using any compatible C++ compiler.

To calculate the Cumulative Grade Point Average (CGPA) in a C++ program, the core functionality typically involves:

Input the Grades: The program accepts the grades (often in numerical or letter form) for different subjects or courses.
Convert Grades to Points: If grades are in letter format (A, B+, etc.), they need to be converted to Grade Points (for example, A = 4.0, B+ = 3.5, etc.). If the grades are already numeric, this step may be skipped.
Compute Total Points: For each subject, the Grade Point is multiplied by the credit hours for that subject to get the weighted points.
Calculate CGPA: The CGPA is the total weighted points divided by the total credit hours

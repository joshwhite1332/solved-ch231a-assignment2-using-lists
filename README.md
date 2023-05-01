Download Link: https://assignmentchef.com/product/solved-ch231a-assignment2-using-lists
<br>
Write a program which does the following using two list objects:

<ol>

 <li>Create two lists (A and B).</li>

 <li>Read integers from the keyboard until the entered integer is negative or zero.</li>

 <li>Insert the positive integers into list A by adding to the end.</li>

 <li>Insert the same positive integers into list B by adding to the beginning.</li>

 <li>Print list A (separated by spaces) on the standard output and print list B (separated by spaces) into a file called “listB.txt”.</li>

 <li>Print an empty line on the standard output.</li>

 <li>Move the first element of the lists to the end (for both lists).</li>

 <li>Print list A, print list B on the standard output (both separated by comma) using an iterator. Make sure that you do not print a comma after the last element.</li>

 <li>Print an empty line on the standard output.</li>

 <li>Merge list B into list A.</li>

 <li>Print the result of the merging as a sorted list on the standard output (separated by spaces). <em>You can assume that the input will be valid.</em></li>

</ol>

<h2>Problem 2.2 <em>Using deques                                                                                      </em></h2>

<h3>Language: C++</h3>

Write a program which does the following using a deque object:

<ol>

 <li>Create a deque A able to store float values.</li>

 <li>Read floats from the keyboard until the entered float value is 0.</li>

 <li>Insert the positive elements at the end of A and the negative elements at the beginning of A.</li>

 <li>Print the elements of A on the standard output separated by spaces.</li>

 <li>Print an empty line on the standard output.</li>

 <li>Add the value 0 into the middle of the deque (between the last negative and before the first positive element).</li>

 <li>Print the elements of A on the standard output separated by semicolons. Make sure that you do not print a semicolon after the last element.</li>

</ol>

<em>You can assume that the input will be valid.</em>

<h2>Problem 2.3 <em>Another deque                                                                               </em></h2>

<h3>Language: C++</h3>

A company that provides a special service for wind surfers installs wind gauges at popular windsurfing locations. Each gauge reports the current wind speed to a central computer every 5 minutes. When a user connects to the service she or he is able to retrieve recent high, low, and average wind speeds for her or his selected location. The central computer creates a WindGauge object for each gauge. The WindGauge class interface looks as follows:

class WindGauge {

public:

WindGauge(int period = 12); void currentWindSpeed(int speed); int highest() const; int lowest() const; int average() const;

private:

// add properties and/or method(s) here

};

The constructor argument specifies how much history is retained by the object (default 12 periods which is 1 hour). When currentWindSpeed() is called, the current wind speed is added to the history. If the history is then longer than the specified period, the oldest wind speed is discarded. The other three functions return the highest, lowest, and average wind speeds reported during the history period.

Implement the WindGauge class as specified above. Add properties to the class and write a dump function that prints out the lowest, highest, and average wind speed for a WindGauge’s data. Write a test program that does the following:

<ol>

 <li>Create a WindGauge object.</li>

 <li>Add five wind speeds: 15, 16, 12, 15, and 15, and then dump the gauge.</li>

 <li>Add ten more measurements: 16, 17, 16, 16, 20, 17, 16, 15, 16, and 20 (bringing the total to over 12) and dump the numbers again.</li>

</ol>

Separate your code into three files: WindGauge.h (class definition), WindGauge.cpp (implementation of methods) and testWindGauge.cpp (test program).

<h2>Problem 2.4 <em>Reversing a vector                                                                              </em></h2>

<h3>Language: C++</h3>

Write a program which fills a vector with the integer values from 1 to 30. Then add the value 5 at the end of the vector. Reverse the vector using the reverse() function from the algorithm library and print the content of the vector on the standard output using an iterator. Then replace all occurrences of the value 5 by the value 129 using the replace() function from the algorithm library and print the modified vector again on the standard output.

<h1>Problem 2.5 <em>Lotto                                                                                              </em></h1>

<h2>Language: C++</h2>

In the lottery 6 out of 49 numbers are randomly drawn. Draw six different numbers using the formula rand() % 49 + 1. Then add the drawn number to a container that stores all drawn numbers (but make sure that your container will not contain duplicates).

After you have drawn all numbers, print them on the standard output in ascending order. Use a suitable STL container that supports the needed operations and corresponding iterators for all actions. Make sure that you initialize the random number generator with the local time of your system at the beginning of your program.

<h1>Bonus Problem 2.6 <em>Another set                                                                              </em></h1>

<h2>Language: C++</h2>

A building security system has door locks that are opened by typing a four-digit access code into a keypad. The access code is validated by querying an Access object with the following interface:

class Access {

public:

void activate(unsigned int code); void deactivate(unsigned int code); bool isactive(unsigned int code) const;

private:

// add properties and/or method(s) if necessary

};

Each employee is given a different access code, which is activated using the activate() method. When an employee leaves the company, his or her access code is deactivated using the deactivate() method.

Implement the Access class specified above. Write a test program that does the following:

<ol>

 <li>Create an Access object.</li>

 <li>Activate the codes 1234, 9999, and 9876.</li>

 <li>Ask the user for an access code. Read the code from the keyboard.</li>

 <li>Tell the user whether the door opened successfully.</li>

 <li>Repeat the last two steps until the door opens.</li>

 <li>Deactivate the code that worked. Also, deactivate code 9999 and activate code 1111.</li>

 <li>Repeat steps 3 and 4 until the door opens.</li>

</ol>

Separate your code into three files: Access.h (class definition), Access.cpp (implementation of methods) and testAccessSet.cpp (test program). <em>You can assume that the input will be valid.</em>

<h1>Problem 2.7 <em>Using maps                                                                                </em></h1>

<h2>Language: C++</h2>

Write a program which creates a collection of names and birthday dates. Your program should read the data from a file called “data.txt” which contains a name followed by a corresponding birthday date on different lines repeated for many persons. A name consists of first name and last name separated by space. Your program should read the content of the file and use a map to store names and birthday dates.

Then “simulate” querying your collection (i.e., the map) by asking for a name from the keyboard and printing on the standard output the corresponding birthday date. If the name is not in your container then print “Name not found!” on the screen.

<em>You can assume that the input will be valid and the content of the file will be valid if existing.</em>

<h1>Bonus Problem 2.8 <em>Another map                                                                          </em></h1>

<h2>Language: C++</h2>

The customer that uses the security system described in the previous exercise now wants to associate an access level with each access code. Users with high access levels can open doors to more security-sensitive parts of the building than users with lower access levels. Begin with your solution to <strong>Problem 2.6</strong>. Modify the Access class from the previous exercise so that an integer access level is associated with each code. The new interface should be as follows:

class Access {

public:

void activate(unsigned int code, unsigned int level); void deactivate(unsigned int code);

bool isactive(unsigned int code, unsigned int level) const;

private:

// add properties and/or method(s) if necessary

};

The isactive() method returns true if the specified access code has an access level greater than or equal to the specified access level. Of course, it should return false if the access code is not active at all. Modify the main program to do the following:

<ol>

 <li>Create an Access object.</li>

 <li>Activate code 1234 with access level 1, code 9999 with access level 5, and code 9876 with access level 9.</li>

 <li>Ask the user for an access code. Read the code from the keyboard.</li>

 <li>Assuming a door that requires access level 5 for entry, tell the user whether the door opened successfully.</li>

 <li>Repeat the last two steps until the door opens.</li>

 <li>Deactivate the code that worked. Change the access level of code 9999 to 8. Activate code 1111 with access level 7.</li>

 <li>Ask the user for an access code. Read the code from the keyboard.</li>

 <li>Assuming a door that requires access level 7 for entry, tell the user whether the door opened successfully.</li>

 <li>Repeat the last two steps until the door opens.</li>

</ol>

Separate your code into three files: Access.h (class definition), Access.cpp (implementation of methods) and testAccessMap.cpp (test program). <em>You can assume that the input will be valid.</em>
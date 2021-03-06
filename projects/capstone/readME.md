# CPPND: Capstone mini Back simulator

## project Steps
* Step 1: Proposed Project
    * mini bank system simulation

* Step 2: Scope the Project
    * add user database contains userName, hashed password  and balance
    * provide the operations to userRegisters and loginUser
    * User can't register new account with the same username
    * provide user panel to withdraw deposit and balance checking after sucessuful login
    * all the changes should be reflected in the users database
    * the database is implemented as a file and the program read and write inside it
    * add the abillity to exit the program safely

* Step 3: Build your application
    * the application can be found in /src folder

* Step 4: Document Your Work
    * the details are mentioned below

## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./miniBankSimulator`.

## an overview of the code structure
    * Finite state machine to handle different window states and the transitions
    * Classes for UserDB, UserLogin, UserRegister and bankOperations  
    * Pointer for UserDB is passed to other classes
    * Pointer to UserLogin is passed to bankOperations
    * main to create the objects and start running FSM

## Rubric point addressed
1. A variety of control structures are used in the project.
    * Ex file FSM.cpp line 27, 76, 103, 191
    * Ex file UserDB.cpp line 31, 61, 64, 84
2. The project code is clearly organized into functions.
    * Ex file FSM.h line 7:13 and definitions inside FSM.cpp line 17, 59, 67, 94, 119, 189
    * Ex file UserLogin.h line 11:13 and definitions inside UserLogin.cpp line 13, 29, 34
3. The project reads data from an external file or writes data to a file as part of the necessary operation of the program.
    * Ex file UserDB.cpp line 60, 78
4. The project accepts input from a user as part of the necessary operation of the program.
    * Ex file FSM.cpp line 29, 74, 102, 133, 141, 151
5. The project code is organized into classes with class attributes to hold the data, and class methods to perform tasks.
    * Ex file  UserLogin.h line 6, 8, 15
    * Ex file  UserDB.h line 13, 15, 27
6. All class data members are explicitly specified as public, protected, or private.
    * Ex file  UserLogin.h line 6, 8, 15
    * Ex file  UserDB.h line 13, 15, 27
7. At least two variables are defined as references, or two functions use pass-by-reference in the project code.
    * Ex file  bankOperations.h line 11
    * Ex file  UserLogin.h line 12

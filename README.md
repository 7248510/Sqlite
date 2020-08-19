# Compiling applications with sqlite3 Windows 10
<br>The compiler being used is below
<br>** Visual Studio 2019 Developer Command Prompt v16.0
* Files needed: 
    * sqlite3.def, sqlite3.h & sqlite3.dll(Same directory as your application) 
0. Download "Precompiled Binaries for Windows", & "Source Code", select your architecture of windows
    Extract the files to a directory of your choice
1. First you have to create the library.
    Launch Visual Studio's command prompt
    LIB /MACHINE:X86 /DEF:sqlite3.def (This creates the local library for linking)
2. Compile the program with the library
    cl main.cpp /link sqlite3.lib (Compiling your program)
3. Run your program
    For the program to run sqlite3's dll has to be in the same directory as your application!
    You can then delete any leftover files, *.def, *.h, *lib
    Example directories files = main.exe sqlite3.dll[Final folder]

# Largest-Square-Problem

This program finds the largest square on a map by avoiding obstacles. With the _examples/perl_ program you can generate a square of given dimensions and obstacle density (`./examples/perl.sh 100 100 2`) By passing the file to the bsq program (`./bsq example.ox`) or via standard input (`./examples/perl.sh 100 100 2 | ./bsq` or `cat example.ox | ./bsq`).
The first line of the map contains the information for reading the map:
- The number of lines on the map;
- The "empty" character;
- The "obstacle" character;
- The "full" character;

the program replaces empty spaces with filled spaces to represent the largest possible square. Multiple solutions are handled by placing the square as high and to the left as possible. The map is composed of lines of 'empty' characters and 'obstacle' characters. The aim of the programme is to replace the 'empty' characters by 'filled' characters in order to represent the largest possible square. In case there are several solutions, it will be decided to represent the square as high and as far to the left as possible. The program accepts 1 to n parameters and includes a Makefile for compilation.

Definition of a valid map:
- All lines must have the same length.
- At least one line must have at least one square.
- At the end of each line there is a line break.
- The characters appearing in the map must only be those that have appeared in the first line.
- The map will not be valid if any character is missing in the first line or if there are two characters (between empty, full and obstacles) that are identical.
- Characters can be any printable character, including digits.
- If the map is invalid, it shall output the error: map error followed by a line break. The program will then move on to the processing of the next
map.

### Example
![1.png](/img/1.png)
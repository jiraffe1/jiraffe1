GOOSECODE instructions and documentation:

GOOSECODE is an esoteric programming language where you may only use the characters H O N K, and in that order.

But fear not! I shall explain how this all works.

GOOSECODE is a binary based system in which two of a character(so as in the KK in HONKK represents a 1, and just one character(as in H in HOONNK) represents a zero. This means that each command can be represented by a binary number from 0000 to 1111, or HONK to HHOONNKK

A NUMBER is an int represented by one line of GOOSECODE. It can have a value from 0 (HONK, 0000) to 15 (HHOONNKK, 1111)

An ADDRESS is a number represented by 2 lines of GOOSECODE. It can have a value from 0:

HONK
HONK
(00000000)

to 255:

HHOONNKK
HHOONNKK
(11111111)

## Table of GOOSECODE commands
	COMMAND | CODE    | EXPECTED NUMBER OF PARAMETERS | MEANING
	HONK    | 0000    | 0  			          | IGNORE REST OF LINE
	HONKK   | 0001    | 3: [address], and [number]    | SET ADDRESS

To begin with, let's create a hello world program. To let the interpreter know that there is some GOOSECODE, we need to write a header

## Header at the beginning of every GOOSECODE script

	$GOOSECODE

Next we will need a command to print out the text to a console.


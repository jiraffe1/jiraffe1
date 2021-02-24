Ello Mates

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
(1111 1111)

A BIGNUMBER is a single character represented by 2 lines of GOOSECODE. It can have a value from 0:

HONK
HONK
(00000000, 0, '0')

to 255:

HHOONNKK
HHOONNKK
(1111 1111, 255, '')

Where the 0-9 take up 0000 0000 to 0000 1001
And A-Z take up 0000 1010 to 0001 0100
And 0001 0101 is a space
And 0001 0110
to 1111 1111 are all '.'


## Table of GOOSECODE commands
	COMMAND | CODE    | EXPECTED NUMBER OF PARAMETERS                                 | MEANING
	________________________________________________________________________________________________________________________________________
	HONK    | 0000    | 0  			                                          | IGNORE REST OF LINE(comment)
	HONKK   | 0001    | 3: [address], and [number]                                    | SET ADDRESS [address] to [number]
	HONNK	| 0010	  | 5: [number], [address1], and [address2]                       | OPERATOR(address to address) see further down
	HONNKK  | 0011    | 4: [number], [address1], and [number]                         | OPERATOR(address to number) see further down
	HOONK   | 0100	  | 2: [address]                                                  | GET ADDRESS can be used as a parameter where there is a [number]
	HOONKK  | 0101    | 5: [number x], [number y], [number r], [number g], [number b] | SET SCREEN pixel at x, y to the colour r, g, b
	HOONNK  | 0110    | 8: [bignumber], [bignumber], [bignumber], [bignumber]         | PRINTLN 4 letter word, where each bignumber is a letter
	HOONNKK | 0111    | 2: [bignumber]						  | JUMP BACK [bignumber] lines in the program
	HHONK   | 1000    | 3: [number], [number a], [number b]                           | LOGIC where [number] is the mode of operation and [number a] and [number b] are the numbers to be compared if the statement is false, the program will skip to the next END LOGIC
	HHONKK  | 1001    | 0                                                             | END LOGIC placeholder								
	HHONNK  | 1010    |
	HHONNKK | 1011    |
	HHOONK  | 1100    |
	HHOONKK | 1110    |
	HHOONNKK| 1111    | 0								  | EXIT stop the program. anything after this is ignored by the interpreter

To begin with, let's create a hello world program. To let the interpreter know that there is some GOOSECODE, we need to write a header

## Header at the beginning of every GOOSECODE script

	$GOOSECODE

Next we will need a command to print out the text to a console.

## GOOSECODE hello world program
	$GOOSECODE
	HOONNK
		HONK
		HHHONNK
		HONK
		HHONNK
		HONK
		HHONNK
		HONK
		HHONNK
	HHOONNKK
	ok it looks more ridiculous than i thought



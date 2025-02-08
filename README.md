# EDSAC-Craps
A nice history lesson with a twist of poker :) 

![screenshot](pythonimage.PNG)
## History of the EDSAC Machine

The EDSAC (Electronic Delay Storage Automatic Calculator) was one of the first stored-program computers, built at the University of Cambridge by Maurice Wilkes and his team. It became operational on May 6, 1949, and was inspired by John von Neumann's stored program concept. The EDSAC used mercury delay line memory, a type of sequential-access memory that stored bits as sound waves traveling through a tube filled with mercury. Each delay line could hold a fixed number of bits, and the entire memory was divided into words of 17 bits (with 1 bit for the sign and 16 bits for data or instructions). The EDSAC instruction set was designed around a simple single-address architecture where each instruction consisted of a 5-bit opcode, an 11-bit memory address, and a 1-bit modifier for certain operations. The machine primarily worked with the accumulator, meaning most operations involved loading, modifying, or storing values in it. The basic arithmetic operations included adding a number from memory to the accumulator with the "A" instruction and subtracting a number with "S." The "L" instruction loaded a value from memory into the accumulator, while "T" stored the current accumulator value back into memory. It was designed primarily for scientific calculations and helped advance early computer science. It also ran the first computer game—a version of tic-tac-toe. The machine was decommissioned in 1958 but left a lasting legacy, influencing the design of commercial computers like the LEO I.

![screenshot](pythonimage.PNG)

## Inspiration and Completion for the CRAPS Project

For my CSCI470 Comparison of Programming course with Dr. Lowe, I programmed a Craps poker game on EDSAC, which was both a challenge and a fascinating dive into early computing. Since EDSAC operates with a single-address architecture and only has basic arithmetic and control instructions, my partner and I had to break the game logic down into the simplest possible operations. While implementing this version of Craps, it only supports pass or don't pass bets and starts the player off with 500 dollars. 

![screenshot](pythonimage.PNG)

## Challenges for this project

One of the biggest challenges I ran into while programming my Craps poker game on EDSAC was printing two-digit numbers. Since EDSAC operates on 17-bit words, it doesn’t have built-in support for formatted output like modern programming languages.  By default, the output routine could only handle single-digit numbers, so if a dice roll resulted in a number like 10, it would print it as just 0, which obviously wasn’t helpful.

To fix this, I had to use the P6 subroutine, which is one of the standard EDSAC routines designed for printing multi-digit numbers. Instead of directly outputting a raw value, I had to break down a two-digit number into its tens and ones place. The P6 routine took care of converting numerical values into proper character output so that, for example, a roll of 10 would actually appear as "10" rather than just "0". Implementing it meant carefully passing the accumulator value through P6 at the right point in my program, ensuring it printed correctly after each dice roll.

Another key part of structuring the game was implementing the Wheeler jump to handle function calls more cleanly. Since EDSAC doesn’t have a built-in stack or return instructions like modern architectures, I had to manually manage function calls using jump instructions. The Wheeler jump technique involves storing the return address before jumping to a subroutine, then using that stored address to jump back when the subroutine is finished.

## Where to download 

https://dcs.warwick.ac.uk/~edsac/ 

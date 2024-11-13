# RandomNumberGenerator



include iostream
include ctime
include cstdlib

include iostream: Includes the standard input/output stream library, allowing the use of std::cout for printing to the console.
include ctime: Includes the time library, which provides functions related to date and time, such as std::time.
include cstdlib: Includes the C standard library, which contains the std::rand() and std::srand() functions for random number generation.


int main(){

The main function serves as the program's entry point.

Seeding the Random Number Generator
std::srand(std::time(0)); // Seed

std::srand(std::time(0)): Seeds the random number generator with the current time, ensuring different random numbers each time the program runs. Without this line, std::rand() would generate the same sequence of numbers every time.

Generating a Random Number
int random_num = std::rand();
std::cout << "random_num : " << random_num << std::endl;

std::rand(): Generates a random integer between 0 and RAND_MAX (a constant defined in <cstdlib>, typically 32767).
std::cout << random_num: Prints the random number to the console.


Generating More Random Numbers in a Loop
int random_num1;
for(size_t i {0} ; i < 20 ; ++i){
    random_num1 = std::rand();
    std::cout << "random_num1 " << i << ":" <<  random_num1 << std::endl;
}

This loop generates 20 random integers, printing each one.
size_t i {0}; i < 20; ++i: Uses a loop counter i that goes from 0 to 19 (20 iterations).
Each iteration assigns a new random number to random_num1 and prints it.

Generating Random Numbers in a Different Range (1 to 10)
int random_num3 = std::rand() % 10 + 1; // [1 ~10]
for(size_t i {0} ; i < 20 ; ++i){
    random_num3 = std::rand() % 10 + 1;
    std::cout << "random_num3 " << i << "  :   " <<  random_num3 << std::endl;
}

std::rand() % 10 + 1: Generates a random number between 1 and 10 (inclusive).
The for loop generates and prints 20 random numbers in the range [1, 10].

Summary

The code demonstrates generating random numbers and controlling their range using modulus (%) operations. It seeds the random number generator with the current time, allowing different results with each run, and prints sets of random numbers in different ranges to the cons




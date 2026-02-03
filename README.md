#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Seed the random number generator
    srand(time(0));
    
    // Generate a secret number between 1 and 100
    int secretNumber = rand() % 100 + 1;
    int playerGuess = 0;

    std::cout << "Welcome to the Number Guessing Game!\n";
    std::cout << "I've picked a secret number between 1 and 100. Try to guess it.\n";

    // Loop until the player guesses the correct number
    while (true) {
        std::cout << "Enter your guess: ";
        std::cin >> playerGuess;

        if (playerGuess == secretNumber) {
            std::cout << "Congratulations! You guessed the secret number!\n";
            break;
        } else if (playerGuess > secretNumber) {
            std::cout << "Too High! Try again.\n";
        } else {
            std::cout << "Too Low! Try again.\n";
        }
    }

    return 0;
}

# NUMBER GUESSING GAME 
#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    srand(time(0));
    
    int randomNumber = rand() % 100 + 1;
    int userGuess;

    std::cout << "Guess the number between 1 and 100: ";
    std::cin >> userGuess;

    while (userGuess != randomNumber) {
        if (userGuess > randomNumber) {
            std::cout << "Your guess is too high. Try again: ";
        } else {
            std::cout << "Your guess is too low. Try again: ";
        }
        std::cin >> userGuess;
    }
        
    std::cout << "Congratulations! You guessed the correct number!" << std::endl;
    return 0;
}
 

# numberguess
#codsoft third task
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int generateRandomNumber(int min, int max) {
    // Seed the random number generator
    srand(time(0));

    // Generate a random number within the specified range
    return min + rand() % (max - min + 1);
}

void guessTheNumber() {
    int secretNumber = generateRandomNumber(1, 100);
    int guess;

    cout << "Guess the number between 1 and 100: ";

    while (true) {
        cin >> guess;

        if (guess == secretNumber) {
            cout << "Congratulations! You guessed the number." << endl;
            break;
        } else if (guess < secretNumber) {
            cout << "Too low. Try again." << endl;
        } else {
            cout << "Too high. Try again." << endl;
        }
    }
}

int main()
{
    guessTheNumber();
    return 0;
    
}

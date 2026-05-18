# pat2-subtask2
Morse Code 

/*
* Name: Liyema
* Surname: Goboodwana
* Group: ITR3
* Student Number: 172502018
*/

#include <iostream>
#include <iomanip> // Required for fixed and setprecision

using namespace std;

const int NUM_EXPERIMENTS = 3;
const int NUM_READINGS = 3;

int main() {
    int i, j; // Changed from char to int for loop counters
    double readingValue, total, average;

    for (i = 1; i <= NUM_EXPERIMENTS; i++) {
        total = 0;
        cout << "\nEXPERIMENT " << i << endl;
        cout << "==================\n";

        for (j = 1; j <= NUM_READINGS; j++) {
            cout << "Enter reading " << j << " value: ";
            cin >> readingValue; // Fixed variable name
            total = total + readingValue; // Fixed subtraction error
        }

        average = total / NUM_READINGS; // Fixed incorrect formula

        // Evaluation logic directly inside the loop
        if (average < 100) { // Fixed comparison operator to match the text
            cout << "Experiment " << i << " average: "
                 << fixed << setprecision(2)
                 << average << " is Below acceptable range\n";
        } 
        else if (average >= 100 && average <= 300) { // Fixed 'OR' to logical '&&'
            cout << "Experiment " << i << " average: "
                 << fixed << setprecision(2)
                 << average << " is Within acceptable range\n";
        } 
        else {
            cout << "Experiment " << i << " average: "
                 << fixed << setprecision(2)
                 << average << " is Above acceptable range\n";
        }
    }

    return 0;
}





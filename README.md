# pat2-subtask2
Morse Code 

/*
* Name: Liyema
* Surname: Goboodwana
* Group: ITR3
* Program: Morse Code Sender
* Student Number: 172502018
*/

#include <iostream>
#include <string>
#include <map>
#include <Algorithm>
#include <limits>

#include <iostream>
#include <string>
#include <map>
#include <sstream>

using namespace std;

map<char, string> morseMap = {
    {'A', ".-"}, {'B', "-..."}, {'C', "-.-."}, {'D', "-.."}, {'E', "."},
    {'F', "..-."}, {'G', "--."}, {'H', "...."}, {'I', ".."}, {'J', ".---"},
    {'K', "-.-"}, {'L', ".-.."}, {'M', "--"}, {'N', "-."}, {'O', "---"},
    {'P', ".--."}, {'Q', "--.-"}, {'R', ".-."}, {'S', "..."}, {'T', "-"},
    {'U', "..-"}, {'V', "...-"}, {'W', ".--"}, {'X', "-..-"}, {'Y', "-.--"},
    {'Z', "--.."}, {'1', ".----"}, {'2', "..---"}, {'3', "...--"}, {'4', "....-"},
    {'5', "....."}, {'6', "-...."}, {'7', "--..."}, {'8', "---.."}, {'9', "----."},
    {'0', "-----"}, {'.', ".-.-.-"}, {',', "--..--"}, {'?', "..--.."}, {' ', "/"}
};

string encryptSentence(string text) {
    string cipher = "";
    for (char c : text) {
        c = toupper(c);
        if (morseMap.count(c)) {
            cipher += morseMap[c] + " "; // Add space between letters
        }
    }
    return cipher;
}

int main() {
    string userSentence;

    cout << "Enter a full sentence to translate: ";
    // getline reads the entire line, including spaces, until you hit Enter
    getline(cin, userSentence);

    string result = encryptSentence(userSentence);

    cout << "\nYour Morse Code:\n" << result << endl;
    cout << "\n(Note: '/' represents the space between words)" << endl;

    return 0;
}





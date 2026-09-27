🔤 Pattern 18 – Reverse Alphabet Triangle in C++

A C++ program that generates a reverse alphabet triangle pattern using nested loops and character manipulation. The pattern starts from a progressively earlier alphabet character in each row and continues up to E.

📌 Overview

The program prints an alphabet pattern where each row begins with a character that moves backward through the alphabet.

For example, when n = 5, the output is:

E
D E
C D E
B C D E
A B C D E

The program also supports multiple test cases, allowing the pattern to be generated for different values of n.

✨ Features
Generates a reverse alphabet triangle pattern.
Uses nested for loops.
Demonstrates character arithmetic in C++.
Supports multiple test cases.
Uses a dedicated function for pattern generation.
Simple and beginner-friendly implementation.
🛠️ Technologies Used
Technology	Purpose
C++	Programming language
iostream	Input and output
Character Arithmetic	Alphabet manipulation
📝 Problem Statement

Given an integer n, print an alphabet pattern containing n rows.

Each row:

Starts with a character that decreases by one alphabet position.
Ends at the character E.
Contains all characters between the starting character and E.
Example

For n = 5:

E
D E
C D E
B C D E
A B C D E
🧠 Approach

The outer loop controls the number of rows:

for (int i = 0; i < n; i++)

For each row, the starting character is calculated using:

'E' - i

The inner loop then prints characters from the calculated starting character up to E:

for (char ch = 'E' - i; ch <= 'E'; ch++)

This creates the progressively expanding alphabet pattern.

💻 Source Code
#include <iostream>
using namespace std;

void Pattern18(int n) {
    for (int i = 0; i < n; i++) {
        for (char ch = 'E' - i; ch <= 'E'; ch++) {
            cout << ch << " ";
        }
        cout << endl;
    }
}

int main() {
    int t;
    cin >> t;

    for (int i = 0; i < t; i++) {
        int n;
        cin >> n;
        Pattern18(n);
    }

    return 0;
}
📥 Example Input
2
3
5
📤 Example Output
E 
D E 
C D E 

E 
D E 
C D E 
B C D E 
A B C D E 

Each test case produces its own pattern.

▶️ How to Run
1. Clone the repository
git clone <repository-url>
cd <repository-folder>
2. Compile the program
g++ main.cpp -o main
3. Run the program
./main

Windows: Use main.exe instead of ./main.

📚 Learning Concepts

This program demonstrates:

Nested loops
Character variables
Character arithmetic
ASCII character representation
Functions in C++
Multiple test cases
Pattern printing
Input/output using cin and cout
⏱️ Complexity Analysis

For a single test case with n rows:

Time Complexity: O(n²)
Auxiliary Space: O(1)

The total number of characters printed grows approximately as:

1 + 2 + 3 + ... + n

which results in O(n²) operations.

📸 Screenshot

Add your program output screenshot to:

screenshots/output.png

Then include it in the README:

![Program Output](<img width="192" height="188" alt="Screenshot 2026-09-27 at 9 41 00 AM" src="https://github.com/user-attachments/assets/889aa47e-dd9d-4a0f-8218-5b6da400a509" />
)

Recommended project structure:

Pattern18/
│
├── main.cpp
├── README.md
└── screenshots/
    └── output.png
👤 Author

Rishab Raj Chourasia

C++ | Data Structures & Algorithms | Problem Solving

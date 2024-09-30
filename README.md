This repository contains a simple multi-threaded C program that increments a counter and allows the user to suspend and resume the counter using keyboard input. It demonstrates the use of threads and mutexes in C.

Features
Increments a counter every second.
Suspends and resumes counter updates based on user input.
Thread-safe operations using mutexes.
Requirements
A C compiler (e.g., GCC)
pthread library (typically included with most Unix-like systems)

How to Compile
1. Clone the repository:
git clone https://github.com/yourusername/repo-name.git cd repo-name
2. Compile the code:
gcc -o counter_app counter_app.c -lpthread

How to Run
./counter_app

User Input
Enter s to suspend the counter.
Enter r to resume the counter.

Code Explanation
Global Variables:

volatile int counter: Holds the current count value.
volatile int suspended: Indicates whether the counter is suspended.
pthread_mutex_t lock: Mutex for thread safety.
Functions:

increment_counter: Increments the counter every second if not suspended.
toggle_suspend: Waits for user input to suspend or resume the counter.
Main Function:

Initializes the mutex.
Creates the counter and suspend threads.
Joins threads to ensure they finish before exiting.
Destroys the mutex.

To run your code in OnlineGDB, follow these steps:

Visit OnlineGDB: Go to OnlineGDB.

Select C Language: On the main page, choose "C" from the language dropdown menu.

Paste Your Code: Copy your C code and paste it into the editor.

Modify for Input: Since OnlineGDB runs in a web-based environment, it may handle input differently. You can simulate input by using predefined input in the “Input” section if necessary.

Compile and Run: Click on the "Run" button to compile and execute your program.

View Output: The output will appear in the console below. You can provide input directly in the console if prompted.

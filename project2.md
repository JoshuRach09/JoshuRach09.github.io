[Back to Portfolio](./)

CSCI 332 - Airdrop
===============

-   **Class: CSCI 332** 
-   **Grade: 100** 
-   **Language(s): C++, Binary** 
-   **Source Code Repository:** ([lab04](https://github.com/JoshuRach09/CSCI-301-code-repository/tree/master/lab04))  
    (Please [email me](mailto:jrachel@csuniv.edu?subject=GitHub%20Access) to request access.)

## Project description

This C++ project implements a reliable file-transfer application called “Air Drop” using UDP sockets in Ubuntu Linux. The client reads a binary file specified by the user, sends the filename first, then transmits the file in 1000-byte packets prefixed with a “Data” header. After each packet, the client waits for an acknowledgment from the server. The server receives the filename, creates a new binary output file, reconstructs the the file from the incoming packets, and sends back either a "Data" or a "Done" acknowledgement. The program will send a final “Done” packet to signal the end of transfer. This creates a custom stop-and-wait protocol that guarantees reliable delivery over UDP.

## How to run the program

The programs must be compiled before use. Ensure the source files (client.cpp and server.cpp) are in the working directory. Place the file you wish to transfer into the client folder. Right click the "udpclient" and "udpserver" cpp files and open an integrated terminal for each.
You will run the code as follows:

Server
```bash
cd ./lab04
perl lab04.pl
```

This program will generate three output files: average.txt, winner.txt, and sorted.txt

## UI Design

This is a command-line script without an interactive user interface. The user runs the script in a terminal, and it processes the input file silently, producing output files. Users can view the results by opening or using the Linux command "cat" to view the output files. The program execution starts in the terminal (see Fig 1). After running, the example output can be viewed in the generated files (see Fig 2), such as the average score (see Fig 3), sorted scores (see Fig 4), and the winner (see Fig 5). If an error occurs, such as a missing input file, Perl will display an error message in the terminal (see Fig 6).

![screenshot](images/Lab04/Figure1.PNG)  
Fig 1. The launch screen

![screenshot](images/Lab04/Figure2.PNG)  
Fig 2. The generated files.

![screenshot](images/Lab04/Figure3.PNG)  
Fig 3. Average Score.

![screenshot](images/Lab04/Figure4.PNG)  
Fig 4. Sorted Scores.

![screenshot](images/Lab04/Figure5.PNG)  
Fig 5. Winning Score.

![screenshot](images/Lab04/Figure6.PNG)  
Fig 6. Error if score file is missing.

![screenshot](images/Lab04/Figure7.PNG)  
Fig 7. scores.txt

## 3. Additional Considerations

Please ensure the input file 'scores.txt' is properly formatted (see Fig 7), with one player per line and numeric scores. The script uses strict and warnings for better error handling. For deployment, it can be run on any system with Perl installed. You can run the program in VS code, ensure that it can run perl.

[Back to Portfolio](./)

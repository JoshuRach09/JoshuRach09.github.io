[Back to Portfolio](./)

CSCI 332 - Airdrop
===============

-   **Class: CSCI 332** 
-   **Grade: 100** 
-   **Language(s): C++, Binary** 
-   **Source Code Repository:** ([Airdrop](https://github.com/JoshuRach09/csci-332-Airdrop))  
    (Please [email me](mailto:jrachel@csuniv.edu?subject=GitHub%20Access) to request access.)

## Project description

This C++ project implements a reliable file-transfer application called “Air Drop” using UDP sockets in Ubuntu Linux. The client reads a binary file specified by the user, sends the filename first, then transmits the file in 1000-byte packets prefixed with a “Data” header. After each packet, the client waits for an acknowledgment from the server. The server receives the filename, creates a new binary output file, reconstructs the file from the incoming packets, and sends back either a "Data" or a "Done" acknowledgement. The program will send a final “Done” packet to signal the end of transfer. This creates a custom stop-and-wait protocol that guarantees reliable delivery over UDP.

## How to run the program

The programs must be compiled before use. Ensure the source files (client.cpp and server.cpp) are in the working directory. Place the file you wish to transfer into the client folder. Right-click the "udpclient" and "udpserver" cpp files and open an integrated terminal for each. Be sure to run the compilation code for both the server and the client, and then run the server starter command first, then the client.

server.cpp
```bash
g++ udpserver.cpp -o udpserver
./udpserver
```

The server will ask the user to enter the port number to use for the project. For simplicity's sake, use 12345.

client.cpp
```bash
g++ udpclient.cpp -o udpclient
./udpclient
```

The client will ask for the server's IP address, which will be the VM/Linux machine's IP(V4) address. Next, it will ask for the port number, and the user will enter the one used for the server. Finally, it will ask the user for the file name and check whether it is valid; if not, it will tell them it could not open it and prompt them again.


## UI Design

This is a command-line application consisting of two separate programs (client and server) that must run in two terminal windows. 

![screenshot](images/Airdrop/Final-Project-Demo.png)  
Fig 1. The final result.

![screenshot](images/Airdrop/Ask-for-ServerIP.png)  
Fig 2. The program will ask for the server IP address.

![screenshot](images/Airdrop/Ask-for-Serverport.png)  
Fig 3. The program will ask for the port number.

![screenshot](images/Airdrop/ServerIPAdd.png)  
Fig 4. This is how you find the server's IP address(your VM IP).

![screenshot](images/Airdrop/EnterServerIPAdd.png)  
Fig 5. Enter the IP address of your VM.

![screenshot](images/Airdrop/EnterServerinfoClientSide.png)  
Fig 6. Error if score file is missing.

![screenshot](images/Airdrop/Final-Product.png)  
Fig 7. Received file on the server (identical to original).

## Demo Video

Below, you can find a demo video I did for the class that shows the program in action.

[Demo for Airdrop](https://youtu.be/vvuQGXbCeOc)

## 3. Additional Considerations

The source code files contain the relevant information, such as the Student Name, Program Name, Creation Date, Last Modified Date, CSCI Course, Grade Received, and are thoroughly commented throughout the program. The code itself uses binary Input/Output (std::ios::binary), proper UDP socket handling, and strict packet formatting (“Data” / “Done”). The GitHub repo contains the source code, and the executables are provided with the release. This program was created to run on any Linux machine that has g++ installed; however, I coded and demonstrated this project in Ubuntu Linux. The code can be run and modified using VS Code. **Ensure the client and server are tested on the same machine, or across machines with the correct IP address format (IPV4 in this case) and open ports.** 

[Back to Portfolio](./)

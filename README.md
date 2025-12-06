# CN-PROJECT-fall2025
Computer Networks Semester Project - Multi-Campus Network System


------------------------------------------------Project Overview-------------------------------------------------------

This project implements a distributed communication system where: Islamabad Campus acts as the Central Server Other Campuses (Lahore, Karachi, Peshawar, CFD, Multan) act as clients Communication uses hybrid TCP/UDP protocol approach Real-time messaging and broadcast announcements supported


--------------------------------------------------------Features----------------------------------------------------------

Core Functionality

Central Server with admin interface
Multiple campus clients with individual authentication
Direct messaging between any two campuses
System-wide broadcasts from admin
Heartbeat monitoring for campus status


Protocol Implementation
TCP for reliable authentication and messaging
UDP for efficient broadcasts and heartbeats
Custom text-based protocol for message formatting


Concurrency & Performance
Multi-threaded server handles concurrent connections
Non-blocking I/O for responsive user interfaces
Thread-safe data structures with mutex protection




-----------------------------User Guide-------------------------------------------------------------------

Step 1: Download the Code Files Download these three files to the same folder: server.c - Central Server code client.c - Campus Client code

Step 2: Compile the Code Open Ubuntu vmware workstation Open terminal in the folder containing the files. (“cd foldername”) Then run these commands Server: touch server.c Chmod +x server.c gcc server.c -o server Client: Touch client.c Chmod +x client.c gcc client.c -o client Expected output: Two executable files created: server and client

Step 3: Run the System Step 3.1: Start the Central Server (Islamabad Campus) Command: ./server Keep this terminal open. Step 3.2: Start Campus Clients Open new terminal windows for each campus: Terminal 2 - Lahore Campus: Command: ./client Enter: Lahore Terminal 3 - Karachi Campus: Command: ./client Enter: Karachi

Step 4: Test Communication Test 1: Send Message from Lahore to Karachi In Lahore terminal: • Choose option 1 (Send message) • Enter target campus: Karachi • Enter department: IT • Enter message: Hello Lahore! • Message appears automatically in Karachi terminal Test 2: Send Broadcast from Admin • In Server terminal: • Choose option 2 (Send broadcast) • Enter message: System maintenance tonight • Message appears in all client terminals Test 3: Check Connected Campuses • In Server terminal: • Choose option 1 (Show connected campuses) • See list of all active campuses

Step 5: Exit the System In any client terminal: • Choose option 3 (Disconnect) • Client disconnects gracefully • To stop server: Press Ctrl+C in server terminal

# MULTITHREADED-CHAT-APPLICATION

COMPANY : CODTECH IT SOLUTIONS

NAME : MULA SAMEERA

INTERNID : CT04DN836

DOMAIN : JAVA PROGRAMMING

DURATION : 4 WEEKS

MENTOR : NEELA SANTOSH

##DESCRIPTION

## Description of the Java Chat Application

The Java Chat Application is a client-server based text communication system implemented using Java's core networking and I/O libraries. It consists of two main components: ChatServer and ChatClient. The application allows multiple clients to connect to a central server and communicate with each other in real-time. It serves as a fundamental example of socket programming, multithreading, and inter-client message broadcasting.

This simple chat system is ideal for learners and educators looking to understand how real-time communication works under the hood, particularly how clients and servers communicate over TCP sockets.

## Components:

1. ChatServer.java:

.The ChatServer class is responsible for:

.Accepting connections from clients.

.Creating a dedicated thread (ClientHandler) for each client to handle input/output streams.

.Broadcasting messages received from any one client to all other connected clients.

.The server listens on a predefined port (12345 in this case) and uses a ServerSocket to continuously accept incoming client connections. Each client is handled in its own thread using the ClientHandler class, which reads messages sent by the client and forwards them to other connected clients via a broadcast method.

.To manage concurrent client connections, the server uses a Set of ClientHandler instances, stored in a synchronized collection (Collections.synchronizedSet) to ensure thread-safe operations.

## Key Features:

.Multithreaded handling of clients

.Synchronized client management

.Graceful client disconnection

.Message broadcasting to all clients except sender

2. ChatClient.java:
   
.The ChatClient class is designed to:

.Connect to the server using the server’s address and port.

.Allow the user to send messages to the server.

.Listen for incoming messages from the server and display them in real time.

.Once connected, the client spawns a thread dedicated to reading incoming messages from the server. Meanwhile, the main thread waits for user input and sends it to the server. If the user types "exit", the client disconnects cleanly.

## Key Features:

.Bi-directional communication with the server

.Real-time message display

.Asynchronous listening via multithreading

.Simple and user-friendly interface

##How It Works:

.The server starts and listens on a port (e.g., 12345).

.Each client connects to the server using a socket.

.When a client sends a message, the server reads it and broadcasts it to all other clients.

.Each client displays the received messages from the server in real time.

.Typing "exit" closes the connection on both client and server ends.

## Learning Objectives:

This project is ideal for understanding:

.Java socket programming (ServerSocket, Socket)

.Multithreading using Thread class

.Handling concurrent clients

.Broadcasting messages

Reading user input from the terminal

.Buffered I/O streams (BufferedReader, PrintWriter)

## How to Run
Step 1: Compile both files

javac ChatServer.java ChatClient.java

Step 2: Start the server

java ChatServer

Step 3: Start multiple clients (each in a new terminal)


java ChatClient

Each client can now send messages to the server, which are broadcasted to all other connected clients.

##Use Cases
1.Learning and teaching basic networking

2.Building the base for a more advanced chat system

3.Exploring threading and inter-client communication

4.Creating prototypes for real-time collaboration tools

##OUTPUT:

![Image](https://github.com/user-attachments/assets/1eaf2197-fea3-466d-b11c-38841d9343c2)

![Image](https://github.com/user-attachments/assets/daa14a76-2320-43e8-b55e-ab8de88d27ee)

![Image](https://github.com/user-attachments/assets/5eb8a165-7985-4686-b0c8-baf18b7ab8e5)

![Image](https://github.com/user-attachments/assets/743dd20b-f10b-4f5c-ad9d-6913d916733f)



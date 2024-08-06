
# Chat Application

This is a simple chat application implemented in Java using socket programming. It consists of a server (`ChatServer`) and a client (`ChatClient`). The server listens for incoming client connections, and clients can connect to the server to send and receive messages in real time.

## Features

- Multiple clients can connect to the server simultaneously.
- Each client can send messages to the server, which then broadcasts the messages to all connected clients.
- Clients are prompted to enter their name upon connection, and messages are prefixed with the client's name.
- Handles client disconnections gracefully.

## Requirements

- Java Development Kit (JDK) 8 or later

## Setup and Running the Application

### Server

1. **Compile the server code**:
   ```sh
   javac server/ChatServer.java
   ```

2. **Run the server**:
   ```sh
   java server.ChatServer
   ```

   The server will start and listen for client connections on port `12345`.

### Client

1. **Compile the client code**:
   ```sh
   javac client/ChatClient.java
   ```

2. **Run the client**:
   ```sh
   java client.ChatClient
   ```

   When prompted, enter your name. You can then start sending messages which will be broadcast to all connected clients.

## Usage

1. **Start the server**:
   Run the server code as shown above. The server will print "Chat server started..." and wait for client connections.

2. **Start the clients**:
   Run the client code as shown above. Multiple clients can be started, and they will all connect to the same server.

3. **Send messages**:
   After entering your name, you can start typing messages. Press `Enter` to send a message. All connected clients will receive the message.

4. **View messages**:
   Messages sent by any client will be displayed on the console of all connected clients.

## Code Structure

- `server/ChatServer.java`: Contains the server code, which listens for client connections and handles message broadcasting.
- `client/ChatClient.java`: Contains the client code, which connects to the server and handles sending and receiving messages.

## Exception Handling

The application includes basic exception handling to manage common issues such as:

- Network failures
- Client disconnections
- Input/output errors

## Future Improvements

- Implement a graphical user interface (GUI) for better user experience.
- Add features like private messaging between clients.
- Enhance security by adding encryption for messages.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

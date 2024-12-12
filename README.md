# Samyog: Chatting App Interface

Samyog is a simple client-server messaging application built using Java Swing for the user interface and socket programming for communication. This project demonstrates the use of multi-threading, socket connections, and GUI components in Java to create a chat application.

## Features

- **Real-Time Messaging:** Exchange messages between a client and a server.
- **Graphical User Interface:** Simple and intuitive GUI using Java Swing.
- **User Profiles:** Display user profiles with icons and statuses.
- **Typing Interface:** Includes a text field and "Send" button for message input.
- **Timestamps:** Each message displays a timestamp for better context.

## Requirements

- **Java Development Kit (JDK):** Version 8 or above.
- **Java Swing:** Comes pre-installed with the JDK.
- **Icons:** Ensure the `icons` folder is in the project's root directory, containing required icons (`left_arrow.png`, `2.png`, `video.png`, `phone.png`, `3icon.png`, etc.).

## How to Run

### Server
1. Compile the `Server.java` file:
   ```bash
   javac Server.java
   ```
2. Run the server:
   ```bash
   java Server
   ```
   The server will listen for connections on port `6001`.

### Client
1. Compile the `Client.java` file:
   ```bash
   javac Client.java
   ```
2. Run the client:
   ```bash
   java Client
   ```
   The client connects to the server at IP `192.168.0.111` and port `6001`. You can modify these values in the code if needed.

## Code Overview

### Server
- **Class Name:** `Server`
- **Responsibilities:**
  - Listens for incoming client connections on port `6001`.
  - Reads and sends messages to/from the connected client.
- **Key Components:**
  - `ServerSocket` for listening to connections.
  - `DataInputStream` and `DataOutputStream` for communication.

### Client
- **Class Name:** `Client`
- **Responsibilities:**
  - Connects to the server.
  - Sends and receives messages.
  - Displays messages with timestamps in the GUI.
- **Key Components:**
  - `Socket` for connecting to the server.
  - `DataInputStream` and `DataOutputStream` for communication.
  - `JPanel`, `JTextField`, and `JButton` for GUI.

## Folder Structure

```
ChatApp/
├── src/
│   ├── ChatApp/
│   │   ├── Client.java
│   │   ├── Server.java
├── icons/
│   ├── 1.png
│   ├── 2.png
│   ├── left_arrow.png
│   ├── video.png
│   ├── phone.png
│   ├── 3icon.png
├── README.md
```

## How It Works

1. **Server Initialization:**
   - The `Server` class starts a `ServerSocket` on port `6001`.
   - Waits for a client connection.
   - Handles message exchange with the client.

2. **Client Connection:**
   - The `Client` class establishes a connection to the server.
   - Sends user input to the server.
   - Displays incoming messages in the GUI.

3. **Message Display:**
   - Messages are displayed in `JPanel` with a timestamp, styled using Java Swing components.


## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

Feel free to customize and improve the application as needed. Contributions are welcome!

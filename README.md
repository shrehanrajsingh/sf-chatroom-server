SF-CHATROOM-SERVER
==================

A lightweight, real-time chat application built with the Sunflower programming
language. This project demonstrates a complete web application stack featuring
a custom backend written in Sunflower and a terminal-inspired frontend interface.

DESCRIPTION
-----------

SF-Chatroom-Server is a web-based chat room application that provides real-time
messaging capabilities through a clean, retro terminal-style user interface. The
application showcases the capabilities of the Sunflower programming language for
web server development while maintaining simplicity and performance.

The application features a minimalist design inspired by classic terminal
interfaces, with green text on a black background, providing a unique user
experience reminiscent of early computing systems.

FEATURES
--------

* Real-time message polling and display
* Terminal-style user interface
* User authentication with username system
* Message persistence during session
* Timestamp tracking for all messages
* Special character handling (quote encoding/decoding)
* Clean, distraction-free chat interface
* Responsive design for various screen sizes
* About page with developer information
* Contact page with social links

REQUIREMENTS
------------

* Sunflower programming language interpreter
* Modern web browser with JavaScript support
* HTTP server capabilities (provided by Sunflower backend)

INSTALLATION
------------

1. Clone the repository:

   git clone https://github.com/shrehanrajsingh/sf-chatroom-server.git

   cd sf-chatroom-server

2. Ensure Sunflower is installed on your system. If not, install it from:

   https://github.com/shrehanrajsingh/sunflower-cpp

3. Verify the installation:

   sunflower --version

USAGE
-----

Starting the Server:

1. Navigate to the project directory:

   cd simple-sf-webapp

2. Run the Sunflower backend:

   sunflower main.sf

3. Open your web browser and navigate to:

   http://localhost:PORT

   (Replace PORT with the port specified in main.sf)

Using the Application:

1. On the login screen, enter your desired username
2. Press "ENTER SYSTEM" or hit Enter to join the chat
3. Type your message in the input field at the bottom
4. Press "SEND" or hit Enter to send messages
5. Messages appear in real-time for all connected users
6. Use "DISCONNECT" to exit the chat and return to login

Navigation:

* Click "CONTACT ADMIN" to view contact information
* Click "ABOUT" to learn more about the developer and project
* Access the VS Code replica at /explore for project visualization

ARCHITECTURE
------------

Backend:
  - Written in Sunflower programming language
  - Handles HTTP requests and routing
  - Manages chat message storage and retrieval
  - Provides RESTful API endpoints

Frontend:
  - Pure HTML, CSS, and vanilla JavaScript
  - No external framework dependencies
  - Polling-based message updates (800ms interval)
  - Terminal-inspired UI design

API Endpoints:

  GET /chats
    Returns all chat messages in JSON format
    Response: {"chats": [{"user": "username", "message": "text"}]}

  POST /addchat
    Accepts new chat message
    Request body: {"user": "username", "message": "text"}
    Note: Double quotes in messages are encoded as &quot;

FILE STRUCTURE
--------------

```
simple-sf-webapp/
├── main.sf               # Sunflower backend server
├── template/
│   ├── home.html         # Main chat interface
│   ├── contact.html      # Contact information page
│   ├── about.html        # About developer page
│   └── explore.html      # VS Code replica visualization
└── README.md             # This file
```

TECHNICAL DETAILS
-----------------

Message Handling:
  - Messages are polled every 800 milliseconds
  - Incremental rendering prevents timestamp refresh issues
  - Double quotes are encoded as &quot; on send, decoded on display
  - HTML special characters are properly escaped for security

UI Design:
  - Font: Courier New (monospace)
  - Color scheme: Black background (#000), green text (#0f0)
  - Minimalist design with no distractions
  - Fixed-height chat container with scrolling
  - Responsive layout adapts to mobile devices

State Management:
  - Client-side tracking of displayed message count
  - Session-based username storage
  - No persistent storage (messages cleared on server restart)

KNOWN LIMITATIONS
-----------------

* Messages are stored in-memory only (not persistent across restarts)
* No user authentication or authorization
* No message encryption
* No private messaging or rooms
* No file sharing capabilities
* Polling-based updates (no WebSocket support yet)

CONTRIBUTING
------------

Contributions are welcome. Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (git checkout -b feature-name)
3. Commit your changes (git commit -am 'Add new feature')
4. Push to the branch (git push origin feature-name)
5. Create a Pull Request

Code Style:
  - Follow existing code formatting
  - Add comments for complex logic
  - Test thoroughly before submitting
  - Update documentation as needed

AUTHOR
------

Shrehan Raj Singh

Second year undergraduate student at IIT Kharagpur

Creator of Sunflower Programming Language

Contact:
  Email: shrehanofficial@gmail.com
  GitHub: https://github.com/shrehanrajsingh
  LinkedIn: https://www.linkedin.com/in/shrehanrajsingh/
  Instagram: https://instagram.com/shrehanrajsingh

PROJECT LINKS
-------------

Repository: https://github.com/shrehanrajsingh/sf-chatroom-server
Sunflower Language: https://github.com/shrehanrajsingh/sunflower-cpp

LICENSE
-------

Copyright (C) 2026 Shrehan Raj Singh

This project's license will be specified in a separate LICENSE file.
For inquiries about usage and licensing, please contact the author.

ACKNOWLEDGMENTS
---------------

* Inspired by classic UNIX terminal interfaces
* Built to demonstrate Sunflower programming language capabilities
* Terminal UI design influenced by retro computing aesthetics

CHANGELOG
---------

Version 1.0.0 (Initial Release):
  - Basic chat functionality
  - Terminal-style UI
  - User authentication
  - Real-time polling
  - Message persistence during session
  - About and Contact pages
  - VS Code replica visualization

SUPPORT
-------

For bug reports, feature requests, or questions:
  - Open an issue on GitHub
  - Contact via email: shrehanofficial@gmail.com
  - Submit pull requests for fixes or improvements

NOTES
-----

This is an educational project demonstrating web application development
with the Sunflower programming language. It is designed to be simple,
readable, and extensible for learning purposes.

The backend is intentionally minimalist to showcase Sunflower's web server
capabilities without overwhelming complexity. The frontend similarly avoids
modern frameworks to demonstrate core web technologies.

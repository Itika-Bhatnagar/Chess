## Deployment:

* Deployed the application to a hosting service *(Vercel)*  

DIRECTLY ACCESSABLE TO USE : 

## High Level Overview

* The project is an online chess game that allows two players to play against each other in real-time.
* It includes features for game management, move validation, and real-time communication between clients.
* It is built using Node.js , express , socket.IO , Chess.js


## Tech Stack
* Node.js:
    * The runtime environment for the server-side code.  
    * Handles requests and responses, manages the server, and interacts with other components.
* Express:  
   * A web application framework for Node.js.   
   * Simplifies server-side code by providing middleware for handling HTTP requests, routing, and static files.
* Socket.IO:  
   * A library for real-time, bidirectional communication between web clients and servers.  
   * Facilitates the real-time updating of the game state, allowing players to see their opponent's moves instantaneously.  
* Chess.js:
   * A library for chess move generation, validation, and game state management.
   * Ensures that all moves are legal and manages the game state, including check, checkmate, and draw conditions.
 

## Example Workflow  
#### Player A and Player B connect to the game:  
* The server assigns each player to a game session.   
* Player connected first will be assigned to white pawn.    
#### Player A makes a move:  
* The client-side code validates the move using Chess.js.  
* If the move is valid, it is sent to the server via Socket.IO.  
* The server updates the game state and broadcasts the move to Player B.    
#### Player B receives the move:
* The move is processed and the game state is updated on Player B's client.  
* Player B then makes a move, and the cycle repeats.  
#### Game Over:     
* Chess.js detects checkmate, stalemate, or draw conditions.    
* The server notifies both clients of the game outcome.    
* The game session is terminated or reset based on the outcome.

### Chess Game Project  
├── public  
│   └── chess.js  
├── views  
│   └── index.ejs  
├── README.md  
├── app.js  
├── package.json  
└── pckage-lock.json  


### Low Stack Overview  
#### public  
* chess.js:  
   * Client-side JavaScript file responsible for handling the chess logic, move validation, and possibly some UI updates.  
#### views
* index.ejs:  
   * EJS (Embedded JavaScript) template file that renders the HTML for the main game page. It may include the chessboard layout and integrate the client-side scripts.

* package.json:  
Configuration file for the Node.js project. It lists the project dependencies, scripts, and other metadata.   
* pckage.json:  
This appears to be a typo or a duplicate of package.json. It should be corrected or removed to avoid confusion.   


# Installation 
```bash
git clone https://github.com/Itika-Bhatnagar/Online-Code-Editor.git  
```

## Run Locally

```bash

# install dependencies

npm init -y
npm i express chess.js ejs socket.io

# start the dev server  

npx nodemon
```
The application will be available at http://localhost:3000/

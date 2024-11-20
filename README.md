# Console-Based Chess Game in C++
## Overview
This project is a fully functional console-based chess game implemented in C++. It focuses on enforcing the core rules of chess, including move validation for all pieces and detection of check conditions. The game emphasizes game logic over graphics, showcasing the application of object-oriented design in a complex system.

## Features
Object-Oriented Design: Each chess piece (King, Queen, Rook, Bishop, Knight, and Pawn) is represented as a class derived from a base ChessPiece class. This modular design enhances code extensibility and maintainability.

Move Validation: The game ensures proper movement for all pieces. Rooks move in straight lines, bishops diagonally, and pawns have unique rules for initial two-square moves and capturing.

Check Detection: The game continuously checks for situations where a move puts the player's own King in check. If a move results in check, it is considered invalid, adding depth to the gameplay strategy.

Text-Based Input/Output: The chessboard is displayed as an 8x8 grid with pieces represented by initials (e.g., "WP" for White Pawn, "BK" for Black King). Players input moves using standard chess notation (e.g., "e2 to e4").

## How to Play
Upon launching the game, the chessboard will be displayed with pieces arranged in their standard starting positions.

Input Format: Players take turns entering moves using the format start_position end_position (e.g., e2 e4 to move a White Pawn from e2 to e4).

Error Handling: If a player attempts an invalid move (e.g., moving into check or violating movement rules), an error message will be displayed, and the player must enter a valid move.

The game continues until players decide to stop or a winner is manually declared. Note: Checkmate detection is planned for future updates.

## How It Works
Chess Pieces: Each piece type is represented by a separate class (e.g., Pawn, King), inheriting common functionality from the ChessPiece base class. Each class implements specific movement rules for the corresponding piece.

Move Simulation: Before executing a move, the game simulates it to check if the King's safety is compromised. If a move places the player's own King in check, it will be rejected.

Check Detection: The game can detect when the opponent's King is in check after a move and will alert the players.

## Code Structure
ChessPiece: The base class for all chess pieces, containing shared attributes and functions.

Pawn, Rook, Knight, Bishop, Queen, King: Classes for individual pieces, each implementing their own movement rules.

ChessBoard: Manages the board state, facilitates piece movement, and handles game conditions like check detection.

## Future Enhancements
Checkmate Detection: Implement game-ending logic when a player checkmates their opponent.

Advanced Rules: Add castling, en passant, and pawn promotion to enhance the gameplay experience.

AI Opponent: Potential implementation of an AI opponent for single-player mode.

## Installation
To run the game, follow these steps:

Clone the repository:

```bash

git clone <repository-url>
cd chess
```
Compile the source code:

```bash

g++ chess.cpp -o chess
```
Run the game:

```bash

./chess
```
Enjoy playing!

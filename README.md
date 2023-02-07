### About OnChess
The OnChess chess program is a single-screen multiplayer chess program that allows users to play new games, open previous games, save current games, and create custom games.

There are two ways of moving a chess piece in the OnChess program: the Click-Click method, and the Click-and-Drag method.
Click-Click – Click over a chess piece you wish to move and click again on one of the highlighted squares.
Click-and-Drag – Click over a chess piece you wish to move, and without letting go, move the cursor to one of the highlighted squares. Once your cursor reaches the destination of your choice (one of the highlighted squares), you may let go to execute the move. Prior to a release, the field of the destination square should be populated with a miniature transparent “ghost” piece of the piece being moved.
After you move a piece, the square on which you moved will be highlighted with a light-blue color, to let the opponent player which piece on the board you moved and where it was moved to.
The game is won by checkmating the opponent’s king, which may be done by threatening to take the square occupied by it (a.k.a. “check”) on the next move. Once the king has nowhere to move after a “check,” the game is over!
As a chess player, I decided to build this program for the purpose of using it to recreate infamous chess games and play them through one-by-one. I also wanted to bring nostalgia to the table by offering the option to play single-screen multiplayer chess!

![image](https://user-images.githubusercontent.com/50674368/217136153-fcc8cc51-fa13-48cd-af8c-a0af20e0a312.png)

![image](https://user-images.githubusercontent.com/50674368/217136412-2d35c3b7-17a6-4920-ba97-dff945c5bf97.png)

![image](https://user-images.githubusercontent.com/50674368/217136518-030441f9-e223-4767-87f2-51eefbba2956.png)

![image](https://user-images.githubusercontent.com/50674368/217136802-52370ca2-192c-4f50-a17b-6fbb97a2987e.png)

### Domain Objects
Chess Board – The Chess Board hosts the playing field for chess games, allowing chess pieces to move freely around the board (albeit following the standard rules of chess). A Chess Board is created when a new game is created, or when a game is loaded from a saved file from disk. The board can be edited in the settings panel (e.g., changing the color of the squares, or enabling board rotations, etc.).

Customizer Board – The Customizer Board is a board that allows for users to pre-set their desired game of chess, which is executed by placing any type of piece (elucidated below) anywhere on the board. Users may create any type of chess piece in any square of the board, edit/change the piece in a square to transition over to the next piece in line, and finally delete the piece—rendering the square empty once again.

Pieces – Chess pieces on this board may be added (e.g., when starting a game), deleted (e.g., when overtaking an enemy piece), and edited (e.g., when promoting a pawn to a queen). A series of deletion and additions also partake whenever a piece moves over the board; in essence, when a chess piece moves from one square to another, what actually takes place behind the scenes is: the piece is deleted from the square it was in and is re-created in the destination square.

•	Pawn – The pawn has the most restricted capabilities when it comes to moving pieces across the board. The pawn may move only in the forward direction to an empty spot, one square at a time (except during the first move, which the game allows for it to move two squares). It captures pieces (i.e., deletes an opponent’s piece off of the board) by moving diagonally in the forward direction, which is exclusively allowed when there already exists a piece occupying by the square. When the pawn reaches the top of the board, it is immediately promoted to a queen.

•	Bishop – The bishop piece can freely move across the board in the diagonal direction, so long as a piece does not block its path, whether it be a piece owned by the opponent, or a piece owned by the player. If the piece that is blocking the bishop’s path is the opponent’s piece, then the bishop can capture that piece, replacing the occupied space with itself.

•	Knight – The knight is the only piece in the game that is not affected by being “blocked” by other pieces occupying the path in which it moves, and the only square it cannot move to is a square owned by a player’s piece. The knight moves one square diagonally and one square straight in any direction.

•	Rook- The rook, located in all corners of the board, may move horizontally or vertically across the board. Its blockage and piece overtaking concept is the same as that of the bishop, and the only difference is that it moves up, down, left, or right.

•	The Queen – Like the King, there exists only one Queen on the board for each side. As the most powerful piece on the board, this piece’s abilities combine that of the bishop’s and the rook’s, allowing it to move freely in the diagonal, horizontal and vertical directions. Its blockage and piece overtaking concept is also the same as both the bishop and the rook.

•	The King – As the most crucial  piece in the game, the survival of the king decides whether or not a game plays on or terminates as a loss. However, it is not a very mobile piece, as it can only move (and overtake a piece if the moved square is occupied by an unprotected piece) one square at a time, albeit in any direction.


### Views
Three main views are offered in the Chess GUI model. 
The first view is the start screen, which is introduced when the application is executed. It includes buttons to play a new game, open a pre-set game, access the customizer panel, edit in-game settings, or view the about information of the project. 
The second view is the view of the main chess board model. This view was created by combining a series of Stack Panes, which amounts to 64 in total. The resulting 8X8 board is a Grid Pane that contains and manages each of the individual stack panes.
The last view, the Customizer view (made for the Customizer model), provides a view of the board where users can pre-configure a chess board and save it to a local .csv file. This view was created by extending the standard chess board view.


### Widgets
The main custom-designed widget is the Settings panel, which allows the editing of the board’s colors, displaying a preview of the color that was chosen by the JColorPicker. The panel also allows users to enable or disable automatic board rotation after each turn, as well as turning the board flip animation on or off. Users are also provided with the option to write the names of each player, which are used in naming the ‘save’ file. Other minor widgets, like the File Chooser widget and the menu pane widget, have been integrated to the project.
Another major custom widget implemented in the project is the Customizer board. In this widget, a click (left-click for white and right-click for black) will create or transition the piece in the clicked square using the following sequence: Pawn->Knight->Bishop->Rook->Queen 
For instance, right clicking on an empty square will create a black pawn. Clicking the same square again will transition that pawn into a knight, and the piece's color will depend on whether or not the click was a left-click (white) or a right-click (black).
When finished, users may click File -> Save to download your customized game file. By default, the file is saved within the "saves" folder, under a file name with the timestamp of the exact date/time it was saved.



### Pre-populated Fields
The pre-populated fields on a standard board are: 8 pawns, 2 rooks, 2 bishops, 2 knights, a queen, and a king. Created for each side at the start of the game, each of these pieces are deleted when pieces from the opponent’s side overtakes the same square (i.e., the piece is moved to a square that is already occupied by a piece from the opponent).

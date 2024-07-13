7/13/24
Johnathan Reinhart explanation of using OOP to articulate game logic in Chess


Player Class:

Attributes: checked, color, castled, king, kingMoved, promote, moved
Instances:
white (new Player("white"))
black (new Player("black"))
SquareObject Class:

Attributes: x, y, color, selected, element, piece
Methods: setPiece, unsetPiece, update, select, deselect, hasPiece
Instances: Created dynamically in the setup function for each square on the board
Piece Class:

Attributes: x, y, color, type, captured, lastmoved, advancedtwo
Methods: capture
Subclass of Piece: Castle:

Attributes: Inherits from Piece
Methods: Inherits from Piece and overrides isValidMove
Instances: Created in the setup function for initial board setup
Subclass of Piece: Knight:

Attributes: Inherits from Piece
Methods: Inherits from Piece and overrides isValidMove
Instances: Created in the setup function for initial board setup
Subclass of Piece: Bishop:

Attributes: Inherits from Piece
Methods: Inherits from Piece and overrides isValidMove
Instances: Created in the setup function for initial board setup
Subclass of Piece: Queen:

Attributes: Inherits from Piece
Methods: Inherits from Piece and overrides isValidMove
Instances: Created in the setup function for initial board setup
Subclass of Piece: King:

Attributes: Inherits from Piece, adds checkedBy
Methods: Inherits from Piece and overrides isValidMove
Instances: Created in the setup function as white.king and black.king
Subclass of Piece: Pawn:

Attributes: Inherits from Piece


Methods: Inherits from Piece and overrides isValidMove
Instances: Created in the setup function for initial board setup
Object Instances and Extensions
Player Objects:

white and black are instances of the Player class.
SquareObject Objects:

Created dynamically in the setup function, representing each square on the chessboard.
Piece Objects and their Subclasses:

Castle:
Instances: new Castle(x, y, color)
Extends: Piece
Methods: Overrides isValidMove
Knight:
Instances: new Knight(x, y, color)
Extends: Piece
Methods: Overrides isValidMove
Bishop:
Instances: new Bishop(x, y, color)
Extends: Piece
Methods: Overrides isValidMove
Queen:
Instances: new Queen(x, y, color)
Extends: Piece
Methods: Overrides isValidMove
King:
Instances: new King(x, y, color)
Extends: Piece
Methods: Overrides isValidMove, adds checkedBy attribute
Pawn:
Instances: new Pawn(x, y, color)
Extends: Piece
Methods: Overrides isValidMove
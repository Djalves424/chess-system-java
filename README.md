# Projeto Sistema de Jogo de Xadrez

Feito esse projeto acompanhando as aulas do Prof. Dr. Nelio Alves, na Udemy

1° Etapa:

(Criando Primeira classe) ➝ First class: Position

Checklist:

• Class Position [public]

• OOP Topics:

• Encapsulation

• Constructors

• ToString (Object / overriding)

#################################################

2° Etapa:

(Começando a implementar as seguintes classes) ➝ Starting to implement Board and Piece

Checklist:

• Classes Piece, Board [public]

•  OOP Topics:

•  Associations

• Encapsulation / Access Modifiers

• Data Structures Topics:

• Matrix

##################################################

3° Etapa:

(Camada de xadrez e impressão do tabuleiro) ➝ Chess layer and printing the board

8 - - - - - - - -

7 - - - - - - - -

6 - - - - - - - -

5 - - - - - - - -

4 - - - - - - - -

3 - - - - - - - -

2 - - - - - - - -

1 - - - - - - - -

a b c d e f g h

Checklist:

Methods: Board.Piece(row, column) and Board.Piece(position)

• Enum Chess.Color

• Class Chess.ChessPiece [public]

• Class Chess.ChessMatch [public]
 
• Class ChessConsole.UI

• OOP Topics:

• Enumerations

• Encapsulation / Access Modifiers

• Inheritance

• owncasting

• Static members

• Layers pattern

##################################################

4° Etapa:

(Colocando as peças no tabuleiro) ➝ Placing pieces on the board

Checklist:

•	Method: Board.PlacePiece(piece, position)

•	Classes: Rook, King [puhlic]

•	Method: ChessMatch.InitialSetup

•	OOP Topics:

• Inheritance

•  Overriding

• Polymorphism 

• Data Structures Topics:

• Matrix

##################################################

5° Etapa:

BoardException and defensive programming

Checklist:

•	Class BoardException [puhlic]

•	Methods: Board.PositionExists, Board.ThereIsAPiece

•	Implement defensive programming in Board methods

•	OOP Topics:

•	Exceptions

•	Constructors (a string must he informed to the exception)

##################################################

6° Etapa:

(Criando as seguintes classes) ➝ ChessException and ChessPosition

Checklist:

•	Class ChessException [puhlic]

•	Class ChessPosition [puhlic]

•	Refactor ChessMatch.InitialSetup

•	OOP Topics:

•	Exceptions

•	Encapsulation

•	Constructors (a string must he informed to the exception)

•	Overriding

•	Static memhers

•	Layers pattern

##################################################

7° Etapa:

Little improvement in board printing

Color in terminal:

•	Windows: Git Bash

•	Mac: Google "osx terminal color"

Checklist:

•	Place more pieces on the hoard

•	Distinguish piece colors in UI.PrintPiece method

##################################################

8° Etapa:

Moving pieces

Checklist:

•	Method Board.RemovePiece

•	Method UI.ReadChessPosition

•	Method ChessMatch.PerformChessMove

•	Method ChessMatch.MakeMove

•	Method ChessMatch.ValidadeSourcePosition

•	Write hasic logic on Program.cs

•	OOP Topics:

•	Exceptions

•	Encapsulation

##################################################

9° Etapa:

(Manipulando exceções e tela de limpeza) ➝ Handling exceptions and cOearing screen

Clear screen using Java:

// https://stackoverflow.com/questions/2979383/java-clear-the-console

public static void clearScreen() { System.out.print(w\033[H\033[2Jw); System.out.flush();

 }


Checklist:

•	ChessException

•	InputMismatchException

(Possíveis movimentos de uma peça) ➝ Possible moves of a piece

![image](https://github.com/Djalves424/chess-system-java/assets/108296040/9ec44373-50af-4654-888b-d19c710655b8)

(imput a piece) ➝ insira uma peça / (Saída: uma matriz booleana de movimentos possíveis) ➝ Output: a boolean matrix of  possible movements

![image](https://github.com/Djalves424/chess-system-java/assets/108296040/71c4b87c-8fc5-4380-b825-5747b2322486)

Checklist:

•	Methods in Piece:

•	PossihleMoves [ahstract]

•	PossihleMove

•	IsThereAnyPossihleMove

•	Basic PossihleMove implementation for Rook and King

•	Update ChessMatch.ValidadeSourcePosition

•	OOP Topics:

•	Ahstract method / class

•	Exceptions

##################################################

10° Etapa:

(Implementando possíveis movimentos de Torre) ➝ Implementing possible moves of Rook

Checklist:

•	Method ChessPiece.IsThereOpponentPiece(position) [protected]

•	Implement Rook.PossihleMoves

•	Method ChessMatch.ValidateTargetPosition

•	OOP Topics:

•	Polymorphism

•	Encapsulation / access modifiers [protected]

•	Exceptions

##################################################

11° Etapa:

(Imprimindo movimentos possíveis) ➝ Printing possible moves

Checklist:

•	Method ChessMatch.PossihleMoves

•	Method UI.PrintBoard [overload]

•	Refactor main program logic

•	OOP Topics:

•	Overloading

##################################################

12° Etapa:

(Implementando possíveis movimentos de Rei) ➝ Implementing possible moves of King

Checklist:

•	Method King.CanMove(position) [private]

•	Implement King.PossihleMoves

•	OOP Topics:

•	Encapsulation

•	Polymorphism

##################################################

13° Etapa:

(Trocar de jogador a cada turno) ➝ Switching player each turn

Checklist:

•	Class ChessMatch:

•	Properties Turn, CurrentPlayer [private set]

•	Method NextTurn [private]

•	Update PerformChessMove

•	Update ValidadeSourcePosition

•	Method UI.PrintMatch

•	OOP Topics:

•	Encapsulation

•	Exceptions

##################################################

14° Etapa:

(Manuseio de peças capturadas) ➝ Handling captured pieces

Checklist:

•	Method UI.PrintCapturedPieces

•	Update UI.PrintMatch

•	Update Program logic

•	Lists in ChessMatch: _piecesOnTheBoard, _capturedPieces

•	Update constructor

•	Update PlaceNewPiece

•	Update MakeMove

•	OOP Topics:

•	Encapsulation

•	Constructors

•	Data Structures Topics:

•	List

##################################################

15° Etapa:

(Verifique a Lógica) ➝ Check Logic

(Regras) ➝ Rules:

•	(Xeque significa que seu rei está ameaçado por pelo menos uma peça do oponente) ➝ Check means your king is under threat hy at least one opponent piece

•	(Você não pode se colocar em xeque) ➝ You can't put yourself in check

Checklist:

•	Property ChessPiece.ChessPosition [get]

•	Class ChessMatch:

•	Method UndoMove

•	Property Check [private set]

•	Method Opponent [private]

•	Method King(color) [private]

•	Method TestCheck

•	Update PerformChessMove

•	Update UI.PrintMatch

##################################################

16° Etapa:

(Lógica do xeque-mate) ➝ Checkmate Logic

Checklist:

•	Class ChessMatch:

•	Property Checkmate [private set]

•	Method TestCheckmate [private]

•	Update PerformChessMove

•	Update UI.PrintMatch

•	Update Program logic

##################################################

17° Etapa:

(Contagem de movimentos de peças) ➝ Piece move count
 
Checklist:

•	Class ChessPiece:

•	Property MoveCount [private set]

•	Method IncreaseMoveCount [internal]

•	Method DecreaseMoveCount [internal]

•	Class ChessMatch:

•	Update MakeMove

•	Update UndoMove

•	OOP Topics:

•	Encapsulation

##################################################

18° Etapa:

(Peão) ➝ Pawn

Checklist:

•	Class Pawn

•	Update ChessMatch.InitialSetup

•	OOP Topics:

•	Encapsulation

•	Inheritance

•	Polymorphism

##################################################

19° Etapa:

(Bispo) ➝ Bishop

Checklist:

•	Class Bishop

•	Update ChessMatch.InitialSetup

•	OOP Topics:

•	Encapsulation

•	Inheritance

•	Polymorphism

##################################################

20° Etapa:

(Cavalo) ➝ Knight

Checklist:

•	Class Knight

•	Update ChessMatch.InitialSetup

•	OOP Topics:

•	Encapsulation

•	Inheritance

•	Polymorphism

##################################################

21° Etapa:
 
(Rainha) ➝ Queen

Checklist:

•	Class Queen

•	Update ChessMatch.InitialSetup

•	OOP Topics:

•	Encapsulation

•	Inheritance

•	Polymorphism

##################################################

22° Etapa:

(Movimento especial - Roque) ➝ Special move - Castling

![image](https://github.com/Djalves424/chess-system-java/assets/108296040/2c18d95d-8c7f-487e-b3b1-82ffe987010e)

Checklist:

•	Update King

•	Update ChessMatch.MakeMove

•	Update ChessMatch.UndoMove

##################################################

23° Etapa:

(Movimento especial - En Passant) ➝ Special move - En Passant

![image](https://github.com/Djalves424/chess-system-java/assets/108296040/7c2f4255-9197-4f0a-a092-2b80c4d3abcc)

##################################################

24° Etapa:

(Movimento especial - Promoção) ➝ Special move - Promotion

![image](https://github.com/Djalves424/chess-system-java/assets/108296040/877a2fe7-d658-4a6e-9e63-3c8e6b6f0273)































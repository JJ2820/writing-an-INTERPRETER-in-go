### writing-an-INTERPRETER-in-go
Monkey programming language from Writing an interpreter in Go and Writing a compiler in Go.

## I will be Documenting the build of interpreter uisng Go 


## Chapter one - Lexer

Building laxer so it can get the  source code as input and output the tokens that represent the source code. It will go through its input and output the next token it recognizes. It doesn’t need to buffer or save tokens, since there will only be one method called **NextToken()** and its Hellpers. 


## Chapter two - Parser

parser we are going to write is a recursive descent parser.
The parser produces an **AST** that accurately represents the information contained in the original let statement.
it needs two different types of nodes: **expressions and statements**
we have three interfaces called Node, Statement and Expression
it has to provide a TokenLiteral() method that returns the literal value of the token it’s associated with **TokenLiteral()** will be used only for debugging and testing
The Parser has three fields: **l, curToken and peekToken**. l is a pointer to an instance of the lexer, on which we repeatedly call **NextToken()** to get the next token in the input. curToken and peekToken act exactly like the two “pointers” our lexer has: position and peekPosition

TODO: We're skipping the expressions until we encounter a semicolon


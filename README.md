### writing-an-INTERPRETER-in-go
Monkey programming language from Writing an interpreter in Go and Writing a compiler in Go.

## I will be Documenting the build of interpreter uisng Go 


## Chapter One - Lexer

The lexer (or tokenizer) breaks the input string into tokens.
Building laxer so it can get the  source code as input and output the tokens that represent the source code. It will go through its input and output the next token it recognizes. It doesn’t need to buffer or save tokens, since there will only be one method called **NextToken()** and its Hellpers. 


## Chapter Two - Parser

The parser processes the tokens and creates an abstract syntax tree (AST).
parser we are going to write is a recursive descent parser.
The parser produces an **AST** that accurately represents the information contained in the original let statement.
it needs two different types of nodes: **expressions and statements**
we have three interfaces called Node, Statement and Expression
it has to provide a TokenLiteral() method that returns the literal value of the token it’s associated with **TokenLiteral()** will be used only for debugging and testing
The Parser has three fields: **l, curToken and peekToken**. l is a pointer to an instance of the lexer, on which we repeatedly call **NextToken()** to get the next token in the input. curToken and peekToken act exactly like the two “pointers” our lexer has: position and peekPosition

TODO: We're skipping the expressions until we encounter a semicolon


## Chapter Three - Evaluation

The evaluator walks the AST and evaluates the expressions.
evaluation process of an interpreter defines how the programming language being interpreted works
we’re going to represent every value we encounter when evaluating Monkey source code as an Object, an interface of our design. 
Eval will take an ast.Node as input and return an object.Object
refer the bok for more info




### This interpreter is quite simple and only supports basic arithmetic operations without parentheses or operator precedence. However, it demonstrates the core concepts of lexing, parsing, and evaluating, which are foundational for more complex language implementations.


Reference - [Book 1](https://interpreterbook.com/)

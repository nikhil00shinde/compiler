### The Kaleidoscope Language
- Procedural Langauge
- Call into Standard Library



#### Lexer
- The First thing needed is the ability to process a text file and recognize what it days.
- A way to do this is to use a *"lexer"* (aka 'Scanner') to break the input up into "tokens".
- Each token returned by the lexer includes a token code and potentially some metadata (e.g. the numeric value of a number).


- Each token returned by our lexer will either be one of the Token enum values or it will be an 'unknown' character like '+', which is returned as its ASCII value.
- If the current token is an identifier, the **IdentifierStr** global variable holds the name of the identifier. 
- If the current token is a numeric literal (like 1.0), **NumVal** holds its value.



##### The gettok function
- *gettok* function is called to return the next token from standard input.
- *gettok* works by calling the **C getchar()** function to read characters one at a time from standard input.


- **The next thing gettok needs to do is recognize identifiers and specific keywords like "def"**. It does this with the simple loop:


##### isalpha isspace isdigit

- **isspace** --> it will check for whitespace

- **isalpha** --> sets the *Identifier* global whenever it lexes an identifier. Also complete the full word by looping (def, extern, tok_identifier)

- **isdigit** --> it will checks for integer & floating point number
   - uses *strod()* --> to convert numeric string to a numberic value.



###### Comment
- We process comment if the *LastChar == '#''*
    - And skip all these until it hit `EOF (End of File), \n, \r`


###### EOF
- At last if it none other than `EOF`, then just return its token otherwise, return characters ASCII Value

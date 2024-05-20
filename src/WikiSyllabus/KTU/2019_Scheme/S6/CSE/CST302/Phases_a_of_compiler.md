# Phases of a Compiler

- Lexical Analysis
- Syntax Analysis
- Semantic Analysis
- Intermediate Code Generation
- Code Optimization
- Target Code Generation

# Lexical Analysis
- The first phase of a compiler is called lexical analysis or scanning.

- The lexical analyzer reads the stream of characters making up the source program and
  groups the characters into meaningful sequences called lexemes.

- For each lexeme, the lexical analyzer produces as output a token of the form
    < token- name, attribute-value >
    that it passes on to the subsequent phase, syntax analysis.

- In the token, the first component token- name is an abstract symbol that is used during
  syntax analysis, and the second component attribute-value points to an entry in the
  symbol table for this token.

- Information from the symbol-table entry 'is needed for semantic analysis and code
  generation.

- For example, suppose a source program contains the assignment statement
  position = initial + rate * 60

- The characters in this assignment could be grouped into the following lexemes and
  mapped into the following tokens passed on to the syntax analyzer:

1. position is a lexeme that would be mapped into a token <id, 1>, where id is an
   abstract symbol standing for identifier and 1 points to the symbol table entry for 
   position. The symbol- table entry for an identifier holds information about the
   identifier, such as its name and type.

2. The assignment symbol = is a lexeme that is mapped into the token < = >. Since
   this token needs no attribute-value, we have omitted the second component.

3. initial is a lexeme that is mapped into the token < id, 2> , where 2 points to the
   symbol-table entry for initial .

4. + is a lexeme that is mapped into the token <+>.

5. rate is a lexeme that is mapped into the token < id, 3 >, where 3 points to the
   symbol-table entry for rate.

6. * is a lexeme that is mapped into the token <* > .

7. 60 is a lexeme that is mapped into the token <60>

- Blanks separating the lexemes would be discarded by the lexical analyzer. The
  representation of the assignment statement position = initial + rate * 60 after
  lexical analysis as the sequence of tokens as:

  < id, l > < = > <id, 2> <+> <id, 3> < * > <60>

# Syntax Analysis

- The second phase of the compiler is syntax analysis or parsing.

- The parser uses the first components of the tokens produced by the lexical analyzer to
  create a tree-like intermediate representation that depicts the grammatical structure of
  the token stream.

- A typical representation is a syntax tree in which each interior node represents an
  operation and the children of the node represent the arguments of the operation.

- The syntax tree for above token stream is:
  //pic

- The tree has an interior node labeled with ( id, 3 ) as its left child and the integer 60 as
  its right child.
- The node (id, 3) represents the identifier rate.
- The node labeled * makes it explicit that we must first multiply the value of rate by 60.
- The node labeled + indicates that we must add the result of this multiplication to the
  value of initial.
- The root of the tree, labeled =, indicates that we must store the result of this addition
  into the location for the identifier position.

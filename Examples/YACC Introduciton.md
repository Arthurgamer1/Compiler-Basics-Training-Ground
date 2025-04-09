Yet Another Compiler Compiler (YACC) is a sintax analyzer (parser) generator. In other words it generates C code for a parser and yes I used ChatGPT to generate a guide for easy breakdown.

## How does it do?

Yacc takes a grammar specification for a language (written in a BNF-like format) and generates C code for a parser. This parser takes a sequence of tokens (usually provided by a lexer, often made with Lex) and builds a syntax tree or performs semantic actions. 

## Typical WorkFlow

Write a grammar file (usually with .y extension) using Yacc.
    • Write a lexer (with Lex or Flex) to tokenize input.
    • Compile both the lexer and parser, then link them together.
    • Run your parser on input data.
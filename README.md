# Compiler-Basics-Training-Ground

This repository serves for training on compiler concepts with Lex, YACC, Flex and Bison. This is design from a student for a student, hence don't expect this repository to be perfect as it used AI like ChatGPT to breakdown concepts or have continuos work. However, you can calm down, these information was verified and examples were tested in order for me to learn and help others learn. Having that said, let's introduce the tools that will be working with!

## 🔨 Tools Instruction & Function

- **YACC**: Yet Another Compiler Compiler is a sintax analyzer (parser) generator. In other words it generates C code for a parser.
- **Lex**: A lexical analyzer generator — it helps you write programs that split input text into meaningful units called tokens. These tokens are usually passed to a parser like Yacc.
- **Bison and Flex**: Bison and Fast Lexical Analyzer (Flex) are modern, GNU versions of Yacc and Lex respectively. They're widely used to build interpreters, compilers, DSLs, and even config file parsers.

### What YACC does?

Yacc takes a grammar specification for a language (written in a BNF-like format) and generates C code for a parser. This parser takes a sequence of tokens (usually provided by a lexer, often made with Lex) and builds a syntax tree or performs semantic actions.

### What Lex does?

You write a Lex specification (usually with .l extension), which defines patterns to match (regular expressions) and actions to perform when those patterns are matched (usually in C). Lex then generates a C program (lex.yy.c) that reads input and executes the actions when patterns are found.


### What Bison Does?

To explain simply, Bison takes a grammar file (usually .y) describing the syntax of a language. Then it generates a parser in C/C++. The parser calls yylex() (provided by Flex) to get tokens from input. Bison handles syntax rules, precedence, and error handling.

### What Flex Does?

Flex takes a lexer spec file (usually .l) containing regex patterns and actions. Then, it generates C code (lex.yy.c) that reads input and emits tokens to the parser. Subsequently, tokens are identified using named constants like NUMBER, PLUS, etc.


## 🌊 Typical WorkFlow

Write a grammar file (usually with .y extension) using Yacc.
    • Write a lexer (with Lex or Flex) to tokenize input.
    • Compile both the lexer and parser, then link them together.
    • Run your parser on input data.

You may got to examples/exaple1 for yacc and lex working together. Or examples/exaple2 to see how Flex and Yacc work together



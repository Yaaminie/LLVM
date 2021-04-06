# LLVM

## Introduction

LLVM stands for low level virtual machine. LLVM is a compiler and a toolkit for building compilers. LLVM project is the collection of modular and reusable compiler and toolchain technologies. LLVM isn’t a compiler for any given language, LLVM is a framework to generate object code from any source code.<br>
LLVM is designed around a language-independent intermediate representation (IR). Intermediate representation (IR), a low-level programming language similar to assembly. IR is a strongly typed reduced instruction set computing (RISC) instruction set which abstracts away most details of the target.

## Working of LLVM
clang->opt(optimization)->llc->lld(object code)

On the front end, the LLVM compiler infrastructure uses clang — a compiler for programming languages C, C++ and Objective-C — to turn source code into an interim format. Then the LLVM clang code generator on the back end turns the interim format into final machine code.
Backend code of LLVM converts the LLVM Intermediate Representation (IR) to code for a specified machine or other languages.
The backend of LLVM features a target-independent code generator <br>

Optimization — Cleans the code for better run-time performance and addresses memory-related issues. <br>
The llc command compiles LLVM source inputs into assembly language for a specified architecture.  <br> 

Linker <br>
The lld subproject is an attempt to develop a built-in, platform-independent linker for LLVM. <br>

## C++11/C++14 features used
In LLVM\lib\AsmParser\Parser.cpp

Use of unique_ptr
In C++11, auto_ptr has been deprecated and the following smart pointers added.

std::unique_ptr: The destructors of this class release memory for the underlying object when the pointer goes out of scope. Through move semantics, it is ensured that only one pointer can bind to the object at a time.

Even nullptr is new feature add in version c++11
nullptr keyword in place of NULL

Use of range based for loops and auto keyword in AliasAnalysis.cpp

template used in LLparser.h 

inline keyword used in AliasAnalysisEvaluator.cpp (C++17)
If a function is inline, the compiler places a copy of the code of that function at each point where the function is called at compile time.

Any change to an inline function could require all clients of the function to be recompiled because compiler would need to replace all the code once again otherwise it will continue with old functionality.

NSDMI - Non-static data member initialisation in LLParser.h inside struct ArgInfo

use of default
This makes the compiler generate the default implementations for explicitly defaulted functions, which are more efficient than manually programmed function implementations.

in StratifiedSets.h

constexp in SmallVector.h

Class hierarchy


OOP concepts
Multiple inheritance in ilist.h
A child/subclass can inherit from more than one class
SmallVector.h - concept of friend class and single inheritance
Use of copy constructors
Direct initialization (C++11 feature) variables inside structure





ADTs
APFloat
ArrayRef
SmallPtrSet
StringRef




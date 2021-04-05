# LLVM
LLVM

LLVM consists of front-end known as clang and uses IR (Intermediate Representation)
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




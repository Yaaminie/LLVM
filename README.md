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
* Use of unique_ptr <br>
  std::unique_ptr: The destructors of this class release memory for the underlying object when the pointer goes out of scope. Through move semantics, it is ensured that only one   pointer can bind to the object at a time. <br>
* In C++11, auto_ptr has been deprecated and the following smart pointers added.
* Even nullptr is new feature add in version c++11
  nullptr keyword in place of NULL <br>
* Use of range based for loops and auto keyword <br>
* use of templates <br>
* use of auto keyword instead of any particular data type. <br>
* use of static_assert to test assertions at compile-time <br> 
* use of =default and =delete <br>
* use of constexpr <br>
* use of Variadic template <br>
* use of override ensures virtual function declared in a derived class has the same function signature as that of the base class.<br>
* NSDMI - Non-static data member initialisation inside struct <br> 
  Any non-static member of the class or a struct is initialized directly in its declaration, and not via a constructor. <br>
  
## Class hierarchy
* One of the core header files in LLVM is Type.h header file inside IR directory and subclasses are     in DerivedTyes.h <br>
  6 subclasses inherits from same base class Type so it is Hierarchical Inheritance <br>
  Superclass: Type <br>
  Subclasses: All the subclasses inherit only from class Type so Single Inheritance <br>
    - IntegerType 
    - FunctionType 
    - StructType
    - ArrayType
    - VectorType
        - FixedVectorType derived from VectorType (so VectorType is Superclass/Base class and                   FixedVectorType is Derived/subclass of VectorType). Multilevel Inheritance.
        - ScalableVectorType is also a subclass of VectorType. Multilevel Inheritance.
    - PointerType
 * Superclass: StringRef <br>
   Subclass: StringLiteral <br>
   Single Inheritence
     

## OOP design decisions for LLVM

OOP concepts
Multiple inheritance in ilist.h
A child/subclass can inherit from more than one class
SmallVector.h - concept of friend class and single inheritance
Use of copy constructors
Direct initialization (C++11 feature) variables inside structure



## Design Patterns
* Language independence<br>
* Lot of optimization: Multiple-stages of analysis & transformations (optimization is possible with the help of IR)
* Modularity (Code divided into many source code files, header files and different folders)
* inline keyword <br>
  If a function is inline, the compiler places a copy of the code of that function at each point where the function is called at compile time.
  Any change to an inline function could require all clients of the function to be recompiled because compiler would need to replace all the code once again otherwise it will     continue with old functionality. <br>
* Use of templates
* Polymorphism
* Use of containers like map,vector,etc.
* Use of enums
* Use of classes that only define interface of member functions and definition is provided in another class


## Usage of iterators and their own data structures
ADTs
APFloat
ArrayRef
SmallPtrSet
StringRef

Iterators
Use of iterator
const_iterator and const_reverse_iterator. (SmallVector.h) <br> 
rbegin(),rend(), begin(), end() and size()   (SmallVector.h) <br>
input_iterator_tag and iterator_traits <br>
move_iterator <br>
Use of operator== and operator!= (Value.h)
Use of reverse_iterator (Type.h)
Iterators to iterate through the array(ADT- ArrayRef) containing pointers of a particular class.
forward_iterator_tag (Value.h)



# JVM, JDK, JRE Basics

## What is JVM?
JVM (Java Virtual Machine) runs Java bytecode.  
It makes Java platform-independent by executing `.class` files on any OS.

## What is JRE?
JRE (Java Runtime Environment) provides libraries + JVM to run Java programs.  
It does NOT contain development tools.

## What is JDK?
JDK (Java Development Kit) = JRE + compiler + tools.  
Used for writing, compiling, and running programs.

## Bytecode & WORA
When we compile Java, source `.java` → `.class` bytecode.  
Bytecode runs anywhere JVM exists.  
This gives Java its property *Write Once, Run Anywhere*.

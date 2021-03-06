# Translator 15.01.2016

This course work on the courses:
- Basic programming.
- C++ and STL library.
- Fundamentals of Object-Oriented Programming.

## The basic idea and motivation

The project was conceived as a serious practical work for the excercises of the previous topics.

#### 1. Procedural programming
 * Variables. 
 * Conditional constructions. 
 * Cycles. 
 * Arrays. 
 * Functions. 
 * IO base operations.
 
#### 2. Structured programming
 - The structures.
 - Complex chains of functions calls.
 - Pointers arithmetic.
 - Exceptions and their handling.
 - File Input-Output.
 
#### 3. Standard tempates library - STL
 - String class and working algorithms with it.
 - Vector as a dynamic array.
 - Associative containers - Map and Set.
 - Base algorithms for work with containers.
 
#### 4. The Object-Oriented Programming and the Object-Oriented Design
 - Base OOP concepts.
 - Data abstraction.
 - Encapsulation.
 - Inheritance and composition as alternative.
 - Polymorphism and its types.
 - Object-Oriented Design and UML class diagrams.

## Architecture and layers
[Common architecture structure.](https://github.com/TankaMelnyk/C_plus_plus_Translator_Course_Work/blob/master/Classes_diag.png)

The project is presented as a set of three layers:
* [Presentation Layer.](https://github.com/TankaMelnyk/C_plus_plus_Translator_Course_Work/blob/master/ui_layer.png)
* [Business Logic.](https://github.com/TankaMelnyk/C_plus_plus_Translator_Course_Work/blob/master/bl_layer.png)
* [Data Layer.](https://github.com/TankaMelnyk/C_plus_plus_Translator_Course_Work/blob/master/dl_layer.png)

## Application key points
- The root of the application is the Application class which encapsulates one Wrapper of each layer.
- Each layer is isolated from each other and only knows about the "bridge" from the layer below.
- The Data Layer is represented by a simple Accessor and text dictionary file in the operating system.
- The BL layer contains the basic algorithms for translating words and sentences, they adding, view and change the dictionary and settings.
- Facade in BL layer is presented by TranslationManager.
- UI layer is presented in the form of State Machine which switches the pre-prepared screens.
- The screens and transitions between them are described in the factory-methods of UI factory.
- Each screen is represented by an independent content, custom actions and transitions to other screens.

##  The build process
The assembly process is simple - just open the file **Translator.vcxproj** by VisualStudio with support for standard C++11 and compile it.

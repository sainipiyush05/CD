# Mini Compiler Implementation using Switch-Case in C++

## 📌 Overview
This project demonstrates the **Six Phases of a Compiler** using a `switch-case` example in C++.  

The program simulates how a compiler processes source code step-by-step from:
- Lexical Analysis
- Syntax Analysis
- Semantic Analysis
- Intermediate Code Generation
- Code Optimization
- Target Code Generation

Finally, the program executes the source code and displays the output.

---

# 🚀 Compiler Phases Implemented

1. Source Program  
2. Lexical Analysis  
3. Syntax Analysis  
4. Semantic Analysis  
5. Intermediate Code Generation  
6. Code Optimization  
7. Target Code Generation  
8. Final Execution Output  

---

# 📖 Source Program

```cpp
#include <stdio.h>

int main() {

   int choice = 2;

   switch(choice) {

       case 1:
           printf("Option 1 selected\n");
           break;

       case 2:
           printf("Option 2 selected\n");
           break;

       case 3:
           printf("Option 3 selected\n");
           break;

       default:
           printf("Invalid choice\n");
   }

   return 0;
}
🔹 1. Lexical Analysis
📌 Purpose

Lexical Analysis scans the source code and converts it into tokens.

✅ Tasks Performed
Identifies keywords
Detects identifiers
Recognizes operators
Detects constants
Identifies functions
🔍 Example Tokens
Token	Type
switch	Keyword
choice	Identifier
2	Constant
==	Operator
printf	Function
📤 Output

The output generated is called a Token Stream.

🔹 2. Syntax Analysis
📌 Purpose

Syntax Analysis validates whether the program follows proper grammar rules.

✅ Tasks Performed
Checks switch-case syntax
Validates statement structure
Generates Parse Tree
🌳 Parse Tree
switch_stmt
|
+-- switch
|
+-- expression
|    |
|    +-- choice
|
+-- case_list
     |
     +-- case 1
     |    |
     |    +-- printf("Option 1 selected")
     |    +-- break
     |
     +-- case 2
     |    |
     |    +-- printf("Option 2 selected")
     |    +-- break
     |
     +-- case 3
     |    |
     |    +-- printf("Option 3 selected")
     |    +-- break
     |
     +-- default
          |
          +-- printf("Invalid choice")
📤 Output

The output of this phase is a Parse Tree.

🔹 3. Semantic Analysis
📌 Purpose

Semantic Analysis checks the meaning and logical correctness of the program.

✅ Tasks Performed
Type checking
Case compatibility checking
Function validation
Semantic rule verification
📋 Semantic Information
Identifier	Type
choice	int
printf	function
✅ Semantic Checks
choice is integer type
Case labels match switch type
printf() is valid
Return statement is valid
📤 Output

The output is an Annotated Syntax Tree / Semantic Information.

🔹 4. Intermediate Code Generation
📌 Purpose

This phase converts source code into machine-independent intermediate code.

⚡ Three Address Code (TAC)
t1 = choice == 1
if t1 goto L1

t2 = choice == 2
if t2 goto L2

t3 = choice == 3
if t3 goto L3

goto L4

L1: print Option1
L2: print Option2
L3: print Option3
L4: print Invalid
📤 Output

Intermediate Code Representation

🔹 5. Code Optimization
📌 Purpose

Optimization improves efficiency by reducing unnecessary operations.

✅ Optimization Techniques
Dead code elimination
Jump reduction
Constant handling
⚡ Optimized Code
if(choice==1) goto L1
if(choice==2) goto L2
if(choice==3) goto L3
goto L4
📤 Output

Optimized Intermediate Code

🔹 6. Target Code Generation
📌 Purpose

This phase converts intermediate code into assembly-level instructions.

⚙️ Generated Assembly Code
MOV R1, choice
CMP R1, 1
JE L1

CMP R1, 2
JE L2

CMP R1, 3
JE L3

JMP L4

L1: PRINT Option1
L2: PRINT Option2
L3: PRINT Option3
L4: PRINT Invalid
📤 Output

Assembly / Machine Code

🔹 7. Final Execution Output

For:

choice = 2
✅ Program Output
Option 2 selected
✨ Features
Demonstrates all compiler phases
Dynamic user input
Parse tree generation
Token classification
Intermediate code generation
Assembly-style target code generation
Educational compiler simulation
🛠️ Technologies Used
C++
Standard Template Library (STL)
Console-based implementation
🎯 Learning Outcomes

This project helps understand:

Tokenization
Parsing
Syntax validation
Semantic checking
TAC generation
Optimization
Target code generation
✅ Conclusion

This project demonstrates the working of a compiler using a switch-case example in C++. It shows how source code is transformed step-by-step through different compiler phases until the final executable output is generated.

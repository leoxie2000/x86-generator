# X-86 generator (Yi Xie, 06/03/2022)

## Design

The design of this generator functions is by adding the operands from the llvm instructions into the X-86 registers accordingly. 

As a general rule, we make x-86 immediate register for all the llvm constants, and otherwise get the source via a query slot operation.  

In addition, the functions headers are added to the x86.hpp file and the codegen.cpp's case switch function calls.

## Using the code

For this code, simply use `make` to compile, and then use `./full_pipeline.sh [filename.ll]`  to run the script on targeted ll file for the full output as well as the assembly.
# Instruction Format and Addressing Modes

Every Instructions contain two fields `Opcode` & `Operand`

    ┌──────────┬─────────┐
    │  Opcode  │ Operand │
    └──────────┴─────────┘

## Opcode
- It's a mandatory field in every Instruction
- It's decscription about what the given Instruction will do
- Usually Opcodes are written in terms of Mnemonics

## Operand
- It's an optional field 
- It tells about the data
- It may contain Source and Destination address

## Types of Instructions

1. Zero address instruction
   - HLT, NOP, START. END

2. One address instruction
   - INC A

3. Two address instruction
   - ADD A, B

4. Three address instruction
   - ADD A, B, C

## Addressing Modes

- This describes how we can access the data.
- This plays an important toel whihe writing the assembly programming

## Types of Addressing Modes

1. **Immediate Addressing Mode**
    - In this the data is avail in the instruction itself 
    - We use this when we want to store the data from the outside world to computer
    - Eg, MOV A, 12H

2. **Register Addressing Mode**
    - In this the data is present in the register
    - whenever we want to transfer the data form a register to another we use this mode
    - This is the fastest addressing mode
    - Eg, MOV R2, R1

3. **Direct Addressing Mode**
    - Here the data is present in the memory location
    - Whenever we want to access the data present in the memory location we use this mode

4. **Register In-Direct Addressing Mode**
    - If the data is present in a memory location whose address is specified in a register then we use this mode

# Instruction set
## Data Transfer Instruction
   - Move / Copy instruction
     - MOV A, B
     - MOV A, $[01_H]$
   - In instruction 
     - IN A, $[77_H]$
   - Push, Pop
     - When we want tranfer data between CPU and Stack
   - Swapping
     - XCHG A. G
## Arthematic Instruction
- ADD, SUB, ADC(Add with carry), SBC(Subtract with Borrow), MUL, DIV, INC, DEC, CMP, etc

## Logical Instruction
- AND, OR, XOR, NEG(1'S Complement), CMA(2'S Complement)

## Shift Rotate Instruction
- SHR - Shift Right (Value Decreases)
- SHL - Shift Left (Value Increases)
- ASHR - Arthematic Shift Right
- ASHl - Arthematic Shift Left

## Machine Control Instruction
- HLT, NOP, START, END
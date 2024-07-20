# I. Fundamentals of Digital Computer

- A Computer is a by the user, a digital gadjel which performs a task computer never thinks by itself. given

## Computer Architechture (CA):

- It describe the structural information of a computer

## Computer Organisation (CO):

- It describes the hireachy of a given computer system

<br>
Fun Fact:

- Group of 4 bits is called Nibble
- Group of 8 bits is called Byte
- Group of 16 bits is called Word
- Group of 32 bits is called Double Word

## Basic Funtional Block Diagram of a Digital Computer

```
                 ┌──────────┐
                 │  Memory  │
                 └──────────┘
                      ↑
                      │    
                      ↓    
                 ┌─────────┐
┌───────┐        │         │       ┌────────┐
│       │        │         │       │        │
│ Input │------> │   CPU   │------>│ Output │
│       │        │         │       │        │
└───────┘        │         │       └────────┘
                 └─────────┘
```

### Input device

- A device through which computer can access the data is called this.

- This also performs the following operations

    - Analog to Digital (Machine understandable language)

    - Serial data to Parallel data

**Eg**: Keyboard (Highest Priority), Mouse, Microphone, Joystick, etc

### Output Device

- A device through which computer can send the data to the outside world

- This also performs the following operations

    - Digital to Analog
    - Parallel data to Serial data

**Eg**: Monitor, Printer, Projector, Spekears, etc

**Fun Fact**: There are some IO Devices which can act as input and output such as Fax, Touch Screen, Pendrive

### CPU

- CPU stands for Central Processing Unit

- Important & crucial component of a computer

- CPU contains CU (control Unit), ALU (Asthematic Logical Unit), On chip memory, etc

- Control Unit generate some control signals to perform a task

- ALU performs Arthematic & Logical operations

- CPU has control over system bus (Address bus, Data bus, Contron bus)

### Memory

- Memory capacity Can be represented as 2^n * m

where,

n = width of bus (or) number of address bits

m = No.of bits in each memory locations

2^n = Total number of memory locations

### Q1. If n = 8, what is the highest memory location address for given memory

- [ ] 1. 0d255
- [ ] 2. 0b11111111
- [ ] 3. 0XFF
- [X] 4. All of the above

### Q2. For 1KB memory the range is

- [ ] 1. 0-FF
- [ ] 2. 0-1F
- [X] 3. 0-3FF
- [ ] 4. 0-FFF

### Q3. Calculate the value of N in 256KB memory

- [ ] 1. 8
- [ ] 2. 16
- [X] 3. 18
- [ ] 4. 32

## Types of communications

### 1. Simplex
- In this type of communication it's only one way communication. For eg: The communication between mouse and CPU
### 2. Half Duplex
- In this type of communication it's only one way communication at a time. For eg: The communication between Walkie-Talkie'es
### 3. Full Duplex
- In this type of communication multi-way communcation. For eg: The communication between router and cell phones

### Types of Lanuages

1) Low Level Language
2) Medium Level aka Assembly level Language
3) High Level Language

Note:
- Assembler converts assembly to .exe or .obj (machine understandable format)

- Compilers & Interpreters are used to convert high level language code into machine understandable language

## System bus
It is a combination of address bus, data bus & control bus

### Address buS
- It Cordaine the memory loc add where the data is present 
- It's uni-directional bus i.e. CPU -> memory or CPU -> IO

Note:
- If Address bus width is more then the memory capacity will be more.

### Data bus
- It contains the data which is going to be stored
- It's bi-directional bus ie. CPU <--> memory or CPU <--> IO

Note:
- If Data bas width is more then speed of the execution becomes better

### Control bus
- It contains the signal which operation is going to be happen.
- Mostly CPU generates some Control signals to perform a specific task
- It's bi-directional bus ie. CPU <--> memory or CPU <--> IO
Eg for some Control Signals:

MEMW, MEME, IOR, IOW, CS, RST, etc

## Simple Accumulator Based CPU

### PC (Program Counter)
- It contains the address of the next instruction to be executed

### IR (Instruction Register)
- It contains the instruction which is currently executing

### MDR (Memay Data Register)
- It contains the data schich is stored in the memory / fetched the memory

### MAR (Memory Address Register)
- It contains the mem loc add where the data is stored / fetched

### On-Chip Memory

- It stores the frequently used data by the CPU

- It's accessing speed a very high

- They are manfacutured by semi-conductors

- It's very expensive

- They are very limited

## Instruction Cycle:

### Instruction fetch:
- In this phase the instruction will be fetched into the CPU

### Instruction Decode:
- In this phase the instruction will be decoded into machine understandable format

### Instruction Execution:
- In this phase the specified task will be performed

## Stored Program Concept:


| Architecture        | Von Neumann    | Harvard          |
|---------------------|----------------|------------------|
| **Type**            | Oldest         | Modern           |
| **Complexity**      | Simple         | Complex          |
| **Cost**            | Economical     | Expensive        |
| **Memory**          | Common Memory  | Dedicated Memory |
| **Number of Buses** | Single Bus     | Two Buses        |
| **Speed**           | Good Speed     | High Speed       |

- When CPU uses a single bus to interact with the memory which stores both programs and data, this whole concept is called **Stored Program Concept**.

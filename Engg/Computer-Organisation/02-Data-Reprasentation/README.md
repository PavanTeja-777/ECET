# II. Data Representation
```
DATA
 |-Numerial
 |  |- Mganitude Representation
 |  |   |- Unsigned Mganitude Representation
 |  |   |- Signed Mganitude Representation
 |  |- Complement Representation
 |      |- 1's Complement
 |      |- 2's Complement
 |-Alpha Numerical
    |-ASCII - American Standarad Code for Information Interchange
    |-EBCDIC - Extended Binary Coded Decimal Interchange Code
```
## Unsigned Magnitude Representation

- It's Similar to BCD (Binary Coded Decimal)                                   
Eg:
  - 9 ->  1001
  - 12 -> 1100
  - 13 -> 001101 in 6-bit representation

### Dis Advantages
- Using this we cant represent negative numbers.

### Q. For n bits, the maximum value can be representaded using Unsigned MR is 

- [ ] 1. 2^n
- [X] 2. (2^n) - 1
- [ ] 3. 2^(n - 1)

## Signed Magnitude Representation
- It's same as Unsigned MR but the MSB is used as **Sign bit**.
- If the number is positive then MSB is 0 or else 0.

Eg:
  - -12 -> 1 1100
  - 27  -> 01 1011
  - represnting -7 in 6-bits -> 10 0111

In every example we can see that the except the MSB(The starting bit) the representation is same

### Dis Advantage
Zero has two unique representations 

- +0 -> 0 0000
- -0 -> 1 0000

The range in Singed MR for n bits is, **2^(n-1) - 1 to 2^(n-1) - 1**

## Complemt Representation
- Every number system has 2 complements r-1's and r's complement

| Number System | Binary| Octal | Decimal | Hexadecimal |
|---------------|-------|-------|---------|-------------|
| **r-1**       | 1     | 3     | 9       | 15 / F      |
| **r**         | 2     | 4     | 10      | 16          |

## 1's Complement

For Finding 1's Complement of a number, subtract the given number from its highest digit number

Eg:
- 0110 0011
  1. Find its highest digit number 1111 1111
  2. Subtract the given number
```    
   1111 1111
 - 0110 0011
 -------------
   1001 1100
```
Therefore 01100 0011 1's Complement is 1001 1100
#### Fun Fact:
- Just Change 0 to 1 and vice-versa

### Representation of Postive numbers
- It's same as Signed MR.

Eg:
- 10 -> 0 1010
- 16 -> 01 0000

### Representation of Negative numbers
Step 1: Find the magnitude's signed MR.  
Step 2: Apply 1's Complement.

Eg:
- -10
  1. Magnitude's Signed MR - 0 1100
  2. Apply 1's Complement  - 1 0011
  
  Therefore -10 in 1's Complement Representation is 1 0011

- Represent -16 in 8-bit
  1. Magnitude's Signed MR - 0001 0000
  2. Apply 1's Complement  - 1110 1111
  
  Therefore -10 in 1's Complement Representation is 1 0011

### Dis Advantage
Zero has two unique representations 

- +0 -> 0 0000
- -0 -> 1 1111

The range for n bits is, **2^(n-1) - 1 to 2^(n-1) - 1**

## 2's Complement

For Finding 2's Complement of a number, subtract the given number from its highest digit number and add 1

Eg:
- 0110 0011
  1. Find its highest digit number 1111 1111
  2. Subtract the given number from step1 then add 1.
```    
   1111 1111
 - 0110 0011
 -------------
   1001 1100
 +         1
 -------------
   1001 1101
```

Therefore 01100 0011 2's Complement is 1001 1101
#### Fun Fact:
- Write from left as it is after writing the first 1. Do 1's Complement

### Representation of Postive numbers
- It's same as Signed MR.

Eg:
- 10 -> 0 1010
- 16 -> 01 0000

### Representation of Negative numbers
Step 1: Find the magnitude's signed MR.  
Step 2: Apply 2's Complement.

Eg:
- -10
  1. Magnitude's Signed MR - 0 1100
  2. Apply 2's Complement  - 1 0100
  
  Therefore -10 in 1's Complement Representation is 1 0100

- Represent -16 in 8-bit
  1. Magnitude's Signed MR - 0001 0000
  2. Apply 1's Complement  - 1111 0000
  
  Therefore -10 in 1's Complement Representation is 1 0011

The range for n bits is, **2^(n-1) to 2^(n-1) - 1**

| Decimal |  SMR  |  1's  |  2's  |
|---------|-------|-------|-------|
|    8    | -     | -     | -     |
|    7    | 0111  | 0111  | 0111  |
|    6    | 0110  | 0110  | 0110  |
|    5    | 0101  | 0101  | 0101  |
|    4    | 0100  | 0100  | 0100  |
|    3    | 0011  | 0011  | 0011  |
|    2    | 0010  | 0010  | 0010  |
|    1    | 0001  | 0001  | 0001  |
|    0    | 0000  | 0000  | 0000  |
|   -0    | 1000  | 1111  | 0000  |
|   -1    | 1001  | 1110  | 1111  |
|   -2    | 1010  | 1101  | 1110  |
|   -3    | 1011  | 1100  | 1101  |
|   -4    | 1100  | 1011  | 1100  |
|   -5    | 1101  | 1010  | 1011  |
|   -6    | 1110  | 1001  | 1010  |
|   -7    | 1111  | 1000  | 1001  |
|   -8    |   -   |   -   | 1000  |

## [Floating Point and Fixed Point Representation >>](floating.md)
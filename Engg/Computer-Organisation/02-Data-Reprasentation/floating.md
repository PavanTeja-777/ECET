# Floating Point Representation (FPR)

- This can be expressed as follows

    F = smr^e

where,
  - s = sign
  - m = mantissa
  - r = radix
  - e = exponent

- In Floating Point Representation the decimal point is dynamic i.e. it doesn't have any significance

Eg:
-37.51 can be expressed in many ways follows:
- -375.1 * 10
- -3.751 * 10^-2

Types of FPR

## 1) IEEE 754 with Single Precesion aka Binary-32 Representation
```
  ┌───┬─────┬─────┐
  │ S │  E  │  M  │
  └───┴─────┴─────┘
    1    8     23
```
- In this the numbers are represented in 32 bits.
- The 32 are bits are for
    - 1 bit for Sign bit
    - 8 bits for Exponent
    - 23 bits for Mantissa

Steps for representing a number in Bin-32 Rep.
1. Assign Sign bit 1 if negative number or 0
2. Convert the given Number into Binary format (Magnitude Only).
3. Do Normalization
4. Calculate BE(Baised Exponent) which equals to E(Exponent) + 127 and convert it into Binary


**Eg 1:** 25.125

1) Sign bit (S) = 0
2) 0d25.125 >>  0b110011.001
3) 110011.001 >> 1.11011001 * 2^4 (Here we are pushing the deciaml to right and multiplying with 2 power of bits moved)
4) BE = E+127 here E is the no.of bits moved i.e. 4 >> 4+127 = 131, which can be converted into binary 0b10000011

Now make them in SEM order
```
  ┌───┬──────────┬─────────────────────────┐
  │ 0 │ 10000011 │ 11011001000000000000000 │
  └───┴──────────┴─────────────────────────┘
    S      E                M  
```
which can be also written as: **0b01000001111011001000000000000000** or **0x41C90000**

**Eg 2:** -131.3456

1) S = 1
2) 0d131.3456 >>  0b10000011.01011
3) 10000011.01011 >> 1.000001101011 * 2^7
4) BE = 7 + 127 >> 134 >> 10000110

Now make them in SEM order
```
  ┌───┬──────────┬─────────────────────────┐
  │ 0 │ 10000110 │ 00000110101100000000000 │
  └───┴──────────┴─────────────────────────┘
    S      E                M  
```
which can be also written as: **0b11000011000000110101100000000000** or **0xC3035800**

## 2) IEEE 754 with Double Precesion aka Binary-64 Representation
```
  ┌───┬─────┬─────┐
  │ S │  E  │  M  │
  └───┴─────┴─────┘
    1   11    52
```
- In this the numbers are represented in 64 bits.
- The 64 are bits are for
    - 1 bit for Sign bit
    - 11 bits for Exponent
    - 52 bits for Mantissa

Steps for representing a number in Bin-64 Rep.
1. Assign Sign bit 1 if negative number or 0
2. Convert the given Number into Binary format
3. Do Normalization
4. Calculate BE(Baised Exponent) which equals to E(Exponent) + 1023


### NOTE: 
- Mantissa should be less than 1
- While writng M take only the part after the deciaml
- If the mantissa is less than req bits then add 0 until the mantissa becomes 23 bits, the bits added are called **Guard Bits**
- If the part after the decimal is reapting then repeat them with their periodicity until req bits are achived

**Eg:** -47.625

1) S = 1
2) 0d47.625 >>  0b101111.101
3) 101111.101 >> 1.01111101 * 2^5
4) BE = 5 + 1023 >> 1028 >> 10000000100

Now make them in SEM order
```
  ┌───┬─────────────┬──────────────────────────────────────────────────────┐
  │ 1 │ 10000000100 │ 0111110100000000000000000000000000000000000000000000 │
  └───┴─────────────┴──────────────────────────────────────────────────────┘
    S       E                                     M  
```
which can be also written as: **0b1100000001000111110100000000000000000000000000000000000000000000** or **0xC047D00000000000**

| Representation         | Binary-32 | Binary-64 |
|------------------------|-----------|-----------|
| **No.of bits used**    | 32        | 64        |
| **No.of bits for each**| E-8, M-23 | E-11, M-52|
| **BE**                 | 127+E     | 1023+E    |
| **Accuracy**           | Less      | More      |
| **Memory Usage**       | Less      | More      |
| **Speed**              | Faster    | Slower    |

## [Fixed Point Representation >>](fixed.md)
# Programmed IO
- In this the CPU itself checks each & every IO device wether the given IO device want to communicate with Memory or not.
- This continues checking of the states of the IO device by the CPU is called polling.
- Here the entire operation by a program, hence this technique is called as **Programmed IO** 

## Dis-advantages
- The CPU is un-nessesarily busy by visiting all IO devices.
- The IO device which want to communicate with Memory is un-nessesarily waiting.

## Diagram

![Flow chart](/Engg/Computer-Organisation/05-IO-Organisation/flowcharts/Blank%20diagram.png)

# [Interrupt Initiated IO >>](interrupt.md)
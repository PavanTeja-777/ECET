# IO Organisation

## Introduction
### Input Devices
The devices which sents data from Outside world to CPU
- Eg: Keyboard, Mouse, Scanner, Microphone, Controller, etc..

### Output Devices
The devices which sents data from CPU to Outside World
- Eg: Keyboard, Mouse, Scanner, Microphone, Controller, etc..

### Interfaces
Its a connection medium between CPU to Outside World. Itconverts data to Desirable Format.

### Fun Fact:
- The Comibination of Input and Output Devices is known as **Pheripheral Devices** and **IO Devices**.

# Types Of Transmission
## Single Duplex
- In this the data is passed in one way only.
- The reciver device acts a reciver and the Transmitter device acts as Transmitter Only.
- Eg: Transmission between Radio and Radio Station.

## Half Duplex
- In this the data is passed in one way only at a time.
- The Reciver device acts a Transmitter and the Transmitter device acts as Reciver but not at a time.
- Eg: Transmission between Walkie-Talkie's.

### Full Duplex
- In this the data is passed in two way.
- The Devices can act as Transmitter, Reciver at a time.
- Eg: Transmission in Calling (or) Conferences.

# Types Of Data Transmission
## Synchronous Data Transmission
- Whenever both sopurce and destination operates with the same clock frequency then they said to be in Synchronous Data Transmission.
- This is Full Duplex Transmission.
- The whole data is divided into blocks, each contains some fixed No.of data bits.

        ┌─────────┐                           ┌─────────┐
        │         │                           │         │
        │         ├───┬───┬───┬───┬───┬───┬───┤         │
        │ Sender  │100│110│101│101│101│101│101│ Reciver │
        │         ├───┴───┴───┴───┴───┴───┴───┤         │
        │         │                           │         │
        └─────────┘                           └─────────┘

Eg: Chat rooms, Video Conference, Telephonic conversations.

## Asynchronous Data Transmission
- Whenever both sopurce and destination operates with the different clock frequency then they said to be in Asynchronous Data Transmission.
- This is Half Duplex Transmission.
- The whole data is divided into blocks, each contains data bits, start bit and stop bit.

        ┌─────────┐                             ┌─────────┐
        │         │                             │         │
        │         ├─┬───┬─┐ ┌─┬──────┬─┐ ┌─┬──┬─┤         │
        │ Sender  │1│100│0│ │1│101101│0│ │1│11│0│ Reciver │
        │         ├─┴───┴─┘ └─┴──────┴─┘ └─┴──┴─┤         │
        │         │                             │         │
        └─────────┘                             └─────────┘

Eg: Chat rooms, Video Conference, Telephonic conversations.

|         Data Transmission Type        |    Synchronous   | Asynchronous |
|---------------------------------------|------------------|--------------|
| **Synchronization between Rx and TX** | Perfectly Synced | No Sync      |
| **No.of bits Data**                   | Fixed            | Variable     |
| **Start and stop bits**               | No               | Yes          |
| **Memory Utilization**                | More             | Less         |
| **Speed**                             | Faster           | Slower       |
| **Complexity**                        | Complex          | Simple       |
| **Price**                             | Expensive        | Cheap        |
| **Latency**                           | More             | Less         |

In general there are 3 ways IO Decives Communicate with CPU

# [1. Programmed IO >>](Programmed-IO.md)
# [2. Interrupt Initiated IO >>](interrupt.md)

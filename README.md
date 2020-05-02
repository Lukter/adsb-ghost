# README ADS-B GHOST

The current air traffic infrastructure operate through primary and secondary radar systems.
Among the secondary, one of the most used technologies in civil aviation worldwide is
automatic dependent surveillance — broadcast (ADS–B). This system is capable of sending
information about the aircraft through its broadcasting. In this repository, ADS–B receiver and
transmitter were developed using software-defined radio techniques (SDR), using tools
such as GNU Radio, as well as specific peripherals for SDR applications. An ADS–B
transmitter was developed on the GNU Radio platform, with external code support in
Python. The module was tested using an SDR peripheral called HackRF, an RTL-SDR
dongle, and an open source tool called dump1090. In addition, an ADS–B receiver was
also developed in GNU Radio, tested through integration with the developed transmitter.

This repository has:
* *ADS-B encoder*
* *ADS-B decoder (imported from Mode-S)*
* *ADS-B ghost*
* *CRC calculator*
* *Ghost aircraft*
* *Util package with common functions*


## Requirements

1. python >= 2.7
2. GNU Radio

## Running project

In order to test, there is some options:

### Tx and Rx together
1. To test the entire system in simulation environment, you can set tx grc and rx grc in the same project and connect the blocks.
2. It's possible to use a HackRF + TX to run transmissor in a host and RTLSDR dongle + RX in another hostname. This well you can see real data with noise.

### Tx
1. Use tx project in simulation environment and set a sink block in the end of the system. This way you can see transmited data
2. Use tx project with HackRF to send real data and in another host, use RTL SDR dongle and run dump1090.

### RX

1. Use tx project in simulation environment and set a source block in the end of the system. This way you can see how data is processed.
2. Use rx project with RTL SDR and wait real airplanes send ADS-B packets.


## ADS-B GHOST
This project consists in the implementation of a ghost aircraft, simulating a real one. This aircraft use an ADS-B (Automatic dependent surveillance-broadcast).

### ADS-B encoder features
1. The ADS-B encoder is a WIP (work in progress) package to encode ADS-B frames.
2. This package encode aircraft ID messages and WIP aircraft position.

### ADS-B decoder features
1. The features of this package can be seen at https://github.com/junzis/pyModeS

### ADS-B ghost features
1.  
2.

### CRC calculator features
1. CRC (Cyclic redundancy check) file is used to calculate CRC to frames.

### Ghost aircraft features
1.
2. 

###Util package features
1. This package implements some common functions like hex2bin, bin2int, hex2int, crc, gray2int.

## Notes

### General
1.
2.

### ADS-B encoder
1.
2.

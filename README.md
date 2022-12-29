# linux_goodies
In this repo I drop my (more or less) handy little tools I make in the course of time

## About networks
TCP/IP networks can be a handful.
There's a lot of tools and utilities to handle them. 
Just to apply and further my knowledge about them, I created a couple of tools, at first in bash scripts.

#### Classes 
Networks have ranges of IP addresses, resulting in network sizes. 
An IP (version 4) address consists of four tuples or octets.
Each tuple has 8 bits, so a TCP-IP adress has 32 bits. 
A tuple or octet can span from 0 to 255. In this setup, 0 and 255 are reserved values.

Following are the ranges of Class A, B, and C Internet addresses, each with an example address:

- **Class A** networks use a default subnet mask of 255.0.0.0 and have 0-127 as their first octet. 
The address 10.52.36.11 is a class A address. 
Its first octet is 10, which is between 1 and 126, inclusive.

- **Class B** networks use a default subnet mask of 255.255.0.0 and have 128-191 as their first octet. 
The address 172.16.52.63 is a class B address. 
Its first octet is 172, which is between 128 and 191, inclusive.

- **Class C** networks use a default subnet mask of 255.255.255.0 and have 192-223 as their first octet. 
The address 192.168.123.132 is a class C address. 
Its first octet is 192, which is between 192 and 223, inclusive.

A class C network can be denoted as ***192.x.y.z/24***. 
It is this ***/24*** that is checked for in the `lancheck` script to ensure we have a class C network.
Class A networks are denoted with a ***/8***, class B networks with ***/16***.
These numbers stand for the number if bits that are 'fixed' in the specific network.

## Network utils

#### lancheck
Purpose: scan a class C network for active IP addresses
Range to be scanned can be specified in two numeric parameters.
The first one must be greater than or equal to the second. 
Scan will be performed as follows:
- `lancheck` - this will scan for addresse from 1-254
- `lancheck x` - this will scan only address x
- `lancheck x y` - this will scan addresses from x up to and inclusing y

#### getip
This script will print the computer's IP address in the network.
See for use the `lancheck` script.

#### getnw
This script will print the type of network. This will give the number after the IP address, i.e. '/24' in 'a.b.c.d/24' in a class C network.
See for use the `lancheck` script.

# linux_goodies
In this repo I drop my (more or less) handy little tools I make in the course of time

## Network stuff

### lancheck
Purpose: scan a class C network for active IP addresses
Range to be scanned can be specified in two numeric parameters of which the first one must be greater than or equal to the second. Scan will be performed as follows:
- lancheck
 - this will scan for addresse from 1-254
- lancheck x
 - this will scan only address x
- lancheck x y
 - this will scan addresses from x up to and inclusing y

### getip
This script will print the computer's IP address in the network.

### getnw
This script will print the type of network. This will give the number after the IP address, i.e. '/24' in 'a.b.c.d/24' in a class C network.

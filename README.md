# CS 656 Assignment 2
## name: Jianing Li
#### WatIAM: j2534li
#### Student number: 20899171
This is a project based on University of Waterloo, Computer Network course.
This project contains both the sender, emulator and receiver files.
```
    ─ sender.java
        ─ ACKReceiver.java
    ─ receiver.java   
    ─ network-emulator.py      
```
 ## We should make to build the program firstly
```
 make
```
 ### Running the network_emulator
```
python3 network_emulator.py <emulator receiving UDP port from sender> <receiver hostname> <receiver UDP port> <emulator receiving UDP port> <sender hostname> <sender UDP port> <max delay in ms> <packet discard probability> <verbose-mode>
python3 network_emulator.py 9991 ubuntu2004-004 9994 9993 ubuntu2004-002 9992 0 0.2 1
```
### Running the receiver
```
java receiver <emulator hostname> <emulator receiving UDP port> <receiver UDP port> <output file>
java receiver ubuntu2004-008 9993 9994 file2
```
### Running the sender
```
java sender <emulator hostname> <emulator receiving UDP port from sender> <sender UDP port> <time inteval> <input file>
java sender ubuntu2004-008 9991 9992 100 file1
```
## Editor used in java
The project was coded in Intellij IDEA.
### For the sender
The Server artifacts requires sender.java, ACKReceiver.java and packet.java to build
### For the receiver
The Client artifacts requires receiver.java to build
### For the emulator
The Client artifacts requires network_emulator.py and packet.java to build

Tested on ubuntu1804-002 (sender), ubuntu1804-004 (receiver), ubuntu1804-008 (emulator)

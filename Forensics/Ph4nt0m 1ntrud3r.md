## Ph4nt0m 1ntrud3r
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.

To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!

### SOLUTION 
- i opened the pcap file in wireshark and saw that there were 22 packets and the protocol column only had TCP
- each packet had some base 64 string but when i tried decoding them individually nothing of useful was shown
- in hints it was given
```
1. Filter your packets.
2. Attacks were done in timely manner.
3. Time is essential.
```
- then in the info i found how some were ```TCP Out of Order```
 

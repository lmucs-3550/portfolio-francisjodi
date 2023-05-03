---
description: Screenshots & field notes
---

# Log

#### Step 1: Explore and Record

For the following network environments…

&#x20;   LMU

&#x20;   Private network outside LMU (e.g., home, office)

&#x20;   Public network (coffee shop, shopping area, restaurant)

…and on at least two distinct occasions per environment ("distinct" meaning that you leave/disconnect from that environment at least once between sessions), perform the following explorations:

1. Get your computer's IP address, subnet mask, router, and domain name server(s)

```markup
IP address: 10.27.226.95
Router: 10.27.0.4
Domain name server:  macbook-pro-6
```



2. Examine your computer's full routing table

![](https://lh4.googleusercontent.com/iqpGB8FDcHMZJXMirMrLtpfEWfo0t0QJvHfuHlV5TLQtBfN7xYOB3\_-pekBnODbPr0yQEQYe3v5ex4DpZaIHgwIBagIr01FFi5b2mvVjIvHYgK4tB1\_lFRzfpZfyDwy\_eCXbbuyspO15epczvTXU9F5aawGc0sg6eq7zyzYQipU9pVE-pAbj\_ADrvBYsug)![](https://lh4.googleusercontent.com/SrctuW51roZC3QObqYxY8seHrGqVxbLFhr1nc6Ri9vsCBVWjktMwbsc\_1uHS5H0BV5K2CRaKM2wNEcUZdsBBvNNbRoeqglr8kf3oZG6V08-Y40ktcYq-tASjnhTgYoRcUymWCEy\_i7i6Ro4Kc8iKYV6QUDT1zTnijK-6AvClOvsnu6ur3smS4TkdL140Gw)![](https://lh6.googleusercontent.com/-TUbGq8DM3yHZsU2NTbKQe5Yi4cdSgwcGd3yveQXwrPsXMwXN8flH1M\_Of7ynj9jhFlWn1Ea9f9YIWjHkPEKWl7CMQpHju3Qa6kuWQXVwd\_H7NIPBVrATf90zg1W4bVVgwNq903Z-P1my-KZn9fcE-a\_hUeSY\_QDpN9-SmIyM\_\_9txZCIOwG6H2UqwssFA)



3. Use arp to discover hosts that are on the same network

```markup
? (10.27.0.4) at 0:0:c:9f:f1:56 on en0 ifscope [ethernet]
? (10.27.140.108) at 8e:f9:9d:b3:85:48 on en0 ifscope [ethernet]
? (10.27.150.247) at ee:dc:4e:b2:3c:10 on en0 ifscope [ethernet]
? (10.27.152.140) at 18:3e:ef:d1:af:f3 on en0 ifscope [ethernet]
? (10.27.152.242) at 42:e7:4d:ad:42:d8 on en0 ifscope [ethernet]
? (10.27.178.183) at 3e:7a:fc:fc:78:c9 on en0 ifscope [ethernet]
? (10.27.188.111) at ba:44:bc:59:80:5b on en0 ifscope [ethernet]
? (10.27.191.65) at 1e:77:fe:8f:e8:89 on en0 ifscope [ethernet]
? (10.27.210.251) at 9e:f1:d0:ac:a7:24 on en0 ifscope [ethernet]
? (10.27.223.43) at 5a:5:75:c2:d7:c0 on en0 ifscope [ethernet]
? (10.27.233.52) at 14:7d:da:3d:af:d0 on en0 ifscope [ethernet]
? (224.0.0.251) at 1:0:5e:0:0:fb on en0 ifscope permanent [ethernet]
? (239.255.255.250) at 1:0:5e:7f:ff:fa on en0 ifscope permanent [ethernet]
```



4. Use ping to make contact with:
   * A host you discovered via arp

```
ping 10.27.150.247
PING 10.27.150.247 (10.27.150.247): 56 data bytes
64 bytes from 10.27.150.247: icmp_seq=0 ttl=64 time=59.717 ms
64 bytes from 10.27.150.247: icmp_seq=1 ttl=64 time=81.155 ms
64 bytes from 10.27.150.247: icmp_seq=2 ttl=64 time=103.294 ms
64 bytes from 10.27.150.247: icmp_seq=3 ttl=64 time=21.595 ms
64 bytes from 10.27.150.247: icmp_seq=4 ttl=64 time=41.691 ms
64 bytes from 10.27.150.247: icmp_seq=5 ttl=64 time=476.850 ms
64 bytes from 10.27.150.247: icmp_seq=6 ttl=64 time=456.158 ms
64 bytes from 10.27.150.247: icmp_seq=7 ttl=64 time=304.307 ms
64 bytes from 10.27.150.247: icmp_seq=8 ttl=64 time=24.942 ms
64 bytes from 10.27.150.247: icmp_seq=9 ttl=64 time=45.063 ms
64 bytes from 10.27.150.247: icmp_seq=10 ttl=64 time=66.634 ms
64 bytes from 10.27.150.247: icmp_seq=11 ttl=64 time=89.932 ms
64 bytes from 10.27.150.247: icmp_seq=12 ttl=64 time=733.423 ms
64 bytes from 10.27.150.247: icmp_seq=13 ttl=64 time=334.353 ms
64 bytes from 10.27.150.247: icmp_seq=14 ttl=64 time=153.241 ms
64 bytes from 10.27.150.247: icmp_seq=15 ttl=64 time=342.805 ms
64 bytes from 10.27.150.247: icmp_seq=16 ttl=64 time=719.374 ms
64 bytes from 10.27.150.247: icmp_seq=17 ttl=64 time=239.925 ms
64 bytes from 10.27.150.247: icmp_seq=18 ttl=64 time=30.053 ms
64 bytes from 10.27.150.247: icmp_seq=19 ttl=64 time=53.746 ms
64 bytes from 10.27.150.247: icmp_seq=20 ttl=64 time=75.404 ms
64 bytes from 10.27.150.247: icmp_seq=21 ttl=64 time=96.215 ms
64 bytes from 10.27.150.247: icmp_seq=22 ttl=64 time=30.618 ms
64 bytes from 10.27.150.247: icmp_seq=23 ttl=64 time=39.829 ms


```

&#x20;

* The default router

```
ping 10.27.0.4 
PING 10.27.0.4 (10.27.0.4): 56 data bytes
64 bytes from 10.27.0.4: icmp_seq=0 ttl=255 time=7.185 ms
64 bytes from 10.27.0.4: icmp_seq=1 ttl=255 time=2.963 ms
64 bytes from 10.27.0.4: icmp_seq=2 ttl=255 time=5.835 ms
64 bytes from 10.27.0.4: icmp_seq=3 ttl=255 time=48.900 ms
64 bytes from 10.27.0.4: icmp_seq=4 ttl=255 time=78.055 ms
64 bytes from 10.27.0.4: icmp_seq=5 ttl=255 time=10.326 ms
64 bytes from 10.27.0.4: icmp_seq=6 ttl=255 time=3.985 ms
64 bytes from 10.27.0.4: icmp_seq=7 ttl=255 time=29.965 ms
```

* One of your domain name servers
* [www.lmu.edu](http://www.lmu.edu/)

```
 ping www.lmu.edu
PING lmuedu-lb02-production.terminalfour.net (52.27.135.176): 56 data bytes
Request timeout for icmp_seq 0
Request timeout for icmp_seq 1
Request timeout for icmp_seq 2
```

* A host on the Internet (most likely a website, but for more variety, see if you can find a different kind of public host, such as a game server, mail server, chat server, or cloud storage)

```
ping www.cnn.com         
PING cnn-tls.map.fastly.net (151.101.67.5): 56 data bytes
64 bytes from 151.101.67.5: icmp_seq=0 ttl=56 time=11.909 ms
64 bytes from 151.101.67.5: icmp_seq=1 ttl=56 time=137.681 ms
64 bytes from 151.101.67.5: icmp_seq=2 ttl=56 time=184.125 ms
64 bytes from 151.101.67.5: icmp_seq=3 ttl=56 time=36.933 ms
64 bytes from 151.101.67.5: icmp_seq=4 ttl=56 time=83.960 ms
64 bytes from 151.101.67.5: icmp_seq=5 ttl=56 time=126.709 ms
64 bytes from 151.101.67.5: icmp_seq=6 ttl=56 time=173.762 ms
64 bytes from 151.101.67.5: icmp_seq=7 ttl=56 time=214.358 ms
64 bytes from 151.101.67.5: icmp_seq=8 ttl=56 time=7.942 ms
```



5. Use traceroute to discover the path taken to these same hosts

```
Arp -
 traceroute 10.27.150.247
traceroute to 10.27.150.247 (10.27.150.247), 64 hops max, 52 byte packets
 1  10.27.150.247 (10.27.150.247)  538.166 ms  93.484 ms  424.278 ms
```

```
Default router - 
traceroute to 10.27.0.4 (10.27.0.4), 64 hops max, 52 byte packets
 1  * * *
 2  * * *
 3  10.27.0.5 (10.27.0.5)  7.316 ms *  18.041 ms
```

```

www.lmu.edu
:
traceroute to lmuedu-lb02-production.terminalfour.net (50.112.10.240), 64 hops max, 52 byte packets
 1  10.27.0.5 (10.27.0.5)  10.306 ms  231.996 ms  10.817 ms
 2  10.8.254.153 (10.8.254.153)  7.403 ms  3.471 ms  3.568 ms
 3  10.8.255.1 (10.8.255.1)  6.723 ms  3.684 ms  3.985 ms
 4  157.242.255.19 (157.242.255.19)  8.693 ms  4.539 ms  4.875 ms
 5  157.242.254.82 (157.242.254.82)  8.069 ms  4.187 ms  5.348 ms
 6  dc-riv-agg8--losnettos-100ge.cenic.net (137.164.23.193)  36.033 ms  7.507 ms  8.845 ms
 7  dc-lax-agg10--riv-agg8-300g.cenic.net (137.164.11.86)  14.877 ms  12.214 ms  11.885 ms
 8  99.82.182.178 (99.82.182.178)  15.500 ms
    99.82.179.202 (99.82.179.202)  14.822 ms  15.679 ms
 9  * * *
10  * * *
11  * * *
12  * * *
13  * * *
14  * * *
15  * * *
16  * * *
17  108.166.240.10 (108.166.240.10)  44.630 ms
    108.166.240.9 (108.166.240.9)  43.260 ms
    108.166.232.45 (108.166.232.45)  40.118 ms
18  * 108.166.240.17 (108.166.240.17)  43.871 ms *
19  108.166.240.13 (108.166.240.13)  42.223 ms
    108.166.240.19 (108.166.240.19)  39.680 ms
    108.166.240.27 (108.166.240.27)  39.933 ms
```

```

www.cnn.com
:
traceroute: Warning: www.cnn.com has multiple addresses; using 151.101.67.5
traceroute to cnn-tls.map.fastly.net (151.101.67.5), 64 hops max, 52 byte packets
 1  10.27.0.5 (10.27.0.5)  12.117 ms  7.704 ms  3.713 ms
 2  10.8.254.153 (10.8.254.153)  5.873 ms  3.380 ms  3.830 ms
 3  10.8.255.1 (10.8.255.1)  6.926 ms  3.538 ms  4.276 ms
 4  157.242.255.19 (157.242.255.19)  7.459 ms  14.283 ms  7.057 ms
 5  157.242.254.82 (157.242.254.82)  7.423 ms  3.978 ms  4.043 ms
 6  dc-riv-agg8--losnettos-100ge.cenic.net (137.164.23.193)  11.578 ms  8.289 ms  8.161 ms
 7  dc-lax-agg10--riv-agg8-300g.cenic.net (137.164.11.86)  15.518 ms  12.378 ms  13.072 ms
```

6. For [www.lmu.edu](http://www.lmu.edu/) and the chosen Internet host, use dig to discover their IP addresses

```
www.lmu.edu. 743 IN CNAME lmuedu-lb02-production.terminalfour.net.
lmuedu-lb02-production.terminalfour.net. 12 IN A 50.112.10.240
lmuedu-lb02-production.terminalfour.net. 12 IN A 52.27.135.176
```

```

www.cnn.com. 177 IN CNAME cnn-tls.map.fastly.net.
cnn-tls.map.fastly.net. 11 IN A 151.101.131.5
cnn-tls.map.fastly.net. 11 IN A 151.101.195.5
cnn-tls.map.fastly.net. 11 IN A 151.101.67.5
cnn-tls.map.fastly.net. 11 IN A 151.101.3.5
```

7. Use nmap to see what ports are open on these hosts

```
nmap www.lmu.edu
Starting Nmap 7.93 ( https://nmap.org ) at 2023-01-20 14:07 PST
Nmap scan report for www.lmu.edu (50.112.10.240)
Host is up (0.037s latency).
Other addresses for www.lmu.edu (not scanned): 52.27.135.176
rDNS record for 50.112.10.240: ec2-50-112-10-240.us-west-2.compute.amazonaws.com
Not shown: 993 filtered tcp ports (no-response)
PORT     STATE  SERVICE
53/tcp   open   domain
80/tcp   open   http
135/tcp  closed msrpc
443/tcp  open   https
1080/tcp closed socks
4662/tcp closed edonkey
5000/tcp closed upnp
Nmap done: 1 IP address (1 host up) scanned in 120.03 seconds
```

```
 nmap www.cnn.com
Starting Nmap 7.93 ( https://nmap.org ) at 2023-01-20 14:09 PST
Nmap scan report for www.cnn.com (151.101.195.5)
Host is up (0.0070s latency).
Other addresses for www.cnn.com (not scanned): 151.101.67.5 151.101.131.5 151.101.3.5
Not shown: 995 filtered tcp ports (no-response)
PORT     STATE  SERVICE
53/tcp   open   domain
80/tcp   open   http
443/tcp  open   https
5000/tcp closed upnp
6667/tcp closed irc
Nmap done: 1 IP address (1 host up) scanned in 42.04 second
```



8. Use nmap to see what ports are open on one of the intermediate "stops" discovered by traceroute to any host outside of your network

\


![](https://lh6.googleusercontent.com/bEgv-RR3pXgMV-EcUdFtZORm2zvJVyhJ5-ICTyYs5ZZvXpI0CvwI\_3ivFBbuYvduvlSAZcPyJpXkU6e7z3DExd87btOXLr441LKW-ctULf4nCybkdGYp6dQ2Q6D6Fz94zOj0GoccQwZg\_xGPNfw4iyjHxmd4CVCOSl5ECe-uzeVwHylzx9XQckHLm1Cm0Q)![](https://lh6.googleusercontent.com/IAIqSzkTUFcjW5S8GMJa6LU7OD-\_SX6I25iFB\_7R9qFmpoZ4D7Kw2nC9yWhibKgN8X9N6nywtAsC\_m3zZSjtJA2PXhsikSCoE4DXJXqpFVskO1Uy4jRDRJeDKZUfem2z-gvE9nUXxquP4JZI4evmzhXE3zjUyYKTnPWD9vpZJX5oTfUDGy6AdOxxwd7R6A)![](https://lh3.googleusercontent.com/xYSpeQZ2CyEviIg3kUQdOgVgNit9mCxxcPlkQvWKRYYOFubIK2nz1lpZOqfDT8BIhhXjF9bB\_SYYBvqgPAnZMPr2s0UX9LYcT2Wm\_YQovzA9UCOHnrzG9AQMEf0hseb6sTbvwXvwFQqCCMAsU\_AxOfmVbHu2NFk2ePUV2zxopWSKm945ZCYznHJ0nwH5Tw)









\


### REFERENCES&#x20;

I used google to find nmap installation&#x20;

```
brew nmap install 
```


---
description: >-
  For those who are on the same network (LAN), no port forwarding or ZeroTier
  is needed.
---

# Local setup

### Host machine

1. Open the command prompt on the host machine
2. Enter `ipconfig` (or `ipconfig | FindStr /i ipv4` to find the exact line we're looking for)
3. Note the IPv4 Address, this will be given to other players on the network to connect with
4. The server address that the host machine (and only the host machine) uses is: `127.0.0.1`


### Other players on the network

1. The server address that any other player joining from the same network as the host machine uses is the IPv4 Address from the above "Host machine" steps

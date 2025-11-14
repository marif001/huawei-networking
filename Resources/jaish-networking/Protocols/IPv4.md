A `32-bit` Address, made up of four 8-bit binary octets (each ranging from Decimal 0-255) separated by dots. **Dotted Decimal Format**
$$
192\cdot168\cdot10\cdot1
$$

- First IP Address (`X.X.X.0` is known as the "Network IP" used to identify a network.
- Last IP Address (`X.X.X.255`) is known as the "Broadcast IP" used to send messages to everyone.

**Subnet Mask** is a 32-bit value made up of four 8-bit binary octets where a
- $1$ --> Network Part
- $0$ --> Host Part

This can also be represented using a `/24` where 24 is the number of 1s in the subnet mask.
$$\begin{align}
\text{IP Address} = 192\cdot168\cdot10\cdot0 \\
\text{Subnet Mask} = 255\cdot255\cdot255\cdot0
\end{align}$$
Binary Representation:
$$\begin{align}
IP = 11000000\cdot10101000\cdot00001010\cdot00000000 \\
SM = 11111111\cdot11111111\cdot11111111\cdot00000000
\end{align}$$
Since, there are twenty-four 1s in the subnet mask, we can write it like this:
$$
192\cdot168\cdot10\cdot0 \ /24
$$
## Classful Addressing


| Class | Network-Host Size | Subnet Mask                 | Range     |
| ----- | ----------------- | --------------------------- | --------- |
| A     |                   | $255\cdot0\cdot0\cdot0$     | 0 - 127   |
| B     |                   | $255\cdot255\cdot0\cdot0$   | 128 - 191 |
| C     |                   | $255\cdot255\cdot255\cdot0$ | 192 - 223 |
| D     |                   |                             | 224 - 239 |
| E     |                   |                             | 239 - 255 |
The class is identified by the "First Octet" of an IP address.
## Classless Addressing


---

Class D is for Multicast

Class E is for Research

  

Default Subnet

Class A - 255.0.0.0 /8

Class B - 255.255.0.0 /16

Class C - 255.255.255.0 /24

  

/n is the Network bits

32 - n = h is the Host bits

  

Networks = $2^n$

Hosts = $2^h - 2$

  

Class A - 256n, 16777214h

Class B - 65536n, 65534h

Class C - 16777216n, 254h

  

`127.X.X.X /8` reserved for Loopback.

`169.254.X.X /16` reserves for Link-Local.

## Private IPs

  

Class A: `10.X.X.X`

Class B: `172.16.X.X` to `172.32.X.X`

Class C: `192.168.x.x`

  

## Classful vs Classless

  

Default Subnet Mask -> Classful

~~Default Subnet Mask~~ -> Classless

  

### Assignment of IPs

  

IANA

- ARIN (North America)

- LACNIC (Central and South America)

- AFRINIC (Africa)

- APNIC (Asia and Australia)

- RIPE (Europe, Middle East and Russia)

192-128 = 24 (1)
64-64 = 0 (1)
0-32
0-16
0-8
0-4
0-2
0-1

168-128 = 40 (1)
40-64
40-32 = 8 (1)
8-16
8-8 = 0 (1)
0-4
0-2
0-1

192.168.10.0

$$
11000000\cdot10101000\cdot00001010\cdot00000000
$$

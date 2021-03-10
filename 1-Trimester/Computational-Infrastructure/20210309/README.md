## Open Systems Interconnection (OSI)
- OSI was developed in 1984 by the international Organization for Standardization
- A host or node is a component on the network, like a server, a router, a switch or a firewall.
- OSI consists of a set of seven layers that define the different stages that data must go through to travel from one host to another over the network

TODO GET Image:32 from page 142

- Main benefit from OSI stack is that it allows implementing network components independently of each other. For instace, TCP/IP protocal in layer 4 with the IP protocol in layer 3 is used to send information over the internet. Without changing the IP protocol, an UDP/IP stack can be used as well, by changing the level 4 protocol from TCP to UDP


- Each Layer's payload contains the protocol for the next layer
 TODO GET Image:33 from page 142

Figure 33 shows an Ethernet frame with an IP packet in it, with a TCP segment in it, with a HTTP command in it. The nesting of these protocols allows sending HTTP traffic (like web pages) to another computer using an Ethernet network in a reliable way.

## OSI Physical Layer
The physical layer defines physical hardware components of the network, such as Network Interface Cards (NICs ~ Placa de rede), copper and fiber optic cables, leased lines (private telecommunications circuit between two or more locations provided according to a commercial contract), cable internet, and DSL.

### Cables 
Twisted pair cables
    - consist of paired insulated wires that are twisted around each other to prevent interference. A cable contains multiple wire pairs

Coax cable
    - e consists of an inner conductor surrounded by a flexible, tubular insulating layer, surrounded by a tubular conducting shield
    - Historically, coax cable provided the highest bandwidth possible in copper cabling. It is still heavily used by cable companies, but improvements in UTP and STP cables allow higher bandwidths, eliminating coax cables for most other uses

Fiber optic cable
    - A fiber optic cable contains multiple strands of fiber glass or plastic, that each
provide an optical path for light pulses.
    - Light source LED or laser
    - Max transmission distance depends on: optical power of tramsmitter, wavelenght utilized, quality of the fiber optic cabe and sensitivity of the optical receiver
    - Types of fiber Optic cable : MMF (multi-mode fiber), SMF (single mode fiber)
        - SMF is used for long distance communication (up to 80 km), and MMF is used for distances of 500m or less, typically used in the datacenter or on a campus setup.
        - TODO GET Image?34 e 35 page 145
    -  Using Dense Wavelength-Division
Multiplexing (DWDM) the capacity of fiber optics cables can be extended. By using multiple light sources, each having a distinct color (wave length), multiple channels can travel though the fiber optics cable simultaneously. This way up to 80 channels can be created, leading to a total bandwidth of 800 Gbit/s

### Leased lines


# Modern Ethernet

### 100BaseT

Hubs are only used with 10MB/s or slower

**Half-dulpex** - walkie-talkie: one party talks, then stops; the other party talks thereafter

**Full-duplex** - phone: both parties can talk simultaneously

> In half-duplex, you can either listen or talk: in full-duplex you can both listen and talk

+ 100BaseT4 - 100Mbps, 1024 nodes per hub, 100m, cat 3 cabling, all four pairs - basically gone (obsolete)
+ 100BaseTX - 100Mbps, 1024 nodes per hub, 100m, cat 5e cabling, 2 pairs - now known as 100BaseT
+ 100BaseFX - 100Mbps, 1024 nodes per hub, Multimode, 2km

For exam:
+ Hubs vs Switches
+ Duplex vs half-duplex
+ 3 versions of 100Base Ethernet (a few lines ago, literally)

### Connecting switches

**Patch cables** are used and:
+ *Regular patch cables* - TIA 568A (A on both ends), TIA 568B (B on both ends) aka *straight through cable*
+ *Crossover cable* - TIA 568A on one end, TIA 568B on the other end

In the olden days, switches were connected by connecting a crossover cable into one switch and the other end would be plugged into a different switch

Some switches have an uplink port (it already has the crossover inside of it, so a regular cable can be used)

Modern switches have *auto-sensing ports* to determine if they're connected to a port or another switch and adjust behaviour

### Gigabit Ethernet and 10-Gigabit Ethernet

##### 1Gbps

4 standards:
1. Coaxial side
  + 1000BaseCX - *copper* standard and a coaxial cable called *Twinax*, 25 meters between switch and the individual nodes
1. Fiber-optic side
  + 1000BaseSX - multimode fiber-optic cable, w/ distances of up to 500m
  + 1000BaseLX - single-mode w/ distance up to 5km
1. Unshielded twisted pair (UTP)
  + 1000BaseT - cat 6, 100m

| Nomenclature | Cabling     | Distance | Mode   |
| ------------ | ----------- | -------- | ------ |
| 1000BaseCX   | Twinax      | 25m      | N/A    |
| 1000BaseSX   | Fiber-optic | 500m     | multi  |
| 1000BaseLX   | Fiber-optic | 5km      | single |
| 1000BaseT    | UTP - cat6  | 100m     | N/A    |

##### 10Gbps

  + 10GBaseT - designed to work on cat6 w/ 55m distance or cat6a w/ 100m distance, UTP
  + 10GBaseSR - multimode, 26m - 400m
  + 10GBaseLR - single-mode, 1310nm single-mode fiber, up to 10 km
  + 10GBaseER - single-mode 1550nm, 40km

| Nomenclature | Works with | Mode   | Cabling      | Distance  |
| ------------ | ---------- | ------ | ------------ | --------- |
| 10GBaseT     | Ethernet   | single | cat6(a)      | 55 - 100m |
| 10GBaseSR    | Ethernet   | multi  | optic        | 26 - 400m |
| 10GBaseLR    | Ethernet   | single | 1310nm fiber | 10km      |
| 10GBaseER    | Ethernet   | single | 1550nm fiber | 40km      |
| 10GBaseSW    | SONET      | N/A    | ? || N/A     | 26 - 400m |
| 10GBaseLW    | SONET      | N/A    | ? || N/A     | 10km      |
| 10GBaseEW    | SONET      | N/A    | ? || N/A     | 40km      |

### Tranceivers

**Multisource Agreement (MSA)** - modules for different connectors

Some pluggable module connectors
+ **Gigabit interface converter (GBIC)**
+ **Small form-factor pluggable (SFP)**
+ **Enhanced small form-factor pluggable (SFP+)**
+ **Quad small form-factor pluggable QSFP)**

Half-duplex can use different coloured lasers for sending and receiving data. This is called *bidirectional (bidi)*

### Connecting Ethernet Scenarios

+ Loop issues

Sc: 2 switches connected to another switch. When connecting another one, make sure its connected to the **root switch** (which holds the connection to 2 previous switches). Connecting it to any other would cause a ***bridging loop***

Sol: **Spanning Tree Protocol (STP)** was created to solve this issue. If a bridging loop is detected, the problematic port on the root switch will be shut down, thereby preventing the loop.

+ Flooding hacks

Sol: Smart switches might realize that a flooding (DoS or MitM attack) is happening and shut down the problematic port causing it.

+ Mismatched switch issues

Sc: An old switch is connected to a new switch

Sol: Most modern switches are *auto-sensing*, so they will slow down when communicating with an older switch

+ Dedicated high-speed ports

Sc: 4 switches: 2 regular 100BaseT switches and 2 100BaseT switches with a dedicated 1GIG port

Sol: Connect 2 1GIG ports to each other and use different ports to connect to the other switches: the high-speed ports will act as a backbone

+ Uplink and crossover

Sc: 2 connected switches (with a straight-through cable) with 2 computers connected to each of them. The machines can talk to each other on their own switch, but can't communicate between switches

Sol: Connect the straight-through cable to an uplink port and a regular port or use a crossover cable to connect switches through regular ports

+ Duplex mismatch

Sc: 2 computers are connected with a crossover cable, but cannot communicate

Sol: Change the NIC properties from *auto-negotiate* to *half-duplex*

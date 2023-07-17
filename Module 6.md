# Module 6 : Power Infrastructure

## Power Supply Quality
- Bad quality of power can cause:
  - System lockups
  - Hardware Failure
  - Damage equipment
  - Uncoverable corrupted files
- Sometimes not brand issue, but power quality issue
- UPS does not always take the problem away

## Increasing Power Requirement
- More powerful equipment and smaller system packaging have more power consumption -> Higher power density
- Higher power desity per rack require stronger cooling equipment
- Temperature difference at the front (IN) and in the back (OUT): Delta-T

## Redundancy Options
- Automatic Transfer Switch (ATS) - Mechanical Breaker
  - Choose power between Primary / Secondary Power Source
  - > 50ms
- Static Transfer Switch (STS) - Electrical Breaker
    - < 20ms
- Break Before Make
  - Inputs power are not synchronized
  - Have a small break when re-directed, cover by UPS
 
## Three phase power cabling
- G N L1 L2 L3
- Three phase to single phase conversion is done in Power Distribution Unit / Distribution Board (PDU/DB)

## Three phase & Single phase usage
- UPS System : Three Phase
- ICT equipment : Single Phase
- Imbalance load design of phases may cause power quality issues and potential issues on UPS
- Load imbalance should not exceed more than 10-15%

## Proper Power Cable Routing
- Install all three phases on all rack rows

## Rack Power Distribution - Dual Feed
|  | |  | |  | |  | |  | |  |
R  R S  S T  T R  R S  S T  T
Left = Path A
Right = Path B

## Dual Power Source
- Each power strip in the rack to have its own breaker
- STS for single source equipment

## Common techniques for power availability
- Use dua or tri cord equipment for mission critical servers
- Reduce SPOF
- Separate UPS and non-UPS supply
- User breaker as much as possible as close to the load as possible, avoid share breaker
- Check loading and earth leakage regularly
- Check balance and load before add/removing loads

## Power distribution within the data centre
- Reliable, Scalable, Flexible
- Distribution choice:
  - Location: Overhead / Under raised floor
  - Type:
    - Standard cabling : less flexible, fixed power rating, inexpensive
    - Busbar Trunking (BBT): 1-phase / 3-phase, Flexible Power Rating, Breaker at each tap-off, Expensive

## Cable Distribution MEthod
- Trunking - enclosed
- Trays - lay power cables to PDU or DB within data centre
- Ladders - heavy, large dimension cables
- Baskets - usually for network cables

## Grouding in Data Centre
- Get noise out of the Data Centre
- Ground wire:
  - Establish voltage reference
  - Clear electrical faults
  - Provide RF/ESD discharge path (Signal Reference Grid)
  - Carry Lightning Current
- Electrical earth - protect human
- Clear Earth - protect ICT equipment; dissipate noise. eg. cable tray, raised floor, equipment rack, equipment
- Lightning Earth - to ground lightning
- Ground resistance < 1 Ohm, not to exceed 5 Ohms, lower resistance carry more current
- All metal objects should be bounded to ground.
  - Cabinets
  - PDU
  - Air Conditioner
  - UPS
  - Raised Floor

## Common Mode Noise (CMN)
- Voltage between neutral and ground
- Long Cable Runs, harmonics and imbalance between phases could lead to an increase of CMN
- To Reduce CMN, add in an isolation transformer
  
## Bonding of Neutral & Ground
- Bonding should be as close to the ICT equipment as possbile
  - Require isolation transformer
  - Not too close to avoid EMF
 
## Location of isolation transformer
- Centralized - Good
- PDU - Best

## Isolation Transformer
- Create Galvanic Isolation
  - Filter of power disturbance (limited)
  - Reduction of Common Mode Noise
- Most used K-Factor Transformer : K-13
- 25M distance between bonding point and ICT equipment

## Distribution Boards
- Have to be compliance to EN61439
- EN61439 Section 6.1.1.1
  - Ambient operating -5 to +40 (degree celcius)
  - Average temperature over 24 hours < 35C
  - Form factor 3 is required
  - Relative humidity not exceeding 50% at maximum 40C

## Form Factors
- Form 1 - No separation
- Form 2 - Separation of busbars from other functional unit
- Form 3 - Separation of busbars from all functional units and between all functional components but not their terminals
- Form 4 - Separation of busbars from all functional units and between all functional components including their terminals

## Ingress Protection (IP) grades
- First number : Dust
- Second number : Liquid
- The higher the stronger

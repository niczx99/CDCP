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
  - \> 50ms
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

## Cable Distribution Method
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
- Voltage (difference) between neutral and ground
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

## Power Quality
- Parameters to consider:
  - Voltage: Nominal +/- 10%
  - Frequency: Nominal +/- 1%
  - CMN: < 1% of Phase to Neutral
  - Total Harmonics Distortion of Voltage (THDv): < 8% (non-linear load)
  - Total Harmonics Distortion of Current (THDi): < 12%
- Harmonics
  - Distortion of sine wave
  - Cause heat, resulting in reliability issues
  - Active or passive filters and/or oversize the incoming supply with generator
  - THDi - measured on the input
    - 6 pulse Thyristor Rectifier: 30%
    - 12 pulse Thyristor Rectifier: 12%
    - IGBT based Rectifier: 3-5%
  - THDv - measured on the output
    - Linear load: < 3-5%
    - non linear load: < 5-8%
  - THDi created THDv

## Power: Real versus apparent
- Real power = Watt
- Apparent power = VA
- Power Factor = ratio between real and apparent power
- Watt = Volt * Ampere * Power Factor
- Power Factor = 0 - 1

## Power: Label versus actual consumption
- Rating on ICT-equipment does not reflect the actual power usage
- 20-40% < label power

## Power: Sizing up power usage
6.53

## Power: Data Centre Incoming Power Sizing
6.55

## Power: Generator sets
- Size of generator set depends on
  - kVA/kW of the installation attached
  - Expected inrush currents (spike) on the generators during operations
  - Harmonics returning from the connected installation
- Test regularly
  - Free-running: at least monthly
  - Full Load test: at least quarterly
- Fuel level test and contamination
- Emergency lights

## UPS
- Static
  - Electronic component
  - Need batteries
  - One of the oldest technology
  - 500VA - 1.6MVA
  - Require Cooling
- Dynamic (combine ups and generator)
  - Mechanical component
  - Diesel engine, fly wheel, power generator
  - Heavy
  - 200kVA - 3000kVA
  - Small batteries to start engine
  - Does not require cooling

- Static UPS technology
  - 6.61: Offline/VFD (Voltage and Frequency Dependent), Line interactive/VI (Voltage Independent)
  - True online double conversion/VFI (Voltage and Frequency Independent)

- UPS running mode
  - UPS in normal
  - UPS running on batteries (Utility fail)
  - UPS running on static bypass (UPS fail)
  - UPS running on maintenance bypass (UPS in maintenance, no power)

- UPS installation
  - Parallel of UPS to increase: Availability and Power rating
  - Parallel configuration:
    - Bypass/ Hot-Standby Parallel - old
    - Parallel Redundant - SPOF, not flexible for scaling 
    - Isolated Parallel Redundant - most reliable, easy to scale
  - Centralised battery bank
    - Multiple UPS connect to same battery bank
   
- Dynamic UPS
  - 6.81-6.83

## Batteries
- Flooded Cell
  - High current
  - Long life span (15-20 years)
  - Required maintenance
  - Upright position
  - Electrolyte subject to burn
- Sealed Lead Acid/Valve Regulated Lead Acid (SLA/VRLA)
  - 5 years/10-12 years
  - Ambient temperature (25C)
  - Cheap
  - Low self discharge
  - No memory effect
  - Slow recharging (8hours or more)
  - Must store in charged state
  - Cannot stand high temperature
- Lithium-Ion (Li-ion)
  - Long life-time (10 years)
  - no memory effect
  - allows for fast charging
  - smaller footprint and lighter weight
  - Expensive
  - Prevent unsafe temperature during charging/discharging * risk of fire
- Nickel-Cadmium (Ni-Cd)
  - Long life-time (20 years)
  - No cooling required
  - Reliable/predictable life
  - Fast Charging
  - Have memory effect
  - Need special charger
  - Expensive


## Renewable Energy Factor (REF)
- REF = Eren(Energy from renewable energy source)/Edc(Total annual energy used by the data centre)


## Summary
:OOOOOOO

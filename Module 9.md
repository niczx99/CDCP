# Module 9 : Cooling
## Data Centre Cooling
- Electronic Component Failure
  - Temperature  - 55%   - Air conditioning
  - Vibration    - 20%   - Seismic protection
  - Humidity     - 19%
  - Dust         - 6%    - Clean the blocking vent
- Power consumption
  - IT           - 52%
  - Cooling      - 30%    - look into this factor to save cost
  - Fans         - 8%
  - UPS          - 5%
  - PDU          - 1%
  - Lighting     - 1%
  - Others       - 3%

### Recommended Temperature
ASHRAE (American Society of Heating, Refrigerating and Air-Conditioning Engineers)
TC9.9
- Equipment inlet : 18-27 C (Apply across all the classes A1-A4)  ##Notes
- Air-conditiing system's settings are set to return air temperature
- Delta-T, cold air go in equipment and bring heat out. If Delta-T is abnormal, possible the heat sink is covered, heat not dissipated properly

### Recommended Humidity
ASHRAE recommend 70%
- Too high = corrosion
- Too low = Electrostatic Discharge (ESD)

### Cooling and its impact on reliability
- Military and Telcordia standards:
  - Rule of thumb = every 10 C increase cause 50% reduction in the long term reliability of ICT Hardware
- Most CPU 60-95 C
  - Continuos running at high temperature will limit CPU life time
 
### Future cooling
- radiators
- liquid cooling
- immersion cooling

### Cooling Capacity
- Ton
- BTU
- Horsepower
- Watt

### Sensible/Latent Heat
- Sensible Heat
  - Change in temperature (become hot)
- Latent Heat
  - Change in substance (water -> steam)
ICT equipment is purely Sensible Heat, which it does not create any moisture

## Cooling System
- Comfort air conditioners
  - no humidification
  - de-humidification due to high latent cooling capacity
  - no proper interface for monitoring and control
- Precision air conditioners
  - high sensible heat load capacity
  - energy efficiency
  - can monitor
  - can connect to fire panel

### Basic principle of refrigerant circuit
Air conditioners help to eject hot air from this room (absence of heat), hot air pass through evaporator and contact with the refrigerant
- Evaporator: eject the heat from air-conditioned space
- Compressor: keep refrigerant flow
- Condenser: eject heat to outdoor (typically just a fan)
- Expansion valve: control the quantity of the refrigerant
- Refrigerant: liquid to gas, gas to liquid (eject the heat)
** hot air boils the refrigerant 
Precision air conditioner, condenser inside data centre

### Refrigerant
R410a, R22 phase out as got impact to environment

### Air conditioning
- Air cooled, Self contained
  - Cheap installation, Easy to maintain
  - Heat exhaust pipe, low sensible cooling capacity, high operating cost
- Air cooled, Split System/Direct Expansion(DX)
  - Low purchase cost, easy to maintain and expand
  - Limitation to length of pipe run, operation cost can be high, one CRAC one cooler
- Fluid cooled (Water-Glycol)
  - Longer pipe runs, Multiple CRACs can use same dry cooler, can be more cost effective than DX
  - High purchase cost, Glycol is used to prevent freezing, higher operational cost
- Chilled water
  - Lower cost in long run than DX, water is more efficient than gas, longer pipe runs, share chiller (n+1 for redundancy)
  - High initial cost, typically for large computer room
- Hybrid
  - Water to save cost
  - Change to gas to maintenance chiller

- Chiller Plants
  - Outdoor (air-cooled), indoor (water-cooled)
  - Require redundant for pipe and chillers (Concurent Maintainable, Rated 3)
  - High energy efficient due to hybrid and free cooling
  - Design
    - Pumps
    - Buffer tanks
    - Acoustic
  
### Direct/Indirect Air Handler
  - Direct Air Handler
    - Supply outdoor air directly into the data centre
    - Require Filter for air contamination (quality and humidity)
  - Indirect Air Handler
    - Use cold air from outside to cool down hot air from inside
    - Reduce risk of air contamination

  - Pros
    - Energy efficient
    - Lowest possible Power Usage Effectiveness (PUE)
    - Down sizing of electrical infrastructure 
    - Fast Return on Investment
    - Unit is located outside
  - Cons
    - High water usage (for indirect air handler with adiabatic cooling)
    - Direct air handler might pollute the data centre

### Up Flow / Down Flow
- Up flow
  - Limited air flow guidance (mixture of hot and cold air)
  - Cold air bottom, hot air top
- Down flow
  - Air guided through raise floor
  - Cold air top, hot air bottom

## Raised floor setup
### Placement of equipment
- Classroom
- Hot and Cold Aisle setup
- Hot and Cold Aisle setup with suspended ceiling
- Air conditioning position
  - Perpendicular to hot aisle
    - Fast return of hot air
    - More evenly equalised air pressure
- Higher density equipment at bottom
- Avoid air leakage and short circuit air
  - Blanking panel, grommets

### Temperature and Air Volume
CFM = Cubic Feet per minute
1kW cooling required about 1000/1100 CFM
- Most of the time cooling issues are not caused by temperature / humidity set points on the air conditioners but because of air volume shortage
- Measure airflow and compare to requirement

### Placement of perforated tile and equipment
- Distribute head load in data centre
- Closest rack need to be place 1.8m/6 feet away from air conditioner to avoid negative pressure

### Computer/Server room
- 12-18 meters throw
- VSD
- Too long required placement of air conditioners on both sides

## Non-raised floor cooling
- front-to-rear cooling air flow
- all cabling run over head
- Slab must be treated with proper paint to avoid contamination

### In-row cooling
- Close to heat lead for better efficiencies for air flow
- Less rack per m2

### Overhead duct
- cold air blow from overhead duct to cold aisle (front)
- hot air flow back to overhead duct from hot aisle (back)
- Require well design to ensure enough air volume can be dumped and extracted at the right locations
- Require to inspect and clean regularly

### Wall flow
- Air conditioners mounted in the service corridor and blow air horizontally into the data centre
- Return air is ducted to the service corridor
- Require containment for hot aisle

## Supplemental Cooling
### Floor mount
- Cold air ducting system to increase CFM
  - Neighboring rack could have potential cooling impact
### Hot air fans
- Return hot air quickly back to CRAC
  - assist on hot air removal
### In row cooling
- Close to racks to increase efficiency on airflow
### Rear door heat exchanger
- Pre-cool the hot air so it can be circulated back into the existing room
- Reduce working load of CRAC
- 15kW
### Self-contained racks
- Fully ducted supply and return
- Speciallized racks
- Water, Dielectric, Refrigerant, Gas
- Fire supression considerations
- 18-35 kW

## Liquid immersion cooling
- Submerging computer components in dielectric coolant
- Advantages:
  - Better efficiency
  - 10X heat rejection
  - No noise, no fan
  - Less space 
- Disadvantages:
  - Specific hardware design
  - Leakage / spills
  - Higher initial cost
### Single phase immersion
- Energy is required to pump the coolant
- No state change of coolant
- No vapor to contaminate the environment

### Two phase immersion
- 2x heat rejection compare to one phase
- Heat is removed by liquid-to-gas phase change
- More expensive but can cool equipment with very high heat load 

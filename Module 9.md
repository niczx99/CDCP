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

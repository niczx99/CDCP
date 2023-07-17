# Module 2 : Data Centres Standards

## Data Centre Standards
1. Uptime
  * Power and Cooling
2. **ANSI/TIA-942** - has official accreditation scheme for audit and certification
3. BICSI-002
4. EN-50600, ISO-22237 - Look into redundancy 

## ANSI/TIA-942 - First and currently the only official accredited data centre standard
* Rated - 1 Data Centre; Basic
  * Single path for power and cooling without redundancy
  * Many Single Point of Failure (SPF)
* Rated - 2 Data Centre; Redundant Components
  * Single path for power and cooling with redundancy
  * Redundancy: N+1
* Rated - 3 Data Centre; Concurrently Maintanable - one sub-station with two route / two different sub-station with one group genset, n+1 (not necessary 2n)
  * Dual path for power and cooling of which one is active  **Most rated 3 has active-active (50%-50%)**
  * Allow maintenance or testing on one path without causing interruption to the critical load
* Rated - 4 Data Centre; Fault Tolerant - two different sub-station and separate genset, n+n genset (two different group of genset)
  * Dual active paths for power and cooling (**difference with rated 3 is path switching, rated - 4 have to be automated, rated - 3 can be manual**)
  * Allow for one fault
  * Costy
 
## Standards sub-component
- Electrical
- Earthing
- EMF
- Environmental
- Raised Floors
- Networks; TIA-568A/B (RJ45)
- Fire protection
**Generic standards**

## International Standards vs National Standards
- Local standards > Internation standards
  - Standards, code of practice and guidelines
 
## Summary
- Most standards look after redundancy
- Conflicts on International and Local Standard; International standards is met if Local standards has been met.

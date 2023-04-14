# Revision Message (REV)
## Purpose of the REV Message
The purpose of the REV message is described in section 6.4.1. In a dialogue procedure, the REV message is used to meet these requirements provided that the transfer conditions for the flight are standard and the transferring controller does not require to refer to the flight to the accepting controller for acceptance.

## Message Contents
OLDI-REV-510-M	The contents of the REV message used in the dialogue procedure shall be the same as described for the REV message in the basic procedure.

## Rules of Application
General
OLDI-REV-520-O	One or more REV messages may be sent to the unit to which a flight has been currently co-ordinated by the use of an Activate or RAP message.
OLDI-REV-530-M	REV messages shall be sent under the conditions specified for the REV message in the basic procedure for flights with standard transfer conditions.

## Initiation of Transmission
OLDI-REV-540-M	The REV message shall be transmitted immediately following a detection of a change in the co-ordination data required to be co-ordinated specified for the REV message in the basic procedure.

## Processing in the Receiving Unit
OLDI-REV-550-M	If a corresponding flight plan is found in the co-ordinated state and no discrepancy is found that would inhibit correct processing of the message, the REV message shall be acknowledged.
OLDI-REV-560-M	If a corresponding flight plan is not found in the co-ordinated state or discrepancy is found that would inhibit correct processing of the message, then the acknowledgement shall be inhibited.
OLDI-REV-570-M	The transfer conditions shall be examined to ensure that they are standard.
OLDI-REV-580-M	If the transfer conditions are found to be not standard they shall be presented to the accepting controller.
OLDI-REV-590-M	If the proposed transfer conditions are found to be standard, they shall be included with the flight plan.
OLDI-REV-600-M	If the proposed transfer conditions are found to be standard, the required data shall
be output at operational ATC and other positions as appropriate.
OLDI-REV-610-R	If the transfer conditions in an REV message are found to be non-standard (there is a discrepancy between the filters in the two systems), the fact that the REV is non- standard should be drawn to the attention of supervisory staff in order that the discrepancy be resolved.
 


## Acknowledgement of REV
### Acknowledgement
OLDI-REV-620-M	If the REV message is to be acknowledged, it shall be acknowledged by:
•	a LAM message if the transfer conditions are found to be standard;
•	a SBY message if the transfer conditions are found to be non-standard.
OLDI-REV-630-M	When a LAM has been received, the operational contents of the REV message shall
become operationally binding to both of the ATC units.
OLDI-REV-640-O	Where bilaterally agreed, an ACP may be used in place of a LAM to indicate the acceptance by the accepting unit of a REV containing standard transfer conditions.

### No Acknowledgement Cases
OLDI-REV-650-M	If no acknowledgement is received for a REV message, a warning shall be displayed at the ATC position responsible for the co-ordination of the flights.

### Operational Reply to REV
As the REV message is used to send standard transfer conditions, it will normally be accepted by the system in the accepting unit.
OLDI-REV-660-M	If the transfer conditions are found to be non-standard by the filter in the accepting unit, the message shall be processed as an RRV message.


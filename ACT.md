# Activate Message (ACT)
## Purpose of the ACT Message
The ACT message satisfies the following operational requirements:
-	Replace the verbal boundary estimate by transmitting automatically details of a flight from one ATC unit to the next prior to the transfer of control;
-	Update the basic flight plan data in the receiving ATC unit with the most recent information;
-	Facilitate distribution and display of flight plan data within the receiving ATC unit to the working positions involved;
-	Enable display of correlation in the receiving ATC unit;
-	Provide transfer conditions to the receiving ATC unit.

## Message Contents
OLDI-ACT-10-M	The ACT message shall contain the following items of data:
-	Message Type;
-	Message Number;
-	Aircraft Identification;
-	SSR Mode and Code
-	Departure Aerodrome;
-	Estimate Data;
-	Destination Aerodrome;
-	Number and Type of Aircraft;
-	Type of Flight;
-	Equipment Capability and Status.
Note:	If the SSR code is not assigned or not available, it may be omitted, but only in exceptional cases (e.g. transponder failure) or in cases where it is bilaterally agreed (e.g. Military or VFR flights exempted from SSR code assignment). Depending on the aircraft identification method applied, the SSR code and Mode element (data item A.7) may contain the current SSR code or the SSR code at the transfer of control point.
OLDI-ACT-20-M	If bilaterally agreed, the ACT message shall contain any of the following items of data:
-	Route;
-	Other flight plan data
-	Actual Take-Off Time.
Note:	The Actual Take-Off Time is normally used in the cases where the ACT follows a PAC or CRQ message that included the Estimated Take-Off Time.

## Rules of Application
General
OLDI-ACT-30-M	One ACT message shall be sent for eligible flights crossing the boundary except as provided for in requirement OLDI-ACT-130-M.
OLDI-ACT-40-M	The ACT message shall be generated and transmitted automatically at the calculated time as specified in the LoA, unless manually initiated at an earlier time.
OLDI-ACT-50-R	ATC staff should be provided with a means to trigger the transmission of ACT messages prior to the calculated time of transmission.
OLDI-ACT-60-M	An ACT message shall be generated on the departure of a flight if a PAC or CRQ message, relating to the flight, containing boundary estimate data has previously been transmitted.
Note:	ACT message can also be sent if PAC or CRQ contain ETOT.
OLDI-ACT-70-M	The operational contents of the ACT message due to be transmitted shall be made available at the working position responsible for the co-ordination of the flight prior to the actual transmission.
OLDI-ACT-80-R	In relation to requirement OLDI-ACT-70-M, the time at which it is calculated that the ACT is to be transmitted automatically should be displayed together with its contents.
OLDI-ACT-90-M	The ACT message shall contain the most recent information on the flight, reflecting the expected exit conditions.
OLDI-ACT-100-M	The relevant working position shall be notified of the transmission of the ACT message.
OLDI-ACT-110-M	Acceptance by the receiving unit of the transfer conditions implied in the ACT message shall be assumed, unless the receiving unit initiates co-ordination to amend them.
OLDI-ACT-120-M	The co-ordinated transfer conditions and the fact that the LAM has been received
shall be presented to the ATC staff at the transferring unit.
Note:	As soon as a LAM has been received, the ACT message data becomes operationally binding to both of the ATC units unless the receiving unit initiates co-ordination in accordance with OLDI-ACT-110-M.
OLDI-ACT-130-M	A further ACT message shall only be sent to the same co-ordination partner if the previous one has been abrogated by the use of a MAC.

## Processing in the Receiving Unit
OLDI-ACT-140-M	The ATC system receiving an ACT message shall attempt association with the corresponding flight plan.
OLDI-ACT-150-M	If a corresponding flight plan is found and no discrepancy is present in the message that would inhibit correct processing, the operational content shall be included with the flight plan.
OLDI-ACT-160-M	If a corresponding flight plan is found and no discrepancy is present in the message that would inhibit correct processing, the required data shall be output at operational ATC and other positions as appropriate.
OLDI-ACT-170-M	If a corresponding flight plan is found and no discrepancy is present in the message that would inhibit correct processing, an acknowledgement shall be returned.
OLDI-ACT-180-M	If the corresponding flight plan is found and a discrepancy is found that inhibits correct processing of the message and the sector responsible for accepting control of the flight can be identified, the operational content of the message shall be displayed at the appropriate working position.
OLDI-ACT-190-M	If the corresponding flight plan is found and a discrepancy is found that inhibits correct processing of the message and the sector responsible for accepting control of the flight can be identified, an acknowledgement shall be returned.
Note:	Bi-lateral agreements can determine specific cases where a sector/position cannot be identified for acceptance of control of the flight (and the LAM cannot be returned, in line with section 6.7.1 “Purpose of the LAM”).
OLDI-ACT-200-M	If a corresponding flight plan cannot be found and the sector responsible for accepting control of the flight can be identified, the operational content of the message shall be displayed at the appropriate working position.
OLDI-ACT-210-M	If a corresponding flight plan cannot be found and the sector responsible for accepting control of the flight can be identified, an acknowledgement shall be returned.
 


OLDI-ACT-220-M	If a corresponding flight plan cannot be found and the sector responsible for accepting control of the flight can be identified, a system flight plan shall be created.
OLDI-ACT-230-M	In all other cases, the acknowledgement shall be inhibited.

## Criteria for Message Transmission
OLDI-ACT-240-M The message shall be transmitted at or as soon as possible after the earlier of the times determined from the following:
-	a parameter number of minutes before the estimated time at the COP;
-	the time at which the flight is at a bilaterally agreed distance from the COP.
Note: When a flight is transferred on a direct routing the requirement above will refer to the point determined in accordance with OLDI-DCT-90-M, OLDI- DCT-110-M and OLDI-DCT-120-M.
OLDI-ACT-245-R	Upon a change in the sequence of concerned ATS units, a delay should be applied between the MAC transmission to the unit to which co-ordination had previously been effected for the flight and the initiation of ACT to the new unit.
OLDI-ACT-250-M	The ACT generation parameter(s) shall be included in the LoA between the ATC units concerned.
OLDI-ACT-260-M	The ACT generation parameter(s) shall be variable based on the provisions of the LoA.
OLDI-ACT-270-R	ACT generation parameters should be defined separately for each of the COPs.
OLDI-ACT-280-M	The specified parameters shall allow sufficient time for:
-	the transmitting unit to update the transfer flight level to reflect the expected conditions at the COP; and
-	the receiving unit to process the ACT and generate and transmit a LAM but still allow for verbal co-ordination to be carried out by the transferring unit and resultant action initiated by the accepting unit if the exchange of data fails.

## Acknowledgement of ACT
### Acknowledgement
OLDI-ACT-290-M	The ACT message shall be acknowledged by the generation and transmission of a LAM message.

### No Acknowledgement Cases
OLDI-ACT-300-M	If no LAM message is received as an acknowledgement for an ACT message, a warning shall be displayed at the ATC position responsible for the co-ordination of the flight.

### Change of State to Co-ordinated
OLDI-ACT-310-M	For the purposes of this document, following the transmission of an ACT message, a flight shall be considered to be co-ordinated either after the message has been acknowledged by a LAM or when the completion of co-ordination has been indicated manually at the transferring unit.

Examples
The following examples are an extension of those provided for the ABI message in section 6.2 - Advance Boundary Information Message (ABI); all details are the same except the ETO at the COP, which is 1226 in the ACT message shown.

### ICAO
(ACTE/L005-AMM253/A7012-LMML-ALESO/1226F350-EGBB-8/I-9/2B757/M-15/N0480F390 UT10 ALESO UT420 BUZAD UL10 HON-80/N-81/W/EQ Y/NO R/EQ/O1D1 S/UN-
 


18/DEP/LUQA AIRPORT DEST/BIRMINGHAM OPR/AIR 2000 LTD ALTN/EGLL RALT/EGKK RMK/ONE ENG INOP)

### ADEXP
-TITLE ACT
-REFDATA
-SENDER -FAC E
-RECVR -FAC L
-SEQNUM 005
-ARCID AMM253
-SSRCODE A7012
-ADEP LMML
-COORDATA
-PTID ALESO
-TO 1226
-TFL F350
-ADES EGBB
-ARCTYP B757
-NBARC 2
-WKTRC M
-FLTTYP N
-BEGIN EQCST
-EQPT W/EQ
-EQPT Y/NO
-EQPT R/EQ
-SUREQPT S/UN
-END EQCST
-PBN O1D1
-ROUTE UT10 ALESO UT420 BUZAD UL10 HON
-FLTRUL I
-OPR AIR 2000 LTD
-ALTRNT1 EGLL
-ALTRNT2 EGKK
-RMK ONE ENG INOP
-ATOT 1309
 

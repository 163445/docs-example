# Preliminary Activation Message (PAC)
## Purpose of the PAC Message
The PAC message satisfies the following operational requirements:
•	notification and pre-departure co-ordination of a flight where the time of flight from departure to the COP is less than that which would be required to comply with the agreed time parameters for ACT message transmission;
•	notification and pre-departure co-ordination of a flight by a local (aerodrome /approach control) unit to the next unit that will take control of the flight;
•	provide for acquisition of missing flight plan data in case of discrepancies in the initial distribution of flight plan data;
•	request the assignment of an SSR code from the unit to which the above notification/co-ordination is sent, if required.

## Message Contents
OLDI-PAC-10-M	The PAC message shall contain the following items of data:
•	Message Type;
•	Message Number;
•	Aircraft Identification;
•	SSR Mode and Code;
•	Departure Aerodrome;
•	Estimated Take-Off Time or Estimate Data;
•	Destination Aerodrome;
•	Number and Type of Aircraft.
Note: If the SSR code is not assigned or not available, it may be omitted, but only in exceptional cases (e.g. transponder failure) or in cases where it is bilaterally agreed (e.g. Military or VFR flights exempted from SSR code assignment). Depending on the aircraft identification method applied, the SSR code and Mode element (data item A.7) may contain the current SSR code or the SSR code at the transfer of control point.
OLDI-PAC-20-M	A PAC message sent from a TMA control unit or an ACC shall contain the following items of data:
•	Type of Flight;
•	Equipment Capability and Status;
OLDI-PAC-30-M	If bilaterally agreed, the PAC message shall contain any of the following items of data:
•	Route;
•	Other flight plan data;
•	Message Reference.
OLDI-PAC-40-M	If bilaterally agreed and the data is required to be included for the flight, the PAC message shall contain one or more of the following items of data:
•	Departure Runway;
•	SID Identifier;
•	Cleared Flight level.
 


## Rules of Application
### General
OLDI-PAC-50-M	One or more PAC messages shall be sent for each flight planned to cross the boundary of areas of responsibility where the time from departure to the COP would not permit the ACT message to be sent at the required time.
OLDI-PAC-60-M	One or more PAC messages shall be sent by the Aerodrome/Approach unit to the next unit for each departing flight for which either notification or co-ordination is required.
OLDI-PAC-70-R	For the implementation of the PAC / LAM message exchange between units, the relevant TWR/APP systems should be provided with a means to input and forward "start-up", "push-back", "taxi" or similar information from which the ETOT may be derived in order to calculate the ETO at the COP and initiate the transmission of the PAC.
OLDI-PAC-80-M	As bilaterally agreed, the message shall contain either:
•	Estimated Take-Off Time, or
•	Estimate Data.
OLDI-PAC-90-M	When the message reference is included by bilateral agreement, it shall contain the message number of the first PAC message sent for the flight.
OLDI-PAC-100-M	When the message reference is included, by bilateral agreement, it shall be included on second and subsequent PAC messages.
OLDI-PAC-110-M	The use of the code request facility, if required, shall be agreed bilaterally.
OLDI-PAC-120-M	A revised PAC message shall be sent if, before departure, there is a change to any item of data included in the previous PAC message.
OLDI-PAC-130-M	The route shall be included where bilaterally agreed between the sending and receiving units.
OLDI-PAC-135-O	If CRQ and/or CRP messages are not implemented, a PAC message may be sent from a TWR unit to the downstream ATS unit (TMA or ACC).

### Processing in the Receiving Unit
OLDI-PAC-140-M	The ATC system receiving a PAC message shall attempt association with the corresponding flight plan.
OLDI-PAC-150-M	If a corresponding flight plan is found and no discrepancy is present in the message that would inhibit correct processing, the operational content shall be included with the flight plan;
OLDI-PAC-160-M	If a corresponding flight plan is found and no discrepancy is present in the message that would inhibit correct processing, the required data shall be output at operational ATC and other positions as appropriate;
OLDI-PAC-170-M	If a corresponding flight plan is found and no discrepancy is present in the message that would inhibit correct processing, an acknowledgement shall be returned.
OLDI-PAC-180-M	If a corresponding flight plan cannot be found, or a discrepancy is found that inhibits correct processing of the message and the sector responsible for accepting control of the flight can be identified, the operational content of the message shall be displayed at the appropriate working position.
OLDI-PAC-190-M	If a corresponding flight plan cannot be found, or a discrepancy is found that inhibits correct processing of the message and the sector responsible for accepting control of the flight can be identified, an acknowledgement shall be returned.
OLDI-PAC-200-M	If a corresponding flight plan cannot be found, or a discrepancy is found that inhibits correct processing of the message and the sector responsible for accepting control of the flight can be identified, a flight plan shall be created.
OLDI-PAC-210-M	If a corresponding flight plan cannot be found, or a discrepancy is found that inhibits correct processing of the message and the sector responsible for accepting control of the flight cannot be identified, the acknowledgement shall be inhibited.
OLDI-PAC-220-M	The data in a second or subsequent PAC message shall supersede the data in the previous message.
OLDI-PAC-230-M		If the PAC message includes a request for the assignment of an SSR code and is correctly processable as described in requirements OLDI-PAC-150-M, OLDI-PAC- 160-M and OLDI-PAC-170-M, a COD message shall be returned in addition to the LAM.
Note: As the code assignment process requires detailed flight plan route information, no requirement is made in this document for the return of a COD message by the receiving unit where such data may not be available. This does not prevent a message being returned under such circumstances if a specific local capability exists and the procedure has been agreed bilaterally.

### Criteria for Message Transmission
OLDI-PAC-240-M	PAC message transmission shall be initiated by a start-up, push-back, taxi or ETOT confirmed event.
OLDI-PAC-245-R	Upon a change in the sequence of concerned ATS units, a delay should be applied between the MAC transmission to the unit to which notification/coordination had previously been effected for the flight and the initiation of PAC to the new unit.

## Acknowledgement of PAC
### Acknowledgement
The messages to be sent in response to a PAC message are described in section 6.6.3.2.

### No Acknowledgement
OLDI-PAC-250-M	If no LAM message is received as an acknowledgement for a PAC message, a warning shall be displayed at the position in the ATC unit responsible for co- ordination with the next unit.

### No-LAM cases
OLDI-PAC-260-M	In no-LAM cases, verbal co-ordination shall be initiated.

### No COD Message
OLDI-PAC-270-M	If a COD message is not received in response to a code request included in the PAC message, a warning shall be displayed at an appropriate position.
OLDI-PAC-280-M	Where the code request function is to be used, the time-out value to be applied shall
be agreed bilaterally.

### Action on Departure
Boundary Estimate Data Format
Requirement OLDI-ACT-60-M identifies that an ACT message is sent following the departure of a flight previously co-ordinated by the use of a PAC message using boundary estimate data.

### Estimated Take-off Time Format
See section 12.1.7.
 


## Examples
Estimated Take-Off Time and Code Request
### ICAO
(PACBA/SZ002-CRX922/A9999-LFSB1638-LSZA-8/I-9/2B737/M-15/N0480F390 UB4 BNE UB4 BPK UB3 HON-80/N-81/W/EQ Y/NO R/NO S/UN-18/DEP/BALE MULHOUSE DEST/LUGANO OPR/CROSS AVIATION LTD ALTN/EGLL RALT/EGKK RMK/ONE ENG INOP)
### ADEXP
-TITLE PAC
-REFDATA
-SENDER -FAC BA
-RECVR -FAC SZ
-SEQNUM 002
-ARCID CRX922
-SSRCODE REQ
-ADEP LFSB
-ETOT 1638
-ARCTYP B737
-NBARC 2
-WKTRC M
-FLTTYP N
-ADES LSZA
-BEGIN EQCST
-EQPT W/EQ
-EQPT Y/NO
-EQPT R/NO
-SUREQPT S/UN
-END EQCST
-ROUTE N0480F390 UB4 BNE UB4 BPK UB3 HON
-MSGREF
-SENDER -FAC BA
-RECVR -FAC SZ
-SEQNUM 0012
-FLTRUL I
-OPR CROSS AVIATION LTD
-ALTRNT1 LSZH
-ALTRNT2 LSGG
-RMK ONE ENG INOP
-RWYDEP 16
-SID 5
-CFL
-FL F210
Time at COP
### ICAO
(PACD/L025-EIN636/A5102-EIDW-LIFFY/1638F290F110A-EBBR-9/B737/M)
### ADEXP
-TITLE PAC
-REFDATA
-SENDER -FAC D
-RECVR -FAC L
-SEQNUM 025
-ARCID EIN636
-SSRCODE A5102
-ADEP EIDW
-COORDATA
-PTID LIFFY
-TO 1638
-TFL F290
-SFL F110A
-ARCTYP B737
-ADES EBBR


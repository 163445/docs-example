# Advance Boundary Information Message (ABI)
## Purpose of the ABI Message
The ABI satisfies the following operational requirements:
-	provide for acquisition of missing flight plan data;
-	provide advance boundary information and revisions thereto for the next ATC unit;
-	update the basic flight plan data;
-	facilitate early correlation of radar tracks;
-	facilitate accurate short-term sector load assessment;
-	request the assignment of an SSR code from the unit to which the above notification is sent, if required.
The ABI is a notification message.

## Message Contents
OLDI-ABI-10-M	The ABI message shall contain the following items of data:
-	Message Type;
-	Message Number;
-	Aircraft Identification;
-	SSR Mode and Code (if available);
-	Departure Aerodrome;
-	Estimate Data;
-	Destination Aerodrome;
-	Number and Type of Aircraft;
-	Type of Flight;
-	Equipment Capability and Status.
Note:	If the SSR code is not assigned or not available, it may be omitted.
Depending on the aircraft identification method applied, the SSR code and Mode element (data item A.7) may contain the current SSR code or the SSR code at the transfer of control point.
OLDI-ABI-20-M	If bilaterally agreed, the ABI message shall contain any of the following items of data:
-	Route;
-	Other Flight Plan Data

## Rules of Application
### General
OLDI-ABI-30-M	Except as provided for in OLDI-ABI-60-M and OLDI-ABI-70-R below, one or more ABI messages shall be sent for each flight planned to cross the boundary of areas of responsibility subject to OLDI procedures.
OLDI-ABI-40-M	The use of the code request facility shall be agreed bilaterally.
OLDI-ABI-50-M	When sent, the ABI message shall precede the Activate (ACT) or Referred Activate Proposal (RAP) message.
OLDI-ABI-60-M	ABI message generation shall be inhibited if a Preliminary Activation (PAC) message is to be sent.
OLDI-ABI-70-R	ABI transmission should be inhibited if the ACT or RAP message is due for transmission immediately or within a bilaterally agreed time interval.
 


Note: The purpose of this recommendation is to avoid the attempted simultaneous resolution of anomalies at different positions at the receiving unit in respect of ABI and ACT messages for the same flight.
OLDI-ABI-80-M	A revised ABI message shall be sent if the subsequent ACT message has not been generated and any of the following change or are modified:
-	COP;
-	expected SSR code at the transfer of control point;
-	aerodrome of destination;
-	type of aircraft;
-	equipment capability and status.
Note:	The revised ABI messages in ICAO format with a different aerodrome of destination are difficult to process automatically. Consequently the ADEXP format is recommended.
OLDI-ABI-85-O	A revised ABI message may contain both the Estimate Data and the Route Field if there is a change of COP.
OLDI-ABI-90-R	A revised ABI message should be sent if the subsequent ACT message has not been generated and one of the following items is subject to change:
-	the expected boundary crossing level;
-	the estimated time over (ETO) at the COP differs from that in the previous ABI message by more than the time specified in the Letter of Agreement (LoA);
-	any other data as bilaterally agreed.
Processing in the Receiving Unit
OLDI-ABI-100-M	The ATC system receiving an ABI message shall attempt association with the corresponding flight plan data.
OLDI-ABI-110-M	If the flight plan association is unsuccessful, a flight plan shall be created automatically or manually in the receiving system.
Note:	If no syntax and/or semantic discrepancies are found in the received ABI message, a flight plan could be automatically created by the receiving system. If syntax and/or semantic discrepancies are found in the received ABI message, the ABI message could be referred to the operator for correction and manual creation of a system flight plan by the receiving system.
OLDI-ABI-120-M	If the flight plan association is successful but a discrepancy is identified between the data in the message and corresponding data in the receiving system that would result in the need for corrective action on receipt of the following ACT message, the discrepancy shall be referred to an appropriate position for resolution.
OLDI-ABI-130-M	If the ABI message includes a request for the assignment of an SSR code and is correctly processed, a COD message shall be returned in addition to the LAM.
Note: As the code assignment process requires detailed flight plan route  information, no requirement is made in this document for the return of a COD message by the receiving unit where such data may not be available. This does not prevent a message being returned under such circumstances if a specific local capability exists and the procedure has been agreed bilaterally.

## Criteria for Message Transmission
OLDI-ABI-140-M	The message shall be transmitted a parameter number of minutes before the estimated time at the COP.
OLDI-ABI-145-R	Upon a change in the sequence of concerned ATS units, a delay should be applied between the MAC transmission to the unit to which notification had previously been effected for the flight and the initiation of ABI to the new unit.
 


OLDI-ABI-150-M	The ABI generation parameter(s) shall be included in the LoA between the ATC units concerned.
OLDI-ABI-160-R	The ABI generation parameter(s) should be variable, based on the provisions of the LoA.
OLDI-ABI-170-R	The ABI generation parameter(s) should be defined separately for each of the COPs.
OLDI-ABI-175-O	An ABI message may be sent to the downstream ATC unit upon reception of an ABI message.

## Acknowledgement of ABI
Acknowledgement
OLDI-ABI-180-M	The ABI message shall be acknowledged by generating and transmitting a LAM message.
Note:	A LAM message is generated regardless of the results of the flight plan association attempt.

## No Acknowledgement
OLDI-ABI-190-R	If no LAM message is received as an acknowledgement for an ABI message, a warning should be displayed at the appropriate position.

## No COD Message
OLDI-ABI-200-M	If a COD message is not received in response to a code request included in the ABI message, a warning shall be displayed at the appropriate position.
OLDI-ABI-210-M	Where the code request function is to be used, the time-out value to be applied shall
be agreed bilaterally.

## Examples
"Air 2000" 253, a Boeing 757 from Malta to Birmingham estimating ALESO at 1221 UTC, flying at FL350 at a true airspeed of 480 knots, planned to route via UT10 ALESO UT420 BUZAD UL10 HON, transponding on A7012 and requesting FL390. The following are equivalent examples of the ABI message sent from Reims to London ACC.

## Normal Situation
### ICAO
Example 1
(ABIE/L001-AMM253/A7012-LMML-ALESO/1221F350-EGBB-8/I-9/2B757/M-15/N0480F390 UT10 ALESO UT420 BUZAD UL10 HON-80/N-81/W/EQ Y/NO-18/DEP/LUQA AIRPORT DEST/BIRMINGHAM OPR/AIR 2000 LTD ALTN/EGLL RALT/EGKK RMK/ONE ENG INOP)
Example 2 (including PBN capability and Mode S capability and status)
(ABIE/L001-AMM253/A7012-LMML-ALESO/1221F350-EGBB-9/B757/M-15/N0480F390 UT10 ALESO UT420 BUZAD UL10 HON-80/N-81/W/EQ Y/NO R/EQ/B1D1 S/EQ/E)
### ADEXP
Example 1
-TITLE ABI
-REFDATA
-SENDER -FAC E
-RECVR -FAC L
-SEQNUM 001
-ARCID AMM253
-SSRCODE A7012
-ADEP LMML
-COORDATA
-PTID ALESO
-TO 1221
-TFL F350
-ADES EGBB
-ARCTYP B757
-NBARC 2
-WKTRC M
-FLTTYP N
-BEGIN EQCST
-EQPT W/EQ
-EQPT Y/NO
-END EQCST
-ROUTE N0480F390 UT10 ALESO UT420 BUZAD UL10 HON
-FLTRUL I
-OPR AIR 2000 LTD
-ALTRNT1 EGLL
-ALTRNT2 EGKK
-RMK ONE ENG INOP

Example 2 (including Mode S capability and status)
-TITLE ABI
-REFDATA
-SENDER -FAC E
-RECVR -FAC L
-SEQNUM 001
-ARCID AMM253
-SSRCODE A7012
-ADEP LMML
-COORDATA
-PTID ALESO
-TO 1221
-TFL F350
-ADES EGBB
-ARCTYP B757
-FLTTYP N
-BEGIN EQCST
-EQPT W/EQ
-EQPT Y/NO
-EQPT R/EQ
-SUREQPT S/EQ/E
-END EQCST
-PBN B1D1
-ROUTE N0480F390 UT10 ALESO UT420 BUZAD UL10 HON
-ADESOLD EGCC

SSR Code Request
    ICAO
(ABIE/L001-AMM253/A9999-LMML-ALESO/1221F350-EGBB-9/B757/M-15/N0480F390 UT10 ALESO UT420 BUZAD UL10 HON-80/N-81/W/EQ Y/NO)
    ADEXP
-TITLE ABI
-REFDATA
-SENDER -FAC E
-RECVR -FAC L
-SEQNUM 001
-ARCID AMM253
-SSRCODE REQ
-ADEP LMML
-COORDATA
-PTID ALESO
-TO 1221
-TFL F350
-ADES EGBB
-ARCTYP B757
-FLTTYP N
-BEGIN EQCST
-EQPT W/EQ
-EQPT Y/NO
-END EQCST
-ROUTE N0480F390 UT10 ALESO UT420 BUZAD UL10 HON

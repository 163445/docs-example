# Message for the Abrogation of Co-ordination (MAC)
## Purpose
A MAC message is used to indicate to the receiving unit that the co-ordination or notification previously effected for a flight is being abrogated.
The MAC is not a replacement for a Cancellation (CNL) message, as defined by ICAO, and therefore, shall not be used to erase the basic flight plan data.

## Message Contents
OLDI-MAC-10-M	The MAC message shall contain the following items of data:
•	Message Type;
•	Message Number;
•	Aircraft Identification;
•	Departure Aerodrome;
•	Co-ordination Point;
•	Destination Aerodrome.
OLDI-MAC-20-M	If bilaterally agreed, the MAC message shall contain any of the following items of data:
•	Message Reference;
•	Co-ordination Status and Reason.

## Rules of Application
### General
OLDI-MAC-30-M	A MAC message shall be sent to a unit to which co-ordination had previously been effected for a flight, by the use of an ACT or RAP message, when one of the following occurs:
•	the expected level at the transfer of control point is different from the level contained in the previous message resulting in a change of the next unit in the co-ordination sequence;
•	the route of flight has been altered which results in change of the next unit in the co-ordination sequence;
•	the system flight plan is cancelled in the sending unit and the co-ordination is no longer relevant;
•	a MAC is received from the previous unit in respect of the flight that requires an effective abrogation towards the downstream unit based on bi-lateral agreements.
Note: The operational requirement to send a MAC on reception of a MAC from the previous unit is to be assessed. If operational procedures make that a new ACT is received shortly after the reception of the MAC (e.g. because traffic climbs faster/slower than expected and is re-coordinated by another unit), there might be no need to immediately send a MAC to the downstream unit if this has no impact. Sending a MAC in this case might even create nuisance to the ATCO at the receiving unit.

OLDI-MAC-40-M	When the MAC message is sent due to a flight level or route change, notification and/or co-ordination, as appropriate, shall be effected with the new unit in the co- ordination sequence.
OLDI-MAC-45-R	A delay should be applied between the MAC transmission to the unit to which co- ordination or notification had previously been effected for the flight and the initiation of co-ordination or notification to the new unit, if bilaterally agreed.
Note: This is to avoid that the ABI/ACT/PAC/RAP to the new unit be received before the MAC abrogating the previous coordination or notification.
OLDI-MAC-50-M	A MAC message shall be sent when the co-ordination for a departing flight, effected by the use of a PAC or CRQ message, is abrogated.
OLDI-MAC-60-R	A MAC message should be sent when the notification (ABI message) previously effected for a flight is cancelled due to any of the reasons specified in requirement OLDI-MAC-30-M or the flight is delayed en-route and a revised estimate cannot be determined automatically.
OLDI-MAC-80-M	If included, the message reference shall contain the message number of the last ABI, PAC, ACT, REV or RRV message transmitted for the flight and acknowledged.
OLDI-MAC-90-M	The co-ordination point shall be the COP through which the flight had been previously notified or co-ordinated.
OLDI-MAC-100-R	The MAC message should identify the status to which the co-ordination or notification is to revert and the reason for the abrogation.
OLDI-MAC-110-M	If included, the status and reason shall be one of the following three options:
1.	when the receiving unit is no longer the next co-ordination partner:
a.	the status is INI (initial);
b.	the reason is one of the following:
i.	TFL if the reason is a change of transfer flight level;
ii.	RTE if the reason is a change of route (including diversion);
iii.	CAN if the reason is a cancellation;
iv.	OTH for any other reason or if the reason is unknown.
2.	the co-ordination effected by the use of the previous PAC, CRQ or ACT message (as modified by any subsequent REV message) is abrogated but the flight is expected to be the subject of a new co-ordination sequence with the same unit;
a.	the status is NTF (notification);
b.	the reason is one of the following:
i.	DLY if the reason is a delay prior to departure;
ii.	HLD if the reason is a hold;
iii.	OTH for any other reason, or if the reason is unknown.
3.	the transmission of an ABI, RAP (if applicable) or ACT message, the flight is holding for an indefinite period and is expected to be subject to a revised ABI, RAP or ACT, as appropriate:
a.	the status is NTF (notification);
b.	the reason is one of the following:
i.	DLY if the reason is a delay prior to departure;
ii.	HLD if the reason is a hold;
iii.	OTH for any other reason, or if the reason is unknown.
OLDI-MAC-120-M	If the flight is to be re-notified or re-co-ordinated, a new notification and/or co- ordination message, as appropriate, shall be sent.
OLDI-MAC-130-M	If the flight is to be re-notified or re-co-ordinated, the system shall retain the capability to correctly process a new notification and/or co-ordination message from either the previous transferring unit or a different unit in a new co-ordination sequence.
Processing in the Receiving Unit
OLDI-MAC-140-M	The working position(s) in the receiving ATC unit which are provided with flight details shall be notified of the abrogation.
Note:	the basic flight plan data stored in the receiving ATC unit remains unchanged upon reception of a MAC message.

OLDI-MAC-145-O	The received MAC message may be referred to the appropriate position for manual intervention.
Note: This can be necessary to allow further actions e.g. decorrelation of the flight.
OLDI-MAC-150-R	On the reception of a MAC message, a previously received LOF and/or NAN message should be abrogated.

## Acknowledgement of MAC
Acknowledgement
OLDI-MAC-160-M	If the MAC message can be associated with a flight plan within the receiving system and can be processed, a LAM message shall be transmitted in acknowledgement.
OLDI-MAC-170-M	If the MAC message cannot be associated with a flight plan within the receiving system, or cannot be processed, the transmission of a LAM message shall be inhibited.

## No Acknowledgement
OLDI-MAC-180-M	If ATC co-ordination is being abrogated and no LAM message is received, a warning
shall be displayed at the ATC position responsible for the co-ordination.
Note: In such cases a verbal abrogation of co-ordination should be effected by the transferring ATC unit, as bi-laterally agreed.


## Examples
An ABI message was sent by Amsterdam ACC to Brussels ACC for flight HOZ3188, planned at FL190; the flight subsequently requests to climb to FL270 and is so cleared, thus entering Maastricht airspace instead of Brussels. Examples 6.5.5.1 – 1. and 6.5.5.2 – 1. show how the MAC sent to Brussels by Amsterdam would appear both in ICAO and ADEXP formats.

An ABI and, later, an ACT message are sent to Maastricht, but, before reaching the COP, the aircraft returns to Amsterdam Airport and the route and destination are amended in the sending unit's system; a MAC is sent to Maastricht as shown in examples 6.5.5.1 – 2. and 6.5.5.2 - 2.

### ICAO
1.	(MACAM/BC112 AM/BC105-HOZ3188-EHAM-NIK-LFPG-18/STA/INITFL)
2.	(MACAM/MC096-HOZ3188-EHAM-NIK-LFPG-18/STA/INIRTE)

### ADEXP
1.
-TITLE MAC
-REFDATA
-SENDER -FAC AM
-RECVR -FAC BC
-SEQNUM 112
-ADEP EHAM
-COP NIK
-ADES LFPG
-ARCID HOZ3188
-CSTAT
 -MSGREF
-STATID INI
-STATREASON TFL
-SENDER -FAC AM
-RECVR -FAC BC
-SEQNUM 105
 


2.
-TITLE MAC
-REFDATA
-SENDER -FAC AM
-RECVR -FAC MC
-SEQNUM 096
-ADEP EHAM
-COP NIK
-ADES LFPG
-ARCID HOZ3188
-CSTAT
-STATID INI
-STATREASON RTE


# FOREWORD

##	Responsible Body
The EUROCONTROL Specification for On-Line Data Interchange (OLDI), Edition 5.0, has been prepared by the EUROCONTROL Network Manager Directorate (NMD) in cooperation with the operational stakeholders within the OLDI group of the NETOPS working arrangement.
The need for additional OLDI guidance material was identified by the OLDI group and acknowledged by NETOPS. Such OLDI guidance material is published as a separate EUROCONTROL Guidelines document [GUID].

##	Maintenance of this Document
This EUROCONTROL Specification has been developed under the EUROCONTROL Regulatory and Advisory Framework (ERAF) and is maintained by EUROCONTROL in accordance with this Framework as further detailed in Annex E.

##	Relationship with Regulatory Framework
The implementation and operational use of the notification, co-ordination and transfer processes are prescribed in EUROCONTROL or Community regulatory material (i.e. European Commission implementing rules) depending on the area of applicability of these processes. In particular, OLDI has been recognised as a Community specification for the single European sky (SES).
This new Edition will be proposed to the European Commission as a Community specification to be used notably as a means of compliance with Commission Regulation (EC) No 1032/2006 of 6 July 2006 laying down requirements for automatic systems for the exchange of flight data for the purpose of notification, co-ordination and transfer of flights between Air Traffic Control Units and the European Commission Regulation (EC) No 30/2009 of 16 January 2009 amending Regulation (EC) No 1032/2006 as far as the requirements for automatic systems for the exchange of flight data supporting data link services are concerned.
This document does not mandate the implementation of OLDI messages but specifies the requirements that need to be met when implementing such facilities. If OLDI messages are implemented as the result of regulatory provisions, or based on bilateral agreement between Air Traffic Control Units, then the requirements outlined as mandatory in this specification for those messages become mandatory for implementation. This is required in order to meet the purpose of the messages and to ensure interoperability between systems.

##	Editorial Practices
The following editorial practice has been followed in the writing of the requirements:
- Requirements using the operative verb "shall" are mandatory to claim compliance with the Specification;
- For the Recommended Requirements the operative verb "should? is used;
- For the Optional Requirements the operative verb "may? is used.

Every requirement within this document follows a pre-defined format, namely: OLDI-[procedure / message]-[nnn]-[M | R | O] [Text of requirement] where:
- [procedure / message]: 3-5 characters, which identifies the procedure or message to
which the requirements apply, e.g. ACT;
- [nnn]: numeric, which identifies the sequence number of the requirement;
- [M | R | O]: M (mandatory), R (recommended), O (optional), which identifies the
type of requirements
Requirements may be followed by a free text note to give additional explanation.
 




## Relationship to Edition 4.3 of the EUROCONTROL Specification for On Line Data Interchange
This Specification when approved will supersede Edition 4.3.

## Significant Changes from Edition 4.3
It is to be noted that the EUROCONTROL Guidelines for OLDI [GUID] included proposed content for a future release of the OLDI Specification, these have been further reviewed by the OLDI group for integration into this Edition of the OLDI Specification. The following are the most significant changes and additions from Edition 4.3 to Edition 5.0:

1. Optional requirements concerning the processing of destination airport within REV message (new OLDI-REV-86-O, OLDI-REV-135-O and OLDI-REV-145-O);

2. Clarification of MAC message and deletion of MAC redundant requirements (new OLDI-MAC- 145-R, amended OLDI-MAC-80-M, deleted OLDI-MAC-70-M and OLDI-MAC-190-M);

3. MAC message optional and recommended requirements concerning the delay of transmission (OLDI-MAC-30-M 4th bullet and new note, new OLDI-MAC-45-R, new note for OLDI-MAC-180-M);

4. Recommended requirements for ABI/PAC/ACT/RAP transmission delay in cases where an abrogation changes the sequence between the ATS unit (new OLDI-ABI-145-R, OLDI-ACT- 245-R, OLDI-PAC-245-R, OLDI-RAP-155-R);

5. Optional LOF field for catering ATNB2 (OLDI-LOF-25-O and new section 18.55);

6. Former Annex A and B integrated to the main part of OLDI Specification as sections 18 and 17 (respectively) including updated cross-references;

7. Former Annex G transferred to OLDI Guidelines [GUID];


8. Alignment of OLDI Specification with ADEXP Specification [ADEXP] concerning the handling of Assigned heading optional field and inclusion of note concerning the relative heading (OLDI-FC-AHD-13-O and new OLDI-FC-AHD-15-M);

9. New note for OLDI-REV-200-M;

10. Reviewed ROF message purpose (2nd bullet) and additional message optional fields (OLDI- ROF-25-O) and amended OLDI-ROF-70-R;

11. Update OLDI-SBY-20-M, OLDI-RJC-30-M and section 8.8.1 for operational reply to RRQ message;

12. Correction in 18.39.1 to replace "point" by "pt"

13. Editorial corrections in OLDI-BAS-10-M and Annex B.1;

14. New introductory text for Annex D, new maintenance Annex E.

## Relationship to Other Documents
This document makes reference to the use of two types of field format in the compilation of messages; these are ICAO and ADEXP.
- ICAO field formats are described [PANS-ATM]. In the event that [PANS-ATM] is superseded by another document, the definition of ICAO field types shall be as described in that document.
-  ADEXP field formats are described in [ADEXP]. Referenced documents are listed at Section 2.
 


# Introduction
## Purpose
This Edition of the EUROCONTROL Specification for OLDI has been thoroughly reviewed and updated by the OLDI Specification Review Group, established under the NETOPS working arrangement. This Edition will be proposed to the European Commission as a Community specification as a means of compliance for the European Commission implementing rule- Regulation (EC) No 1032/2006 of 6 July 2006 as amended by the European Commission Regulation (EC) No 30/2009 of 16 January 2009.

Flights which are being provided with an ATC service are transferred from one ATC unit to the next in a manner designed to ensure complete safety. In order to accomplish this objective, it is a standard procedure that the passage of each flight across the boundary of the areas of responsibility of the two units is co- ordinated between them beforehand and that the control of the flight is transferred when it is at, or adjacent to, the said boundary.

Where it is carried out by telephone, the passing of data on individual flights as part of the co-ordination process is a major support task at ATC units. The operational use of connections between Flight Data Processing Systems (FDPSs) for the purpose of replacing such verbal "estimates", referred to as On-Line Data Interchange (OLDI), began within Europe in the early nineteen eighties.

In order to facilitate implementation, common rules and message formats were elaborated and agreed by the agencies concerned and incorporated in Edition 1 of the EUROCONTROL Standard for On-Line Data Interchange first published in 1992. The EUROCONTROL Specification for OLDI has evolved following regular implementation feedback. Edition 5.0, of the Specification has been produced to meet the latest requirements and comments submitted by operational stakeholders.

## Scope
This document specifies the facilities and messages to be provided between FDPSs serving ATC units for the purpose of achieving:
- the notification of flights;
- the co-ordination required prior to the transfer of flights from one unit to the next;
- the civil / military co-ordination;
- situational awareness;
- the transfer of communication of such flights;
- support to air-ground data link;
- co-ordination between Area Control Centres and Oceanic Control Centres. This document:
- defines the message formats and rules for the content;
- describes the facilities required at such units which are prerequisite to the use of data interchange for this purpose.
It is recommended that the data flows specified in this document be used for the internal system interfaces between units served by the same system to facilitate interoperability between internal and external units.
OLDI-GEN-10-R This Specification should be applied by ANSPs to OLDI facilities between units providing an ATC service.
OLDI-GEN-20-O The operational data within the messages defined within this Specification may be applied within systems which provide service to more than one ATSU.
OLDI-GEN-30-O The operational data within the messages defined within this Specification may be applied between systems used by other types of units than ATSUs (i.e. Military units, Airports, etc.).
 


# References

ICAO  Document  4444 -  Procedures  for Air  Navigation Services Air Traffic Management (PANS-ATM)
The following document contains provisions which, through reference in this text, constitute provisions of this EUROCONTROL Specification:
[PANS-ATM] Procedures for Air Navigation Services - Air Traffic Management, ICAO Document 4444, 16th Edition dated 10 November 2016.
At the time of publication of this EUROCONTROL Specification, the editions indicated for the referenced documents were valid.
OLDI-REF-10-M Any revision of the referenced ICAO documents shall be immediately taken into account to revise this EUROCONTROL Specification.
Note: The revision of this document will be done in accordance with the agreed update mechanism for the OLDI Specification.
OLDI-REF-20-M Revisions of the other referenced documents shall form part of the provisions of this EUROCONTROL Specification after they are formally reviewed and incorporated into this EUROCONTROL Specification.
OLDI-REF-30-M In the case of conflict between the requirements of this EUROCONTROL Specification and the contents of other EUROCONTROL documents, this EUROCONTROL Specification shall take precedence.

ICAO Annex 10
The following document contains references to ICAO Annex 10 for ATN B1 and B2 related messages.

EUROCONTROL Documents
The following EUROCONTROL document is referenced in this Specification:
[ADEXP] EUROCONTROL Specification for ATS Data Exchange Presentation, SPEC-107, Edition 3.3, dated 14/07/2020.

[GUID] EUROCONTROL Guidelines for On-Line Data Interchange, GUID-176, Edition 1.1, dated 14/07/2020.
 


# Definitions and Abbreviations
## Message Field Definitions
The data fields which are given in each of the messages in this document are described in section 18 Data Insertion Rules. This section makes reference either to [PANS-ATM] or [ADEXP] and describes the derivation of the content in general. Any unique requirements applicable to a particular message or circumstance are specified in the description of the message concerned.
OLDI-GEN-40-M The requirements for the format and content of data fields described under the 'Data Content' section for each message shall be as described in section 18 unless described specifically for the message concerned.

## Definitions - General
OLDI-GEN-50-M For the purposes of this EUROCONTROL Specification, the following definitions shall apply.

- Accepting Unit: The Air Traffic Control unit next to take control of an aircraft.
- Acknowledgement: Notification that a message has been received and found to be correctly
processable.
- Activation: The process in a receiving ATC unit whereby the flight plan for the referent
flight is upgraded to include the data provided by the transferring unit as part of the co-ordination process between the two units and which results in the provision of the data to controllers.
- ADEXP Format: One of the formats utilised for the ground - ground transmission of ATS
messages and which uses the field types and separators described in [ADEXP].
- Altitude: The vertical distance of a level, a point or an object considered as a point, measured from mean sea level.
Application: That part of an ATS sub-system that conforms to this specification and
interfaces with such entities in other ATS systems.
- Area of Responsibility: An airspace of defined dimensions within which an ATC unit provides air
traffic services.
- Area of Interest The airspace volume for which the ATC unit requires information such as
entering flights, airspace status, etc.
This area includes the area of responsibility and its vicinity.
- Association: A procedure in which a system connects a received OLDI message with a
flight plan entry in the database.
- ATC Unit: ATC Unit means variously area control centre, approach control unit or aerodrome control tower.
- Automated acceptance: Acceptance of the co-ordination/transfer conditions as a result of an
automated system processing.
- Availability: The degree to which the system or component is operational and accessible when required for use.
Boundary: The planes (lateral and vertical) delineating the area of responsibility of an
ATC unit.
- Cleared Flight Level: The flight level to or at which a flight has currently been cleared by ATC.
- Community Specification: Means of defining the technical and operational conditions necessary to
meet the essential requirements and relevant implementing rules for interoperability; compliance with published Community Specifications, which remains voluntary, crates a presumption of conformity with the essential requirements and relevant implementing rules for interoperability.
- Co-ordination, ATC: Co-ordination between Air Traffic Control Units of the planned passage of
flights across the common boundary, in order to ensure flight safety.
- Co-ordination Message: A generic term referring to a message used for accomplishing ATC co-
ordination. These include the CDN which is a specific message described in section 14.6.
- Co-ordination Phase: In respect of a given flight, the phase during which the transferring and
receiving ATC units agree the conditions under which a flight will pass from the control of one to the other.
- Co-ordination Point: A point on or adjacent to the boundary known by the ATC units in a co-
ordination sequence and referred to in co-ordination messages.
- Correlation: The process of linking flight plan data and the radar track of the same flight.
- Departure Flight Level: The flight level to which the flight is initially to climb issued as part of a
departure clearance.
Executive Control: Executive control is performed by the controller having executive
responsibility of separation of flight.
- Flight Plan: Specified information provided to air traffic service units, relative to an
intended flight or portion of flight of an aircraft.
- Flight Level Block: A flight level block defining an airspace vertically, inclusive of the flight levels given.
Generate: A process in an ATC system where relevant data are extracted from the data base(s) and a message is created for transmission to a receiving ATC unit.
- ICAO Format: One of the formats utilised for the ground - ground transmission of ATS
messages and which uses the field types and separators described in [PANS-ATM].
- Letter of Agreement: Document that specifies the exchange of flight data and the associated procedures between ATC Units for the purpose of notification, co-ordination and transfer of flights or for information exchange for flights for which the responsibility of the control does not change.
- Level: A generic term relating to vertical position of an aircraft in flight; within this Specification the term level or flight level includes altitude in those cases where it is used.
- Manual acceptance: Acceptance of the co-ordination/transfer conditions as a result of a controller action.
- Notification: Transmission by the transferring unit of data to update the system at the receiving unit in preparation for the co-ordination phase.
- Non standard conditions: Conditions that are not in accordance with the ones specified in Letters of
Agreement.
- Operational data: Data of interest to operational staff in connection to the provision of ATC service as distinct from message control data such as the message type and number.
- Receiving Unit: The ATC unit who receives data.
- Reliability: The probability that the ground installation operates within the specified tolerances.
- Requested Flight Level: A flight level requested by the flight in the flight plan.
- Revision: An amendment to data sent previously by the transferring ATC unit to the receiving ATC unit.
- Sending Unit: The ATS Unit who sends the data.
- Standard conditions: Conditions that are in accordance with the ones specified in Letters of Agreement.
- Supplementary Flight Level: A level, at or above which, or at or below which a flight has been co-ordinated to cross the transfer of control point. The supplementary level, if present, is an element of the exit level.
- System Flight Plan: Information derived from the flight plan of a specific flight held within an FDPS.
- Time-out; A mechanism applied at the sending and at the receiving units in order to synchronise the reply to messages that are referred to the controller.
- Transaction Time: A time interval following the initiation of a message during which transmission, initial processing in the receiving system, generation and transmission of an acknowledgement message, and its identification in the transferring system are performed.
- Transfer Flight Level: The flight level agreed during the co-ordination if in level flight, or the cleared flight level to which the flight is proceeding if climbing or descending at the co-ordination point.
Transfer of Control Point: A point, on the flight path of an aircraft, at which the responsibility for providing ATS to the aircraft is transferred from one ATC unit to the next.
Note: The transfer of control point is not necessarily coincident with the co- ordination point.
- Transfer Phase: A phase of flight following the co-ordination phase, during which the transfer of communication is executed.
- Transferring Unit: ATC unit in the process of the transferring the responsibility for providing an air traffic control service to an aircraft to the next ATC unit along the route of flight.
- Transmit: Communicate a message from one system to another.
- Transmission error: Any error associated to a message that prevents the processing of that message in the receiving unit.
- Warning: A message displayed at a working position when the automated co- ordination process has failed.

## Abbreviations
OLDI-GEN-60-M The following abbreviations shall apply for the purposes of this document.
ABI Advance Boundary Information message
ACC Area Control Centre
ACM ATC Communication Management
ACP Accept message
ACT Activate message
ADEXP ATS Data Exchange Presentation
AFN ATS Facilities Notification
AMA Arrival Management message
APP Approach Control Unit
ATC Air Traffic Control
ATM Air Traffic Management
ATS Air Traffic Services
ATSU Air Traffic Services Unit
BFD Basic Flight Data message
CDA Current Data Authority
CDN Co-ordination message
CFD Change To Flight Data message
CFL Cleared Flight Level
CM Context Management
CNL Flight Plan Cancellation
COD SSR Code Assignment message
COF Change Of Frequency message
COP Co-ordination Point
CPDLC Controller- Pilot Data Link Communications
CRP Clearance Response message
CRQ Clearance Request message
CWP Controller Working Position
EOBT Estimated Off-Block Time
ETA Estimated Time of Arrival
ETO Estimated Time Over
ETOT Estimated Take-Off Time
FDPS Flight Data Processing System
FRF Further Route of Flight
GAT General Air Traffic
HMI Human Machine Interface
HOP Hand Over Proposal message
ICAO International Civil Aviation Organisation
ICD Interface Control Document
IFR Instrument Flight Rules
INF Information message
LACK Logical acknowledgement (air-ground data link)
LAM Logical Acknowledgement message
LOF Log-On Forwarding message
MAC Message for Abrogation of Co-ordination
MAS Manual Assumption of Communication message
MIL Military
NAN Next Authority Notified message
NDA Next Data Authority
NM Nautical Mile
OCM Oceanic Clearance message
OLDI On-Line Data Interchange
ORCAM Originating Region Code Assignment Method
PAC Preliminary Activation message
PANS Procedures for Air Navigation Services
PNT Point message
RAP Referred Activate message
REV Revision message
RJC Reject message
RLS Release message
ROF Request on Frequency message
RRQ Release Request message
RRV Referred Revision message
RTF Radio Telephony Facilities
RTI Request Tactical Instructions message
RVSM Reduced Vertical Separation Minimum
SBY Stand-By message
SCO Skip Communication message
SDM Supplementary Data message
SFL Supplementary Flight Level
SID Standard Instrumental Departure
SKC Skip Cancellation message
SSR Secondary Surveillance Radar
SYSCO System Supported Co-ordination
TI Transfer Initiation
TIM Transfer Initiation message
TIP Tactical Instructions Proposal message
TWR Aerodrome Control Tower
UTC Universal Time Coordinated
VCI Voice Contact Information
VFR Visual Flight Rules
VOR VHF Omni-directional Range
XAP Crossing Alternate Proposal message
XCM Crossing Cancellation message
XIN Crossing Intention Notification message
XRQ Crossing Clearance Request message
 


# General Requirements
Introduction
This section describes the general operational requirements necessary for the implementation of an OLDI facility between ATC units and the classification and performance requirements of the different types of message used.

## Flight Data Processing System Requirements
Flight Data Base
OLDI-GEN-70-M Units which utilise a facility described in this document shall be provided with data from an FDPS which contains all the information required for the display, processing and compilation of the messages as specified.
Note: The primary source of data for each flight is the flight plan as filed by, or on behalf of, the pilot in command.
Further items of data are obtained by the processing of flight plans with reference to the environment of the unit concerned.

## Operation in Real Time
The OLDI procedure includes events in the transferring ATC unit to initiate functions necessary for the timely presentation of data to the transferring controller and the transmission of co-ordination data to the accepting unit.
OLDI-GEN-80-M The FDPS shall be able to initiate functions by the comparison of Co-ordinated Universal Time and applicable time parameters with times at specified positions on the route of flight as determined from the flight database.

## Data Communications Capability
OLDI-GEN-90-M The FDPS shall be able to receive and transmit flight data in the format applicable to the message as specified in this document via a data communication medium which supports the OLDI function.
OLDI-GEN-100-R The FDPS should have the development potential to allow the addition of new messages that may be included in future editions of this specification.
OLDI-GEN-110-M Within the performance requirements specified in this document, the data communication medium shall provide a rapid and reliable application-to-application data exchange by:
- assuring the integrity of OLDI message transmission;
- monitoring either point-to-point connections or the status of the communications network, as applicable.
OLDI-GEN-120-M The FDPS shall warn the working positions when anomalies are detected by the data communications system.

## Application Functions
OLDI-GEN-130-M The systems used for the provision of OLDI facilities shall be able to automatically receive, store, process, extract and deliver for display, and transmit OLDI related data in real-time.
OLDI-GEN-140-M The FDPS shall reflect current operational data relevant to the OLDI function as required by this Specification, updated either automatically, through manual input, or by a combination of both.
OLDI-GEN-150-M The FDPS shall be able to extract such elements from the flight plan database.
 


OLDI-GEN-160-M The FDPS shall identify the next ATC unit on the aircraft trajectory derived from the route of flight and the expected transfer flight level.
OLDI-GEN-170-M The following shall be agreed bilaterally:
- Co-ordination Points (COPs);
- Reference points used for bearing and distance notations in identifying the COP on direct, off-ATS route segments, where used.
Note: The COPs may not always be identical to the transfer of control points. It is recognised that transfer of control points are subject to bilateral agreement. However, the OLDI messages include only the COPs, and as consequence the agreement of the transfer of control points has not been included in the above OLDI requirement.
OLDI-GEN-180-M The system shall be able to provide co-ordination and transfer message warnings to the operational positions responsible for the co-ordination of the flights concerned.

## Human-Machine Interface (HMI)
OLDI-GEN-190-M The HMI shall be able to display the operational contents of OLDI messages and relevant warnings related to received messages for immediate attention.
Note: The operational content is not meant to be displayed in text form.
OLDI-GEN-200-M The HMI shall provide ATC staff with a means to modify the data from which the operational contents of the messages are derived as required in this document.
OLDI-GEN-210-M The HMI shall indicate that the transmission of the message is in progress or has been successfully transmitted as appropriate.
OLDI-GEN-220-M A warning or notification to the appropriate ATC or technical position(s) shall be generated automatically if no acknowledgement has been received within the parameter time following a transmission of a co-ordination or transfer message.
OLDI-GEN-230-M Such a warning or notification shall be in a form that immediately attracts the attention of the appropriate working position.
OLDI-GEN-240-R The HMI at ATC positions using OLDI should provide a warning if the OLDI facility is not available.

## Initiation of Messages
OLDI-GEN-250-M Each system shall contain a set of system parameters in order to ensure timely, automatic initiation of OLDI messages.
OLDI-GEN-260-R The capability to manually initiate the transmission of a co-ordination message prior to the calculated transmission time should be provided.
OLDI-GEN-270-M The automatic event shall always be assured, if manual initiation is not executed.
OLDI-GEN-280-M The system shall utilise time parameters to define the following:
- lead time, prior to transmission, when the operational contents of the messages within the transferring unit are displayed;
- lead time, global or per COP, to transmit the message, where applicable;
- time after transmission of a message within which an application level acknowledgement is to be received (time-out).
OLDI-GEN-290-M The system shall permit the transmission of messages, triggered by events.
OLDI-GEN-300-O The system may permit message initiation, triggered by advanced functions.
OLDI-GEN-310-M A message shall be transmitted without delay when the required information becomes available at a time later than that at which it would otherwise have been transmitted.
Note: A flight commences a GAT IFR segment at a point close to the boundary which it is then to cross; the ETO at the point is communicated eight minutes before the COP at which time transmission of the ACT message is already late based on the applicable time parameter(s); the message is sent without delay.

## Reception of Messages
OLDI-GEN-320-M The ATC system shall be able to receive OLDI messages;
OLDI-GEN-330-M The ATC system shall be able to process them automatically in accordance with this Specification;
OLDI-GEN-340-M The ATC system shall be able to output flight data in accordance with the message received, and display required warnings in case of inconsistency in the data received;
OLDI-GEN-350-M The ATC system shall be able to generate and transmit acknowledgement messages automatically at the application level.
OLDI-GEN-360-M An acknowledgement message (Logical Acknowledgement (LAM), Accept (ACP) or Stand-by (SBY) Message) shall be generated and transmitted when the corresponding message has been processed and the presentation of the results of the processing to the appropriate position(s), as necessary, is assured.
Note: The detailed conditions for the generation of an acknowledgement are specified in this document individually for each message.

## Time Estimate Derivation
OLDI-GEN-370-R In order to ensure the accuracy of time estimate data, information derived from the most accurate data source should be used.

## Route Data
OLDI-GEN-380-R Whenever inserted in OLDI messages the item Route shall contain the current operational data and as such is based on the most up to date information available.

## Recording of OLDI Data
Content
OLDI-GEN-390-M The contents of all OLDI messages and the time of reception shall be recorded.

## Facilities
OLDI-GEN-400-M Facilities shall be available for the retrieval and display of the recorded data.

## Availability, Reliability, Data Security and Data Integrity
Availability
OLDI-GEN-410-M The OLDI facility shall be available during the hours of normal and peak traffic flows between the two units concerned.
OLDI-GEN-420-R The OLDI facility should be available 24 hours every day.
OLDI-GEN-430-M Any scheduled down-time periods (and thus the planned availability time) shall be bilaterally agreed between the two units concerned.
 


## Reliability
OLDI-GEN-440-M Reliability on every OLDI link shall be at least 99.86 % (equivalent to a down-time of not more than 12 hours per year based on 24-hour availability).
OLDI-GEN-450-R Where operationally justified, a reliability of at least 99.99% (equivalent to a down- time of not more than 52 minutes per year, based on 24 Hour availability) should be provided.

## Data Security
OLDI-GEN-460-R Data security methods (e.g. access rights, source verification) and, where applicable, network management should be applied to OLDI facilities.

## Data Integrity
OLDI-GEN-470-M The failure rate at application level shall be less than or equal to one transmission error per 2000 messages.

## Operational Evaluation
Evaluation Period
OLDI-GEN-480-M Each new OLDI facility, including a new facility on an existing link, shall be subject to an evaluation period to verify the data integrity, accuracy, performance, compatibility with ATC procedures and overall safety prior to its operational implementation.

## Operational Introduction Date
OLDI-GEN-490-M The date of the operational introduction, implying completion of the evaluation period, shall be formally agreed between the two units.

Management of Bilaterally Agreed and Optional requirements
OLDI-GEN-500-R Each individual item of data marked as bilaterally agreed and/or optional should be defined in the LOA with each adjacent ATC unit and be separately configured for each OLDI connection.
 


## Message Categories
General
This section of the document indicates the OLDI message transaction times

## Transaction Times
The transaction times specified include transmission, initial processing at the receiving / accepting unit, creation of the acknowledgement message, its transmission and reception at the transferring unit.
OLDI-MSG-10-M The maximum transaction times for the OLDI messages shall be as specified in Table 5.1.
Table 5.1 ? Maximum OLDI Message Transaction Times
90 % of transmitted/received messages 99.8 % of transmitted/received
messages
4 sec 10 sec
OLDI-MSG-20-M If no acknowledgement has been received within the specified time after transmission, a message shall be considered to have been unsuccessfully transmitted or processed and a warning output as specified in the pertinent section in this document.

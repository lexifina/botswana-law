# SCHEDULE 1 Materials Permitted in AFS Messages
(regs 29, 36 and 40)
1.1
Material Permitted in AFS Messages
Note: The provisions contained in this Schedule do not apply to ATS voice communications.
1.1.1
The following characters are allowed in text messages-
Letters: ABCDEFGHIJKLMNOPQRSTUVWXYZ
Figures: 1 2 3 4 5 6 7 8 9 0
Other signs:- (hyphen)
? (question mark)
: (colon)
((open bracket)
) (close bracket)
. (full stop, period, or decimal point)
, (comma)
' (apostrophe)
= (double hyphen or equal sign)
/ (oblique)
+ (plus sign)
Characters other than those listed above shall not be used in messages unless absolutely necessary for understanding of the text. When used, they shall be spelled out in full.
1.1.2
For the exchange of messages over the teletypewriter circuits, the following characters of International Alphabet No. 5 (IA-5) shall be permitted-
- characters 0/1 to 0/3, 0/7 - in the priority alarm, 0/10, 0/11 - in the ending sequence, 0/13;
- characters 2/0, 2/7 to 2/9, 2/11 to 2/15;
- characters 3/0 to 3/10, 3/13, 3/15;
- characters 4/1 to 4/15;
- characters 5/0 to 5/10; and
- character 7/15.
1.1.3
The exchange of messages using the full IA-5 shall be subject to agreement between the Administrations concerned.
Roman numerals shall not be employed. If the originator of a message wishes the addressee to be informed that roman figures are intended, the Arabic figure or figures shall be written and preceded by the word ROMAN.
1.1.4
Messages using IA-5 shall not contain-
(1) character 0/1 (SOH) other than the one in the heading;
(2) character 0/2 (STX) other than the one in the origin line;
(3) character 0/3 (ETX) other than the one in the ending;
(4) any uninterrupted sequence of characters 5/10, 4/3, 5/10, 4/3 in this order (ZCZC);
(5) any uninterrupted sequence of characters 2/11, 3/10, 2/11, 3/10 in this order (+: +:);
(6) any uninterrupted sequence of four times character 4/14 (NNNN); and
(7) any uninterrupted sequence of four times character 2/12 (,,,,).
1.1.5
The text of messages shall be drafted in plain language or in abbreviations and codes. The originator shall avoid the use of plain language when reduction in the length of the text by appropriate abbreviations and codes is practicable. Words and phrases which are not essential, such as expressions of politeness, shall not be used.
1.1.6
If the originator of a message wishes alignment functions [<<=] to be transmitted at specific places in the text part of such message, the sequence [<<=] shall be written on each of those places.
SCHEDULE 2 Routing of Messages (regs 43, 44 and 50)
1.1
Routing of messages
1.1.1
All communications shall be routed by the most expeditious route available to effect delivery to the addressee.
1.1.2
Predetermined diversion routing arrangements shall be made, when necessary, to expedite the movement of communication traffic. Each communication centre shall have the appropriate diversion routing lists, agreed to by the administration(s) operating the communication centres affected and shall use them when necessary.
1.1.2.1
Diversion routing shall be initiated-
(1) in a fully automatic communication centre-
(a) immediately after detection of the circuit outage, when the traffic is to be diverted via a fully automatic communication centre;
(b) within a 10-minute period after detection of the circuit outage, when the traffic is to be diverted via anon-fully automatic communication centre;
(2) in a non-fully automatic communication centre within a 10-minute period after detection of the circuit outage.
Service message notification of the diversion requirement shall be provided where no bilateral or multilateral prearranged agreements exist.
1.1.3
As soon as it is apparent that it will be impossible to dispose of traffic over the aeronautical fixed service within a reasonable period, and when the traffic is held at the station where it was filed, the originator shall be consulted regarding further action to be taken, unless-
(a) otherwise agreed between the station concerned and the originator; or
(b) arrangements exist whereby delayed traffic is automatically diverted to commercial telecommunication services without reference to the originator.
Note: The expression "reasonable period" means a period of time such that it seems probable that the traffic will not be delivered to the addressee within any fixed transit period applicable to the category of traffic concerned, or, alternatively, any predetermined period agreed between originators and the telecommunication station concerned.
1.2
Supervision of message traffic
1.2.1
Continuity of message traffic. The receiving station shall check the transmission identification of incoming transmissions to ensure the correct sequence of channel sequence numbers of all messages received over that channel.
1.2.1.1
When the receiving station detects that one or more channel-sequence numbers are missing, it shall send a complete service message to the previous station rejecting receipt of any message that may have been transmitted with such missing number(s). The text of this service message shall comprise the signal QTA, the procedure signal MIS followed by one or more missing transmission.
Note: The following examples illustrate application of the above-mentioned procedure. In example
2) the hyphen (-) separator is understood to mean "through" in plain language.
(a) when one channel-sequence number is missing-
(b) when several channel-sequence numbers are missing-
1.2.1.1.1
When the provisions of 1.2.1.1 are applied, the station notified of the missing message(s) condition by the service message shall reassume its responsibility for transmission of the message (or messages) that it had previously transmitted with the transmission identification concerned, and shall retransmit that message (or those messages) with a new (correct in sequence) transmission identification. The receiving station shall synchronise such that the next expected channel-sequence number is the last received channel-sequence number plus one.
1.2.1.2
When the receiving station detects that a message has a channel sequence number less than that expected, it shall advise the previous station using a service message with a text comprising-
(1) the abbreviation SVC;
(2) the procedure signal LR followed by the transmission identification of the received message;
(3) the procedure signal EXP followed by the transmission identification expected;
(4) the end-of-text signal.
Note: The following example illustrates application of the above-mentioned procedure-
1.2.1.2.1
When the provisions of 1.2.1.2 are applied, the station receiving the out-of sequence message shall synchronise such that the next expected channel-sequence number is the last received channel-sequence number plus one. The previous station shall check its outgoing channel-sequence numbers and, if necessary, correct the sequence.
1.2.2
Misrouted messages
Note: A message is considered to have been misrouted when it contains no relaying instructions, expressed or implied, on which the receiving station can take action.
1.2.2.1
When the receiving station detects that a message has been misrouted to it, it shall either-
1) send a service message to the previous station rejecting receipt of the misrouted message; or
2) itself assume responsibility for transmission of the message to all addressee indicators.
Note: The procedure of 2) may be preferred at stations using fully automatic relay methods or a semi-automatic relay technique without continuous tape.
1.2.2.2
When the provisions of 1.2.2.1 are applied, the text of the service message shall comprise the abbreviation SVC, the signal QTA, the procedure signal MSR followed by the transmission identification and of the misrouted message and the end-of-text signal.
Note: The following example illustrates application of the above-mentioned procedure-
1.2.2.3
When, as a result of the provisions of 1.2.2.2, a sending station is notified of the misrouted message condition by service message, it shall reassume its responsibility for the message and shall retransmit as necessary on the correct outgoing channel or channels.
1.2.3
When a circuit becomes interrupted and alternative facilities exist, the last channel-sequence numbers sent and received shall be exchanged between the stations concerned. Such exchanges shall take the form of complete service messages with the text comprising the abbreviation SVC, the procedure signals LR and LS followed by the transmission identifications of the relevant messages and the end-of-text signal.
Note: The following example illustrates application of the above-mentioned procedure-
1.3
Failure of communications
1.3.1
Should communication on any fixed service circuit fail, the station concerned shall attempt to re-establish contact as soon as possible.
1.3.2
If contact cannot be re-established within a reasonable period on the normal fixed service circuit, an appropriate alternative circuit shall be used. Attempts shall be made to establish communication on any authorised fixed service circuit available.
1.3.2.1
If these attempts fail, use of any available air-ground frequency shall be permitted only as an exceptional and temporary measure when no interference to aircraft in flight is ensured.
1.3.2.2
Where a radio circuit fails due to signal fadeout or adverse propagation conditions, a receiving watch shall be maintained on the regular fixed service frequency normally in use. In order to re-establish contact on this frequency as soon as possible there shall be transmitted-
(a) the procedure signal DE;
(b) the identification of the transmitting station transmitted three times;
(c) the alignment function ;
(d) the letters RY repeated without separation for three lines of page copy;
(e) the alignment function ;
(f) end-of-message signal (NNNN). The foregoing sequence shall be repeated as required.
1.3.2.3
A station experiencing a circuit or equipment failure shall promptly notify other stations with which it is in direct communication if the failure will affect traffic routing by those stations. Restoration to normal shall also be notified to the same stations.
1.3.3
Where diverted traffic will not be accepted automatically or where a predetermined diversion routing has not been agreed, a temporary diversion routing shall be established by the exchange of service messages. The text of such service messages shall comprise-
1) the abbreviation SVC;
2) the procedure signal QSP;
3) if required, the procedure signal RQ, NO or CNL to request, refuse or cancel a diversion;
4) identification of the routing areas, States, territories, locations, or stations for which the diversion applies;
5) the end-of-text signal.
Note: The following examples illustrate application of the above-mentioned procedures-
a) to request a diversion:
b) to accept a diversion:
c) to refuse a diversion:
d) to cancel a diversion:
SCHEDULE 3 Message Format - International Alphabet No. 5 (IA-5) (regs 28, 52, 53 and 54)
1.0
Message format - international alphabet No. 5 (IA-5)
1.1
When it has been agreed between the administrations concerned to use International Alphabet No. 5 (IA-5) the format described in 1.1 through 1.3 shall be used. All messages, other than those prescribed in regulation 47 and 1.1.5 shall comprise the components specified in 1.1.1 to 1.1.6 inclusive.
Note 1: An illustration of the IA-5 message format is given in Figure 1-1.
Note 2: In the subsequent standards relative to message format the following symbols have been used in making reference to the functions assigned to certain signals in IA-5. Symbol signification-
<< CARRIAGE RETURN (character position 0/13)
LINE FEED (character position 0/10)
SPACE (character position 2/0).
1.1.1
Heading
1.1.1.1
The heading shall comprise-
(a) start-of-heading (SOH) character 0/1;
(b) transmission identification comprising-
1) circuit or link identification;
2) channel-sequence number;
(c) additional service information (if necessary) comprising-
1) one SPACE;
2) no more than 10 characters.
1.1.1.1.1
On point-to-point circuits or links, the identification shall consist of three letters selected and assigned by the transmitting station; the first letter identifying the transmitting, the second letter the receiving end of the circuit, and the third letter the channel. Where only one channel exists, the letter A shall be assigned. Where more than one channel between stations is provided, the channels shall be identified as A, B, C, etc., in respective order. On multipoint channels, the identification shall consist of three letters selected and assigned by the circuit control or master station.
1.1.1.1.2
Except as provided in 1.1.1.3 three-digit channel-sequence numbers from 001 to 000 (representing 1000) shall be assigned sequentially by telecommunication stations to all messages transmitted directly from one station to another. A separate series of these numbers shall be assigned for each channel and a new series shall be started daily at 0000 hours.
1.1.1.1.3
The expansion of the channel-sequence number to preclude duplication of the same numbers during the 24-hour period shall be permitted subject to agreement between the Authorities responsible for the operation of the circuit.
1.1.1.1.4
The transmission identification shall be sent over the circuit in the following sequence-
a) transmitting-terminal letter;
b) receiving-terminal letter;
c) channel-identification letter;
d) channel-sequence number.
1.1.1.1.5
Additional service information shall be permitted to be inserted following the transmission identification subject to agreement between the Authorities responsible for the operation of the circuit. Such additional service information shall be preceded by a SPACE () followed by not more than 10 characters inserted into the heading of message immediately following the last digit of the channel-sequence number and shall not contain any alignment functions. When no such additional service information is added the information in 1.11.1.4 shall be followed immediately by that of 1.1.2.
1.1.2
Address
1.1.2.1
The address shall comprise-
a) alignment function ;
b) priority indicator;
c) addressee indicator(s);
d) alignment function .
1.1.2.1.1
The priority indicator shall consist of the appropriate two-letter group assigned by the originator in accordance with the following-
Message part
Component of the message part
Elements of the component
Teletypewriter character
H
HEADING LINE
Start-of- Heading Character
One character (0/1)
SOH
Transmission Identification
a) Transmitting-terminal letter
-
E
b) Receiving-terminal letter
c) Channel-identification letter
A
d) Channel-sequence number
If necessary, additional service indication
a) One SPACE
D
b) No more than the remainder of the line
I
ADDRESS
Alignment function
One CARRIAGE RETURN, one LINE FEED
<
N
Priority Indicator
The relevant 2-letter group
-
G
Addressee Indicator(s)
One SPACE and an 8-letter group Example: EGLLZRZX EGLLYKYX EGLLACAD
Alignment Function(s)
One CARRIAGE RETURN, one LINE FEED
<
ORIGIN
Filing time
6 digit date-time group specifying when the message was filed for transmission
..................
Originator indicator
a) One SPACE
...........
b) 8-letter group identifying the message originator
Priority Alarm(used only in teletypewriter operation for distress messages)
Five characters (0/1)(BEL)
Optional Heading Information
a) One SPACE
b) Additional data not to exceed the remainder of the line
Alignment function
One CARRIAGE RETURN, one LINE FEED
<
Start of text character
One character (0/2)
STX
TEXT
Beginning of Text
Specific identification of Addressees (if necessary) with each followed by on CARRIAGE RETURN, one LINE FEED (if necessary) The English word FROM (if necessary)
Specific identification of Originator (if necessary)
The English word STOP followed by one CARRIAGE RETURN, one LINE FEED (if necessary) and/or Originator's reference (if used)
Message Text
Message Text with one CARRIAGE RETURN, one LINE FEED at the end of each printed line of the Text except for the last one
Confirmation (if necessary)
a) One CARRIAGE RETURN, one LINE FEED
b) The abbreviation CFM followed by the portion of the TEXT being confirmed.
Correction (if necessary)
a) One CARRIAGE RETURN, one LINE FEED
b) The abbreviation COR followed by the correction of an error made in the preceding TEXT
ENDING
Alignment function
One CARRIAGE RETURN, one LINE FEED
<
Page-feed Sequence
One character (0/11)
VT
End-of Text Character
One character (0/3)
ETX
Figure 1-1. Message format International Alphabet No. 5 (IA-5)
Priority indicator
Message category
SS
distress messages
DD
urgency messages
FF
flight safety messages
GG
meteorological messages
GG
flight regularity messages
GG
aeronautical information services messages
KK
aeronautical administrative messages as appropriate service messages
1.1.2.1.2
The order of priority shall be the same as specified in regulation 41.
1.1.2.1.3
An addressee indicator, which shall be immediately preceded by a SPACE, except when it is the first address indicator of the second or third line of addresses, shall comprise-
a) the four-letter location indicator of the place of destination;
b) the three-letter designator identifying the organisation/function (aeronautical authority, service or aircraft operating agency) addressed;
c) an additional letter, which shall represent a department, division or process within the organisation/function addressed. The letter X shall be used to complete the address when explicit identification is not required.
1.1.2.1.3.1
Where a message is to be addressed to an organisation that has not been allocated an ICAO three-letter designator of the type prescribed in 1.1.2.1.3 the location indicator of the place of destination shall be followed by the ICAO three-letter designator YYY (or the ICAO three-letter designator YXY in the case of a military service or organisation). The name of the addressee organisation shall then be included in the first item in the text of the message. The eighth position letter following the ICAO three-letter designator YYY or YXY shall be the filler letter X.
1.1.2.1.3.2
Where a message is to be addressed to an aircraft in flight and, therefore, requires handling over the AFTN for part of its routing before retransmission over the Aeronautical Mobile Service, the location indicator of the aeronautical station which is to relay the message to the aircraft shall be followed by the ICAO three-letter designator ZZZ. The identification of the aircraft shall then be included in the first item of the text of the message. The eighth position letter following the ICAO three-letter designator ZZZ shall be the filler letter X.
1.1.2.1.4
The complete address shall be restricted to three lines of page-printing copy, and, except as provided in 1.2 a separate addressee indicator shall be used for each addressee whether at the same or different locations.
1.1.2.1.5
The completion of the addressee indicator group(s) in the address of a message shall be immediately followed by the alignment function.
1.1.2.1.6
Where messages are offered in page-copy form for transmission and contain more addressee indicators than can be accommodated on three lines of a page copy, such messages shall be converted, before transmission, into two or more messages, each of which shall conform with the provisions of 1.1.2.1.5. During such conversion, the addressee indicators shall, in so far as practicable, be positioned in the sequence which will ensure that the minimum number of retransmissions will be required at subsequent communication centres.
1.1.2.2
Origin
The origin shall comprise-
a) filing time;
b) originator indicator;
c) priority alarm (when necessary);
d) optional heading information;
e) alignment function [<<=];
f) start-of-text character, character 0/2 (STX).
1.1.2.2.1
The filing time shall comprise the 6-digit date-time group indicating the date and time of filing the message for transmission.
1.1.2.2.2
The originator indicator, which shall be immediately preceded by a SPACE, shall comprise-
a) the four-letter location indicator of the place at which the message is originated;
b) the three-letter designator identifying the organisation/function (aeronautical authority, service or aircraft operating agency) which originated the message;
c) an additional letter which shall represent a department, division or process within the organisation/function of the originator. The letter X shall be used to complete the address when explicit identification is not required.
1.1.2.2.3
Where a message is originated by an organisation that has not been allocated an ICAO three-letter designator of the type prescribed in 1.2.2.2, the location indicator of the place at which the message is originated shall be followed immediately by the ICAO three-letter designator YYY followed by the filler letter X (or the ICAO three-letter designator YXY followed by the filler letter X in the case of a military service or organisation). The name of the organisation (or military service) shall then be included in the first item in the text of the message.
1.1.2.2.3.1
Messages relayed over the AFTN that have been originated in other networks shall use a valid AFTN originator indicator that has been agreed for use by the relay or gateway function linking the AFTN with the external network.
1.1.2.2.4
Where a message originated by an aircraft in flight requires handling on the AFTN for part of its routing before delivery, the originator indicator shall comprise the location indicator of the aeronautical station responsible for transferring the message to the AFTN, followed immediately by the ICAO three-letter designator ZZZ followed by the filler letter X. The identification of the aircraft shall then be included in the first item in the text of the message.
1.1.2.2.5
The priority alarm shall be used only for distress messages. When used it shall consist of five successive BEL (0/7) characters.
Note: Use of the priority alarm will actuate a bell (attention) signal at the receiving teletypewriter station, other than at those fully automatic stations which may provide a similar alarm on receipt of priority indicator SS, thereby alerting supervisory personnel at relay centres and operators at tributary stations, so that immediate attention may be given to the message.
1.1.2.2.6
The inclusion of optional data in the origin line shall be permitted provided a total of 69 characters is not exceeded and subject to agreement between the Administrations concerned. The presence of the optional data field shall be indicated by one occurrence of the SPACE character immediately preceding optional data.
1.1.2.2.6.1
When additional addressing information in a message needs to be exchanged between source and destination addresses, it shall be conveyed in the optional data field (ODF), using the following specific format-
a) characters one and full stop (1.) to indicate the parameter code for the additional address function;
b) three modifier characters, followed by an equal sign (=) and the assigned 8-character ICAO address; and
c) the character hyphen (-) to terminate the additional address parameter field.
1.1.2.2.6.1.1
When a separate address for service messages or inquiries is different from the originator indicator, the modifier SVC shall be used.
1.1.2.2.7
The origin line shall be concluded by an alignment function [<<=] and the start-of-text (STX) (0/2) character.
1.1.3 Text
1.1.3.1
The text of messages shall be drafted in accordance with 1.1.5 and shall consist of all data between STX and ETX.
Note - When message texts do not require conversion to the ITA-2 code and format and do not conflict with ICAO message types or formats in PANS-ATM (ICAO Doc 4444), Administrations may make full use of the characters available in International Alphabet No. 5 (IA-5).
1.1.3.2
When an originator's reference is used, it shall appear at the beginning of the text, except as provided in 1.1.3.3 and 1.1.3.4.
1.1.3.3
When the ICAO three-letter designators YXY, YYY or ZZZ comprise the second element of the addressee indicator and it, therefore, becomes necessary to identify in the text the specific addressee of the message, such identification group shall precede the originator's reference (if used) and become the first item of the text.
1.1.3.4
When the ICAO three-letter designators YXY, YYY or ZZZ comprise the second element of the originator indicator and it thus becomes necessary to identify in the text the name of the organisation (or military service) or the aircraft which originated the message, such identification shall be inserted in the first item of the text of the message.
1.1.3.5
When applying the provisions of 1.1.3.3 and 1.1.3.4 to messages where the ICAO three-letter designator(s) YXY, YYY, ZZZ refer to two or more different organisations (or military services), the sequence of further identification in the text shall correspond to the complete sequence used in the address and originator indicator of the message. In such instance, each addressee identification shall be followed immediately by an alignment function. The name of the (YXY, YYY or ZZZ) organisation originating the message shall then be preceded with "FROM", "STOP" followed by an alignment function shall then be included in the text at the end of this identification and preceding the remainder of text.
1.1.3.6
An alignment function shall be transmitted at the end of each printed line of the text. When it is desired to confirm a portion of the text of a message in teletypewriter operation, such confirmation shall be separated from the last text group by an alignment function , and shall be indicated by the abbreviation CFM followed by the portion being confirmed.
1.1.3.7
Where messages are prepared off-line, e.g. by preparation of a paper tape, errors in the text shall be corrected by backspacing and replacing the character in error by character DEL (7/15).
1.1.3.8
Corrections to textual errors made in on-line operations shall be corrected by inserting following the error, then retyping the last correct word (or group).
1.1.3.9
When it is not discovered until later in the origination process that an error has been made in the text, the correction shall be separated from the last text group, or confirmation, if any, by an alignment function . This shall be followed by the abbreviation COR and the correction.
1.1.3.10
Stations shall make all indicated corrections on the page-copy prior to local delivery or a transfer to a manually operated circuit.
1.1.3.11
When messages are transmitted only on low-speed circuits, the text of messages entered by the AFTN origin station shall not exceed 1 800 characters in length. AFTN messages exceeding 1 800 characters shall be entered by the AFTN origin station in the form of separate messages.
Note 1. - Low-speed circuits operate at 300 bits per second or less.
Note 2. - The character count includes all printing and non-printing characters in the text from, but not including, the start-of-text signal to, but not including, the first alignment function of the ending.
1.1.3.11.1
The transmission on medium-or high-speed circuits of AFTN messages with text exceeding 1 800 characters that have not been entered by the AFTN origin station in the form of separate messages shall be subject to agreement between the Administrations concerned and not diminish the performance characteristics of the network or link.
Note 1: Medium-speed circuits operate at speeds in the range between 300 and 3 000 bits per second. High-speed circuits operate at speeds in excess of 3 000 bits per second.
Note 2: The character count includes all printing and non-printing characters in the text from, but not including,
1.1.3.12
Ending
1.1.3.12.1
The ending of a message shall comprise the following in the order stated-
a) an alignment function following the last line of text;
b) page-feed character, character 0/11 (VT);
c) end-of-text character 0/3 (ETX).
1.1.3.12.1.1
Station terminal equipment (page printers) on the International Alphabet Number 5 (IA-5) shall be provided with a capability to generate sufficient line feed functions for local station use upon the reception of a VERTICAL TAB character (0/11).
1.1.3.12.1.2
When the message does not transit ITA-2 portions of the AFTN, or where Administrations have made provisions to add automatically the second carriage return before transmission to an ITA-2 circuit, one carriage return in the alignment function and end-of-line function shall be permitted subject to agreement between the Administrations concerned.
1.1.3.12.1.3
Messages entered by the AFTN origin station shall not exceed 2 100 characters in length, when transmitted only on low-speed circuits.
Note 1: Low-speed circuits operate at 300 bits per second or less.
Note 2: The character count includes all printing and non-printing characters in the message from and including the start-of-heading character (SOH) to and including the end-of-text character.
1.1.3.12.1.4
The transmission on medium- or high-speed circuits of AFTN messages exceeding 2 100 characters that have not been entered by the AFTN origin station in the form of separate messages shall be subject to agreement between the Administrations concerned and not diminish the performance characteristics of the network or link.
Note 1: Medium-speed circuits operate at speeds in the range between 300 and 3 000 bits per second. High-speed circuits operate at speeds in excess of 3 000 bits per second.
Note 2: The character count includes all printing and non-printing characters in the message from and including the start-of-heading character (SOH) to and including the end-of-text character.
1.1.4
Except as provided in 1.1.5 to 1.1.6 and 116, the procedures of regulations 49 to 51 shall be used for messages using IA-5 code.
1.1.4.1
The transmission of message texts that do not require conversion to the IA-2 code and format and with message lines containing more than 69 printable and non-printable characters shall be subject to agreement between the Administrations concerned.
1.1.5
Channel-check transmissions. In the case where continuous control of channel condition is not provided the following periodic transmissions shall be sent on teletypewriter circuits-
1) heading line;
S
2) alignment function T
X
3) the procedure signal CH;
E
4) alignment function T.
X
The receiving station shall then check the transmission identification of this incoming transmission to ensure its correct sequence in respect of all messages received over that incoming channel.
Note: Application of this procedure provides some measure of assurance that channel continuity is maintained; however, a continuously controlled channel is much more preferable in that data integrity can also be improved.
1.1.5.1
Where a circuit is unoccupied and uncontrolled, the transmission identified in 1.1.5 shall be sent at H + 00, H + 20, H + 40.
1.1.6
The receipt of distress messages (priority indicator SS) shall be individually acknowledged by the AFTN destination station by sending a service message to the AFTN origin station. Such acknowledgement of receipt shall take the format of a complete message addressed to the AFTN origin station, shall be assigned priority indicator SS and the associated priority alarm, and shall have a text comprising-
1) the procedure signal R;
2) the origin line without priority alarm, or optional heading information of the message being acknowledged;
3) the ending.
Note: The following example illustrates the application of the 1.6 procedures-
Heading
SS LECBZRZX
121322 EGLLYFYX (Priority Alarm)
S
TR 121319 LECBZRZX
X
Ending (see 1.1.3.12.1).
1.2
Action taken on mutilated messages in IA-5 detected in computerised AFTN relay stations
1.2.1
On channels employing continuous control the mutilation detection and subsequent recovery shall be a function of the link control procedures and shall not require the subsequent sending of service or CHECK TEXT NEW ENDING ADDED messages.
1.2.2
On channels not employing continuous control the relay station shall employ the following procedures-
1.2.2.1
If, during the reception of a message a relay station detects that the message has been mutilated at some point ahead of the end-of-text character, it shall-
1) cancel the onward routing responsibility for the message;
2) send a service message to the transmitting station requesting a retransmission.
Note: The following example illustrates a typical text of a service message in which the foregoing procedure has been applied in respect of a mutilated message-
1.2.2.2
When the provisions of 1.2.2.1 are applied, the station receiving the service message shall reassume responsibility for the referenced message with a new (i.e. correct in sequence) transmission identification. If that station is not in possession of an unmutilated copy of the original message, it shall send a message to the originator as identified by the originator indicator in the origin of the mutilated message, requesting repetition of the incorrectly received message.
Note: The following example illustrates a typical text of a service message in which the foregoing procedure has been applied in respect of a mutilated message having as its origin-
"141335 CYULACAX":
1.2.3
If, after transmission of the text material of a message, a relay station can detect that there is no complete end-of-text character, but has no practical means of discovering whether the irregularity has affected only the end-of-text character, or whether it has also caused part of the original text to have been lost, it shall insert into the channel the following-
1) CHECKTEXT NEWENDING ADDED;
2) its own station identification;
3) (ending -see 1.1.3.12.1).
1.3
Transfer of AFTN messages over code and byte independent circuits and networks
When AFTN messages are transferred across code and byte independent circuits and networks of the AFS, the following shall apply.
1.3.1
Except as provided in 1.3.3 the heading line of the message shall be omitted. The message shall start with an alignment function followed by the address.
1.3.2
The message shall end with a complete ending.
1.3.3
For the purposes of technical supervision, entry centres shall be permitted to insert additional data preceding the first alignment function and/or following the ending of the message.
1.3.3.1
When the provisions of 1.3.3 are applied, the data added shall not include either carriage return or line feed characters or any of the combinations listed in 1.1.3 of Schedule 1.
SCHEDULE 4 ATS Message Handling Services (TSMHS) and Inter-Centre Communications (ICC) (reg 55)
1.1
ATS Message Handling Services (ATSMHS)
The ATS message service of the ATS (air traffic services) message handling service (ATSMHS) application shall be used to exchange ATS messages between users over the aeronautical telecommunication network (ATN) internet.
Note 1: The ATS message service comprised in the ATS message handling service application aims at providing generic message services over the ATN internet communication service (ICS). It may, in turn, be used as a communication system by user-applications communicating over the ATN. This may be achieved, for example, by means of application programme interfaces to the ATS message service.
Note 2: The detailed specification of the ATS message handling service application is included in the Manual of Technical Provisions for the Aeronautical Telecommunication Network (ATN) (ICAO Doc 9705), Sub-volume III.
Note 3: The ATS message service is provided by the implementation over the ATN internet communication service of the message handling systems specified in ISO/lEC (International Organisation for Standardisation/International Electrotechnical Commission) 10021 and ITU-T (International Telecommunication Union - Telecommunication Standardisation Sector) X.400 and complemented by the additional requirements specified in the Manual of Technical Provisions for the Aeronautical Telecommunication Network (ATN) (ICAO Doc 9705). The two sets of documents, the ISO/IECMOTIS (Message-Oriented Text Interchange System) International Standards and the ITU-T X.400 Series of Recommendations (1988 or later) are, in principle, aligned with each other. However, there are a small number of differences. In the above-mentioned document, reference is made to the relevant ISO International Standards and International Standardised Profiles (ISP), where applicable. Where necessary, e.g. for reasons of interworking or to point out differences, reference is also made to the relevant X.400 Recommendations.
Note 4.- The following types of ATN end systems performing ATS message handling services are defined in the Manual of Technical Provisions for the Aeronautical Telecommunication Network (ATN) (ICAO Doc 9705), Sub-volume III-
1) an ATS message server;
2) an ATS message user agent;
3) an AFTN/AMHS gateway (aeronautical fixed telecommunication network/ATS message handling system); and
Connections may be established over the internet communications service between any pair constituted of these ATN end systems (see Table 1-1).
1.2
Inter-Centre Communications (ICC)
The inter-centre communications (ICC) applications set shall be used to exchange ATS messages between air traffic service users over the ATN internet.
Note 1: The ICC applications set enables the exchange of information in support of the following operational services-
a) flight notification;
b) flight coordination;
c) transfer of control and communications;
Table 1-1: Communications between ATN end systems implementing ATS message handling services
ATN End System 1
ATN End System 2
ATS Message Server
ATS Message Server
ATS Message Server
AFTN/AMHS Gateway
ATS Message Server
ATS Message User Agent
AFTN/AMHS Gateway
AFTN/AMHS Gateway
d) flight planning;
e) airspace management; and
f) air traffic flow management.
Note 2: The first of the applications developed for the ICC set is the ATS inter-facility data communication (AIDC).
Note 3: The AIDC application exchanges information between ATS units (ATSUs) for support of critical air traffic control (ATC) functions, such as notification of flights approaching a flight information region (FIR) boundary, coordination of boundary conditions and transfer of control and communications authority.
Note 4: The detailed specification of the AIDC application is included in the Manual of Technical Provisions for the Aeronautical Telecommunication Network (ATN) (ICAO Doc 9705), Sub-volume III.
Note 5: The AIDC application is strictly an ATC application for exchanging tactical control information between ATS units. It does not support the exchange of information with other offices or facilities.
Note 6: The AIDC application supports the following operational services-
a) flight notification;
b) flight coordination;
c) transfer of executive control;
d) transfer of communications; and
e) transfer of general information (flight-related data or free text messages, i.e. unstructured).
SCHEDULE 5 Aeronautical Mobile Service - Voice Communications (regs 58, 69 and 70)
1. Categories of messages in aeronautical mobile service - voice communications
Table 1.1: Categories of Messages
Message category and order of priority
Radio telephony signal
a)
Distress call, distress messages and distress traffic
MAYDAY
b)
Urgency messages, including messages preceded by the medical transports' signals
PAN, PAN or PAN, PAN MEDICAL
c)
Communications relating to direction finding
-
d)
Flight safety messages
-
e)
Meteorological messages
-
f)
Flight regulatory messages
-
2.1 Radiotelephony procedures
2.1.1 General
2.1.1.1
When a controller or pilot communicates via voice, the response shall be via voice. Except when a controller or pilot communicates via CPDLC, the response shall be via CPDLC
2.1.1.2
Language to be used.
2.1.1.2.1
The air-ground radiotelephony communications shall be conducted in the language normally used by the station on the ground or in the English language.
2.1.1.2.2
The English language shall be available, on request from any aircraft station, at all stations on the ground serving designated airports and routes used by international air services.
2.1.1.2.3
The languages available at a given station on the ground shall form part of the Aeronautical Information Publications and other published aeronautical information concerning such facilities.
2.1.1.3
Word spelling in radiotelephony. When proper names, service abbreviations and words of which the spelling is doubtful are spelled out in radiotelephony the alphabet in Figure 2-1 shall be used.
2.1.1.4
Transmission of numbers in radiotelephony
2.1.1.4.1
Transmission of numbers
2.1.1.4.1.1
All numbers, except as prescribed in 2.1.1.4.1.2, shall be transmitted by pronouncing each digit separately.
The following examples illustrate the application of this procedure
Aircraft Call Signs
Transmitted As
CCA 238
Air China two three eight
OAL 242
Olympic two four two
Flight Levels
Transmitted As
FL 180
flight level one eight zero
FL 200
flight level two zero zero
Headings
Transmitted As
100 degrees
heading one zero zero
080 degrees
heading zero eight zero
Wind Direction And Speed
Transmitted As
200 degrees 70 knots
wind one six zero degrees one
160 degrees 18 knots
wind one six zero degrees one gusting 30 knots eight knots gusting three zero knots
Transponder Codes
Transmitted As
2 400
squawk two four zero zero
4 203
squawk four two zero three
Runway
Transmitted As
27
runway two seven
30
runway three zero
Altimeter Setting
Transmitted As
1010
QNH one zero one zero
1000
QNH one zero zero zero
2.1.1.4.1.2
All numbers used in the transmission of altitude, cloud height, visibility and runway visual range (RVR) information, which contain whole hundreds and whole thousands, shall be transmitted by pronouncing each digit in the number of hundreds or thousands followed by the word HUNDRED or THOUSAND as appropriate. Combinations of thousands and whole hundreds shall be transmitted by pronouncing each digit in the number of thousands followed by the word THOUSAND followed by the number of hundreds followed by the word HUNDRED.
The following examples illustrate the application of this procedure
Letter
Word
Approximate pronunciation
International Phonetic Convention
Latin alphabet representation
A
Alfn
'ælfa
AL FAH
B
Bravo
'bra:'vo
BRAH VOH
C
Charlie
CHAR LEE or SHAR LEE
D
Delta
'delta
DELL TAH
E
Echo
'eko
ECK OH
F
Foxtrot
'fokstrot
FOKS TROT
G
Golf
gAlf
GOLF
H
Hotel
ho'tel
HO TELL
I
India
'indi.a
IN DEE AH
J
Julielt
d3u:li.'et
JEW LEE ETT
K
Kilo
'ki:lo
KEY LOH
L
Lima
'li:ma
LEE MAH
M
Mike
moik
MIKE
N
November
NO VEM BER
O
Oscar
OSS CAH
P
Papa
PAH PAH
Q
Quebec
ke'bek
KEH BECK
R
Romeo
'ro:mi.o
ROW ME OH
S
Sierra
si'era
SEE AIR RAH
T
Tango
'tœngo
TANG GO
U
Uniform
'ju:nifo:m or 'u:niform
YOU NEE FORM or OO NEE FORM
V
Victor
'vikta
VIK TAH
W
Whisky
'wiski
WISS KEY
X
X-ray
'eks'rei
ECKS RAY
Y
Yankee
'jænki
YANG KEY
Z
Zulu
'zu:lu:
ZOO LOO
Note: In the approximate representation using the Latin alphabet, syllables to be emphasised are underlined.
Note 1: The pronunciation of the words in the alphabet may vary according to the language habits of the speakers. In order to eliminate wide variations in pronunciation, posters illustrating the desired pronunciation are available from ICAO.
Figure 2-1
altitude
transmitted as
800
eight hundred
3400
three thousand four hundred
12000
one two thousand
cloud height
transmitted as
2200
two thousand two hundred
4300
four thousand three hundred
visibility
transmitted as
1000
visibility one thousand
700
visibility seven hundred
runway visual range
transmitted as
600
RVR six hundred
1700
RVR one thousand seven hundred
2.1.1.4.1.3
Numbers containing a decimal point shall be transmitted as prescribed in 2.1.1.4.1.1 with the decimal point in appropriate sequence being indicated by the word DECIMAL.
Note 1: The following examples illustrate the application of this procedure-
Number
Transmitted as
100.3
ONE ZERO ZERO DECIMAL THREE,
38143.9
THREE EIGHT ONE FOUR THREE DECIMAL NINE
Note 2: For identification of VHF frequencies the number of digits used after the decimal point are determined on the basis of the channel spacing (2.1.1.7.3.4.3 refers to frequencies separated by 25 kHz, 2.1.1.7.3.4.4 refers to frequencies separated by 8.33 kHz).
Note 3: The channelling/frequency pairing relationship for 8.33 kHz and 25 kHz is found in Table 4-1(bis), (CNS Technical Standards Volume V).
2.1.1.4.1.4
When transmitting time, only the minutes of the hour shall normally be required. Each digit shall be pronounced separately. However, the hour shall be included when any possibility of confusion is likely to result.
Note: The following example illustrates the application of this procedure when applying the provisions of 2.1.1.4.1.4-
Time
Statement
0920 (9:20 A.M.) TOO ZE-RO or ZE-RO NIN-er TOO ZE-RO
1643 (4:43 P.M.) FOW-er TREE or WUN SIX FOW-er TREE
2.1.1.4.2
Verification of numbers
2.1.1.4.2.1
When it is desired to verify the accurate reception of numbers the person transmitting the message shall request the person receiving the message to read back the numbers.
2.1.1.4.3
Pronunciation of numbers
2.1.1.4.3.1
When the language used for communication is English, numbers shall be transmitted using the following pronunciation-
Numeral or numeral element
Pronunciation
0
ZE-RO
1
WUN
2
TOO
3
TREE
4
FOW-er
5
FIFE
6
SIX
7
SEV-en
8
AIT
9
NIN-er
Decimal
DAY-SEE-MAL
Hundred
HUN-dred
Thousand
TOU-SAND
Note: The syllables printed in capital letters in the above list are to be stressed; for example, the two syllables in ZE-RO are given equal emphasis, whereas the first syllable of FOW-er is given primary emphasis.
2.1.1.5
Transmitting technique
2.1.1.5.1
Each written message shall be read prior to commencement of transmission in order to eliminate unnecessary delays in communications.
2.1.1.5.2
Transmissions shall be conducted concisely in a normal conversational tone.
2.1.1.5.3
Speech transmitting technique shall be such that the highest possible intelligibility is incorporated in each transmission. Fulfilment of this aim requires that air crew and ground personnel shall-
a) enunciate each word clearly and distinctly;
b) maintain an even rate of speech not exceeding 100 words per minute. When a message is transmitted to an aircraft and its contents need to be recorded the speaking rate shall be at a slower rate to allow for the writing process. A slight pause preceding and following numerals makes them easier to understand;
c) maintain the speaking volume at a constant level;
d) be familiar with the microphone operating techniques particularly in relation to the maintenance of a constant distance from the microphone if a modulator with a constant level is not used;
e) suspend speech temporarily if it becomes necessary to turn the head away from the microphone.
2.1.1.5.4
Speech transmitting technique shall be adapted to the prevailing communications conditions.
2.1.1.5.5
Messages accepted for transmission shall be transmitted in plain language or ICAO phraseologies without altering the sense of the message in any way. Approved ICAO abbreviations contained in the text of the message to be transmitted to aircraft shall normally be converted into the unabbreviated words or phrases which these abbreviations represent in the language used, except for those which, owing to frequent and common practice, are generally understood by aeronautical personnel.
2.1.1.5.6
To expedite communication, the use of phonetic spelling shall be dispensed with, if there is no risk of this affecting correct reception and intelligibility of the message.
2.1.1.5.7
The transmission of long messages shall be interrupted momentarily from time to time to permit the transmitting operator to confirm that the frequency in use is clear and, if necessary, to permit the receiving operator to request repetition of parts not received.
2.1.1.5.8
The following words and phrases shall be used in radiotelephony communications as appropriate and shall have the meaning ascribed hereunder-
Phrase
Meaning
ACKNOWLEDGE
"Let me know that you have received and understood this message."
'AFFIRM
"Yes."
APPROVED
"Permission for proposed action granted."
BREAK
"I hereby indicate the separation between portions of the message." (To be used where there is no clear distinction between the text and other portions of the message.)
BREAK BREAK
"I hereby indicate the separation between messages transmitted to different aircraft in a very busy environment."
CANCEL
"Annul the previously transmitted clearance."
CHECK
"Examine a system or procedure." (Not to be used in any other context. No answer is normally expected.)
CLEARED
"Authorised to proceed under the conditions specified."
CONFIRM
"I request verification of: (clearance, instruction, action, information)."
CONTACT
"Establish communications with..."
CORRECT
"True" or "Accurate".
CORRECTION
"An error has been made in this transmission (or message indicated). The correct version is..."
DISREGARD
"Ignore."
HOW DO YOU READ
"What is the readability of my transmission?"
I SAY AGAIN
"I repeat for clarity or emphasis."
MAINTAIN
"Continue in accordance with the condition(s) specified" or in its literal sense, e.g. "Maintain VFR".
MONITOR
"Listen out on (frequency)."
NEGATIVE
"No" or "Permission not granted" or "That is not correct" or "Not capable".
OVER
"My transmission is ended, and I expect a response from you."
Note: Not normally used in VHF or satellite voice communications.
OUT
"This exchange of transmissions is ended and no response is expected."
Note: Not normally used in VHF or satellite voice communications.
READ BACK
"Repeat all, or the specified part, of this message back to me exactly as received."
RECLEARED
"A change has been made to your last clearance and this new clearance supersedes your previous clearance or part thereof."
REPORT
"Pass me the following information..."
REQUEST
"I should like to know..." or "I wish to obtain..."
ROGER
"I have received all of your last transmission."
Note: Under no circumstances to be used in reply to a question requiring "READBACK" or a direct answer in the affirmative (AFFIRM) or negative (NEGATIVE).
SAY AGAIN
"Repeat all, or the following part, of your last transmission,"
SPEAK SLOWER
"Reduce your rate of speech."
Note: For normal rate of speech.
STANDBY
"Wait and I will call you."
Note: The caller would normally re-establish contact if the delay is lengthy. STANDBY is not an approval or denial.
UNABLE
"I cannot comply with your request, instruction, or clearance."
Note: UNABLE is normally followed by a reason.
WILCO
(Abbreviation for "will comply".) "I understand your message and will comply with it."
WORDS TWICE
a) As a request: "Communication is difficult. Please send every word, or group of words, twice.
b) As information: "Since communication is difficult, every word, or group of words, in this message will be sent twice."
2.1.1.6
Composition of messages
2.1.1.6.1
Messages handled entirely by the aeronautical mobile service shall comprise the following parts in the order stated-
a) call indicating the addressee and the originator;
b) text.
Note: The following examples illustrate the application of this procedure-
(call)
NEW YORK RADIO SWISSAIR ONE ONE ZERO
(text)
REQUEST SELCAL CHECK or
(call)
SWISSAIR ONE ONE ZERO NEW YORK RADIO
(text)
CONTACT SAN JUAN ON FIVE SIX
2.1.1.6.2
Messages requiring handling by the AFTN for part of their routing and similarly messages which are not handled in accordance with predetermined distribution arrangements shall be composed as follows-
2.1.1.6.2.1
When originated in an aircraft-
1) call;
2) the word FOR;
3) the name of the organisation addressed;
4) the name of the station of destination;
5) the text.
2.1.1.6.2.1.1
The text shall be as short as practicable to convey the necessary information; full use shall be made of ICAO phraseologies.
Note: The following example illustrates the application of this procedure-
(call)
BOSTON RADIO SWISSAIR ONE TWO EIGHT (address) FOR SWISSAIR BOSTON
(text)
NUMBER ONE ENGINE CHANGE REQUIRED
2.1.1.6.2.2
When addressed to an aircraft. When a message is retransmitted by an aeronautical station to an aircraft in flight, the heading and address of the AFTN message format shall be omitted during the retransmission on the aeronautical mobile service.
2.1.1.6.2.2.1
When the provisions of 2.1.1.6.2.2 are applied, the aeronautical mobile service message transmission shall comprise-
(a) the text [incorporating any corrections (COR) contained in the AFTN message];
(b) the word FROM;
(c) the name of the originating organisation and its location (taken from the origin section of the AFTN message).
2.1.1.6.2.2.2
When the text of a message to be transmitted by an aeronautical station to an aircraft in flight contains approved ICAO abbreviations, these abbreviations shall normally be converted during the transmission of the message into the unabbreviated words or phrases which the abbreviations represent in the language used, except for those which, owing to frequent or common practice, are generally understood by aeronautical personnel.
2.1.1.7
Calling
2.1.1.7.1
Radiotelephony call signs for aeronautical stations
2.1.1.7.1.1
Aeronautical stations in the aeronautical mobile service shall be identified by-
a) the name of the location; and
b) the unit or service available.
2.1.1.7.1.2
The unit or service shall be identified in accordance with the table below except that the name of the location or the unit/service may be omitted provided satisfactory communication has been established.
Unit/service available
Call sign suffix
area control centre
CONTROL
approach control
APPROACH
approach control radar arrivals
ARRIVAL
approach control radar departures
DEPARTURE
aerodrome control
TOWER
surface movement control
GROUND
radar (in general)
RADAR
precision approach radar
PRECISION
direction-finding station
HOMER
flight information service
INFORMATION
clearance delivery
DELIVERY
apron control
APRON
company dispatch
DISPATCH
aeronautical station
RADIO
2.1.1.7.2
Radiotelephony call signs for aircraft
2.1.1.7.2.1
Full call signs
2.1.1.7.2.1.1
An aircraft radiotelephony call sign shall be one of the following types-
Type a)
- the characters corresponding to the registration marking of the aircraft;
Type b)
- the telephony designator of the aircraft operating agency, followed by the last four characters of the registration marking of the aircraft; or
Type c)
- the telephony designator of the aircraft operating agency, followed by the flight identification.
2.1.1.7.2.2
Abbreviated call signs
2.1.1.7.2.2.1
The aircraft radiotelephony call signs shown in 2.1.1.7.2.1.1, with the exception of Type c), may be abbreviated in the circumstances prescribed in 2.1.1.7.3.3.1. Abbreviated call signs shall be in the following form-
Type a)
- the first character of the registration and at least the last two characters of the call sign;
Type b)
- the telephony designator of the aircraft operating agency, followed by at least the last two characters of the call sign;
Type c)
- no abbreviated form.
Table 2-1: Examples of full call signs and abbreviated call signs
Type a)
Type b)
Type c)
Full call sign
N 57826
*CESSNA FABCD
* CITATION FABCD
VARIG PVMA
SCANDINAVIAN 937
Abbreviated call sign
N26
CESSNA CD
CITATION CD
VARIG MA
(no abbreviated form)
or
or
Ol
or
N826
CESSNA
CITATION
VARIG
BCD
BCD
VMA
Note: Either the name of the aircraft manufacturer or of the aircraft model may be used in place of the first character in Type a).
2.1.1.7.3
Radiotelephony procedures
2.1.1.7.3.1
An aircraft shall not change the type of its radiotelephony call sign during flight, except temporarily on the instruction of an air traffic control unit in the interests of safety.
2.1.1.7.3.1.1
Except for reasons of safety no transmission shall be directed to an aircraft during take-off, during the last part of the final approach or during the landing roll.
2.1.1.7.3.2
Establishment of radiotelephony communications
2.1.1.7.3.2.1
Full radiotelephony call signs shall always be used when establishing communication. The calling procedure of an aircraft establishing communication shall be in accordance with Table 2-2.
Table 2-2 Radiotelephony calling procedure
Type a)
Type b)
Type c)
Designation of the station called
NEW YORK RADIO
NEW YORK RADIO
NEW YORK RADIO
Designation of the station calling
GABCD**
SPEEDBIRD ABCD**
AEROFLOT 321**
* In certain cases where the call is initiated by the aeronautical station, the call may be effected by transmission of coded tone signals.
** With the exception of the telephony designators and the type of aircraft, each character in the call sign shall be spoken separately.
When individual letters are spelled out, the radiotelephony spelling alphabet prescribed in 2.1.1.3
shall be used. Numbers are to be spoken in accordance with 2.1.1.4.
2.1.1.7.3.2.2
Stations having a requirement to transmit information to all stations likely to intercept shall preface such transmission by the general call ALL STATIONS, followed by the identification of the calling station.
Note: No reply is expected to such general calls unless individual stations are subsequently called to acknowledge receipt.
2.1.1.7.3.2.3
The reply to the above calls shall be in accordance with Table 2-3. The use of the calling aeronautical station's call sign followed by the answering aeronautical station's call sign shall be considered the invitation to proceed with transmission by the station calling.
Table 2-3 Radiotelephony reply procedure
Type a)
Type b)
Type c)
Designation of the station called
GABCD*
SPEEDBIRD ABCD*
AEROFLOT 321*
Designation of the answering station
NEW YORK RADIO
NEW YORK RADIO
NEW YORK RADIO
* With the exception of the telephony designators and the type of aircraft, each character in the call sign shall be spoken separately. When individual letters are spelled out, the radiotelephony spelling alphabet prescribed in 2.11.3 shall be used. Numbers are to be spoken in accordance with 2.1.1.4.
2.1.1.7.3.2.4
When a station is called but is uncertain of the identification of the calling station, it shall reply by transmitting the following-
STATION CALLING... (station called) SAY AGAIN YOUR CALL SIGN
Note: The following example illustrates the application of this procedure-
(CAIRO station replying) STATION CALLING CAIRO (pause) SAY AGAIN YOUR CALL SIGN
2.1.1.7.3.2.5
Communications shall commence with a call and a reply when it is desired to establish contact, except that, when it is certain that the station called will receive the call, the calling station may transmit the message, without waiting for a reply from the station called.
2.1.1.7.3.2.6
Interpilot air-to-air communication shall be established on the air-to-air channel 123.45 MHz by either a directed call to a specific aircraft station or a general call, taking into account conditions pertaining to use of this channel.
Note: For conditions on use of air-to-air channels see ANS Technical Standards, Part II Volume V, 4.1.3.2.1, also 2.1.2.1.1.4 in this Schedule.
2.1.1.7.3.2.6.1
As the aircraft may be guarding more than one frequency, the initial call shall include the distinctive channel identification "INTERPILOT".
Note: The following examples illustrate the application of this calling procedure.
CLIPPER 123 - SABENA 901 - INTERPILOT - DO YOU READ or
ANY AIRCRAFT VICINITY OF 30 NORTH 160 EAST - JAPANAIR 401- INTERPILOT - OVER
2.1.1.7.3.3
Subsequent radiotelephony communications
2.1.1.7.3.3.1
Abbreviated radiotelephony call signs shall be used only after satisfactory communication has been established and provided that no confusion is likely to arise. An aircraft station shall use its abbreviated call sign only after it has been addressed in this manner by the aeronautical station.
2.1.1.7.3.3.2
After contact has been established, continuous two-way communication shall be permitted without further identification or call until termination of the contact.
2.1.1.7.3.3.3
In order to avoid any possible confusion, when issuing ATC clearances and reading back such clearances, controllers and pilots shall always add the call sign of the aircraft to which the clearance applies.
2.1.1.7.3.4
Indication of transmitting channel
2.1.1.7.3.4.1
As the aeronautical station operator generally guards more than one frequency, the call shall be followed by an indication of the frequency used, unless other suitable means of identifying the frequency are known to exist.
2.1.1.7.3.4.2
When no confusion is likely to arise, only the first two digits of the High Frequency (in kHz) shall be used to identify the transmitting channel.
Note: The following example illustrates the application of this procedure-
(PAA 325 calling Kingston on 8 871 kHz)
KINGSTON CLIPPER THREE TWO FIVE - ON EIGHT EIGHT
2.1.1.7.3.4.3
Except as specified in 2.1.1.7.3.4.4 all six digits of the numerical designator shall be used to identify the transmitting channel in VHF radiotelephony communications, except in the case of both the fifth and sixth digits being zeros, in which case only the first four digits shall be used.
Note 1: The following examples illustrate the application of the procedure in 2.1.1.7.3.4.3-
Channel
Transmitted as
118.000
ONE ONE EIGHT DECIMAL ZERO
118.005
ONE ONE EIGHT DECIMAL ZERO ZERO FIVE
118.010
ONE ONE EIGHT DECIMAL ZERO ONE ZERO
118.025
ONE ONE EIGHT DECIMAL ZERO TWO FIVE
118.050
ONE ONE EIGHT DECIMAL ZERO FIVE ZERO
118.100
ONE ONE EIGHT DECIMAL ONE
Note 2.: Caution must be exercised with respect to the indication of transmitting channels in VHF radio telephony communications when all six digits of the numerical designator are used in airspace where communication channels are separated by 25 kHz, because on aircraft installations with a channel separation capability of 25 kHz or more, it is only possible to select the first five digits of the numerical designator on the radio management panel.
Note 3.: The numerical designator corresponds to the channel identification in ANS Technical Standards Part II, Volume V, Table 4-1(bis).
2.1.1.7.3.4.4
In airspace where all VHF voice communications channels are separated by 25 kHz or more and the use of six digits as in 2.1.1.7.3.4.3 is not substantiated by the operational requirement determined by the appropriate authorities, the first five digits of the numerical designator shall be used, except in the case of both the fifth and sixth digits being zeros, in which case only the first four digits shall be used.
Note 1: The following examples illustrate the application of the procedure in 2.1.1.7.3.4.4 and the associated settings of the aircraft radio management panel for communication equipment with channel separation capabilities of 25 kHz and 8.33/25 kHz-
Channel
Transmitted as
Radio management panel setting for communication equipment with
25kHz (5 digits)
8.33/25kHz (6 digits)
118.000
ONE ONE EIGHT DECIMAL ZERO
118.00
118.000
118.025
ONE ONE EIGHT DECIMAL ZERO TWO
118.02
118.025
118.050
ONE ONE EIGHT DECIMAL ZERO FIVE
118.05
118.050
118.075
ONE ONE EIGHT DECIMAL ZERO SEVEN
118.07
118.075
118.100
ONE ONE EIGHT DECIMAL ONE
118.10
118.100
Note 2." Caution must be exercised with respect to the indication of transmitting channels in VHF radiotelephony communications when five digits of the numerical designator are used in airspace where aircraft are also operated with channel separation capabilities of 8.33/25 kHz. On aircraft installations with a channel separation capability of 8.33 kHz and more, it is possible to select six digits on the radio management panel. It should therefore be ensured that the fifth and sixth digits are set to 25 kHz channels (see Note 1).
Note 3.: The numerical designator corresponds to the channel identification in ANS Technical Standards, Part II, Volume V, Table 4-1(bis).
2.1.1.8
Test procedures
2.1.1.8.1
The form of test transmissions shall be as follows-
a) the identification of the station being called;
b) the aircraft identification;
c) the words "RADIO CHECK";
d) the frequency being used.
2.1.1.8.2
The reply to a test transmission shall be as follows-
(a) the identification of the aircraft;
(b) the identification of the aeronautical station replying;
(c) information regarding the readability of the aircraft transmission.
2.1.1.8.3
The test transmission and reply thereto shall be recorded at the aeronautical station.
2.1.1.8.4
When the tests are made, the following readability scale shall be used-
Readability Scale
1 Unreadable
2 Readable now and then
3 Readable but with difficulty
4 Readable
5 Perfectly readable
2.1.1.9
Exchange of communications
2.1.1.9.1
Communications shall be concise and unambiguous, using standard phraseology whenever available.
2.1.1.9.2
Abbreviated procedures shall only be used after initial contact has been established and where no confusion is likely to arise.
2.1.1.9.3
Acknowledgement of receipt. The receiving operator shall make certain that the message Has been received correctly before acknowledging receipt.
Note: Acknowledgement of receipt is not to be confused with acknowledgement of intercept in radiotelephony network operations.
2.1.1.9.3.1
When transmitted by an aircraft station, the acknowledgement of receipt of a message shall comprise the call sign of that aircraft.
2.1.1.9.3.2
An aircraft station shall acknowledge receipt of important air traffic control messages or parts thereof by reading them back and terminating the readback by its radio call sign.
Note 1.: Air traffic control clearances, instructions and information requiring readback are specified in Civil Aviation (Air Traffic Services) Regulations 2020.
Note 2.: The following example illustrates the application of this procedure: (ATC clearance by network station to an aircraft)
Station:
TWA NINE SIX THREE MADRID
Aircraft:
MADRID TWA NINE SIX THREE
Station:
TWA NINE SIX THREE MADRID - ATC CLEARS TWA NINE SIX THREE TO DESCEND TO NINE THOUSAND FEET
Aircraft (acknowledging):
CLEARED TO DESCEND TO NINE THOUSAND FEET - TWA NINE SIX THREE
Station (denoting accuracy of readback):
MADRID
2.1.1.9.3.3
When acknowledgement of receipt is transmitted by an aeronautical station-
(1) to an aircraft station: it shall comprise the call sign of the aircraft, followed if considered necessary by the call sign of the aeronautical station;
(2) to another aeronautical station: it shall comprise the call sign of the aeronautical station that is acknowledging receipt.
2.1.1.9.3.3.1
An aeronautical station shall acknowledge position reports and other flight progress reports by reading back the report and terminating the readback by its call sign, except that the readback procedure may be suspended temporarily whenever it will alleviate congestion on the communication channel.
2.1.1.9.3.4
It is permissible for verification for the receiving station to read back the message as an additional acknowledgement of receipt. In such instances, the station to which the information is read back shall acknowledge the correctness of readback by transmitting its call sign.
2.1.1.9.3.5
If both position report and other information - such as weather reports - are received in the same message, the information shall be acknowledged with the words such as "WEATHER RECEIVED" after the position report has been read back, except when intercept of the information is required by other network stations. Other messages shall be acknowledged, the aeronautical station transmitting its call sign only.
2.1.1.9.4
End of conversation. A radiotelephone conversation shall be terminated by the receiving station using its own call sign.
2.1.1.9.5
Corrections and repetitions
2.1.1.9.5.1
When an error has been made in transmission, the word "CORRECTION" shall be spoken, the last correct group or phrase repeated, and then the correct version transmitted.
2.1.1.9.5.2
If a correction can best be made by repeating the entire message, the operator shall use the phrase-
"CORRECTION, I SAY AGAIN" before transmitting the message a second time.
2.1.1.9.5.3
When an operator transmitting a message considers that reception is likely to be difficult, he shall transmit the important elements of the message twice.
2.1.1.9.5.4
If the receiving operator is in doubt as to the correctness of the message received, he shall request repetition either in full or in part.
2.1.1.9.5.5
If repetition of an entire message is required, the words "SAY AGAIN" shall be spoken. If repetition of a portion of a message is required, the operator shall state: "SAY AGAIN ALL BEFORE... (first word satisfactorily received)"; or "SAY AGAIN... (word before missing portion) TO... (word after missing portion)"; or "SAY AGAIN ALL AFTER... (last word satisfactorily received)".
2.1.1.9.5.6
Specific items shall be requested, as appropriate, such as "SAY AGAIN ALTIMETER", "SAY AGAIN WIND"
2.1.1.9.5.7
If, in checking the correctness of a readback, an operator notices incorrect items, he shall transmit the words "NEGATIVE I SAY AGAIN" at the conclusion of the readback followed by the correct version of the items concerned.
2.1.1.9.6
"Operations normal" reports
When "operations normal" reports are transmitted by aircraft, they shall consist of the prescribed call followed by the words "OPERATIONS NORMAL".
2.1.2
Establishment and assurance of communications
2.1.2.1
Communications watch/Hours of service
2.1.2.1.1
During flight, aircraft stations shall maintain watch as required by the appropriate Authority and shall not cease watch, except for reasons of safety, without informing the aeronautical station(s) concerned.
2.1.2.1.1.1
Aircraft on long over-water flights, or on flights over designated areas over which the carriage of an emergency locator transmitter (ELT) is required, shall continuously guard the VHF emergency frequency 121.5 MHz, except for those periods when aircraft are carrying out communications on other VHF channels or when airborne equipment limitations or cockpit duties do not permit simultaneous guarding of two channels.
2.1.2.1.1.2
Aircraft shall continuously guard the VHF emergency frequency 121.5 MHz in areas or over routes where the possibility of interception of aircraft or other hazardous situations exist, and a requirement has been established by the appropriate authority.
2.1.2.1.1.3
Aircraft on flights other than those specified in 2.1.2.1.1.1 and 2.12.1.1.2 shall guard the emergency frequency 121.5 MHz to the extent possible.
2.1.2.1.1.4
The user of the air-to-air VHF communications channel shall ensure that adequate watch is maintained on designated ATS frequencies, the frequency of the aeronautical emergency channel, and any other mandatory watch frequencies.
2.1.2.1.2
Aeronautical stations shall maintain watch as required by the appropriate Authority.
2.1.2.1.3
Aeronautical stations shall maintain a continuous listening watch on VHF emergency channel 121.5 MHz during the hours of service of the units at which it is installed.
2.1.2.1.4
When it is necessary for an aircraft station or aeronautical station to suspend operation for any reason, it shall, if possible, so inform other stations concerned, giving the time at which it is expected that operation will be resumed. When operation is resumed, other stations concerned shall be so informed.
2.1.2.1.4.1
When it is necessary to suspend operation beyond the time specified in the original notice, a revised time of resumption of operation shall, if possible, be transmitted at or near the time first specified.
2.1.2.1.5
When two or more ATS frequencies are being used by a controller, consideration shall be given to providing facilities to allow ATS and aircraft transmissions on any of the frequencies to be simultaneously retransmitted on the other frequencies in use thus permitting aircraft stations within range to hear all transmissions to and from the controller.
2.1.2.2
Principles of network operation (HF communications)
2.1.2.2.1
The aeronautical stations of a radiotelephony network shall assist each other in accordance with the following network principles, in order to provide the air-ground communication service required of the network by aircraft flying on the air routes for which the network is responsible.
2.1.2.2.2
When the network comprises a large number of stations, network communications for flights on any individual route segment shall be provided by selected stations, termed "regular stations" for that segment.
Note 1: The selection of stations to act as regular stations for a particular route segment will, where necessary, be undertaken by regional or local agreement, after consultation, if necessary, between the States responsible for the network.
Note 2: In principle, the regular stations will be those serving the locations immediately concerned with flights on that route segment, i.e. points of take-off and landing, appropriate flight information centres or area control centres and, in some cases, additional suitably located stations required to complete the communication coverage or for intercept purposes.
Note 3: In selecting the regular stations, account will be taken of the propagation characteristics of the frequencies used.
2.1.2.2.3
In areas or on routes where radio conditions, length of flights or distance between aeronautical stations require additional measures to ensure continuity of air-ground communication throughout the route segment, the regular stations shall share between them a responsibility of primary guard whereby each station will provide the primary guard for that portion of the flight during which the messages from the aircraft can be handled most effectively by that station.
2.1.2.2.4
During its tenure of primary guard, each regular station shall, among other things-
(a) be responsible for designating suitable primary and secondary frequencies for its communications with the aircraft;
(b) receive all position reports and handle other messages from and to the aircraft essential to the safe conduct of the flight;
(c) be responsible for the action required in case of failure of communications (see 2.1.2.7.2).
2.1.2.2.5
The transfer of primary guard from one station to the next will normally take place at the time of the traversing of flight information region or control area boundaries, this guard being provided at any time, as far as possible, by the station serving the flight information centre or area control centre in whose area the aircraft is flying. However, where communication conditions so demand, a station shall be required to retain primary guard beyond such geographical boundaries or release its guard before the aircraft reaches the boundary, if appreciable improvement in air-ground communication can be effected thereby.
2.1.2.3
Frequencies to be used
2.1.2.3.1
Aircraft stations shall operate on the appropriate radio frequencies.
2.1.2.3.1.1
The air-ground control radio station shall designate the frequency(ies) to be used under normal conditions by aircraft stations operating under its control.
2.1.2.3.1.2
In network operation, the initial designation of primary and secondary frequencies shall be made by the network station with which the aircraft makes pre-flight check or its initial contact after take-off. This station shall also ensure that other network stations are advised, as required, of the frequency(ies) designated.
2.1.2.3.2
An aeronautical station, when designating frequencies in accordance with 2.1.2.3.1.1 or 2.1.2.3.1.2, shall take into account the appropriate propagation data and distance over which communications are required.
2.1.2.3.3
If a frequency designated by an aeronautical station proves to be unsuitable, the aircraft station shall suggest an alternative frequency.
2.1.2.3.4
When, notwithstanding the provisions of regulations 57-63, air-ground frequencies are used for the exchange between network stations of messages essential for coordination and cooperation between the stations, such communication shall, so far as possible, be effected over network frequencies not being used at that time for the bulk of the air-ground traffic. In all cases, the communication with aircraft stations shall take priority over the inter-ground station communications.
2.1.2.4
Establishment of communications
2.1.2.4.1
Aircraft stations shall, if possible, communicate directly with the air-ground control radio station appropriate to the area in which the aircraft are flying. If unable to do so, aircraft stations shall use any relay means available and appropriate to transmit messages to the air-ground control radio station.
2.1.2.4.2
When normal communications from an aeronautical station to an aircraft station cannot be established, the aeronautical station shall use any relay means available and appropriate to transmit messages to the aircraft station. If these efforts fail, the originator shall be advised in accordance with procedures prescribed by the appropriate Authority.
2.1.2.4.3
When, in network operation, communication between an aircraft station and a regular station has not been established after calls on the primary and secondary frequencies, aid shall be rendered by one of the other regular stations for that flight, either by calling the attention of the station first called or, in the case of a call made by an aircraft station, by answering the call and taking the traffic.
2.1.2.4.3.1
Other stations of the network shall render assistance by taking similar action only if attempts to establish communications by the regular stations have proved unsuccessful.
2.1.2.4.4
The provisions of 2.1.2.4.3 and 2.1.2.4.3.1 shall also be applied-
(a) on request of the air traffic services unit concerned; and
(b) when an expected communication from an aircraft has not been received within a time period such that the occurrence of a communication failure is suspected.
Note: A specific time period may be prescribed by the appropriate ATS Authority.
2.2 Transfer of HF communications
2.2.1.1.1
An aircraft station shall be advised by the appropriate aeronautical station to transfer from one radio frequency or network to another. In the absence of such advice, the aircraft station shall notify the appropriate aeronautical station before such transfer takes place.
2.2.1.1.2
In the case of transfer from one network to another, the transfer shall preferably take place while the aircraft is in communication with a station operating in both networks to ensure continuity of communications. If, however, the change of network must take place concurrently with the transfer of communication to another network station, the transfer shall be coordinated by the two network stations prior to advising or authorising the frequency change. The aircraft shall also be advised of the primary and secondary frequencies to be used after the transfer.
2.2.1.1.3
An aircraft station which has transferred communications watch from one radio frequency to another shall, when so required by the appropriate ATS Authority, inform the aeronautical station concerned that communications watch has been established on the new frequency.
2.2.1.1.4
When entering a network after take-off, an aircraft station shall transmit its take-off time or time over the last check-point, to the appropriate regular station.
2.2.1.1.5
When entering a new network, an aircraft station shall transmit the time over the last checkpoint, or of its last reported position, to the appropriate regular station.
2.2.1.1.6
Before leaving the network, an aircraft station shall in all cases advise the appropriate regular station of its intention to do so by transmitting one of the following phrases, as appropriate-
a) when transferring to a pilot-to-controller channel: Aircraft: CHANGING TO...
(air traffic services unit concerned)
b) after landing: Aircraft: LANDED... (location)... (time)
2.2.1.2
Transfer of VHF communications
2.2.1.2.1
An aircraft shall be advised by the appropriate aeronautical station to transfer from one radio frequency to another in accordance with agreed procedures. In the absence of such advice, the aircraft station shall notify the appropriate aeronautical station before such a transfer takes place.
2.2.1.2.2
When establishing initial contact on, or when leaving, a VHF frequency, an aircraft station shall transmit such information as may be prescribed by the appropriate Authority.
2.2.1.3
Voice communications failure
2.2.1.3.1
Air-ground
2.2.1.3.1.1
When an aircraft station fails to establish contact with the appropriate aeronautical station on the designated channel, it shall attempt to establish contact on the previous channel used and, if not successful, on another channel appropriate to the route. If these attempts fail, the aircraft station shall attempt to establish communication with the appropriate aeronautical station, other aeronautical stations or other aircraft using all available means and advise the aeronautical station that contact on the assigned channel could not be established. In addition, an aircraft operating within a network shall monitor the appropriate VHF channel for calls from nearby aircraft.
2.2.1.3.1.2
If the attempts specified under 2.2.1.3.1.1 fail, the aircraft station shall transmit its message twice on the designated channel(s), preceded by the phrase "TRANSMITTING BLIND" and, if necessary, include the addressee(s) for which the message is intended.
2.2.1.3.1.2.1
In network operation, a message which is transmitted blind shall be transmitted twice on both primary and secondary channels. Before changing channel, the aircraft station shall announce the channel to which it is changing.
2.2.1.3.1.3
Receiver failure
2.2.1.3.1.3.1
When an aircraft station is unable to establish communication due to receiver failure, it shall transmit reports at the scheduled times, or positions, on the channel in use, preceded by the phrase "TRANSMITTING BLIND DUE TO RECEIVER FAILURE". The aircraft station shall transmit the intended message, following this by a complete repetition. During this procedure, the aircraft shall also advise the time of its next intended transmission.
2.2.1.3.1.3.2
An aircraft which is provided with air traffic control or advisory service shall, in addition to complying with 2.2.1.3.1.3.1, transmit information regarding the intention of the pilot-in-command with respect to the continuation of the flight of the aircraft.
2.2.1.3.1.3.3
When an aircraft is unable to establish communication due to airborne equipment failure it shall, when so equipped, select the appropriate SSR code to indicate radio failure.
Note - General rules which are applicable in the event of communications failure are contained in Civil Aviation (Rules of the Air) Regulations 2020.
2.2.1.3.2
Ground-to-air-communication
2.2.1.3.2.1
When an aeronautical station has been unable to establish contact with an aircraft station after calls on the frequencies on which the aircraft is believed to be listening, it shall-
(a) request other aeronautical stations to render assistance by calling the aircraft and relaying traffic, if necessary; and
(b) request aircraft on the route to attempt to establish communication with the aircraft and relay traffic, if necessary.
2.2.1.3.2.2
The provisions of 2.2.1.3.2.1 shall also be applied-
(a) on request of the air traffic services unit concerned; and
(b) when an expected communication from an aircraft has not been received within a time period such that the occurrence of a communication failure is suspected.
Note: A specific time period may be prescribed by the appropriate ATS Authority.
2.2.1.3.2.3
If the attempts specified in 2.2.1.3.2.1 fail, the aeronautical station shall transmit messages addressed to the aircraft, other than messages containing air traffic control clearances, by blind transmission on the frequency(ies) on which the aircraft is believed to be listening.
2.2.1.3.2.4
Blind transmission of air traffic control clearances shall not be made to aircraft, except at the specific request of the originator.
2.2.1.3.3
Notification of communications failure. The air-ground control radio station shall notify the appropriate air traffic services unit and the aircraft operating agency, as soon as possible, of any failure in air-ground communication.
2.2.2
HF message handling
2.2.2.1
General
2.2.2.1.1
When operating within a network, an aircraft station shall, in principle, whenever communications conditions so permit, transmit its messages to the stations of the network from which they can be most readily delivered to their ultimate destinations. In particular, aircraft reports required by air traffic services shall be transmitted to the network station serving the flight information centre or area control centre in whose area the aircraft is flying. Conversely, messages to aircraft in flight shall, whenever possible, be transmitted directly to the aircraft by the network station serving the location of the originator.
Note: Exceptionally, an aircraft may need to communicate with an aeronautical station outside the network appropriate to its particular route segment. This is permissible, provided it can be done without interrupting the continuous watch with the communication network appropriate to the route segment, when such watch is required by the appropriate ATS Authority, and provided it does not cause undue interference with the operation of other aeronautical stations.
2.2.2.1.2
Messages passed from an aircraft to a network station shall, whenever possible, be intercepted and acknowledged by other stations of the network, which serve locations where the information is also required.
Note 1. - Determination of the arrangements for dissemination of air-ground messages without address will be a matter for multilateral or local agreement.
Note 2. - In principle, the number of stations required to intercept are to be kept to a minimum consistent with the operational requirement.
2.2.2.1.2.1
Acknowledgement of intercept shall be made immediately after the acknowledgement of receipt by the station to which the message was passed.
2.2.2.1.2.2
Acknowledgement of an intercept message shall be made by transmitting the radio call sign of the station having intercepted the message, followed by the word ROGER, if desired, and the call sign of the station having transmitted the message.
2.2.2.1.2.3
In the absence of acknowledgement of intercept within one minute, the station accepting the message from the aircraft shall forward it, normally over the aeronautical fixed service, to the station(s) which have failed to acknowledge intercept.
2.2.2.1.2.3.1
If, in abnormal circumstances, forwarding is necessary using the air-ground channels, the provisions of 2.1.2.3.4 shall be observed.
2.2.2.1.2.4
When such forwarding is done over the aeronautical fixed telecommunication network, the messages shall be addressed to the network station(s) concerned.
2.2.2.1.2.5
The station(s) to which the messages have been forwarded shall carry out local distribution of them in the same way as if they had been received directly from the aircraft over the air-ground channel.
2.2.2.1.2.6
The aeronautical station receiving an air-report or a message containing meteorological information transmitted by an aircraft in flight shall forward the message without delay-
(1) to the air traffic services unit and meteorological offices associated with the station; and
(2) to the aircraft operating agency concerned or its representative when that agency has made a specific request to receive such messages.
2.2.2.1.3
The provisions of 2.1.2.3.4 shall also be applied, if practicable, in non-network operation.
2.2.2.1.4
When a message addressed to an aircraft in flight is received by the aeronautical station included in the address, and when that station is not able to establish communication with the aircraft to which the message is addressed, the message shall be forwarded to those aeronautical stations on the route which may be able to establish communication with the aircraft.
Note - This does not preclude the transmission by the forwarding aeronautical station, of the original message to the aircraft addressed, if the forwarding station is later able to communicate with that aircraft.
2.2.2.1.4.1
If the aeronautical station to which the message is addressed is unable to dispose of the message in accordance with 2.2.2.1.4, the station of origin shall be advised.
2.2.2.1.4.2
The aeronautical station forwarding the message shall amend the address thereof, by substituting for its own location indicator the location indicator of the aeronautical station to which the message is being forwarded.
2.2.2.2
Transmission of ATS messages to aircraft
2.2.2.2.1
If it is not possible to deliver an ATS message to the aircraft within the time specified by ATS, the aeronautical station shall notify the originator. Thereafter, it shall take no further action with respect to this message unless specifically instructed by ATS.
2.2.2.2.2
If delivery of an ATS message is uncertain because of inability to secure an acknowledgement, the aeronautical station shall assume that the message has not been received by the aircraft and shall advise the originator immediately that, although the message has been transmitted, it has not been acknowledged.
2.2.2.2.3
The aeronautical station, having received the message from ATS, shall not delegate to another station the responsibility for delivery of the message to the aircraft. However, in case of communication difficulties, other stations shall assist, when requested, in relaying the message to the aircraft. In this case, the station having received the message from ATS shall obtain without delay definite assurance that the aircraft has correctly acknowledged the message.
2.2.2.3
Recording of air-ground communications on teletypewriter
2.2.2.3.1
When recording on teletypewriter, the following procedure should be used-
(a) each line should begin at the left margin;
(b) a new line should be used for each transmission;
(c) each communication should contain some or all of the following items in the order shown-
1) call sign of the calling station;
2) text of the message;
3) call sign of the station called or the receiving station, followed by the appropriate abbreviation to indicate "Received", "Readback", or "No reply heard";
4) call sign of station(s) acknowledging intercept followed by appropriate abbreviation to indicate "Received";
5) designation of frequency used;
6) time in UTC of the communication;
(d) missing parts of the message text should be indicated by typing the three periods (space . space . space . space) or three letters M (space M space M space M space); and
(e) correction of typing errors should be made by keyboard manipulation (space E space E space E space), followed by the correct information. Errors detected after the completion of the entry should be corrected after the last entry, using the abbreviation COR, followed by the correct information.
2.2.3
SELCAL procedures
Note: The procedures contained in 2.2.4 are applicable when SELCAL is used and replace certain of the procedures related to calling contained in 2.1.1.
2.2.3.1
General
2.2.3.1.1
With the selective calling system known as SELCAL, the voice calling is replaced by the transmission of coded tones to the aircraft over the radiotelephony channels. A single selective call consists of a combination of four pre-selected audio tones whose transmission requires approximately 2 seconds. The tones are generated in the aeronautical station coder and are received by a decoder connected to the audio output of the airborne receiver. Receipt of the assigned tone code (SELCAL code) activates a cockpit call system in the form of light and/or chime signals.
Note: Due to the limited number of SELCAL codes, similar code assignments to multiple aircraft may be expected. Therefore, the use of correct radiotelephony (RTF) procedures contained in this chapter is emphasised when establishing communications via SELCAL.
2.2.3.1.2
SELCAL shall be utilised by suitably equipped stations for ground-to-air selective calling on the en route HF and VHF radio channels.
2.2.3.1.3
On aircraft equipped with SELCAL, the pilot is still able to keep a conventional listening watch if required.
2.2.3.2
Notification to aeronautical stations of aircraft SELCAL codes
2.2.3.2.1
It shall be the responsibility of the aircraft operating agency and the aircraft to ensure that all aeronautical stations, with which the aircraft would normally communicate during a particular flight, know the SELCAL code associated with its radiotelephony call sign.
2.2.3.2.2
When practicable, the aircraft operating agency shall disseminate to all aeronautical stations concerned, at regular intervals, a list of SELCAL codes assigned to its aircraft or flights.
2.2.3.2.3
The aircraft shall-
a) include the SELCAL code in the flight plan submitted to the appropriate air traffic services unit; and
b) ensure that the HF aeronautical station has the correct SELCAL code information by establishing communications temporarily with the HF aeronautical station while still within VHF coverage.
Note: Provisions regarding completion of the flight plan are set forth in the Civil Aviation (Air Traffic Services) Regulations 2020
2.2.3.3
Pre-flight check
2.2.3.3.1
The aircraft station shall contact the appropriate aeronautical station and request a pre-flight SELCAL check and, if necessary, give its SELCAL code.
2.2.3.3.2
When primary and secondary frequencies are assigned, a SELCAL check shall normally be made first on the secondary frequency and then on the primary frequency. The aircraft station shall then be ready for continued communication on the primary frequency.
2.2.3.3.3
If the pre-flight check reveal that either the ground or airborne SELCAL installation is inoperative, the aircraft shall maintain a continuous listening watch on its subsequent flight until SELCAL again becomes available.
2.2.3.4
Establishment of communications
2.2.3.4.1
When an aeronautical station initiates a call by SELCAL, the aircraft shall reply with its radio call sign, followed by the phrase "GO AHEAD".
2.2.3.5
En route procedures
2.2.3.5.1
Aircraft stations shall ensure that the appropriate aeronautical station(s) are aware that SELCAL watch is being established or maintained.
2.2.3.5.2
When so prescribed on the basis of regional air navigation agreements, calls for scheduled reports from aircraft shall be initiated by an aeronautical station by means of SELCAL.
2.2.3.5.3
Once SELCAL watch has been established by a particular aircraft station, aeronautical stations shall employ SELCAL whenever they require to call aircraft.
2.2.3.5.4
In the event the SELCAL signal remains unanswered after two calls on the primary frequency and two calls on the secondary frequency, the aeronautical station shall revert to voice calling.
2.2.3.5.5
Stations in a network shall keep each other immediately advised when malfunctioning occurs in a SELCAL installation on the ground or in the air. Likewise, the aircraft shall ensure that the aeronautical stations concerned with its flight are immediately made aware of any malfunctioning of its SELCAL installation, and that voice calling is necessary.
2.2.3.5.6
All stations shall be advised when the SELCAL installation is again functioning normally.
2.2.3.6
SELCAL code assignment to aircraft
2.2.3.6.1
In principle, the SELCAL code in the aircraft shall be associated with the radiotelephony call sign, i.e. where the flight number (service number) is employed in the radio call sign, the SELCAL code in the aircraft shall be listed against the flight number. In all other cases, the SELCAL code in the aircraft shall be listed against the aircraft registration.
Note: The use of aircraft radio call signs, consisting of the airline abbreviation followed by the flight service number, is increasing among aircraft operators throughout the world. The SELCAL equipment in aircraft should, therefore, be of a type which permits a particular code being associated with a particular flight number, i.e. equipment which is capable of adjustment in code combinations. At this stage, however, many aircraft still carry SELCAL equipment of the single code type, and it will not be possible for aircraft with such equipment to satisfy the principle set out above. This should not militate against use of the flight number type of radio call sign by an aircraft so equipped if it wishes to apply this type of call sign, but it is essential when a single code airborne equipment is used in conjunction with a flight number type radio call sign that the ground stations be advised in connection with each flight of the SELCAL code available in the aircraft.
3.1 Distress and urgency radiotelephony communication procedures
3.1.1 General
Note: The distress and urgency procedures contained in 3.1 relate to the use of radiotelephony. The provisions of Article S30 and Appendix S13 of the ITU Radio Regulations are generally applicable, except that S30.9 permits other procedures to be employed where special arrangements between governments exist, and are also applicable to radiotelephony communications between aircraft stations and stations in the maritime mobile service.
3.1.1.1
Distress and urgency traffic shall comprise all radiotelephony messages relative to the distress and urgency conditions respectively. Distress and urgency conditions are defined as-
(a) Distress: a condition of being threatened by serious and/or imminent danger and of requiring immediate assistance; and
(b) Urgency: a condition concerning the safety of an aircraft or other vehicle, or of some person on board or within sight, but which does not require immediate assistance.
3.1.1.2
The radiotelephony distress signal MAYDAY and the radiotelephony urgency signal PAN PAN shall be used at the commencement of the first distress and urgency communication respectively.
3.1.1.2.1
At the commencement of any subsequent communication in distress and urgency traffic, it shall be permissible to use the radiotelephony distress and urgency signals.
3.1.1.3
The originator of messages addressed to an aircraft in distress or urgency condition shall restrict to the minimum the number and volume and content of such messages as required by the condition.
3.1.1.4
If no acknowledgement of the distress or urgency message is made by the station addressed by the aircraft, other stations shall render assistance, as prescribed in 3.2.2 and 3.3.2 respectively.
Note: "Other stations" is intended to refer to any other station which has received the distress or urgency message and has become aware that it has not been acknowledged by the station addressed.
3.1.1.5
Distress and urgency traffic shall normally be maintained on the frequency on which such traffic was initiated until it is considered that better assistance can be provided by transferring that traffic to another frequency.
Note: 121.5 MHz or alternative available VHF or HF frequencies may be used as appropriate.
3.1.1.6
In cases of distress and urgency communications, in general, the transmissions by radiotelephony shall be made slowly and distinctly, each word being clearly pronounced to facilitate transcription.
3.2 Radiotelephony distress communications
3.2.1
Action by the aircraft in distress
3.2.1.1.1
In addition to being preceded by the radiotelephony distress signal MAYDAY, preferably spoken three times, the distress message to be sent by an aircraft in distress shall-
(a) be on the air-ground frequency in use at the time;
(b) consist of as many as possible of the following elements spoken distinctly and, if possible, in the following order-
(1) name of the station addressed (time and circumstances permitting);
(2) the identification of the aircraft;
(3) the nature of the distress condition;
(4) intention of the person in command;
(5) present position, level (i.e. flight level, altitude, etc., as appropriate) and heading.
Note 1.: The foregoing provisions may be supplemented by the following measures-
a) the distress message of an aircraft in distress being made on the emergency frequency 121.5 MHz or another aeronautical mobile frequency, if considered necessary or desirable. Not all aeronautical stations maintain a continuous guard on the emergency frequency;
b) the distress message of an aircraft in distress being broadcast, if time and circumstances make this course preferable;
c) the aircraft transmitting on the maritime mobile service radiotelephony calling frequencies;
d) the aircraft using any means at its disposal to attract attention and make known its conditions (including the activation of the appropriate SSR mode and code);
e) any station taking any means at its disposal to assist an aircraft in distress;
f) any variation on the elements listed under 3.2.1.1 b, when the transmitting station is not itself in distress, provided that such circumstance is clearly stated in the distress message.
Note 2.: The station addressed will normally be that station communicating with the aircraft or in whose area of responsibility the aircraft is operating.
3.2.1.2
Action by the station addressed or first station acknowledging the distress message
3.2.1.2.1
The station addressed by aircraft in distress, or first station acknowledging the distress message, shall-
(a) immediately acknowledge the distress message;
(b) take control of the communications or specifically and clearly transfer that responsibility, advising the aircraft if a transfer is made;
(c) take immediate action to ensure that all necessary information is made available, as soon as possible, to-
(1) the ATS unit concerned;
(2) the aircraft operating agency concerned, or its representative, in accordance with pre-established arrangements;
Note: The requirement to inform the aircraft operating agency concerned does not have priority over any other action which involves the safety of the flight in distress, or of any other flight in the area, or which might affect the progress of expected flights in the area.
(d) warn other stations, as appropriate, in order to prevent the transfer of traffic to the frequency of the distress communication.
3.2.1.3
Imposition of silence
3.2.1.3.1
The station in distress, or the station in control of distress traffic, shall be permitted to impose silence, either on all stations of the mobile service in the area or on any station which interferes with the distress traffic. It shall address these instructions "to all stations", or to one station only, according to circumstances. In either case, it shall use-
- STOP TRANSMITTING;
- the radiotelephony distress signal MAYDAY.
3.2.1.3.2
The use of the signals specified in 3.2.3.1 shall be reserved for the aircraft station in distress and for the station controlling the distress traffic.
3.2.1.4
Action by all other stations
3.2.1.4.1
The distress communications have absolute priority over all other communications, and a station aware of them shall not transmit on the frequency concerned, unless-
(a) the distress is cancelled or the distress traffic is terminated;
(b) all distress traffic has been transferred to other frequencies;
(c) the station controlling communications gives permission;
(d) it has itself to render assistance.
3.2.1.4.2
Any station which has knowledge of distress traffic, and which cannot itself assist the station in distress, shall nevertheless continue listening to such traffic until it is evident that assistance is being provided.
3.2.2
Termination of distress communications and of silence
3.2.2.1
When an aircraft is no longer in distress, it shall transmit a message cancelling the distress condition.
3.2.2.1.1
When the station which has controlled the distress communication traffic becomes aware that the distress condition is ended, it shall take immediate action to ensure that this information is made available, as soon as possible, to-
(1) the ATS unit concerned;
(2) the aircraft operating agency concerned, or its representative, in accordance with pre-established arrangements.
3.2.2.1.2
The distress communication and silence conditions shall be terminated by transmitting a message, including the words "DISTRESS TRAFFIC ENDED", on the frequency or frequencies being used for the distress traffic. This message shall be originated only by the station controlling the communications when, after the reception of the message prescribed in 3.2.2.1, it is authorised to do so by the appropriate authority.
3.2.3
Radiotelephony urgency communications
3.2.3.1
Action by the aircraft reporting an urgency condition except as indicated in 3.2.3.4
3.2.3.1.1
In addition to being preceded by the radiotelephony urgency signal PAN PAN preferably spoken three times and each word of the group pronounced as the French word "panne", the urgency message to be sent by an aircraft reporting an urgency condition shall-
(a) be on the air-ground frequency in use at the time; and
(b) consist of as many as required of the following elements spoken distinctly and, where possible, in the following order-
(1) the name of the station addressed;
(2) the identification of the aircraft;
(3) the nature of the urgency condition;
(4) the intention of the person in command;
(5) present position, level (i.e. flight level, altitude, etc., as appropriate) and heading;
(6) any other useful information.
Note 1.:The foregoing provisions of 3.2.3.1.1 are not intended to prevent an aircraft broadcasting an urgency message, if time and circumstances make this course preferable.
Note 2.: The station addressed will normally be that station communicating with the aircraft or in whose area of responsibility the aircraft is operating.
3.2.3.2
Action by the station addressed or first station acknowledging the urgency message
3.2.3.2.1
The station addressed by an aircraft reporting an urgency condition, or first station acknowledging the urgency message, shall-
(a) acknowledge the urgency message;
(b) take immediate action to ensure that all necessary information is made available, as soon as possible, to-
(1) the ATS unit concerned;
(2) the aircraft operating agency concerned, or its representative, in accordance with pre-established arrangements;
Note: The requirement to inform the aircraft operating agency concerned does not have priority over any other action which involves the safety of the flight in distress, or of any other flight in the area, or which might affect the progress of expected flights in the area.
(c) where necessary, exercise control of communications.
3.2.3.3
Action by all other stations
3.2.3.3.1
The urgency communications have priority over all other communications, except distress, and all stations shall take care not to interfere with the transmission of urgency traffic.
3.2.3.4
Action by an aircraft used for medical transports
3.2.3.4.1
The use of the signal described in 3.2.3.4.2 shall indicate that the message which follows concerns a protected medical transport pursuant to the 1949 Geneva Conventions and Additional Protocols.
3.2.3.4.2
For the purpose of announcing and identifying aircraft used for medical transports, a transmission of the radiotelephony urgency signal PAN PAN, preferably spoken three times, and each word of the group pronounced as the French word "panne", shall be followed by the radiotelephony signal for medical transports MAY-DEE-CAL, pronounced as in the French "médical". The use of the signals described above indicates that the message which follows concerns a protected medical transport. The message shall convey the following data-
(a) the call sign or other recognised means of identification of the medical transports;
(b) position of the medical transports;
(c) number and type of medical transports;
(d) intended route;
(e) estimated time en route and of departure and arrival, as appropriate; and
(f) any other information such as flight altitude, radio frequencies guarded, languages used, and secondary surveillance radar modes and codes.
3.2.3.5
Action by the station addressed or by other stations receiving a medical transports message.
The provisions of 3.2.3.2 and 3.2.3.3 shall apply as appropriate to stations receiving a medical transports message.
SCHEDULE 6 Aeronautical Mobile Service - Data Link communications (regs 78 and 80)
1.1 General
Note 1.: While the provisions of this Schedule are based primarily on the use of controller-pilot data link communications (CPDLC), the provisions of 1.1.1 would apply to other data link applications, where applicable, including Data link - flight information services (e.g. D-ATIS, DVOLMET, etc.).
Note 2.: For the purposes of these provisions, the communication procedures applicable to the aeronautical mobile service, as appropriate, also apply to the aeronautical mobile-satellite service.
1.1.1
Data link initiation capability (DLIC)
1.1.1.1
General
1.1.1.1.1
Before entering an airspace where data link applications are used by the ATS unit, data link communications shall be initiated between the aircraft and the ATS unit in order to register the aircraft and, when necessary, allow the start of a data link application. This shall be initiated by the aircraft, either automatically or by the pilot, or by the ATS unit on address forwarding.
1.1.1.1.2
The logon address associated with an ATS unit shall be published in Aeronautical Information Publications in accordance with Civil Aviation (Aeronautical Information Services) Regulations.
Note: A given FIR may have multiple logon addresses; and more than one FIR may share the same logon address.
1.1.1.2
Aircraft initiation
On receipt of a valid data link initiation request from an aircraft approaching or within a data link service area, the ATS unit shall accept the request and, if able to correlate it with a flight plan, shall establish a connection with the aircraft.
1.1.1.3
ATS unit forwarding
The ground system initially contacted by the aircraft shall provide to the next ATS unit any relevant updated aircraft information in sufficient time to permit the establishment of data link communications.
1.1.1.4
Failure
1.1.1.4.1
In the case of a data link initiation failure, the data link system shall provide an indication of the failure to the appropriate ATS unit(s). The data link system shall also provide an indication of the failure to the flight crew when a data link initiation failure results from a logon initiated by the flight crew.
Note: When the aircraft's logon request results from responding to a contact request by a transferring ATS unit, then both ATS units will receive the indication.
1.1.1.4.2
The ATS unit shall establish procedures to resolve, as soon as practicable, data link initiation failures. Procedures shall include, as a minimum, verifying that the aircraft is initiating a data link request with the appropriate ATS unit (i.e. the aircraft is approaching or within the ATS unit's control area); and if so-
(a) when a flight plan is available, verify that the aircraft identification, aircraft registration, or aircraft address and other details contained in the data link initiation request correspond with details in the flight plan, and where differences are detected verify the correct information and then make the necessary changes; or
(b) when a flight plan is not available, create a flight plan with sufficient information in the flight data processing system, to achieve a successful data link initiation; then
(c) arrange for the re-initiation of the data link.
1.1.1.4.3
The aircraft operator shall establish procedures to resolve, as soon as practicable, data link initiation failures. Procedures shall include, as a minimum, that the pilot-
(a) verify the correctness and consistency of the flight plan information available in the FMS or equipment from which data link is initiated, and where differences are detected make the necessary changes; and
(b) verify the correct address of the ATS unit; then
(c) re-initiate data link.
1.1.2
Composition of data link messages
1.1.2.1
The text of messages shall be composed in standard message format (e.g. CPDLC message set), in plain language or in abbreviations and codes. Plain language shall be avoided when the length of the text can be reduced by using appropriate abbreviations and codes. Non-essential words and phrases, such as expressions of politeness, shall not be used.
1.1.2.2
The following characters are allowed in the composition of messages-
Letters: ABCDEFGHIJKLMNOPQRSTUVWXYZ (uppercase only)
Figures: 1234567890
Other signs-
- (hyphen)
? (question mark)
: (colon)
((open bracket)
) (close bracket)
. (full stop, period, or decimal point)
, (comma)
' (apostrophe)
= (double hyphen or equal sign)
/ (oblique)
+ (plus sign) and the space character.
Characters other than those listed above shall not be used in messages.
1.1.2.3
Roman numerals shall not be employed. If the originator of a message wishes the addressee to be informed that Roman figures are intended, the Arabic figure or figures shall be written and preceded by the word ROMAN.
1.1.3
Display of data link messages
1.1.3.1
Ground and airborne systems shall allow for messages to be appropriately displayed, printed when required, and stored in a manner that permits timely and convenient retrieval should such action be necessary.
1.1.3.2
Whenever textual presentation is required, the English language shall be displayed as a minimum.
1.2 CPDLC procedures
1.2.1
In all communications the highest standard of discipline shall be observed at all times.
1.2.1.1
Consequences of human performance, which could affect the accurate reception and comprehension of messages, shall be taken into consideration when composing a message.
1.2.2
Ground and airborne systems shall provide controllers and pilots with the capability to review and validate any operational messages they send.
1.2.3
Ground and airborne systems shall provide controllers and pilots with the capability to review, validate and when applicable, acknowledge any operational messages they receive.
1.2.4
The controller shall be provided with the capability to respond to messages, including emergencies, to issue clearances, instructions and advisories, and to request and provide information, as appropriate.
1.2.5
The pilot shall be provided with the capability to respond to messages, to request clearances and information, to report information, and to declare or cancel an emergency.
1.2.6
The pilot and the controller shall be provided with the capability to exchange messages which include standard message elements, free text message elements or a combination of both.
1.2.7
Unless specified by the appropriate ATS authority, voice readback of CPDLC messages shall not be required.
1.2.8
Establishment of CPDLC
1.2.8.1
The controller and the pilot shall be informed when CPDLC has been successfully established.
1.2.8.2
CPDLC shall be established in sufficient time to ensure that the aircraft is communicating with the appropriate ATC unit.
1.2.8.3
The controller and pilot shall be informed when CPDLC is available for operational use, at initial establishment, as well as on resumption of CPDLC after a failure.
1.2.8.4
The pilot shall be able to identify the air traffic unit providing the air traffic control service at any time while the service is being provided.
1.2.8.5
When the airborne system detects that CPDLC is available for operational use, it shall send the CPDLC downlink message element CURRENT DATA AUTHORITY.
1.2.8.6
Airborne-initiated CPDLC
1.2.8.6.1
When an ATC unit receives an unexpected request for CPDLC from an aircraft, the circumstances leading to the request shall be obtained from the aircraft to determine further action.
1.2.8.6.2
When the ATC unit rejects a request for CPDLC, it shall provide the pilot with the reason for the rejection using an appropriate CPDLC message.
1.2.8.7
ATC unit-initiated CPDLC
1.2.8.7.1
An ATC unit shall only establish CPDLC with an aircraft if the aircraft has no CPDLC link established, or when authorised by the ATC unit currently having CPDLC established with the aircraft.
1.2.8.7.2
When a request for CPDLC is rejected by an aircraft, the reason for the rejection shall be provided using CPDLC downlink message element NOT CURRENT DATA AUTHORITY or message element NOT AUTHORISED NEXT DATA AUTHORITY, as appropriate. Local procedures shall dictate whether the reason for rejection is presented to the controller. No other reasons for airborne rejection of ATC unit initiation of CPDLC shall be permitted.
1.2.9
Exchange of operational CPDLC messages
1.2.9.1
Controllers and pilots shall construct CPDLC messages using standard message elements, free text message elements or a combination of both.
1.2.9.1.1
When CPDLC is being used, and the intent of the message is included in the CPDLC message set contained in the PANS-ATM, the associated standard message elements shall be used.
1.2.9.1.2
Except as provided by 1.2.12.1, when a controller or pilot communicates via CPDLC, the response shall be via CPDLC, When a controller or pilot communicates via voice, the response shall be via voice.
1.2.9.1.3
Whenever a correction to a message sent via CPDLC is deemed necessary or the contents of a message needs to be clarified, the controller or pilot shall use the most appropriate means available for issuing the correct details or for providing clarification.
Note: The following procedures may be applied by the controller, in terms of correcting clearances, instructions or information, or by a pilot, in terms of correcting a reply to an uplink message or correcting previously advised requests or information.
1.2.9.1.3.1
When voice communications are used to correct a CPDLC message for which no operational response has yet been received, the controller's or pilot's transmission shall be prefaced by the phrase: "DISREGARD CPDLC (message type) MESSAGE, BREAK" - followed by the correct clearance, instruction, information or request.
Note: It is possible that, at the time the voice communicated clarification is transmitted, the CPDLC message being referred to has not yet reached the recipient, or has reached the recipient but has not been acted upon, or has reached the recipient and has been acted upon.
1.2.9.1.3.2
When referring to and identifying the CPDLC message to be disregarded, caution shall be exercised in its phrasing so as to avoid any ambiguity with the issuance of the accompanying corrected clearance, instruction, information or request.
Note: For example, if SAS445, maintaining FL290, had been instructed via CPDLC to climb to FL350, and the controller needs to correct the clearance utilising voice communications, the following phrase might be used-
SAS445 DISREGARD CPDLC CLIMB CLEARANCE MESSAGE, BREAK, CLIMB TO FL310.
1.2.9.1.3.3
If a CPDLC message that requires an operational response is subsequently negotiated via voice, an appropriate CPDLC message closure response shall be sent to ensure proper synchronisation of the CPDLC dialogue. This could be achieved either by explicitly instructing the recipient of the message via voice to close the dialogue or by allowing the system to automatically close the dialogue.
1.2.9.2
The composition of a CPDLC message shall not exceed five message elements, only two of which may contain the route clearance variable.
1.2.9.2.1
The use of long messages or messages with multiple clearance elements, multiple clearance request elements or messages with a combination of clearances and information shall be avoided where possible.
1.2.9.3
CPDLC ground systems and airborne systems shall be capable of using the CPDLC message alert attributes in order to draw attention to higher priority messages.
Note: Message attributes dictate certain message handling requirements for the CPDLC user receiving a message. Each CPDLC message has two attributes: alert and response attributes. When a message contains multiple message elements, the highest precedence message element attribute type becomes the attribute type for the entire message.
1.2.9.3.1
The alert attribute shall delineate the type of alerting required upon message receipt. Alert types are presented in Table 1-1
1.2.9.3.2
The response attribute shall delineate valid responses for a given message element. Response types are presented in Table 1-2 for uplink messages and Table 1-3 for downlink messages.
1.2.9.3.3.1
When a multi-element message requires a response, the response shall apply to all message elements.
Note: For example, a multi-element message containing CLIMB TO FL310 MAINTAIN MACH.84, a WILCO response applies to, and indicates compliance with, both elements of the message.
1.2.9.3.3.2
When a single message element clearance or any part of a multi-element clearance message cannot be complied with, the pilot shall send an UNABLE response for the whole message.
1.2.9.3.3.3
The controller shall respond with an UNABLE message that applies to all elements of the request when no element(s) of a single or multi-element clearance request can be approved. The current clearance(s) shall not be restated.
1.2.9.3.3.4
When a multi-element clearance request can only be partially accommodated, the controller shall respond with an UNABLE message applying to all the message elements of the request and, if appropriate, include a reason and/or information on when a clearance may be expected.
Table 1-1 Alert Attribute (Uplink and Downlink)
Type
Description
Precedence
H
High
1
M
Medium
2
L
Low
3
N
No alerting required
4
Table 1-2. Response Attribute (Uplink)
Type
Response required
Valid responses
Precedence
W/U
Yes
WILCO, UNABLE, STANDBY, NOT CURRENT DATA AUTHORITY, NOT AUTHORISED NEXT DATA AUTHORITY, LOGICAL ACKNOWLEDGEMENT (only if required), ERROR
1
A/N
Yes
AFFIRM, NEGATIVE, STANDBY, NOT CURRENT DATA AUTHORITY, NOT AUTHORISED NEXT DATA AUTHORITY, LOGICAL ACKNOWLEDGEMENT (only if required), ERROR
2
R
Yes
ROGER, UNABLE, STANDBY, NOT CURRENT DATA AUTHORITY, NOT AUTHORISED NEXT DATA AUTHORITY, LOGICAL ACKNOWLEDGEMENT (only if required), ERROR
3
Y
Yes
Any CPDLC downlink message, LOGICAL ACKNOWLEDGEMENT (only if required)
4
N
No, unless logical acknowledgement required
LOGICAL ACKNOWLEDGEMENT (only if required), NOT CURRENT DATA AUTHORITY, NOT AUTHORISED NEXT DATA AUTHORITY, ERROR
5
Table 1-3 Response Attribute (Downlink)
Type
Response Required
Valid Responses
Precedence
Y
Yes
Any CPDLC uplink message, LOGICAL ACKNOWLEDGEMENT (only if required)
1
N
No, unless logical acknowledgement required
LOGICAL ACKNOWLEDGEMENT (only if required), MESSAGE NOT SUPPORTED BY THIS ATC UNIT, ERROR
2
Note: A separate CPDLC message (or messages) may subsequently be transmitted to respond to those elements that can be accommodated.
1.2.9.3.3.5
When all elements of a single or multi-element clearance request can be accommodated, the controller shall respond with clearances corresponding to each element of the request. This response shall be a single uplink message.
Note: For example, while messages containing multi-element clearance requests are to be avoided, a multi-element downlink message containing the indicated message elements-
REQUEST CLEARANCE YQM YYG YYT YQX TRACK X E!NN EDDF REQUEST CLIMB TO FL350 REQUEST MACH 0.84
could be responded to with-
CLEARED YQM YYG YYT YQX TRACK X EINN EDDF CLIMB TO FL350 REPORT MAINTAINING CROSS YYG AT OR AFTER 1150 NO SPEED RESTRICTION.
1.2.9.3.3.6
When a CPDLC message contains more than one message element and the response attribute for the message is Y, when utilised, the single response message shall contain the corresponding number of replies in the same order.
Note: For example, a multi-element uplink message containing
CONFIRM SQUAWK WHEN CAN YOU ACCEPT FL410
could be responded to with
SQUAWKING 5525 WE CAN ACCEPT FL410 AT 1636Z
1.2.9.4
When a ground or airborne system generates the CPDLC message ERROR, the reason for the error shall be included in the message.
1.2.9.5
The appropriate ATS authority shall select those message elements contained in PANS-ATM that support operations in their airspace. Should an ATS authority choose to select a subset of the message elements, and a received message does not belong to this subset, the ATC unit shall respond by up-linking the message element MESSAGE NOT SUPPORTED BY THIS ATC UNIT.
Note: Further processing of the received message is not required.
1.2.9.5.1
Only the uplink messages appropriate to a particular control sector's operations shall be provided to the controller.
Note: The CPDLC message set contained in PANS-ATM was developed to encompass different air traffic management environments.
1.2.9.5.2
Information concerning CPDLC message element subsets, shall be published in the Aeronautical Information Publications (AIPs).
1.2.9.6
Transfer of CPDLC
1.2.9.6.1
When CPDLC is transferred, the transfer of voice communications and CPDLC shall commence concurrently.
1.2.9.6.2
When an aircraft is transferred from an ATC unit where CPDLC is available to an ATC unit where CPDLC is not available, CPDLC termination shall commence concurrent with the transfer of voice communications.
1.2.9.6.3
When a transfer of CPDLC results in a change of data authority, and there are still messages for which the closure response has not been received (i.e. messages outstanding), the controller transferring the CPDLC shall be informed.
1.2.9.6.3.1
If the controller needs to transfer the aircraft without replying to any downlink message(s) outstanding, the system shall have the capability to automatically send the appropriate closure response message(s). In such cases, the contents of any automatically sent closure response message(s) shall be promulgated in local instructions.
1.2.9.6.3.2
When the controller decides to transfer the aircraft without receiving pilot responses to any uplink message(s) outstanding, the ground system shall have the capability to automatically end the dialogue for each message prior to the transfer.
1.2.9.6.3.2.1
The controller shall revert to voice communications to clarify any ambiguity associated with the message(s) outstanding.
1.2.9.6.4
When a transfer of CPDLC does not result in a change of data authority, and there are still messages outstanding, these messages shall either be forwarded to the appropriate controller or shall be closed in accordance with local instructions and, if necessary, letters of agreement.
1.2.10
Display of CPDLC messages
ATC units utilising a CPDLC message contained in the PANS-ATM shall display the associated text pertaining to that message as presented in the PANS-ATM.
1.2.11
Free text messages-elements.
1.2.11.1
The use of free text messages by controllers or pilots, shall be avoided.
Note: Whilst it is recognised that non-routine and emergency situations may necessitate the use of free text, particularly when voice communication has failed, the avoidance of utilising free text messages is intended to reduce the possibility of misinterpretation and ambiguity.
1.2.11.2
When the CPDLC message set contained in the Civil Aviation (Air Traffic Services) Regulations does not provide for specific circumstances, the appropriate ATS authority may determine that it is acceptable to use free text message elements. In such cases, the appropriate ATS authority, in consultation with operators and other ATS authorities that may be concerned, shall define display format, intended use and attributes for each free text message element and publish them with relevant procedures in the Aeronautical Information Publications.
1.2.11.3
Free text message elements shall be stored for selection within the aircraft or ground system to facilitate their use.
1.2.12
Emergencies, hazards and equipment failure procedures
1.2.12.1
When a CPDLC emergency message is received, the controller shall acknowledge receipt of the message by the most efficient means available.
1.2.12.2
When responding via CPDLC to all other emergency or urgency messages, uplink message ROGER shall be used.
1.2.12.3
When a CPDLC message requires a logical acknowledgement and/or an operational response, and such a response is not received, the pilot or controller, as appropriate, shall be alerted.
1.2.12.4
Failure of CPDLC
Note 1.: Action to be taken in the event of a data link initiation failure is covered in 1.1.1.4.
Note 2.: Action to be taken in the event of the failure of a single CPDLC message is covered in 1.2.12.7
1.2.12.4.1
A CPDLC failure shall be detected in a timely manner.
1.2.12.4.2
The controller and pilot shall be alerted to a failure of CPDLC as soon as a failure has been detected.
1.2.12.4.3
When a controller or pilot is alerted that CPDLC has failed, and the controller or pilot needs to communicate prior to CPDLC being restored, the controller or pilot shall revert to voice, if possible, and preface the information with the phrase-
CPDLC FAILURE
1.2.12.4.4
Controllers having a requirement to transmit information concerning a complete CPDLC ground system failure to all stations likely to intercept shall preface such a transmission by the general call ALL STATIONS CPDLC FAILURE, followed by the identification of the calling station.
Note: No reply is expected to such general calls unless individual stations are subsequently called to acknowledge receipt.
1.2.12.4.5
When CPDLC fails and communications revert to voice, all CPDLC messages outstanding shall be considered not delivered and the entire dialogue involving the messages outstanding shall be recommenced by voice.
1.2.12.4.6
When CPDLC fails but is restored prior to a need to revert to voice communications, all messages outstanding shall be considered not delivered and the entire dialogue involving the messages outstanding shall be recommenced via CPDLC.
1.2.12.5
INTENTIONAL SHUTDOWN OF CPDLC
1.2.12.5.1
When a system shutdown of the communications network or the CPDLC ground system is planned, a NOTAM shall be published to inform all affected parties of the shutdown period and if necessary, the details of the voice communication frequencies to be used.
1.2.12.5.2
Aircraft currently in communication with the ATC unit shall be informed by voice or CPDLC of any imminent loss of CPDLC service.
1.2.12.5.3
The controller and pilot shall be provided with the capability to abort CPDLC.
1.2.12.6
FAILURE OF A SINGLE CPDLC MESSAGE
When a controller or pilot is alerted that a single CPDLC message has failed, the controller or pilot shall take one of the following actions, as appropriate-
a) via voice, confirm the actions that will be undertaken with respect to the related dialogue, prefacing the information with the phrase-
CPDLC MESSAGE FAILURE;
b) via CPDLC, reissue the CPDLC message that failed.
1.2.12.7
DISCONTINUATION OF THE USE OF CPDLC PILOT REQUESTS
1.2.12.7.1
When a controller requires all stations or a specific flight to avoid sending CPDLC requests for a limited period of time, the following phrase shall be used-
((call sign) or ALL STATIONS) STOP SENDING CPDLC REQUESTS [UNTIL ADVISED] [(reason)]
Note: Under these circumstances, CPDLC remains available for the pilot to, if necessary, respond to messages, report information, and declare and cancel an emergency.
1.2.12.7.2
The resumption of the normal use of CPDLC shall be advised by using the following phrase-
((call sign) or ALL STATIONS) RESUME NORMAL CPDLC OPERATIONS
1.2.13
Where the testing of CPDLC with an aircraft could affect the air traffic services being provided to the aircraft, coordination shall be effected prior to such testing.
1.2.14
Downstream clearance delivery service
1.2.14.1
The appropriate ATS authority shall determine whether an ATC unit supports downstream clearance delivery service.
1.2.14.2
Establishment of downstream clearance delivery service
1.2.14.2.1
Downstream clearance delivery service shall only be initiated by the airborne system. The initiation shall indicate that this communication is only to receive a downstream clearance.
1.2.14.2.2
When an ATC unit rejects a request for downstream clearance delivery service, it shall provide the pilot with the reason for the rejection using the CPDLC message SERVICE UNAVAILABLE.
1.2.14.3
Operation of downstream clearance delivery service
1.2.14.3.1
The controller and pilot shall be informed when downstream clearance delivery service is available for operational communication.
1.2.14.3.2
The controller and pilot shall be informed of the failure of downstream clearance delivery service.
1.2.14.3.3
The CPDLC message elements that are permitted for downstream clearance delivery service shall be established by regional air navigation agreement.
1.2.14.3.4
A clearance request issued as a downstream clearance request shall be clearly identifiable as such to the controller.
1.2.14.3.5
A clearance issued as a downstream clearance shall be clearly identifiable as such to the pilot.
1.2.14.4
Termination of downstream clearance delivery service
1.2.14.4.1
Termination of downstream clearance delivery service shall only be initiated by the airborne system.
1.2.14.4.2

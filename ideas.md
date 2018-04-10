## Interworking of APNA and TCP
The idea was to create apna session-id/eph-id for each TCP flow(i.e. the standard 5 tuple flow).
So how can we achieve this?
- In my regard it can be transparent i.e. whenever the first SYN packet in sent we create a new apna session-id and whenever both client and server reached closed state in TCP state diagram we destroy the apna session-id as well.
- It is very similar to one more handshake like TCP but for APNA.

Concern:
- Using the same APNA session-id for a TCP flow seems bit counter-intutive for privacy because then an adversay can identify that the two packets are coming from the same host. So host-unlinkability would be violated in that case.

Solution:
- Whenever a sender sends a packet in the payload it also sends a session-ID which should be used while sending the reply back. The process of generation of session-ID could be asynchrously so that it would not cause an extra overhead to create the APNA header.

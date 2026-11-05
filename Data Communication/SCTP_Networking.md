div align="center">SCTP
Stream Control Transmission Protocol
An Academic Presentation on Data Communication

Reliable Message Transfer · Multistreaming · Multihoming

ICT-3101 — Data Communication
Department of Information and Communication Technology
Mawlana Bhashani Science and Technology University
</div>Submitted To
Dr. Nazrul Islam
Associate Professor
Department of Information and Communication Technology
Mawlana Bhashani Science and Technology University
Submitted By
Information	Details
Name	Md. Mashrafi Rahman
Student ID	IT-24034
Year and Semester	3rd Year, 1st Semester
Department	Information and Communication Technology
University	Mawlana Bhashani Science and Technology University
Course Code	ICT-3101
Course Title	Data Communication


About This Presentation
This academic presentation explains the Stream Control Transmission Protocol (SCTP), a reliable, message-oriented transport-layer protocol. It introduces SCTP's main features, association setup, packet structure and applications, with comparisons to TCP and UDP.

The presentation focuses on two important capabilities:
- Multistreaming: multiple streams within one association, with independent ordering within each stream.
- Multihoming: multiple endpoint addresses that can support alternate network paths and failover.
Presentation Outline
Slide	Topic
01	Title and Introduction
02	What Is SCTP?
03	Why Was SCTP Needed?
04	Key Features
05	Multistreaming
06	Multihoming
07	Association Setup: The Four-Way Handshake
08	SCTP Packet Structure
09	SCTP vs. TCP vs. UDP
10	Applications of SCTP
11	Conclusion


Key Concepts
Reliable Message Transfer
SCTP preserves message boundaries and uses acknowledgements and retransmission to recover missing data. CRC32c detects accidental corruption. Flow control manages receiver capacity, while congestion control responds to network load.
Multistreaming
Each ordered stream maintains its own delivery sequence. A missing message in one stream does not impose the same ordering delay on complete messages in another stream. Shared congestion and other delays can still affect multiple streams.
Multihoming
An endpoint can have multiple IP addresses. If a primary path fails, SCTP can use an alternate reachable path while preserving the association. Recovery may introduce a delay. Base SCTP does not automatically combine path bandwidth.
Four-Way Handshake
Step	Direction	Message
1	Endpoint A to Endpoint B	INIT
2	Endpoint B to Endpoint A	INIT ACK with a state cookie
3	Endpoint A to Endpoint B	COOKIE ECHO
4	Endpoint B to Endpoint A	COOKIE ACK


The cookie mechanism helps limit resource exhaustion during setup. SCTP itself does not encrypt application data.
SCTP, TCP and UDP at a Glance
Feature	SCTP	TCP	UDP
Data service	Messages	Byte stream	Datagrams
Built-in reliable delivery	Yes	Yes	No
Ordering	Per stream, or unordered delivery	One ordered byte stream	No guarantee
Multistreaming	Yes	No in base TCP	No stream model
Multihoming with failover	Yes	No in base TCP	No built-in failover
Normal connection setup	Four-way handshake	Three-way handshake	No connection handshake


This comparison covers the base protocols. Applications and extensions can provide additional capabilities.
Applications
SCTP supports telecom signaling and WebRTC data channels. In WebRTC, SCTP runs over DTLS over ICE/UDP for non-media data. WebRTC data channels do not use SCTP multihoming.
Presentation Video
YouTube link: To be added after the video is uploaded.
<!-- Replace the line above with: [Watch the presentation on YouTube](YOUR_ACTUAL_VIDEO_URL) -->Suggested File Organization
The following names provide a simple structure for uploading the presentation materials. Add the files as they become available.
Location	Purpose
README.md	Presentation overview and academic information
slides/SCTP_Presentation.pptx	Final presentation slides
notes/SCTP_Script.pdf	Optional printable speaking script
handnotes/page-01.png to page-05.png	Handwritten-style presentation notes


References
1. RFC 9260 — Stream Control Transmission Protocol
2. RFC 3286 — An Introduction to the Stream Control Transmission Protocol
3. RFC 8831 — WebRTC Data Channels
<div align="center">Prepared by Md. Mashrafi Rahman · IT-24034
Academic coursework for ICT-3101, Data Communication
MBSTU
</div>

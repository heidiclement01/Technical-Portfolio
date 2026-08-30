# Cybersecurity Incident Report:  Network Traffic Analysis

## Summary:  

Several users reported being unable to access the example website 'yummyrecipesforme.com' and received the error "destination port unreachable". IT confirmed the issue was still occurring then used a network analyzer tool (tcpdump) to troubleshoot. I am tasked with writing up and analyzing the findings. These are the relevant excerpts from the example tcpdump output: 

13:24:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain:  35084+ A? yummyrecipesforme.com. (24)
13:24:36.098564 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 254

13:26:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain:  35084+ A? yummyrecipesforme.com. (24)
13:27:15.934126 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 320

13:28:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain:  35084+ A? yummyrecipesforme.com. (24)
13:28:50.022967 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 150


## Part One:  DNS & ICMP Traffic Analysis

**UDP Protocol Findings:**  UDP port 53 is unreachable.

**ICMP Findings:**  UDP port 53 on IP 203.0.113.2 is unreachable.

**Affected Port & Service:**  Port 53, which is used for DNS (Domain Name System) traffic.

**Most Likely Issue:**  The destination port (53) on the destination host (IP 203.0.113.2) is unavailable for DNS (Domain Name System) traffic use.


## Part Two:  Incident Analysis

**Time of Incident:** 13:24:32.192571 is the first recorded attempt, though the incident was reported prior to the examination.

**How the Incident Was Identified:**  Multiple users reported an inability to reach the fictitious website 'yummyrecipesforme.com' and received the error "Destination Port Unreachable" when attempting to load.

**Investigation Performed:**  The IT department first attempted to recreate the issue successfully.  They then used tcpdump as a network analyzer to capture the incident for analysis, resulting in the output above.  They then analyzed the log for errors and other relevant information.

**Key Findings:**  Three attempts were made by the source computer (IP 192.51.100.15, port 52444) to retrieve the A-record from the destination computer (IP 203.0.113.2, port 53).  Each time the response was the ICMP error 'udp port 53 unreachable' in place of the DNS response.  

**Likely Cause:**  The likeliest cause is that the destination host is unable to accept the DNS request on port 53.  There are many reasons this could occur, so this does not give the root cause.  Further investigation would be required to determine the actual issue's underlying cause.

**Next Steps:**  We know the error is occurring somewhere after the third layer of the OSI model.  This does not give us an answer, but does give us a starting point to continue our investigation.  With the destination host being able to return the error, my next focus would be to confirm whether the DNS process is running.  

If not, why?  I'd review various logs to locate any recorded errors or failures, including Event Viewer if it's a Windows server.  Then I'd investigate and remediate the conditions and start the DNS process.  I'd verify the UDP port 53 is listening, then retest.  If it is running, I would instead move on to verifying the port is listening.  I'd check logs after that, remediating and restarting as needed.  I'd check if the port is listening once more and retest it.

If these don't resolve the issue, I'd expand my investigation to other potential causes.  I would check for recent changes, specifically around the start of the issue - not the start of the investigation.  I'd verify if it was a firewall issue, for example.  I would start with the more direct steps I mentioned before diving into the expanded possibilities.  This prevents wasted time and rules out possibilities systematically, helping reduce bias and assumptions.

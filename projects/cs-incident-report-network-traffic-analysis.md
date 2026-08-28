# Cybersecurity Incident Report:  Network Traffic Analysis

## Summary:  

Several users reported being unable to access the example website 'yummyrecipesforme..com' and received the error "destination port unreachable". IT confirmed the issue was still occurring then used a network analyzer tool (tcpdump) to troubleshoot. I am tasked with writing up and analyzing the findings. These are the relevant excerpts from the example tcpdump output: 

13:24:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain:  35084+ A? yummyrecipesforme.com. (24)
13:24:36.098564 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 254

13:26:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain:  35084+ A? yummyrecipesforme.com. (24)
13:27:15.934126 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 320

13:28:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain:  35084+ A? yummyrecipesforme.com. (24)
13:28:50.022967 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 150

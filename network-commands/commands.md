1. ifconfig / ip – View or Configure Network Interfaces

    Syntax:

        ifconfig (legacy)

        ip a or ip addr show (modern replacement)

    What it does: Displays or configures network interfaces.

    Forensic use: To identify active interfaces and their IPs.

Example:

ip a

Checks which IP addresses are assigned to the system—helps detect spoofed or unusual setups.

2. netstat – Display Network Connections

    Syntax:

        netstat -tuln (legacy)

    What it does: Shows listening ports and active connections.

    Forensic use: To identify suspicious or unauthorized services and open ports.

Example:

netstat -tuln

Lists open TCP/UDP ports and services listening on them.
3. tcpdump – Capture Network Traffic

    Syntax: tcpdump [options]

    What it does: Captures and analyzes packet-level traffic on the network.

    Forensic use: To capture live traffic from a suspect machine or interface.

Example:

tcpdump -i eth0 -w capture.pcap

Captures all traffic from eth0 into a .pcap file for later analysis.

4. hostname – Display or Set Hostname

    Syntax: hostname

    What it does: Displays the current hostname of the system.

    Forensic use: Helps identify the system in multi-host environments or when hostname spoofing is suspected.

Example:

hostname

Checks if the system hostname has been tampered with (e.g., to impersonate another machine).

5. ping – Test Network Reachability

    Syntax: ping [hostname or IP]

    What it does: Sends ICMP echo requests to test connectivity.

    Forensic use: To verify if a suspect system or C2 server is online.

Example:

ping 192.168.1.50

Checks if the remote system is up (could be a malicious actor's machine).

6. nslookup – Query DNS for Domain/IP Info

    Syntax: nslookup [domain or IP]

    What it does: Resolves domain names to IPs and vice versa using DNS.

    Forensic use: To investigate suspicious domains or verify if DNS resolution is being tampered with.

Example:

nslookup attacker-server.xyz

Finds the IP address of a potentially malicious domain for further investigation.

7. dig – DNS Lookup

    Syntax: dig [domain]

    What it does: Perform advanced queries on DNS servers for information about a domain.

    Forensic use: To inspect DNS records of suspicious domains (e.g., phishing or C2 domains).

Example:

dig attacker-server.xyz

Checks DNS resolution—could reveal hosting location or redirection behavior.

8. nmap – Network Scanning

    Syntax: nmap [options] [target IP/domain]

    What it does: Scans networks for open ports, services, and OS fingerprinting.

    Forensic use: To assess what services are running on a suspect system or to detect unauthorized hosts.

Example:

nmap -sV 192.168.1.20

Scans and identifies versions of running services on a host.

9. curl – Transfer Data from or to a Server

    Syntax: curl [options] [URL]

    What it does: Fetches data from a remote server (HTTP, FTP, etc.).

    Forensic use: To inspect or download web content from suspicious URLs.

Example:

curl -I http://malicious.site

Fetches HTTP headers for analysis of a potentially malicious site.

10. whois – Domain Ownership Lookup

    Syntax: whois [domain]

    What it does: Provides registration info for a domain.

    Forensic use: To track ownership or hosting information for suspect domains.

Example:

whois attacker-server.xyz

Identifies registrar, creation date, and possible owner of a domain.

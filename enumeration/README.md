# Enumeration

## Objective 

Analyze structure network telemetry to identify indiators of compromise (IOCs), attacker infrastructure, and trough systematic data enumeration.

## Skills Demonstrated
- JSON parsing
- Threat hunting
- DNS analysis
- TLS certificate analysis
- IOC extraction
- Linux command line

## Tools
- jq
- sort
- head
- Kali Linux

## Methodology

## Problem 1

### Step 1 - Analyze Network Telemetry

Network event data stored in JSON format was examined using the 'jq' command-line utility. Relevant fields were extracted to identify suspicious activity and reduce the amount of data requiring manual inspection.

(SS)

### Step 2 - Identify Suspicious Files

Event records were filtered to locate files associated with potentially malicious activity. This helped identify artifacts that warranted further investigation.

(SS)

### Step 3 - Investigate Network Connections

Connection records were analyzed to determine which external systems communicated most frequently with the victim host. Internal infrastructure was distinguished from external IP addresses to focus on the investigation on potential attacker-controlled systems. 

(SS)

### Step 4 - Identify Command-and-Control Infrastructure

DNS, HTTP and TLS events were correlated to identify suspicious domains used during attacker communications. Network metadata was examined to determine the fully qualified domain name (FQDN) associated with the malicious activity

### Step 5 - Inspect TLS Certificate Info

TLS metadata was reviewed to extract certificate information associated with the suspicious domain. Certificate attributes provide valuable threat hunting and incident investigation

(SS)

## Findings
- Identified suspicious files and network artifacts
- Distinguished between internal and external network communication
- Located a suspicious command-and-control domain
- Extracted TLS certificate information associated with attacker infrastructure
- Demonstrated how multiple network artifacts can be correlated to support an investigation

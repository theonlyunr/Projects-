
# Network Packet Analysis Tool

This document outlines the steps to set up and run a network packet analysis tool using Python. The tool analyzes PCAP files and detects potential network issues like port scanning and ARP/DNS spoofing.

## Features

- **PCAP File Analysis**: Reads and processes PCAP files to extract packet information.
- **Bandwidth Calculation**: Computes total bandwidth usage from analyzed packets.
- **Protocol Distribution**: Displays the distribution of different network protocols.
- **IP Communication Analysis**: Analyzes communication between source and destination IP addresses.
- **Port Scanning Detection**: Identifies potential port scanning activity based on packet frequency to multiple ports.
- **ARP Spoofing Detection**: Detects ARP spoofing attempts by monitoring IP-MAC address associations.
- **DNS Spoofing Detection**: Alerts when a domain resolves to multiple IP addresses unexpectedly.

## Requirements

To run the code, you'll need the following Python packages:

- **Scapy**: For packet manipulation and analysis.
- **Pandas**: For data manipulation and analysis.
- **Tabulate**: For formatted table output.
- **TQDM**: For progress bars in loops.

## Installation Steps

1. **Install Python**: Make sure Python (3.6 or higher) is installed on your PC. You can download it from the [official Python website](https://www.python.org/downloads/).

2. **Install Required Modules**: Open your command prompt (CMD) or terminal and run the following commands to install the required modules:

   ```bash
   pip install scapy pandas tabulate tqdm
   ```

3. **Save the Code**: Copy the provided Python code into a file named `network_analysis.py`.

4. **Download a PCAP File**: Ensure you have a PCAP file to analyze. You can find sample PCAP files from [Wireshark Sample Captures](https://wiki.wireshark.org/SampleCaptures).

## Running the Tool

To run the tool, use the command line and execute the following command:

```bash
python network_analysis.py <path_to_pcap_file> [port_scan_threshold]
```

- Replace `<path_to_pcap_file>` with the path to your PCAP file.
- The optional `port_scan_threshold` argument can be set to specify the threshold for detecting potential port scanning (default is 100).

### Example Command

```bash
python network_analysis.py D:\Downloads\example.pcap 150
```

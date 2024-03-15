This Python script utilizes the Scapy library to implement a packet sniffer capable of capturing and logging information about ARP, ICMP, and BOOTP packets. Here's a brief summary of the key components:

1. **Packet Sniffer Function (`packet_sniffer`)**:
   - This function takes a packet as input and attempts to process it.
   - It checks for specific packet types (ARP, ICMP, BOOTP) and logs information about them.
   - If the packet type is unknown or an error occurs during processing, it logs a corresponding message.

2. **Main Script Execution**:
   - The script configures the logging module to log messages to a file named `packet_sniffer.log` at the `INFO` level.
   - It sets up a console handler to print log messages to the console in addition to logging them to the file.
   - The script starts by logging a message indicating that the packet sniffer has started.
   - Using Scapy's `sniff` function, it captures ARP, ICMP, and BOOTP packets based on specified filters (`filter` parameter).
   - For each captured packet, the `packet_sniffer` function is invoked to process and log information about the packet.

3. **Execution Flow**:
   - The script execution starts from the `__name__ == "__main__"` block.
   - The logging configuration is set up.
   - The packet sniffer is initiated with three separate `sniff` calls, each targeting specific packet types.
   - As packets are captured and processed, relevant information is logged both to the console and the log file.

4. **Logging Configuration**:
   - The logging module is configured to include timestamps, log levels, and log messages in a consistent format for both console and file output.

Overall, this script serves as a basic packet sniffer tool capable of monitoring network traffic and logging relevant information for analysis or debugging purposes.

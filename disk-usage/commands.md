1. lsusb – List USB Devices

    Syntax: lsusb

    What it does: Lists all USB devices currently connected.

    Forensic use: Detect unauthorized or suspicious USB devices (e.g., thumb drives, HID injectors).

Example:

lsusb

Check if a rogue USB device (e.g. Rubber Ducky or storage) was inserted.

2. htop – Interactive Process Monitor

    Syntax: htop

    What it does: Displays real-time system resource usage with an interactive UI.

    Forensic use: Spot unusual or hidden processes using CPU/memory.

Example:

htop

Identify suspicious background processes or sudden resource spikes.

3. btop – Modern Resource Monitor (Graphical)

    Syntax: btop

    What it does: Advanced real-time monitoring tool with CPU, RAM, disk, and network stats.

    Forensic use: Visually catch performance anomalies from hidden malware or cryptominers.

Example:

btop

Use in live analysis to detect malicious processes or system stress.

4. mpstat – CPU Usage Stats per Core

    Syntax: mpstat -P ALL 1

    What it does: Displays per-core CPU usage over time.

    Forensic use: Catch CPU spikes caused by stealthy background tasks (e.g., crypto mining, exfil tools).

Example:

mpstat -P ALL 1

Shows CPU activity per second for all cores.

5. vmstat – System Memory and CPU Overview

    Syntax: vmstat 1

    What it does: Displays memory, swap, I/O, and CPU usage periodically.

    Forensic use: Analyze memory pressure or I/O bottlenecks caused by malware or data exfiltration.

Example:

vmstat 1

Continuously monitors system performance every second.

6. cat /proc/meminfo – Show Detailed Memory Info

    Syntax: cat /proc/meminfo

    What it does: Displays memory stats including total/free RAM, buffers, cached pages.

    Forensic use: Review memory consumption patterns or identify anomalies in memory use.

Example:

cat /proc/meminfo

Provides in-depth view of RAM usage — useful in memory forensics.

7. cat /proc/cpuinfo – View CPU Hardware Details

    Syntax: cat /proc/cpuinfo

    What it does: Lists processor model, architecture, number of cores, and flags.

    Forensic use: Profile system hardware to verify environment (e.g., detect virtual machines, spoofed CPUs).

Example:

cat /proc/cpuinfo

Check if system is running in a VM or has virtualization features enabled.

8. df – Show Disk Space Usage

    Syntax: df -h

    What it does: Displays disk space usage of mounted filesystems.

    Forensic use: Check for full or suspiciously filled partitions (e.g., /tmp, /var).

Example:

df -h

Quick overview of disk usage in human-readable format.

9. file – Determine File Type (Detect Hidden Formats)

    Syntax: file [filename]

    What it does: Identifies file types based on content, not just extension.

    Forensic use: Detect renamed or disguised files (e.g., .jpg that’s actually an archive).

Example:

file secret.docx

Reveals if the file is actually a ZIP archive.

10. stat – Show File Metadata

    Syntax: stat [filename]

    What it does: Displays file size, access, modify, and change timestamps.

    Forensic use: Audit timestamps for tampering or recent file manipulation.

Example:

stat /home/suspect/hidden.bin

Check when a suspicious file was last accessed or modified.

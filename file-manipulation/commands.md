1. ls – List Directory Contents

    Syntax: ls [options] [path]

    What it does: Lists files and directories in a specified path.

    Forensic use: To view directory contents and detect suspicious or hidden files.

Example:

ls -la /home/suspect

Shows all files (including hidden ones) with details in the suspect's home directory.

2. cp – Copy Files and Directories

    Syntax: cp [options] source destination

    What it does: Copies files or directories from one location to another.

    Forensic use: To safely duplicate evidence files for analysis.

Example:

cp -p /mnt/usb/evidence.txt /home/analyst/case1/

Copies a file while preserving timestamps and metadata.

3. mv – Move or Rename Files

    Syntax: mv [source] [destination]

    What it does: Moves or renames files/directories.

    Forensic use: To organize collected evidence without modifying content.

Example:

mv report.txt report_case123.txt

Renames a report for better identification in the case.

4. rm – Remove Files or Directories

    Syntax: rm [options] file

    What it does: Deletes files or directories.

    Forensic use: Cautiously used in controlled environments; often for cleanup after copying.

Example:

rm -r /tmp/tempfiles/

Removes temporary working files (after evidence is secured).

5. cat – Concatenate and Display Files

    Syntax: cat filename

    What it does: Displays contents of a file.

    Forensic use: To read log files or suspect data files quickly.

Example:

cat /var/log/auth.log

Reviews authentication logs for unauthorized access.

6. more / less – View Large Files One Page at a Time

    Syntax: less filename or more filename

    What it does: Paginates output for easier viewing of large files.

    Forensic use: Used to analyze long logs or email dumps.

Example:

less /var/log/syslog

Scroll through system logs to find anomalies.

7. file – Determine File Type

    Syntax: file filename

    What it does: Identifies the file type (text, binary, etc.).

    Forensic use: To detect disguised or malicious files (e.g., .jpg files that are actually scripts).

Example:

file suspect_attachment.jpg

Might reveal the file is not really an image.

8. find – Search Files and Directories

    Syntax: find [path] [options]

    What it does: Searches files by name, size, date, etc.

    Forensic use: To locate specific files or recently modified files during the time of a breach.

Example:

find /home/suspect -type f -mtime -2

Finds files modified in the last 2 days.

9. touch – Change File Timestamps or Create Files

    Syntax: touch filename

    What it does: Creates a new file or updates the timestamp of an existing file.

    Forensic use: May be used to check for timestamp tampering.

Example:

touch -t 202507041200 suspicious_file.txt

Sets a fake timestamp for testing analysis tools (note: altering timestamps should be done carefully).

10. stat – Display File Metadata

    Syntax: stat filename

    What it does: Shows detailed info like size, permissions, and timestamps.

    Forensic use: To analyze file metadata (e.g., time of creation, last access).

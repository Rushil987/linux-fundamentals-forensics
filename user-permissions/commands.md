1. whoami – Show Current User

    Syntax: whoami

    What it does: Displays the currently logged-in user.

    Forensic use: Verify if you’re running with elevated or unauthorized user privileges.

Example:

whoami

Check if malware escalated privileges (e.g., returns root unexpectedly).

2. id – Show User and Group IDs

    Syntax: id [username]

    What it does: Displays UID, GID, and group memberships.

    Forensic use: To check which groups a user belongs to (e.g., if a user is in sudo or admin).

Example:

id john

Verifies if "john" has elevated group access.

3. groups – Show User Group Memberships

    Syntax: groups [username]

    What it does: Lists all groups a user belongs to.

    Forensic use: Useful to audit user privileges.

Example:

groups analyst

Checks if an analyst account has unauthorized group assignments.

4. chmod – Change File Permissions

    Syntax: chmod [permissions] [file]

    What it does: Sets read, write, execute permissions.

    Forensic use: Detect files with overly permissive or suspicious access rights.

Example:

chmod 600 secrets.txt

Locks down a sensitive file to owner-only access.

5. chown – Change File Ownership

    Syntax: chown [owner]:[group] [file]

    What it does: Changes the owner and/or group of a file.

    Forensic use: Investigate if attackers changed ownership to hide files.

Example:

chown root:root backdoor.sh

Corrects ownership on a file that was changed by malware.

6. ls -l – List Files with Permissions

    Syntax: ls -l [directory]

    What it does: Displays detailed file permissions, ownership, and type.

    Forensic use: Spot files with unusual permissions (e.g., world-writable scripts).

Example:

ls -l /home/suspect/scripts/

Lists who can read, write, or execute those files.

7. find (with -perm) – Search by Permission

    Syntax: find [path] -perm [mode]

    What it does: Finds files with specific permission modes.

    Forensic use: Identify files with dangerous or suspicious permissions.

Example:

find / -perm -4000

Finds all files with the SUID bit set (often used in privilege escalation).

8. sudo – Execute as Another User

    Syntax: sudo [command]

    What it does: Runs a command as another user, typically root.

    Forensic use: Check logs and configs to see who used or abused sudo rights.

Example:

sudo less /var/log/auth.log

Access restricted logs with elevated privileges for review.

9. w – Show Who is Logged In and What They’re Doing

    Syntax: w

    What it does: Displays logged-in users, their activity, and login times.

    Forensic use: See if an attacker is or was active on the system.

Example:

w

Lists active sessions and what each user is doing (e.g., shell, command).

10. last – Show Login History

    Syntax: last [username]

    What it does: Shows recent login/logout records from /var/log/wtmp.

    Forensic use: Track login activity and possible unauthorized access.

Example:

last hacker

Reveals all logins for "hacker" user, with timestamps and IPs.

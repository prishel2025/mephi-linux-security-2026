# MEPHI Linux Security 2026

Student number: 374526
GitHub: prishel2025

1. Created user1 with UID 1234 and group students.
   Maximum password age: 90 days.
2. SUID files: files-suid.out.
   Processes with EUID 0 and ordinary-user RUID: processes.out.
3. Copied cat to /home/user1/cat-suid.
   Without SUID, reading /root/setuid-demo.txt failed.
   With mode 4755 and root ownership, reading succeeded.
   stat.out records the demonstration permissions.
   SUID was removed after collecting evidence.
4. Copied chown to /home/user1/chown-cap.
   Assigned cap_chown=ep.
   user1 successfully changed owner-demo.txt ownership to root.
5. sudoers permits user1 to run /usr/bin/date as root.
   Verified by running sudo /usr/bin/date as user1.

The shadow file is a sanitized copy:
all password fields were replaced with REDACTED.
The original /etc/shadow is not published.

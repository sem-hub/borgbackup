**borgbackup** is a configurable script for Borg backup system.
It's based on a script from official Borg documentation
	(https://borgbackup.readthedocs.io/en/stable/quickstart.html)
but more flexible. It checks if backup repo exists and create it otherwise.
Do backup with **borg** and clean up before exit.
It gets parameters from environment variables. So, usually you don't
want to run it directly. Use next script instead:

**borgbackup-tohost** gets username@host as an argument, set some environment
variables and run **borgbackup** script with sudo (you need sudo to access ALL
files).
Edit it for your system, especially BORG_LOCAL_INCLUDES and BORG_LOCAL_EXCLUDES.

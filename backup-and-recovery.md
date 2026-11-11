# Backup and recovery

## One nightly backup

A single nightly job can back up Mercury to an encrypted repository outside
the host. It covers PostgreSQL, agent computer volumes, and protected
configuration and keys, plus website Vault data when enabled.

Each managed Linux agent computer stores its workspace on a dedicated
persistent volume, separate from the container that runs it. The same nightly
job backs up those volumes along with the database, so recovery can bring back
both a scheduled job and the workspace files it uses.

## How recovery works

To recover on a replacement host, install the matching Mercury release and
restore the database, volumes, and protected configuration and keys from a
completed backup. Before reopening access, verify sign-in and saved work.
If scheduling is enabled, test a restored workflow that uses a saved workspace
file.

Choose a backup location and retention period. Assign responsibility for
failure alerts and recovery credentials, and test a restore against the
deployment's recovery targets.

[Mercury overview](README.md)

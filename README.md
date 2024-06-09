# albackup
albackup is an rsync wrapper to make backups.
Original written by John Mørck Hansen, but abandoned

Works very well.

# Initial setup

Move sbin/albackup to /sbin/albackup/
Move etc/albackup/ to /etc/albackup/

In each of the /etc/albackup/*.conf (just copy the localhost.conf to each of the machines you like to backup).

In each of the files change these lines.

* CLIENT="localhost" - changes the name below BASEDIR
* CLIENT_IP="127.0.0.1" - IP address of the server to backup
* BASEDIR="/backup" - Location of the backup
* BACKUP_DIRS=(/dir1 /dir2 /dir3) - List of the directories to backup

# Usage
Run /sbin/albackup as root

Copies the /etc/albackup/*.conf files to the backuo directy as a full backup,
but using hardlinks, i.e. the sum of every backup costs roughly the same as one
full backup.

You can delete any data backups without loosing any files in the other
backups. Very clever.

20230704-012047  20240422-011716  20240512-014425  20240527-022511
20231024-030605  20240423-024955  20240513-011820  20240528-011738
20231027-065221  20240428-011904  20240514-022009  20240529-022800
20240420-011713  20240510-112219  20240525-020906  20240609-024338
20240421-025012  20240511-012013  20240526-011904  current
peter.toft@pto-VirtualBox:~/tmp/albackup2$ 

exec into client

scp sumit@<server-pod-ip>:/home/sumit/file.zip ./file-scp.zip
password - sumit

# adding this, will not ask for confirmation
scp -o  StrictHostKeyChecking=no

# sshpass tool to pass password to scp but will not print output

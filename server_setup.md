# Server setup

## Create users
Add the user.

```
adduser <username>
```
Enter user's password.
Set default info (optional).

### Add user to sudo group

```
usermod -aG sudo <username>
```
-a, --append
Add the user to the supplementary group(s). Use only with the -G option.
-G, --groups
A list of supplementary groups which the user is also a member of.

## Create authentication key pair
Create a directory to store public keys and set permissions.
```
mkdir ~/.ssh && chmod 700 ~/.ssh
```
### Add public key
Use Secure Copy Protocol (scp) to copy the public key to the remote server.  
**Windows:**
```
scp $env:USERPROFILE/.ssh/id_rsa.pub <username>@<server-address>:~/.ssh/authorized_keys
```


# Server Setup

`ssh root@YOUR_IP OR ssh -i ~/.ssh/fsfe root@YOUR_IP`

- Make sure keychain is active
`vi ~/.ssh/config`
```
AddKeysToAgent yes
UseKeyChain yes
````

- Add private key to keychain
`ssh-add -K ~/.ssh/fsfe`

- Update software
`apt update`

- Upgrade software
`apt upgrade`

- Add new user
`adduser $USERNAME`

- Add user to “sudo” group
`usermod -aG sudo $YOUR_USERNAME`

- Switch user
`su $YOUR_USERNAME`

- Check sudo access 
`sudo cat /var/log/auth.log`

- Change to home directory
`cd ~`

- Create a new directory if it doesn’t exist
`mkdir -p ~/.ssh`

- Create authorized_keys file and paste PUBLIC key 
`vi ~/.ssh/authorized_keys`

- Restart ssh daemon
`sudo service sshd restart`

- Exit
`exit`
`exit`

- Login with new user
`ssh $USERNAME@IP_ADDRESS`

# Setting Up SSH and Firewall

## Objective
1. Installing an open-ssh server.
2. Setting up the firewall for the server.
3. Allow only a required port so that non-authorized people can't access the Homelab.

## Install and setting up SSH
1. Install the open-ssh by using "sudo apt install openssh-server" command.
2. Start the openssh-server by using "systemctl start ssh" command.
3. check the ssh server by using "systemctl status ssh" command.
4. Change the server IP into static IP by making a config with "sudo nano /etc/netplan/00-installer-config.yaml" command.
5. Apply the configuration "sudo netplan apply" command.
6. When it's done, try to connect to the Homelab server with command prompt on windows.
7. Use the command "ssh admin1@192.168.146.5" in the windows cmd and enter the password.

## Setting up firewall
1. Change the policy of firewall first to deny an incoming to the server by using "sudo ufw default deny incoming"
2. Go to the /etc/ssh directory and edit the sshd_config to set the port that we wanted to open (in this case is port 2222).
3. Update the firewall rules by opening the 2222 port and use "sudo ufw allow 2222/tcp" command.
4. Try to connect to the ubuntu server by doing a SSH.

## Problems
We ran into a problem! it seems that we can't connect to the server. There might be some possibilites such as : 
1. There is a problem in the config file.
2. The firewall policy isn't updated.
3. The firewall isn't activated.

## Troubleshooting and solving the problems
1. Check the firewall status using "ufw status verbose" command. (status inactive)
2. Check if the firewall is using the 2222 port. Use "sudo ss -tlnp | grep ssh" command. (ssh is using the 2222 port)
3. Start the firewall and check the status.
4. Restart the ssh service by using "systemctl restart ssh"
5. Do an ssh again in windows command prompt by using "ssh admin1@192.168.146.5 -p 2222"

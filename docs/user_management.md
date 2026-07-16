# User Management

## Objective
Add user and groups, Manage user and groups, Give permission to user and Groups.

## Users 
1. Admin
2. Developer
3. User

## Groups
1. Admin
2. Developers
3. Users

## Command Used
1. useradd / useradd -G
2. groupadd
3. passwd
4. chmod
5. chown

## Adding Group and User
1. Add a group with sudo groupadd group_name command
2. Add a user with sudo useradd -G group_name user_name command
3. Set a password for a user using passwd command
4. Give he admin group a special permission by editing the visudo files. Use the "sudo visudo" command.
5. Give the admin group a root access by writing a "%admin ALL=(ALL:ALL) ALL" config in the file.

## Validate User and Groups
1. See the list of user and group by using "cat /etc/group" command.
2. See the username of user by using "id username"

# OverTheWire | Bandi

## Background

The password for the next level is stored somewhere on the server and has all of the following properties:  

- owned by user bandit7  
- owned by group bandit6  
- 33 bytes in size  

## Solutions

`find / -user bandit7 -group bandit6 -size 33c`  
..  
/var/lib/dpkg/info/bandit7.password
..  

`cat /var/lib/dpkg/info/bandit7.password`  
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

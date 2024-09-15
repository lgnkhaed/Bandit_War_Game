# WriteUps 

## -> level 17 : 
  i used the command `nmap -p 31000-32000 localhost`  so i can find the port which is open 

i used this command to check the five ports found iif they are connected to ssl/tls , `openssl s_client -connect localhsot:$port` 
   
the two ports found are : 31790 and 31518  

i used the command `echo "kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx" | ncat --ssl localhost 31790` with the two ports and submitted the current password , the port 31790 reponse with the priavte rsakey 

< -----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY----->

i created a file called a raskey , then executed this command `ssh -i rsakey -p 2220 bandit17@bandit.labs.overthewire.org`

## -> level 18 :  password : x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
 i used this command ` diff passwords.new passwords.old` so i can the diffrent line between the file which is the code for the next level 

## -> level 19 : cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
 `ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme`  this command is used to excute the command cat readme without having to login  

## ->level 20 : 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
`ls -l ` : to find the name of the binary file 
`./bandit20-do cat /ec/bandit_pass/bandit20` : the first part of the command is used to excute the setuid binary file , then the other part to cat the password , *** in the descripion they ave the path '/etc/bandit_pass' and this is just a dorectory , so i had to cat the file bandit20 located in this file .  

## -> levzl 21 : EeoULMCra2q0dSkYj561DX7s1CpBuOBt
so i had to open twoterminals and connect to the profile bandit20 , after that i connected to localhost with the command `nc -lvp 9999` in te first terminal and the second i used `./suconnect 9999` in the second terminal , i sent from the first one the password of the previous level and got the password for the next one . 

## -> levzl 22: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
i changed directory with  `cd /etc/cron.d ` the, with `ls` i found the file named "cronjob_bandit22" , i used the command `cat` to see what it contains , it showed me the path for the script file , i used the `cat ` to find which command is runnig with that script , reading the script showed that he password is writtten in a file so i used this command to find the passwrod `cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv` 



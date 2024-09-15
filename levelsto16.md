# -> level 1 : 
## the password to level 1  : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

# -> level 2 : 
## the password to level 2 : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

# -> level 3 : 
## the password to level 3: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx  
spaces files we trat tthem in linux with 2 methods , 1-(we put the name between quots )"file name " 2- we use like this cat file\ name

# -> level 4 : 
## the password to level 4 : 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ   
 we use the command  ` ls -la`  to find  hidden files 

# -> level 5 :  
## the password to level 5  : 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw   

# -> level 6 : 
## the password to level 6 : HWasnPhtq9AVKe0dmk45nxy20cvUa6EG 
 i used the command `find` with the option `-type f` to specify the search about files  and the option `-size 1033` to find with the exact size  

# -> level 7 : 
## the password to level 7 :  morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj  
i used the command ``find``  with the option ``type f``  and the ``-size 33c``  and the option ``-user bandit7``  and `` -group bandit6 `` 

# -> level 8 : 
## the password to level 8 : dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc  
(``grep``  command used with the option ``-w``  for the word 'millionth and data.txt and ``-F``  for patterns )

# -> level 9 : 
## the password to level 9 : 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM 
i used the command ``sort``  to find sort the file into lines and used the command ``uniq``  and the option ``-u``  to find lines that are not repeated 

# -> level 10 : 
## the password to level 10 : FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey  
i used the command ``strings`` and ``grep``  with ``^=*`` 

# -> level 11 : 
## the password to level 11 : dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr 
i  used the command ``base64`` with the option `` --decode``   

# -> level 12 : 
## the password to level 12 : 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 
i used the command ``tr``  to decode the ROT13 code giving USING THIS ``A-za-z`` ``N-ZA-Mn-za-m``

# -> level 13 : 
## the password to level 13 : FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn 
 (i had to extract manu file with ``gzip`` and ``bunzip2`` ) ( i inspected with ``file`` command ) ( inspected zippped file with ``xxd file name | head `` verifiying the first codes ) ( ``tar command`` ) ( had to rename the file adding .gz and .bz2 to be able to extract it )

# -> level 14 : 
## the password to level 14 : MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS 
 in  the level 13 , with the username bandit13 , i found a file called sshkey.private which is the priavte key to log into level 14 , i used the command `` ssh -i sshekey.private -p 2220 bandit14@localhost`` , ones logged i went to /etc/bandit_pass and then ``cat bandit14 `` 

# -> level 15 : 
## the password to level 15 : 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo  
used `` nc localhost 30000 ``  to interact with the machine , i send the password the mean level and i got this password 

# -> level 16 : 
## the password to level 16 :kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx   
( i used the openssl command ``openssl s_client localhost:30001 -quiet``  s_client is an command that allowed me to use SSl/tls in connection , ones this command is done i have to ansswer to enter the local user  password and it responds with the password fot tthe level 16 ) ( in this level , i dived into HTTP protocol and HTTPS , i understood how SSl and TLS work )




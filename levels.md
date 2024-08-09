the password to level 1  : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

the password to level 2 : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

the password to level 3: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx  "spaces files we trat tthem in linux with 2 methods , 1-(we put the name between quots )"file name " 2- we use like this cat file\ name

the password to level 4 : 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ   " we use ls -la " for hidden files "

the password to level 5  : 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw   

the password to level 6 : HWasnPhtq9AVKe0dmk45nxy20cvUa6EG ( i used the command "find" with the option "-type f " to specify the search about files  and the option "-size 1033c" to find with the exact size  )

the password to level 7 :  morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj  (used the command "find" with the option ('type f') and the '-size 33c' and the option '-user bandit7 and '-group bandit6 )

the password to level 8 : dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc  ( "grep" command used with the option -w for the word 'millionth and data.txt and -F for patterns )

the password to level 9 : 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM ( used the command "sort" to find sort the file into lines and used the command uniq and the option "-u" to find lines that are not repeated  )

the password to level 10 : FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey  ( used the command "strings" and grep with '^=*'  )

the password to level 11 : dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr ( used the command "base64" with the option " --decode" )

the password to level 12 : 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 ( used the command "tr" to decode the ROT13 code giving USING THIS "A-za-z' 'N-ZA-Mn-za-m')

the password to level 13 : FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn ( i had to extract manu file with gzip and bunzip2 ) ( i inspected with file command ) ( inspected zippped file woth xxd file name | head verifiying the first codes ) ( tar command ) ( had to rename the file adding .gz and .bz2 to be able to extract it )

the password to level 14 : MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS , in the the level 13 , with the username bandit13 , i found a file called sshkey.private which is the priavte key to log into level 14 , i used the command " ssh -i sshekey.private -p 2220 bandit14@localhost" , ones logged i went to /etc/bandit_pass and then cat bandit14 

the password to level 15 : 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo , used " nc localhost 30000" to interact with the machine , i send the password the mean level and i got this password 





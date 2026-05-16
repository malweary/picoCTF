# MyGit
## Link: https://learn.cylabacademy.org/library/764
I began by cloning the git server on my terminal. 

After it finished cloning, I cd’d into the challenge directory, then ensured that the 'README.md' file was present by using ls.

I then used:

nano 'README.md'

This brought me to the following screen:

<img width="792" height="524" alt="Screenshot from 2026-05-15 20-59-43" src="https://github.com/user-attachments/assets/90cb9105-4e59-49db-9ea4-43fef75529f8" />


So, for this challenge, I needed to log on as root:root@picoctf and push flag.txt. 

I used the following commands to establish my name and email.

git config —global [user.name](http://user.name) “root”

git config —global [user.email](http://user.email) “root@picoctf”

After this, I proceeded to create a test file for flag.txt. I did this using:

echo test > flag.txt.

Then, I added flag.txt to my git repo, committed the change with “add flag”, then pushed, which gave me my final flag. 
<img width="744" height="422" alt="Screenshot from 2026-05-15 21-18-19" src="https://github.com/user-attachments/assets/12b8ed63-aebb-4349-ab9a-e896bb520b30" />

Flag: picoCTF{1mp3rs0n4t4_g17_345y_6877715a}

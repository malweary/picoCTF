This is a text transformation challenge, and the point of it is to take a starter flag and reverse the transformations that have been done.

<img width="798" height="262" alt="Undo1" src="https://github.com/user-attachments/assets/52f2e8ca-de4d-4303-92c7-9c127dfaac67" />

**Step One**

The first step was to reverse a Base64 encoded string. I knew that base64 -d is the correct way to do this, so I input:

<img width="801" height="395" alt="Undo2" src="https://github.com/user-attachments/assets/40824477-03ac-45e9-9a28-9babe0e2ee06" />

This was incorrect. I then went to do echo “flag” | base64 -d to see if this would work, but halfway through I had an epiphany: it wants to know the actual command without the string.

So, I input base64 -d, and this was correct.

<img width="628" height="208" alt="Undo3" src="https://github.com/user-attachments/assets/a67aff12-e498-4206-9cf8-d62a467993f9" />

**Step Two**

For step 2, I knew that the appropriate command for reversing a string is rev, so I input this.

<img width="624" height="208" alt="Undo4" src="https://github.com/user-attachments/assets/c0eab45a-6833-4b84-9a02-1770c3a450eb" />

**Step 3**

Originally for step 3, I thought some iteration of sed would work, so i tried that. That was not the answer, so I took a peek at the hint on the site. It was expecting me to use tr for this.

<img width="617" height="222" alt="Undo5" src="https://github.com/user-attachments/assets/fef3a044-d626-4751-ad66-09813571cbf2" />

The correct command to replace dashes with underscores is tr ‘-’ ‘_’.
<img width="630" height="208" alt="Undo6" src="https://github.com/user-attachments/assets/f346a60f-c049-4708-ab31-00f768cf9c0f" />

**Step Four**

I applied the same command for step 4, but did not expect this to work originally because of the integration of two characters. Fortunately, this did work.

<img width="779" height="518" alt="Undo7" src="https://github.com/user-attachments/assets/3627dbe7-785b-410d-a5ad-8ec1cc8e3d46" />

**Step Five**

Step 5 was more complicated to me, as I could not figure out the proper rotation. I did some trial and error, and eventually landed on “tr ‘A-MN-Za-mn-z’ ‘N-ZA-Mn-za-m’” as the correct answer. This is because A-M contains 13 characters, and vice versa, which will be applied to both uppercase and lowercase.

**Final Flag**

At the end, I was left with picoCTF{Revers1ng_t3xt_Tr4nsf0rm@t10ns_72088a35}, which was the correct flag.

# SHA256-Password-Cracking-Project
This script is a course project through the Python 101 course for Ethical Hacking at TCM Academy. 

This is another project I completed while going through the Python 101 course at TCM Academy,
The purpose of this script is to demonstate how SHA256 password cracking works using wordlists and hashing comparisons

This script takes a SHA256 hash as an input, runs through the "rockyou.txt" file, and hashes each password. It then compares it against the target hash until it finds a match. Even though it's a simple script it helped me understand how hashing, wordlists, and brute force work together in real world password attacks. 

*How the script works:*
- You provide the script with a SHA256 hash from the command line.
- It then loads the rockyou.txt wordlist
- Each candidate password is:
- Cleaned (strip("\n"))
- Encoded (latin-1 to support all characters from the wordlist)
- Hashed using sha256sumhex() from the pwntools library
- The script then compares the generated hash to your target.
- If a match is found, it prints the cracked password and exits immediately.

The script also uses pwntools "log.progress()" feature to show real time updates. 

*How to use the script:*
- First make sure pwntools is installed
- Then run the script in your terminal as this "python3 sha256-cracker.py <insert sha256_hash_here>"
- If the password exists in the text file provided you would then see something like "Password hash found after 56 attempts! hashes to password"
- If a password is *not* found you would get "Password hash not found"

As I mentioned before even though it is a basic password cracking script, As a beginner in cybersecurity it helps me understand how weak security measures can be exploited along with demonstrating core concepts in cybersecurity. It shows me that hashes aren't encrypted and that weak passwords can be cracked through wordlists. In the modern age where cyber crime is becoming more rampant along with data leaks it's important to understand how things like this work which is crucial for both Red team and Blue team. 

*LEGAL DISCLAIMER*

This script is for educational purposes only and was created as part of the Python 101 course on TCM Academy, Use it only on data you own or are authorized to test.

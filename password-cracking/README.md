# Password Cracking

## Objective

Recover plaintext passwords from given password hashes using password-cracking techniques. The goal was to identify the appropriate hash type and apply effective cracking strategies to recover the original password.

## Skills Demonstrated

- Password hash identification
- Hashcat
- Dictionary Attacks
- Linux Command line

## Tools Used

- Hashcat
- Kali Linux Machine

## Methodology

 ### Challenge 1 - Mask Atttack
 
 The first challenge consisted of password hashes that followed a revealed naming convention of ('SKY-MASK-####').

 Rather than performing a full brute-force attack (which can be resource intensive and time consuming), a mask attack was used to target only the unknown portion of each password.

 This can be done by using the hashcat -500 command.

 This significantly reduced the search space while allowing hashcat to effectively recover the passwords.

 (SS)

 ### Challenge 2 - NTLM Dictionary Attack

 The second challenge contained NTML password hashes.

 After preparing the hash file, a dictionary attack was perfomed using the 'Rockyou.txt' wordlist. This approach compared each candidate password against the supplied hashes until matching plaintext passwords were        
 identified.

These first had to be stripped of their first portion (pre-colon portion) then run a hashcat 1000 on the remaining hash.

(SS)

 ## Takeaways

 - Selecting the correct attack is often better than blind bruce force attacks
 - Mask attacks are highly effective when portions of the password are known
 - Dictionary attacks can quickly recover weak passwords
 - Understanding hash formats is essential for password cracking


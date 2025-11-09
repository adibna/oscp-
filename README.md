# First Enumeration 
Default `sudo nmap -sVC -T4 127.0.0.1 -oA results.txt`

UDP `nmap -sU 127.0.0.1` 

# Fuzzing

Directory
`ffuf -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u "http://127.0.0.1/FUZZ" -mc -ic`

Extensions
`ffuf -w wordlist.txt -u "http://127.0.0.1/indexFUZZ"`

Recursive
`ffuf -w wordlist.txt -u "http://127.0.0.1/FUZZ" -recursion -recursion-depth 1 -e .php -v`

VHOST
`ffuf -w wordlist.txt -u http://127.0.0.1/ -H 'Host: FUZZ.127.0.0.1' -fs xxx`

Good wordlists
| **Command**                                                               | **Description**         |
| ------------------------------------------------------------------------- | ----------------------- |
| `/opt/useful/seclists/Discovery/Web-Content/directory-list-2.3-small.txt` | Directory/Page Wordlist |
| `/opt/useful/seclists/Discovery/Web-Content/web-extensions.txt`           | Extensions Wordlist     |
| `/opt/useful/seclists/Discovery/DNS/subdomains-top1million-5000.txt`      | Domain Wordlist         |
| `/opt/useful/seclists/Discovery/Web-Content/burp-parameter-names.txt`     | Parameters Wordlist     |

# Services enumeration

FTP Enumeration

`ftp 127.0.0.1` - Connecting to the FTP server using the ftp client.

`nc -v 127.0.0.1 21` - Connecting to the FTP server using netcat.

`hydra -l user1 -P /usr/share/wordlists/rockyou.txt ftp://127.0.0.1` - Brute-forcing the FTP service.

Attacking SMB 

`netexec smb 127.0.0.1`

`netexec smb host/127.0.0.1 -u user -p pass --shares`

`netexec smb host/127.0.0.1 -u guest -p '' --shares`

`smbclient -N -L //ip`

`smbclient //127.0.0.1/share -N`

`smbclient //127.0.0.1/share -U username password`

Security in mind (Basic Web Enumeration) - `https://www.youtube.com/watch?v=ZE_4ab-fdpk`

Footprinting (Most Important) - `https://academy.hackthebox.com/module/112/section/1060`

Information Gathering - `https://academy.hackthebox.com/module/144/section/1247`

________________________________________________________________________________________

# Great Content (Maybe the most important in the journey)

I highly recommend that anyone who wants to pass the OSCP+, or gain more knowledge about pentesting in general, complete this course on HTB Academy. In my opinion, this is what gave me more than sufficient knowledge to pass the OSCP+ with full points.

CPTS - `https://academy.hackthebox.com/preview/certifications/htb-certified-penetration-testing-specialist`

Ippsec OSCP - `https://www.youtube.com/watch?v=2DqdPcbYcy8&list=PLidcsTyj9JXK-fnabFLVEvHinQ14Jy5tf`

HTB Machines to do - `docs.google.com/spreadsheets/u/1/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/htmlview`

The Cyber Mentor (Attacking Active Directory) - `https://www.youtube.com/watch?v=VXxH4n684HE&t=7392s`

The Cyber Mentor (Windows Privilege Escalation) - `https://www.youtube.com/watch?v=uTcrbNBcoxQ`

The Cyber Mentor (Linux Privilege Escalation) - `https://www.youtube.com/watch?v=ZTnwg3qCdVM&t=9s`

Derron C (Attacking Active Directory) - `https://www.youtube.com/watch?v=gY_9Dncjw-s&list=PLT08J44ErMmb9qaEeTYl5diQW6jWVHCR2&index=1`


# Final Considerations 

In my opinion, the OffSec Academy content for the OSCP+ isn't sufficient on its own, especially if you don't already have a solid background in the CTF and Pentesting field.

If you are starting from scratch, or perhaps transitioning from a Blue Team role and want to pass the OSCP+, the HTB Academy content combined with some boxes on HTB Labs will give you the necessary knowledge to pass more easily. I’ve seen many posts and other people talk about completing Pro Labs, but I didn't complete any of them and I don't feel like I missed out on anything.

I earned my OSWP before taking the OSCP+. One thing I can say is that the allotted time is definitely enough to pass while still taking breaks. My advice is to sleep well before the exam, relax, and maybe drink a lot of coffee (it worked for me XD). You get 23 hours and 45 minutes to score the 70/100 points needed to pass, and then another 23 hours and 45 minutes to finish the report.

I personally felt the Linux machines were easy. I had some difficulty with the Windows machines at one point, but I think that was just because I was very stressed and tired during the exam.

I can also confidently say that many of the machines on HTB nowadays are very similar to OSCP+ boxes. If you can complete Medium-level machines on HTB (or even some of the Easy ones), you will have zero difficulty with the OSCP+.

# YOU ARE THE NEXT OSCP+ MY FRIEND, I WISH GOOD LUCK!

<div class="tenor-gif-embed" data-postid="6610578319413376915" data-share-method="host" data-aspect-ratio="1" data-width="100%"><a href="https://tenor.com/view/trump-donald-trump-thumbs-up-you-the-best-you-are-the-best-gif-6610578319413376915">Trump Donald Trump GIF</a>from <a href="https://tenor.com/search/trump-gifs">Trump GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"></script>


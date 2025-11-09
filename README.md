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



Great Content (Maybe the most important in the journey)

Ippsec OSCP - `https://www.youtube.com/watch?v=2DqdPcbYcy8&list=PLidcsTyj9JXK-fnabFLVEvHinQ14Jy5tf`
HTB Machines to do - `docs.google.com/spreadsheets/u/1/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/htmlview`


**Delivery Machine**
Hack The Box: 

 

Delivery Machine : 

 

IP : 10.10.10.222 

 

 

Scanning and Info-gathering 

**Sudo nmap  -v –n –A 10.10.10.222**

Starting Nmap 7.91 ( https://nmap.org ) at 2021-05-18 12:15 IST 

NSE: Loaded 153 scripts for scanning. 

NSE: Script Pre-scanning. 

Initiating NSE at 12:15 

Completed NSE at 12:15, 0.00s elapsed 

Initiating NSE at 12:15 

Completed NSE at 12:15, 0.00s elapsed 

Initiating NSE at 12:15 

Completed NSE at 12:15, 0.00s elapsed 

Initiating Ping Scan at 12:15 

Scanning 10.10.10.222 [4 ports] 

Completed Ping Scan at 12:15, 0.33s elapsed (1 total hosts) 

Initiating SYN Stealth Scan at 12:15 

Scanning 10.10.10.222 [1000 ports] 

**Discovered open port 80/tcp on 10.10.10.222**

**Discovered open port 22/tcp on 10.10.10.222** 

Completed SYN Stealth Scan at 12:15, 2.20s elapsed (1000 total ports) 

Initiating Service scan at 12:15 

Scanning 2 services on 10.10.10.222 

Completed Service scan at 12:15, 6.56s elapsed (2 services on 1 host) 

Initiating OS detection (try #1) against 10.10.10.222 

Retrying OS detection (try #2) against 10.10.10.222 

Retrying OS detection (try #3) against 10.10.10.222 

Retrying OS detection (try #4) against 10.10.10.222 

Retrying OS detection (try #5) against 10.10.10.222 

Initiating Traceroute at 12:16 

Completed Traceroute at 12:16, 0.28s elapsed 

NSE: Script scanning 10.10.10.222. 

Initiating NSE at 12:16 

Completed NSE at 12:16, 8.39s elapsed 

Initiating NSE at 12:16 

Completed NSE at 12:16, 1.23s elapsed 

Initiating NSE at 12:16 

Completed NSE at 12:16, 0.00s elapsed 

Nmap scan report for 10.10.10.222 

Host is up (0.27s latency). 

Not shown: 998 closed ports 

PORT   STATE SERVICE VERSION 

22/tcp open  ssh     OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0) 

| ssh-hostkey:  

|   2048 9c:40:fa:85:9b:01:ac:ac:0e:bc:0c:19:51:8a:ee:27 (RSA) 

|   256 5a:0c:c0:3b:9b:76:55:2e:6e:c4:f4:b9:5d:76:17:09 (ECDSA) 

|_  256 b7:9d:f7:48:9d:a2:f2:76:30:fd:42:d3:35:3a:80:8c (ED25519) 

80/tcp open  http    nginx 1.14.2 

| http-methods:  

|_  Supported Methods: GET HEAD 

|_http-server-header: nginx/1.14.2 

|_http-title: Welcome 

No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ). 

TCP/IP fingerprint: 

OS:SCAN(V=7.91%E=4%D=5/18%OT=22%CT=1%CU=35593%PV=Y%DS=2%DC=T%G=Y%TM=60A362B 

OS:3%P=x86_64-pc-linux-gnu)SEQ(SP=106%GCD=1%ISR=10D%TI=Z%CI=Z%II=I%TS=A)OPS 

OS:(O1=M54DST11NW7%O2=M54DST11NW7%O3=M54DNNT11NW7%O4=M54DST11NW7%O5=M54DST1 

OS:1NW7%O6=M54DST11)WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)ECN 

OS:(R=Y%DF=Y%T=40%W=FAF0%O=M54DNNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=A 

OS:S%RD=0%Q=)T2(R=N)T3(R=N)T4(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T5(R 

OS:=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F 

OS:=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N% 

OS:T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=40%CD 

OS:=S) 

  

Uptime guess: 9.080 days (since Sun May  9 10:21:30 2021) 

Network Distance: 2 hops 

TCP Sequence Prediction: Difficulty=262 (Good luck!) 

IP ID Sequence Generation: All zeros 

Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel 

  

TRACEROUTE (using port 23/tcp) 

HOP RTT       ADDRESS 

1   274.85 ms 10.10.14.1 

2   274.97 ms 10.10.10.222 

  

NSE: Script Post-scanning. 

Initiating NSE at 12:16 

Completed NSE at 12:16, 0.00s elapsed 

Initiating NSE at 12:16 

Completed NSE at 12:16, 0.00s elapsed 

Initiating NSE at 12:16 

Completed NSE at 12:16, 0.00s elapsed 

Read data files from: /usr/bin/../share/nmap 

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ . 

Nmap done: 1 IP address (1 host up) scanned in 38.60 seconds 

           Raw packets sent: 1125 (53.526KB) | Rcvd: 1082 (46.758KB) 

 

 

 

**Enumeration:** 

 Using Osticket and Mattermost  (via email)

 ssh maildeliverer@10.10.10.222 

 

**Privilege Escalation:** 

- Find the mattermost sql settings file(config file) 

- Note the userid and password and login using(mysql) -mysql –u mmuser –pCrack_The_MM_Admin 

- Select the DB 

- Select the User's password form the table 

- Copy the root password 

- Hashid rootpassword (bcrypt 3200) 

- Use hashcat to crack the password – hashcat –a 0 –m hash.txt -r /usr/share/hashcat/rules/basic64.rules --show 

- To access as root user : su – root 

- Get the root flag 

 

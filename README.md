# Мое домашнее задание № 3

## Задание № 3.1

```bash
root@roman-VB:/home/roman/repo/my-third-repo# ps aux --sort=-%cpu 1> out.txt 2> /dev/null
```
[Результат](out.txt)

```bash
root@roman-VB:/home/roman/repo/my-third-repo# ps aux ------- 2> err.txt
```
[Результат с ошибкой](err.txt)

## Задание № 3.2
```bash
root@roman-VB:/home/roman/repo/my-third-repo# ps aux | head -11 | tee proc.txt
```
[Топ 10 процессов](proc.txt)

## Задание № 3.3
### Сканирование с определением сервисов, ОС и пр.
```bash
root@roman-VB:/home/roman/repo/my-third-repo# nmap -sS -sV -O -p 1-100 scanme.nmap.org
Starting Nmap 7.98 ( https://nmap.org ) at 2026-11-15 23:50 +0300
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.13s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 98 filtered tcp ports (no-response)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 6.6.1p1 Ubuntu 2ubuntu2.13 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    Apache httpd 2.4.7 ((Ubuntu))
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: VoIP adapter|bridge|general purpose
Running (JUST GUESSING): AT&T embedded (92%), Oracle Virtualbox (92%), Slirp (92%), QEMU (89%)
OS CPE: cpe:/o:oracle:virtualbox cpe:/a:danny_gasparovski:slirp cpe:/a:qemu:qemu
Aggressive OS guesses: AT&T BGW210 voice gateway (92%), Oracle Virtualbox Slirp NAT bridge (92%), QEMU user mode network gateway (89%)
No exact OS matches for host (test conditions non-ideal).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 28.03 seconds
```
### Сканирование портов в grepable формате
```bash
root@roman-VB:/home/roman/repo/my-third-repo# nmap -p 1-100 -oG -  scanme.nmap.org
\# Nmap 7.98 scan initiated Sun Nov 15 23:53:41 2026 as: nmap -p 1-100 -oG - scanme.nmap.org
Host: 45.33.32.156 (scanme.nmap.org)	Status: Up
Host: 45.33.32.156 (scanme.nmap.org)	Ports: 8/closed/tcp/////, 21/closed/tcp//ftp///, 22/open/tcp//ssh///, 23/closed/tcp//telnet///, 25/closed/tcp//smtp///, 27/closed/tcp//nsw-fe///, 35/closed/tcp//priv-print///, 40/closed/tcp/////, 53/closed/tcp//domain///, 66/closed/tcp//sqlnet///, 68/closed/tcp//dhcpc///, 79/closed/tcp//finger///, 80/open/tcp//http///, 96/closed/tcp//dixie///	Ignored State: filtered (86)
\# Nmap done at Sun Nov 15 23:53:46 2026 -- 1 IP address (1 host up) scanned in 5.62 seconds
```

## Makarov-Mark-II
This container file was created based on the concept of a disposable pen test container. Stand-alone and basic tools are available. Imagine, if you want to do a little ethical hack on a university or junior college shared computer, or if you want to do ethical hacking or OSINT again on a computer that you don't own, the general method is to use a dedicated OS. Live booting from USB (eg Kali or Parrot) is a common practice, but most educational institutions and rental computers have BISO access restrictions. You can use the Docker engine there. Docker is almost certainly included in the laboratories and school buildings of educational institutions that constantly require advanced equipment and technology resources, and the `docker run -it --rm` command uses the pen test tool with almost no trace. can. So you don't have to install everything from scratch. 

### INSTALL
fast install
```shell
$ docker run -it --rm ghcr.io/hexhelix-xx/makarov:latest
```
manually install
```shell
$ cd ghcr.io/hexhelix-xx/makarov:latest
$ docker build -t makarov:latest .
$ docker run -it --rm  makarov:latest 
▽  / >>
```

### Tools
###### Pentest
```
aircrack-ng     : Key cracker for the 802.11 WEP and WPA-PSK protocols
crackmapexec    : A swiss army knife for pentesting Windows/Active Directory environments.
hydra           : Very fast network logon cracker which support many different services
john            : John the Ripper password cracker
metasploit      : Advanced open-source platform for developing, testing, and using exploit code
nmap            : Utility for network discovery and security auditing
sqlmap          : Automatic SQL injection and database takeover tool
responder       : A LLMNR and NBT-NS poisoner, with built-in HTTP/SMB/MSSQL/FTP/LDAP rogue authentication server supporting NTLMv1/NTLMv2/LMv2 (multirelay version).
wireshark-cli   : Network traffic and protocol analyzer/sniffer - CLI tools and data files
```
###### OSINT
```
buster          : Find emails of a person and return info associated with them.
cardpwn         : OSINT Tool to find Breached Credit Cards Information.
instagramosint  : An Instagram Open Source Intelligence Tool.
osi.ig          : Instagram OSINT Tool gets a range of information from an Instagram account.
twint           : An advanced Twitter scraping & OSINT tool written in Python that doesn't use Twitter's API, allowing you to scrape a user's followers, following, Tweets and more while evading most API limitations.
phoneinfoga     : Information gathering & OSINT framework for phone numbers.
```
###### Defensive
```
tor         : Anonymizing overlay network.
proxychains : A hook preloader that allows to redirect TCP traffic of existing dynamically linked programs through one or more SOCKS or HTTP proxies
tor-router  : A tool that allow you to make TOR your default gateway and send all internet connections under TOR (as transparent proxy) for increase privacy/anonymity without extra unnecessary code.
nipe        : A script to make Tor Network your default gateway.
torsocks    : Wrapper to safely torify applications
```
### Note: Tor
Tor sets it to use the bridge by default, but it's not up to date. This is an urgent issue and we are currently looking for an efficient bridge replacement method.
Regarding use, never use systemctl for security reasons. Again, we have not tested systemctl at all. Be sure to use the `tor &` command when using it. 

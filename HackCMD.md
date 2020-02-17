Comandi Hack:
=============

LAWS:
-----

<https://www.dlapiperdataprotection.com/>

Java JRE:
---------

### Install:

>	apt-get install default-jre

Test your fingerprint:
----------------------

<https://panopticlick.eff.org/>

### Stop Fingerprinting:

Brobser|Plugin
-------|------
Firefox|Firegloves
Chrome|Stop Fireprinting

No Full Screen!

Secur all on HTTPS:
-------------------

Install plugging HTTPS EveryWhere

Ghostery - <https://www.ghostery.com/>

uMatrix - <https://chrome.google.com/webstore/detail/umatrix/ogfcmafjalglgifnmanfmnieipoejdcf/>

Change MAC:
-----------

>   ip link set dev eth0 down

>   ip link set dev eth0 address 00:00:00:00:00:01

>   ip link set dev eth0 up

>   service network-manager restart

### Generare un MAC valido:

>   apt-get install macchanger

### Esecuzione a mano:

>   ifconfig eth0 down macchanger -r eth0 ifconfig eth0 up

Hostname:
---------

### Visualizza informazioni:

>   hostname hostnamectl

### Cambia in modo temporaneo

>   hostaname anonimo

### Cambiamento permanente

>   sysctl kernel.hostname=amnesia

DNS:
----

### Lista dei principali DNS da utilizzare:

>   OpenDNS

>   OpenNIC

### Monificare in Linux:

>   nano /etc/resolv.conf

>   \>COMMENT\> nameserver 192.168.1.1

>   \>ADD\> nameserver 8.8.8.8

>   \>ADD\> nameserver 8.8.4.4

service network-manager restart

### Visualizzazione:

>   nmcli device show eth0 \| grep IP4.DNS

### Pulizia Cache DNS:

>   apt-get install nscd

>   /etc/init.d/nscd restart

Indirizzo IP:
-------------

### Visualizza ip pubblico sul terminal:

>   wget <https://ipinfo.io/ip> -q0 -

Proxy:
------

### Lista web Proxy:

>   <https://whoer.net/>

>   <https://hide.me/>

>   <https://proxysite.com/>

>   <https://vpnbook.com/>

>   <https://hidemyass.com/>

>   <https://kproxy.com/>

>   <https://hidester.com/>

>   <https://filterbypass.me/>

#### Lista completa:

>   <http://www.proxy4free.com/>

### Modifica il Proxy (blando):

>   nano /etc/enviroment

\>ADD\>http_proxy="61.5.207.102:80" // HTTP

\>ADD\>https_proxy="61.5.207.102:80" // HTTPS

\>ADD\>ftp_proxy="61.5.207.102:80" // FTP

\>ADD\>no_proxy="61.5.207.102:80" // SOCKS4/5

ProxyChains-NG:
---------------

### Installazione:

>   apt-get install proxychains

### Utilizzo:

proxychains wget <http://ipinfo.io/ip> -q0 -

### Configurations:

>   mkdir \$HOME/.proxychains

>   nano \$HOME/.proxychains/proxychains.conf

\>ADD\>strict_chain

\>ADD\>proxy_dns

\>ADD\>[ProxyList]

\>ADD\>http 177.73.177.25 8080

VPN:
----

OPENVPN

### Lista VPN:

| Name                    | Nation   | Dates                                       | Log IP | DMCA | Type              | P2P | BTC |
|-------------------------|----------|---------------------------------------------|--------|------|-------------------|-----|-----|
| BTGuard                 | Canada   | Dati personali                              | [ ]    | [ ]  | PPTP OpenVPN      | [x] | [x] |
| MULLVAD                 | Svezia   | \-                                          | [ ]    | [ ]  | PPTP OpenVPN      | [x] | [x] |
| NORDVPN                 | Panama   | mail, username, password, dati fatturazione | [ ]    | [ ]  | PPTP OpenVPN L2TP | [x] | [x] |
| PRQ                     | Svizia   | mail                                        | [ ]    | [ ]  | OpenVPN           | [x] | [x] |
| Private Internet Access | USA      | mail, dati fatturazione, cookie             | [ ]    | [x]  | PPTP OpenVPN L2TP | [x] | [x] |
| SHADEYOU                | Olanda   | Dati personali                              | [ ]    | [x]  | PPTP OpenVPN L2TP | [x] | [x] |
| OCTANEVPN               | USA      | Dati personali                              | [ ]    | [x]  | PPTP OpenVPN      | [x] | [x] |
| SLICKVPN                | USA      | Dati personali                              | [ ]    | [x]  | OpenVPN           | [x] | [x] |
| SECUREVPN.TO            | Multiple | Dati personali                              | [ ]    | [x]  | OpenVPN           | [x] | [x] |

### Install:

>   apt-get install openvpn

>   cd /etc/openvpn

>   wget <https://nordvpn.com/api/files/zip/>

>   unzip zip

>   ls -al

### Use:

>   openvpn it3.nordvpn.com.udp1194.ovpn

#### Testing:

>   wget <http://ipinfo.io/ip/> -q0 -

### Testing VPN:

#### Torrent:

>   <http://ipmagnet.services.cbcdn.com/>

Clear/Deep/Dark Web on Tor:
--------------------

Use di Tor Porject

### Install:

#### From Windows:

Go to <https://www.torproject.org/>

#### From Linux:

<https://2019.www.torproject.org/docs/debian.html.en>

>   nano /etc/apt/sources.list

\>ADD\>\# TOR repository

\>ADD\>deb <http://deb.torproject.org/torproject.org> jessie main

\>ADD\>deb-src <http://deb.torproject.org/torproject.org> jessie main

>   apt-get install tor

>   tor

##### Check Status:

>   service tor status

>   netstat -tanp \| grep tor

### Setup Bridges:

Go to <https://bridges.torproject.org/>

Click on 2\# step

paste the Bridges on Tor Network Settings\> Tor is censored in my country\>

Request a bridge from torproject.org

### Change ProxyChains-NG config to go on Tor net:

>   nano \$HOME/.proxychains/proxychains.conf

\>ADD\>dinamic_chain

\>ADD\>proxy_dns

\>ADD\>[ProxyList]

\>ADD\>socks4 127.0.0.1 9050

### Check IP:

>   proxychains wget <http://ipinfo.io/ip/> -q0 -

I2P:
----

<https://geti2p.net/en/>

### Requirement:

Java JRE

I2P software

### Add Repository:

<http://deb.i2p2.de/>

>   nano /etc/apt/sources.list

\>ADD\>\# TOR repository

\>ADD\>deb https://deb.i2p2.de/ jessie main

\>ADD\>deb deb-src https://deb.i2p2.de/ jessie main

### Install:

>	apt-get install apt-transport-https

>	apt-get update \&\& apt-get upgrade

>	apt-get install i2p-keyring \&\& apt-get update

>	apt-get install i2p i2p-keyring

### Start:

>	i2prouter start

### Console:

<http://127.0.0.1:7657/>

### Set the Porxy:

HTTP: 127.0.0.1 4444

HTTPS: 127.0.0.1 4445

### Create your one Server:

<http://127.0.0.1:7658/>

### Torrent Server:

<http://127.0.0.1:7657/i2psnark/>

#### Dedicated Trackers:

<http://diftracker.i2p/>

<http://tracker2.postman.i2p/>

### Best Project for I2P:

<http://echelon.i2p/>

#### Emule:

<http://echelon.i2p/imule/>

Alternative:

<http://echelon.i2p/nachtblitz/>

#### Susimail:

<http://127.0.0.1:7657/susimail/susimail/>

<http://hq.postman.i2p/>

### Listo of the know sites of I2P:

<http://identiguy.i2p/>

FreeNET:
--------

<https://freenetproject.org/>

### Install:

>	wget '<https://freenetproject.org/assets/jnlp/freenet_installer.jar>' -0 installer.jar

>	java -jar installer.jar

Checksum, Hash:
---------------

### Make a checksum:

>	shasum [ -a \<value of algorithm\> \] \<file_name.txt\>

### GPG:

#### Create your key gpg:

>	gpg -gen-key

#### Listo of Key:

>	gpg -k

#### Export Key:

>	gpg --export -a \<id\> | mail -s "My Pubblic Key" user@mail.com

#### Revoke Key:

gpg --output revoke.key --gen-revoke \<id\>

#### Encrypt a File:

>	pgp --output \<output_file.gpg\> --encrypt --recipient \<id_reciver\> \<file.txt\>

#### Decrypt a File:

>	gpg --output \<output.txt\> --decrypt \<input_file.gpg\>

#### Send File by mail:

>	pgp --armor --encrypt --recipient \<mail_reciver@mail.com\> \<file.txt\>

#### Sign a File:

>	gpg -s \<file.txt\>

### Stenography:

<http://www.spammimic.com/>

Or more clearly:

>	gpg --clearsign \<file.txt\>

#### Verify File:

>	gpg --verify \<file_hash.txt.asc\>

Secure Mail:
------------

### Install:

>	apt-get install icedove

>	apt-get install enigmail

Backup:
-------

### Install:

>	apt-get instakk rsync

### Use:

>	rsync -a --progress $HOME\/rsync\/folder_to_copy $HOME\/rsync_backup

Compressed transport:

>	rsync -az --progress $HOME\/rsync\/folder_to_copy $HOME\/rsync_backup

Remote:

>	rsync -az --progress root\@your_domain.com\:\/home\/rsync\/folder_to_copy $HOME\/rsync_backup

With a different port:

>	rsync -az --progress --rsh\=\"ssh -p 22\" root\@your_domain.com\:\/home\/rsync\/folder_to_copy $HOME\/rsync_backup

DDos:
-----

There are 3 type of DDoS Attack:

> Application-layer DDOS attack

> Protocol DOS attack

> Volume-based DDOS attack

### Application layer

 DDOS attack: Application-layer DDOS attacks are attacks that target Windows,
               Apache, OpenBSD, or other software vulnerabilities 
               to perform the attack and crash the server.

### Protocol DDOS attack

DDOS attack : A protocol DDOS attacks is a DOS attack on the protocol level. 
               This category includes Synflood, Ping of Death, and more.

### Volume-based

 DDOS attack: This type of attack includes ICMP floods,
               UDP floods, and other kind of floods performed via spoofed packets.

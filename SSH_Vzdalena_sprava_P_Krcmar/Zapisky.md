SSH
===
- Univerzální
- Umí přenášet soubory:
	- SFTP
		- Komplexní jako FTP
		- Mladší než FTP
	- SCP
		- Velmi jednoduché
		- jenom kopíruje po SSH
		- pro listování souborů je potřeba normální SSH session
			- MC používá fish: kombinace SSH session pro listování a SCP pro přenos
	- FileZilla, WinSCP, ....
- Bezpečné
- Možnosti přihlášení:
	- Heslo
		- Bruteforce útoky
	- Klíč
		- Lze jej mít uložený na smartcard nebo na serveru
		- `ssh-copy-id` nebo ruční překopírování
		- Při vypnutém přihlašování heslem nehrozí Bruteforce útok
		- `ssh-agent` - drží klíče v paměti, aby nebylo potřeba neustále zadávat heslo
			- `-c` - ptá se při použití klíče
			- + další parametry
- Klienti: PuTTY (Win), ConnectBot (Android), JuiceSSH (Android)

Mosh
----
- UDP míto TCP
- stabilnější - neřeší souvislost spojení
	- Přežije uspání PC, změnu IP, ....
- Lokální echo, neposílá se každá klávesa zpět ze serveru
- Vyžaduje mosh server, který ale ani nepotřebuje root práva

Tmux, screen
------------
- Multiplexer terminálu
- "Terminálová okna" - společná virtuální plochy všech sessions

Sériová linka
=============
- VPSfree má sériovou linku i na VPS - vyvedenou do webového rozhraní
- Záloha když nefnuguje SSH


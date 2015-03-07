Docker
======
Kontejnery
----------
- Jsou jednoduché, nenáročné (a úplně super (možná))
- Zjednidušení přenesení SW - není potřeba řešit systémové požadavky (nainstalované balíky) cílového systému (protože se do dá do kontejneru)
- Kontejnery sdílí knihovny a aplikace
- Kontejner je sada funkcí pro izolaci procesů
- Kontejner se tváří jako virtuální stroj, ovšem procesy kontejneru jsou vidět i na hostitelském systému
- Nejsou úplně bezpečné - Kontejnery nejsou bezpečnosní záležitost, nemají dokonalý sandbox
	- lze použít např. SELinux

Cgroups
-------
- používají se k omezování prostředků procesu

Docker
------
- Snaží se oddělit programátora a operátora
	- *Operátor* se stará o kontejner a ne o to, co tam běží
	- *Programátor* se stará o program a ne o to, na čem běží
- Docker images mají rodiče - vrství se na sebe
	- Různé images můžou mít stejného rodiče - staví nad stejným základem
	- Base image nemá rodiče
- Kontejner je víceméně běžící image
- Docker hub - úložiště vrstev (images)
	- Docker pull <balíček> stáhne balíček včetně jeho rodičů (až po base image)
- Commit uloží kontejner jako image s odkazem na jeho rodiče
- Dockerfile obsahuje: Rodiče, maintainera, příkazy (dockerovské), co se má stát, co se má defaultně spustit
- docker.com

Random
------
- Kernel Namespaces = omezení, co všechno daný proces nevidí


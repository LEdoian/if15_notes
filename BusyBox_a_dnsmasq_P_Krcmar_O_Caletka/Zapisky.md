BusyBox
=======
- Obsahuje v sobě strašně moc utilit (kolem 200: Síťové fce, práce se soubory, .... )
- `busybox <utilita>` spustí danou utilitu
- Utility jsou zjednodušené, nemají plnou funkcionalitu (wget bez HTTPS)
- Určený pro zařízení, která mají málo paměti (router, jednoduchý záchranný shell debianu)
- Pro jednoduchý linuxový systém stačí BusyBox (obsahuje init) a kernel
- Nemá žádné šifrování - šifrovací knihovny jsou velké a děravé

Dnsmasq
=======
- Řeší síťové funkce
- Umí DNS forwarder (+ cacher, DNSSEC (napůl)), DHCP, DHCPv6, TFTP, PXE, ....
- Android tethering, routery, DNS cache v Ubuntu, ....
- Výhodou je velká provázanost služeb

DNS
---
- Původně zamýšlen jako DNS forwarder
- Vyrovná se s výpadkem některého DNS serveru (narozdíl od glibc)
- Podporuje neveřejné domény
- Umí si poradit s nenastavenými hodinami u DNSSECu
- Defaultně nekontroluje nepodepsané domény u DNSSECu -> DNSSEC je víceméně k ničemu
- `unbound` je lepší a podobně malý, ale obtížněji konfigurovatelný

DHCP
----
- IPv4 i IPv6
- umí identifikovat IPv6 klienty podle MAC adresy
- PXE server
- provázaný s DNS

TFTP
----
- určen pro podporu PXE bootu

IPv6
----
- Registrace i SLAAC IPv6 do DNS

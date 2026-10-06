# sysadmin-homelab
Projekt homelab do nauki na Junior SysAdmin: Linux, Docker, Active Directory
## Postęp

- [x] Homelab na Mac mini: UTM + Ubuntu Server VM
- [x] Docker + Pi-hole (domowy filtr DNS)
- [x] Windows Server VM w VirtualBox
- [x] Active Directory Domain Services
- [x] Domena gameforge.local
- [x] Jednostki organizacyjne + użytkownicy
- [x] Reguła Group Policy
- [x] Podstawowe zadania helpdesk w AD
- [x] DNS w domenie
- [x] DHCP
- [ ] Firewall (ufw) na Ubuntu VM
- [ ] Klient w domenie (Windows 10/11)
- [ ] Monitoring (Zabbix/Grafana)

### [27.09.2026] — start projektu
Zacząłem od Pi-hole na Docker. Zrozumiałem, jak docker-compose łączy porty i volumes. Dalej — Windows Server i Active Directory.
### [29.09.2026] — Windows Server, Active Directory, GPO
Zainstalowałem Windows Server 2019 w VirtualBox.

Zainstalowałem rolę Active Directory Domain Services i podniosłem domenę gameforge.local.
  Stworzyłem strukturę organizacyjną: 3 jednostki organizacyjne (IT, Design, QA) z jednym 
użytkownikiem w każdej.
  Skonfigurowałem pierwszą regułę Group Policy (Design-NoWallpaperChange) blokującą zmianę 
tapety wyłącznie dla działu Design

### [05.10.2026] — Podstawowe zadania helpdesk w AD
Przećwiczyłem reset hasła z wymuszeniem zmiany przy logowaniu, odblokowanie i wyłączenie
konta (zamiast usuwania, żeby nie stracić danych) oraz przeniesienie użytkownika między OU.

### [05.10.2026] — DNS w domenie
Sprawdziłem strefę gameforge.local, dodałem rekord A i zweryfikowałem go poleceniem
nslookup. Po usunięciu rekordu nslookup zwrócił błąd.

### [05.10.2026] — DHCP
Zainstalowałem rolę DHCP Server, autoryzowałem ją w AD i utworzyłem zakres
192.168.50.100–150. Lista dzierżaw jest pusta, bo nie ma jeszcze klientów.

### 06.10.2026: Firewall (ufw), teoria
Poznałem zasady działania firewalla: jak porty, usługi i firewall współpracują ze sobą
(terminal → usługa → firewall → sieć) oraz po co stosuje się politykę „deny incoming”
z wyjątkami dla potrzebnych portów (SSH, DNS, panel Pi-hole).

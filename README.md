# sysadmin-homelab
Projekt homelab do nauki na Junior SysAdmin: Linux, Docker, Active Directory
## Postęp

- [x] Homelab na Mac mini — UTM + Ubuntu Server VM
- [x] Docker + Pi-hole (domowy filtr DNS)
- [x] Windows Server VM w VirtualBox
- [x] Active Directory Domain Services
- [x] Domena gameforge.local
- [x] Jednostki organizacyjne + użytkownicy
- [x] Reguła Group Policy
- [ ] Firewall (ufw) na Ubuntu VM
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


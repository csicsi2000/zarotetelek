### Hálózati architektúrák és protokollok

#### Csomagkapcsolt hálózatok működése
A csomagkapcsolt hálózatokban az adatokat kisebb csomagokra bontják, és ezek a csomagok függetlenül haladhatnak át a hálózaton. Minden csomag tartalmazza a címzési információkat, amelyek lehetővé teszik a célállomásra való szállítást.

- **Előnyök**:
  - Hatékony sávszélesség-kihasználás
  - Hibajavítás és adatvesztés csökkentése
  - Skálázhatóság
- **Működés**:
  - Csomagok különböző útvonalakon haladhatnak
  - Csomagok összerakása a célállomáson

#### OSI és TCP/IP modell összehasonlítása

| OSI modell | TCP/IP modell |
| --- | --- |
| 7 réteg (Alkalmazási, Megjelenítési, Viszonylati, Szállítási, Hálózati, Adatkapcsolati, Fizikai) | 4 réteg (Alkalmazási, Szállítási, Internet, Hálózati hozzáférés) |
| Elméleti modell, amely segít megérteni és tervezni a hálózatokat | Gyakorlati modell, amely ténylegesen alkalmazásban van |
| Nagyobb részletezettség | Egyszerűbb és gyakorlatiasabb |

#### Forgalomirányítási és IP címzési alapok

- **Forgalomirányítás (Routing)**:
  - Az adatok útvonalának meghatározása a hálózaton keresztül
  - Statikus és dinamikus forgalomirányítási protokollok (pl. RIP, OSPF, BGP)
  
- **IP címzés**:
  - IPv4: 32 bites címek (pl. 192.168.1.1)
  - IPv6: 128 bites címek (pl. 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
  - Privát és nyilvános IP címek
  - Subnetting és CIDR (Classless Inter-Domain Routing)

#### Kapcsolódó protokollok

- **TCP (Transmission Control Protocol)**:
  - Kapcsolatorientált protokoll
  - Megbízható adatátvitel (hibajavítás, adatvesztés kezelés)
  - Szegmensekre bontás és újra összerakás

- **UDP (User Datagram Protocol)**:
  - Kapcsolat nélküli protokoll
  - Gyors, de kevésbé megbízható (nincs hibajavítás)
  - Alkalmas valós idejű alkalmazásokhoz (pl. videostreaming, VoIP)

- **ICMP (Internet Control Message Protocol)**:
  - Hálózati diagnosztikai és hibajelentési protokoll
  - Ping és traceroute parancsok alapja

- **DNS (Domain Name System)**:
  - Domain nevek és IP címek közötti fordítás
  - Hierarchikus és elosztott adatbázis rendszer

---

Ezek az alapok segítenek megérteni a hálózati architektúrák és protokollok működését, valamint a csomagkapcsolt hálózatok alapelveit és a különböző protokollok szerepét a hálózati kommunikációban.
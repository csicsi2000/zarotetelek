# Szolgáltatás orientált programozás

## Az RPC architektúrája, működési elve, jellemzői

- **Architektúra**: Az RPC (Remote Procedure Call) egy olyan architektúra, amely lehetővé teszi a távoli számítógépek közötti kommunikációt úgy, mintha lokálisan hívnánk meg eljárásokat.
- **Működési elv**: Az RPC-n keresztül a kliens számára úgy tűnik, mintha a távoli szerveren futó eljárásokat helyben hívná meg.
- **Jellemzők**: Egyszerűség, gyorsaság, a fejlesztők számára ismerős programozási modell.

## A Google RPC működési elve, jellemzői

- **Működési elv**: A Google RPC egy nyílt forráskódú RPC rendszer, amelyet a Google fejlesztett ki, és a Protobuf (Protocol Buffers) nyelvet használja az üzenetek átvitelére.
- **Jellemzők**: Hatékonyság, skálázhatóság, támogatás több különböző nyelvhez és platformhoz.

## A protocol buffers szerepe a gRPC-ben

- A Protocol Buffers egy platformfüggetlen interfészleíró nyelv, amelyet strukturált adatok leírására használnak.
- A gRPC-ben a Protocol Buffers segítségével írják le az üzenetek struktúráját és az RPC szolgáltatás interfészeit.

## A WEB, egyrétegű, kliens-szerver modell, többrétegű alkalmazások, vastag és vékony kliensek, elosztott rendszerek jellemzői

- **WEB, egyrétegű, kliens-szerver modell**: A WEB egyrétegű kliens-szerver modellje azt jelenti, hogy a kliensek HTTP kéréseket küldenek a szervereknek, amelyek válaszolnak rájuk.
- **Többrétegű alkalmazások**: Az alkalmazást rétegekre osztják fel, például prezentációs, üzleti logika és adatelérési rétegekre.
- **Vastag és vékony kliensek**: A vastag kliensek sok üzleti logikát tartalmaznak, míg a vékony kliensek inkább csak a felhasználói felületet kezelik.
- **Elosztott rendszerek jellemzői**: Skálázhatóság, rugalmasság, fejlett hibatűrés.

## A REST tulajdonságai

- **Reprezentáció által vezérelt**: A kliens kéréseket küld a szervernek, és a válasz a kliens által kívánt reprezentációban érkezik.
- **Állapot nélküliség**: Minden kérés tartalmazza az összes információt, amelyre a szervernek szüksége van a válaszhoz.
- **Cache-elhetőség**: A válaszok cache-elhetők, hogy csökkentsék a hálózati forgalmat és növeljék a teljesítményt.

## A web service jellemzői

- **Platformfüggetlenség**: A web service-eket különböző platformokon lehet kialakítani és használni.
- **Interoperabilitás**: Különböző technológiák és nyelvek közötti kommunikációt tesz lehetővé.
- **Szabványokon alapulás**: A web service-eket általában meghatározott szabványok és protokollok szerint tervezik és implementálják.

## A WCF architektúrája, az ASMX és a WCF közötti eltérések

- **WCF architektúra**: A WCF (Windows Communication Foundation) egy Microsoft által fejlesztett keretrendszer, amely lehetővé teszi a különböző alkalmazások közötti kommunikációt. Az architektúra többféle kommunikációs protokollt és formátumot támogat.
- **Az ASMX és a WCF közötti eltérések:

- **ASMX (ASP.NET Web Services)**:
  - Kizárólag SOAP alapú szolgáltatásokat támogat.
  - Csak HTTP protokollt használ.
  - Korlátozottabb konfigurációs és biztonsági lehetőségekkel rendelkezik.
  - Kisebb rugalmasságot biztosít a szolgáltatások tervezése és implementálása terén.

- **WCF (Windows Communication Foundation)**:
  - Támogatja a többféle kommunikációs protokollt és formátumot, például SOAP, REST, TCP, HTTP stb.
  - Rugalmasabb konfigurációs és biztonsági lehetőségeket kínál.
  - Teljesítményben hatékonyabb és skálázhatóbb.
  - Összetettebb fejlesztési modellt kínál, de nagyobb funkcionalitással és flexibilitással rendelkezik.

A WCF tehát általánosabb, szélesebb körű funkcionalitást és integrációs lehetőségeket biztosít, míg az ASMX egyszerűbb és könnyebben kezelhető SOAP alapú szolgáltatásokhoz. A választás általában az alkalmazás igényeitől és a fejlesztési környezettől függ.
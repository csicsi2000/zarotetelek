# Szolgáltatás orientált programozás

## Az RPC architektúrája, működési elve, jellemzői

- **Architektúra**: Az RPC (Remote Procedure Call) olyan kommunikációs modell, amely lehetővé teszi, hogy a kliens számára úgy tűnjön, mintha lokális eljárásokat hívnának meg, miközben valójában a hívások távoli szervereken futnak.
- **Működési elv**: A kliens kérésére a távoli szerver végrehajt egy eljárást, és a választ visszaküldi a kliensnek.
- **Jellemzők**: Egyszerű használat, szinkron és aszinkron működés, platformfüggetlenség.

## A Google RPC működési elve, jellemzői

- **Működési elv**: A Google RPC egy elosztott RPC rendszer, amely lehetővé teszi a távoli szolgáltatások egyszerű hívását. Az üzeneteket Protobuf (Protocol Buffers) segítségével serializálja és deserializálja.
- **Jellemzők**: Hatékonyság, skálázhatóság, egyszerűség, támogatás több különböző nyelvhez és platformhoz.

## A protocol buffers szerepe a gRPC-ben

- A Protocol Buffers a Google által fejlesztett nyelvfüggetlen interfészleíró nyelv. A gRPC-ben a Protocol Buffers segítségével írják le a szolgáltatások üzeneteit és interfészeit.

## A WEB, egyrétegű, kliens-szerver modell, többrétegű alkalmazások, vastag és vékony kliensek, elosztott rendszerek jellemzői

- **WEB, egyrétegű, kliens-szerver modell**: A kliensek HTTP kéréseket küldenek a szervereknek, és a szerverek válaszolnak ezekre a kérésekre.
- **Többrétegű alkalmazások**: Az alkalmazások rétegekre vannak osztva, például prezentációs, üzleti logika és adatelérési rétegekre.
- **Vastag és vékony kliensek**: A vastag kliensek sok üzleti logikát tartalmaznak, míg a vékony kliensek inkább csak a felhasználói felületet kezelik.
- **Elosztott rendszerek jellemzői**: A rendszerek több fizikai vagy virtuális gépen futó komponensekből állnak, amelyek egymással kommunikálnak hálózaton keresztül.

## A REST tulajdonságai

- **Reprezentáció által vezérelt**: A kliensek kéréseket küldenek a szervernek, és a szerver válaszokat ad, amelyek tartalmazzák a kliens által kívánt reprezentációt.
- **Állapot nélküliség**: Minden kérés tartalmazza az összes információt, amelyre a szervernek szüksége van a válaszhoz.
- **Cache-elhetőség**: A válaszok cache-elhetők, hogy csökkentsék a hálózati forgalmat és növeljék a teljesítményt.

## A web service jellemzői

- **Platformfüggetlenség**: A web service-eket különböző platformokon lehet kialakítani és használni.
- **Interoperabilitás**: Különböző technológiák és nyelvek közötti kommunikációt tesz lehetővé.
- **Szabványokon alapulás**: A web service-eket általában meghatározott szabványok és protokollok szerint tervezik és implementálják.

## A WCF architektúrája, az ASMX és a WCF közötti eltérések

- **WCF (Windows Communication Foundation)**:
  - Rugalmasabb, több protokollt és formátumot támogat.
  - Kifinomultabb konfigurációs és biztonsági lehetőségeket kínál.
  - Nagyobb teljesítményt és skálázhatóságot biztosít.
- **ASMX (ASP.NET Web Services)**:
  - Kizárólag SOAP alapú szolgáltatásokat támogat.
  - Korlátozottabb konfigurációs és biztonsági lehetőségekkel rendelkezik.
  - Egyszerűbb és könnyebben kezelhető SOAP alapú szolgáltatásokhoz.

A választás az alkalmazás igényeitől és a fejlesztési környezettől függ. A WCF általánosabb és bővebb körű funkcionalitást és integrációs lehetőségeket kínál, míg az ASMX egyszerűbb és könnyebben kezelhető SOAP alapú szolgáltatásokhoz.
# Komunikácia v ethernete
- správy zasialané ethernetom môžu byť:
	- **unicast** - pre jedneho príjemcu
	- **broadcast** - pre všetky stanice v LAN
	- **multicast** - pre skupinu staníc (musia byť v multicastovej skupine)
___
# Ethernetový rámec

protokol - IEEE 802.3:

| preamble       | start of frame delimiter    | destination address            | source address                       | length/type                 | 802.2 header and data | frame check sequence (FCS) |
| -------------- | --------------------------- | ------------------------------ | ------------------------------------ | --------------------------- | --------------------- | -------------------------- |
| začiatok rámca | na synchronizáciu zariadení | cieľová MAC adressa zariadenia | MAC adressa vysielajúceho zariadenia | typ a dĺžka použitého rámca | zapuzdrený paket      | kontrolný súčet            |
| 7B             | 1B                          | 6B                             | 6B                                   | 2B                          | 46B - 1500B           | 4B                         |
___
# MAC adresa

- fyzická adresa
- mac adresa je 48 bitové číslo
- zapísané v hexadecimálnom tvare
- 00-05-9A-3C-78-00, 00:05:9A:3C:78:00 alebo 0005.9A3C.7800
- ľavá polovica je prideľená od IEEE jednotlivým výrobcom OUI
- druhú polovicu určujú výrobcovia tak, aby v rámci ich rozsahu bola jedinečná

| Broadcast | Local | OUI Number | "Vendor Number"<br>Vendor Assignment |
| --------- | ----- | ---------- | ------------------------------------ |
| "OUI"     | "OUI" | "OUI"      | "Vendor Number"<br>Vendor Assignment |
___
# Prepínacia tabuľka na switchi

- Switche používajú k predávaniu sráv MAC adresy
- Pri prijatí správy si priradí MAC adresu odosielateľa v prepínacej tabuľke k portu na kt. bola správa prijatá
- ak je MAC adresa portu príjemcu v tabuľke predá switch správu na daný port
- pokiaľ nie je pošle ju na všetky porty
- keď adresát odpovie, je jeho MAC adresa pridelená príslušnému portu
- k jednému portu môže byť priradených aj viac MAC adries 
___
# Kritéria pre navrh ethernetových sietí
- kolízia - viacerý uživatelia sa delia o to isté prenosové médium
- **1. šírka pásma, priepustnosť**
	- najviac obmedzujúcim faktorom sú kolízie
	- každá kolízia reálnu priepustnosť danej siete, čím viac zariadení je do siete pripojených, tým väčšia je pravdepodobnosť kolízií
- **2. kolízne domény**
	- časť siete, v kt. môže dôjsť ku kolízií sa nazýva kolízna doména
	- switch každým portom ohraničuje vlastnú kolíznu doménu
	- napr. 12 portový switch vytvára 12 kolíznych domén
	- tiež používajú mikrosegmentáciu
	- čiže switche redukujú kolízie a zvyšujú priechodnosť sietí
- **3. Broadcastové domény**
	- switche musia posielať broadcastové rámce všetkým a ďalšie switche ich musia preposielať tiež
	- preto vzájomne prepojené switche vytvárajú broadcastovú doménu
	- hranicu broadcastovej domény vymedzuje router alebo VLAN
- **4. oneskorenie siete**
	- oneskorenie je čas ako dlho trvá cesta rámca od odosielateľa k príjemcovi
	- zdroje oneskorenia sú väčšinou 3:
		- na sieťovej karte - čas potrebný k interpretácií signálu na 0 a 1 a naopak
		- propagation delay - čas, ktorý potrebuje signál na prechod médiom
		- prepojovacie zariadenie - čas potrebný na spracovanie signálu a jeho poslanie ďalej
		- na čím vyššej vrstve zariadenie pracuje, tým je táto doba dlhšia
- **5. zahltenie siete**
	- pokieľ nie je sieť segmenotvaná, môže dôjsť i pri komuniácií niekoľkých uzlov k zahlteniu siete 
	- riziko zahltenia siete zvyšujú zrýchľujúce sa počítače, zvyšujúci sa objem sieťovej prevádzky, broadcasové správy, náročnejšie sieťové aplikácie
- **6. segmentácia LAN**
	- pri návrhu siete je vhodné si naplánovať segmentáciu kolíznych a broadcastových domén
___
# Módy prepínania rámcov

- **Store-and-forward**
	- Switch uloží celý obsah príjmaného rámca do medzipamäte, v priebehu toho rozhodne o prípadnom cieli a overí správnosť prenosu pomocou CRC súčtu
		- pokiaľ CRC, nesedí rámec zahodí
	- túto metódu používajú cisco catalyst switche

- **Cut-through**
	- switch príjme len začiatok rámca - po MAC adresu prijímateľa
	- potom určí kam rámec predať a okamžite ho začne predávať 
	- neskontroluje CRC takže predáva aj poškodené rámce čím mierne zvyšuje prevádzku na sieti výhodou tejto metódy je rýchlosť
		- je rýchlejšia ako store-and-forward
___
# Symetrické a asymetrické prepínanie

- **Asymetrické preínanie**
	- switch má porty s rôznymi prenosovými rýchlosťami - typicky s väčšou kapacitiou dostupnosť pre servre
	- bežne - 24 portov 10/100 mbps, 2 porty 10/100/1000 mbps
- **Symetrické prepínanie**
	- všetky porty switcha majú rovnakú rýchlosť
___
# Vyrovnávacia pamäť
- vyrovnávacia pamäť (buffer memory) slúži k dočasnémi uloženiu rámcov pred ich odoslaním, kým sa port uvolní alebo sa rámec skontroluje
- **Vyrovnávacia pamäť portu (Port-based memory buffering)**
	- každý port má svoju vlasntnú pamäť = frontu rámcov čakajúcich na odoslanie
- **Zdieaľaná pamäť (Shared memory buffering)**
	- rámce ktoré je potrebné uložiť ,sa ukladajú do pamäte spoločnej pre celý switch
	- kapacita fronty pre jednotlivé porty je prideľovaná dynamicky (podľa potreby)
___
# Konfigurácia switchu
- **prístupové úrovne:**
	- user EXEC - uživateľský režim
	- privileged EXEC - privilegovaný režim
	- globálny konfiguračný režim - (config)#
	- nápoveda pomocou znaku ?
- **štart switcha**
	- inicializujuje CPU a pamäť
	- prevedie POST test
	- inicializuje súborový systém flash
	- zavededie sa východzí image - startup config
- OS potom inicializuje jednotlivé rozhrania
___
# Pripojenie k switchu
- pripojenie sa konfiguruje veľmi podobne ako u routera
- postup: PC → COM port → DB-9 → rollover UTP kábel → RJ-45 → console port → switch
- nastavenie softvéru (terminál) je podobné ako u routera
- diódy pri štarte indikujú stav switchu:
	- počas POST môže systémová LED blikať
	- ak POST prejde bez problémov, LED rýchlo zabliká nazeleno
	- ak POST zlyhá, LED svieti nažlto
___
# Základná konfigurácia switcha
- ak chceme switch konfigurovať vzdialene potrebujeme mu nastaviť IP adresu, masku siete a východziu bránu
- to sa nastavuje virtuálnemu rozhraniu VLAN (virtual LAN) a tá sa priradí správnemu/-ym portu/ -om switcha


PC1 ========= S1

| PC1                             | S1                               |
| ------------------------------- | -------------------------------- |
| - IP adress 172.17.99.12        | - Vlan 99                        |
| - connected to console port     | - the mangment VLAN              |
| - connected ro port F0/18 on S1 | - IP address - 172.17.99.11      |
|                                 | - port F0/18 assigned to VLAN 99 |

## konfigurácia - komandy
- interface vlan 99
- ip add ...
- no shutdown

- int fa0/18
- switchport mode access
- switch access vlan 99
- ip default-gateway ip

- príkazy switchport najprv nastavia režim prísutupu a potom príslušnosť portu k zadanej LAN
- príkaz ip default-gateway je potrebný ak má switch komunikovať so vzdialenými sieťami


# Rýchlosť rozhrania duplex
- u každého rozhrania je možné nakonfigurovať manuálne rýchosť rozhrania a "duplexnosť" prevádzky
- v ukážke je nastavená autodetekcia

- conf t
- int fa0/1
- duplex auto
- speed auto
___
# Správa tabuľky MAC adries
- tabuľka MAC adries môže obsahovať:
	- **statické záznamy** - zadané ručne príkazom
	- **dynamické záznamy** - switch sa ich naučí sám z prijatej komunikácie
- obsah tabuľky sa vypíše príkazom `show mac-address-table`
___
# Konfigurácia zabezpečenia switcha
- **zabezpečenie console portu**
	- console port treba zabezpečiť fyzicky aj logicky (heslom)
	- S1(config) #line con 0
	- S1(config-line) #password cisco
	- S1(config-line) #login
	- S1(config-line) #end
	- odstránenie hesla: `no password`, `no login`
- **zabezpečenie vty (telnet)**
	- portov pre vzdialené pripojenie (vty) môže byť viac (vty 0 až 4), umožňujú pripojenie viacerých administrátorov naraz - preto treba zabezpečiť všetky
	- S1(config)# line vty 0 4
	- S1(config-line)# password cisco
	- S1(config-line)# login
	- S1(config-line)# end
- **zabezpečenie privilegovaného režimu**
	- S1(config)# enable password cisco - heslo sa uloží v čitateľnej podobe
	- S1(config)# enable secret cisco - rovnaké heslo, ale uložené hneď v zašifrovanej podobe
	- S1(config)# service password-encryption - zašifruje všetky heslá v konfigurácii
		- použitá šifra je veľmi slabá, silnejšiu šifru treba nastaviť ručne pre každé heslo
___
# Útoky na zabezpečenie switcha
- **MAC address flooding**
	- veľkosť MAC tabuľky je obmedzená
	- pokiaľ switch nemá MAC adresu príjemcu v tabuľke, rozošle (flooduje) rámec na všetky porty - tento stav sa nazýva "fail-open mode"
	- princíp útoku: zaplniť MAC tabuľku nezmyselnými MAC adresami, aby switch prešiel do fail-open mode a útočník tak "počul" cudziu komunikáciu
- **spoofing** (maskovanie vlastnej totožnosti)
	- útočník sa snaží dostať medzi stanicu a jej východziu bránu, napr. pomocou podvrhnutého DHCP servera (stanica dostane IP adresu od útočníka namiesto legitímneho DHCP servera)
	- iná varianta - "vyčerpanie IP adries" - útočník zaplaví DHCP server požiadavkami a vyčerpá rozsah dostupných IP adries
	- obrana sa nazýva **DHCP snooping** - nastavenie dôveryhodnosti portov
		- S(config)# ip dhcp snooping - povolí DHCP snooping
		- S(config)# ip dhcp snooping vlan číslo - nastaví snooping pre danú VLAN
		- S(config-if)# ip dhcp snooping trust - nastaví port ako dôveryhodný
- **CDP**
	- CDP pakety obsahujú info o verzii HW a SW Cisco zariadení a nie sú šifrované
	- odporúča sa CDP vypnúť všade, kde sa nepoužíva
- **telnet**
	- útočník sa môže pokúsiť získať prístup pomocou odchyteného telnet hesla (telnet nie je šifrovaný)
	- obrana - silné heslá, časté zmeny hesiel, obmedzenie kto sa môže pripájať na vty porty
___
# Konfigurácia zabezpečenia portu (port security)
- umožňuje definovať MAC adresu, skupinu MAC adries alebo maximálny počet MAC adries povolených na danom porte - obmedzuje tým dopad útokov ako MAC flooding
- bezpečné MAC adresy môžu byť:
	- **statické** - zadané príkazom `switchport port-security mac-address mac_adresa`, uložené priamo do MAC tabuľky a run-config
	- **dynamické** - vkladané do MAC tabuľky automaticky, nezostávajú v run-config
	- **sticky** - adresy sa učia dynamicky, ale príkazom `switchport port-security mac-address sticky` sa všetky naučené adresy (pred i po zadaní príkazu) uložia do run-config
		- `no switchport port-security mac-address sticky` - vypne sticky režim, naučené adresy sa odstránia z run-config, ale v MAC tabuľke ostávajú
		- `switchport port-security mac-address sticky mac_adresa` - takto zadaná adresa ostáva aj po vypnutí sticky režimu
- **zabezpečenie nepoužívaných portov**
	- nepoužívané porty je vhodné vypnúť príkazom `shutdown`
	- viac portov naraz sa dá vybrať príkazom interface range, napr. `S1(config)#interface range fa0/1, fa0/12-17`
___
# VLAN (Virtual LAN)

## Vlastnosti VLAN
- VLAN je logicky samostatná, nezávislá sieť
- umožňuje oddeliť rôzne stanice aj keď sú fyzicky v jednej IP (pod)sieti
- VLAN je určená číslom (VLAN ID), pre lepšiu identifikáciu môže byť aj pomenovaná
- stanice patriace do rovnakej VLAN musia mať IP adresy v jednej IP (pod)sieti
- VLAN musí byť na switchi nakonfigurovaná
- všetky porty switcha pripájajúce stanice z jednej VLAN musia byť do tejto VLAN zaradené
- port nakonfigurovaný len pre jednu VLAN sa nazýva **access port**

## Výhody VLAN a rozsahy VLAN ID
- **výhody:**
	- zabezpečenie - sieťová prevádzka jednotlivých VLAN je oddelená
	- úspora nákladov - efektívne využitie prenosového pásma
	- výkon - redukovanie broadcastových domén znižuje zaťaženie siete
	- efektivita práce IT zamestnancov
- **štandardný rozsah VLAN ID:** čísla 1 - 1005
	- 1002 - 1005 sú vyhradené pre Token Ring a FDDI VLAN
	- ID 1 a 1002-1005 sa vytvárajú automaticky a nemožno ich odstrániť
	- konfigurácia VLAN sa ukladá do `vlan.dat` v flash pamäti switcha
	- VTP (VLAN Trunking Protocol) pracuje len s týmto rozsahom
- **rozšírený rozsah VLAN ID:** čísla 1006 - 4094
	- poskytuje menej funkcií ako štandardný rozsah
	- ukladá sa do running-config (nie do vlan.dat)
	- VTP tento rozsah nepodporuje
	- používa ho väčšinou poskytovateľ (provider)

## Typy VLAN
- **dátová VLAN** - len pre prenos užívateľských dát (okrem hlasu a manažmentu switchov), nazýva sa aj užívateľská VLAN
- **východzia (default) VLAN** - pri prvom starte switcha sú všetky porty v default VLAN s ID 1; nemožno ju premenovať ani zmazať; protokoly ako CDP a STP ju vždy používajú, preto je vhodné prevádzkové porty zaradiť do inej VLAN
- **native VLAN** - prideľovaná na 802.1Q trunk portoch; tieto porty podporujú komunikáciu z rôznych VLAN (tagged) aj komunikáciu nepochádzajúcu zo žiadnej VLAN (untagged)
- **management VLAN** - akákoľvek VLAN, ktorá umožňuje vzdialenú správu switcha (HTTP, telnet, SSH, SNMP); vhodné oddeliť od VLAN 1
- **hlasová (voice) VLAN** - pre plynulý prenos hlasových služieb; požiadavky: zaistená šírka pásma, priorita dát, oneskorenie menej ako 150 ms

## Režimy pridelenia portu k VLAN
- pri konfigurácii VLAN sa povinne nastaví VLAN ID, voliteľne aj meno; potom sa porty priradia k danej VLAN
- port môže patriť do:
	1. **statickej VLAN**
	2. **dynamickej VLAN** - využíva sa zriedka; príslušnosť k VLAN je definovaná na serveri a port sa prideľuje podľa MAC adresy zariadenia
	3. **hlasovej VLAN** - predpokladá sa pripojený IP telefón (patriaci napr. do voice VLAN 150) a cez neho ďalšia stanica (patriaca do inej VLAN, napr. 20)

## Broadcasty vo VLAN sieťach
- **sieť bez VLAN segmentácie** - switche preposielajú broadcastové rámce na všetky svoje porty
- **sieť s VLAN** - broadcasty sa posielajú len v rámci konkrétnej VLAN nakonfigurovanej na switchoch; ak majú VLAN-y komunikovať medzi sebou, je potrebný router
- **intra-VLAN komunikácia** - komunikácia zariadení v rámci jednej VLAN; pred prenosom dát musí odosielateľ získať MAC adresu cieľa pomocou ARP request, ktorý sa posiela na všetky porty danej VLAN
- **inter-VLAN komunikácia** - komunikácia zariadení medzi rôznymi VLAN; odosielateľ si zistí MAC adresu gateway, router potom zistí MAC adresu cieľa pomocou ARP request do portov cieľovej VLAN, cieľ odpovie ARP reply a router následne posiela rámce od zdroja k cieľu

## Broadcastové domény - L3 switche
- L3 switche podporujú smerovanie na úrovni tretej (sieťovej) vrstvy
- funkciu routera nahradí L3 switch, ktorému sa nakonfigurujú dve **SVI** (Switch Virtual Interface), zastupujúce napr. rozhrania F0/1 a F0/2 routera
- SVI je virtuálne logické rozhranie konfigurované pre danú VLAN, nutné pokiaľ chceme smerovať medzi VLAN
- defaultne sa SVI vytvára pre východziu VLAN (VLAN 1) kvôli vzdialenej správe switcha

## Prepojovanie VLAN - trunk spoje
- **trunk** - spoj medzi dvoma zariadeniami, ktorý prenáša komunikáciu viacerých VLAN
- na Cisco zariadeniach je pre Fast Ethernet a Gigabit Ethernet rozhrania podporovaný protokol **802.1Q**
- trunk nepatrí do konkrétnej VLAN - je to prepojenie medzi VLAN cez switche a routery

## Označovanie rámcov - 802.1Q
- štandardné ethernetové rámce neobsahujú info o VLAN, preto sa k rámcu pridáva 802.1Q hlavička (VLAN tag)
- ak switch prijme rámec na access porte s definovanou statickou VLAN, vloží do rámca VLAN tag, prepočíta FCS a predá rámec na trunk port
- **native VLAN a 802.1Q trunk:**
	- rámce prichádzajúce na porty native VLAN by mali byť neoznačené (untagged)
	- ak switch dostane na trunk port označený rámec patriaci native VLAN, zahodí ho
	- ak má k takému portu byť pripojené zariadenie, ktoré odosiela označené rámce, treba ho nakonfigurovať

## Funkcia trunku - DTP
- **DTP (Dynamic Trunking Protocol)** - Cisco protokol, ktorý automaticky vyjedná nastavenie trunk režimu, pokiaľ je port na druhom switchi v trunk režime podporujúcom DTP

## Konfigurácia VLAN a trunk spojov
- **všeobecný postup:**
	1. vytvoriť VLAN
	2. staticky priradiť porty do VLAN
	3. overiť konfiguráciu VLAN
	4. povoliť trunk na spojoch medzi switchmi
	5. overiť konfiguráciu trunkov
- **overovacie príkazy:**
	- `show vlan brief` - jednoriadkové zhrnutie pre každú VLAN
	- `show vlan id 20` - podrobné info o VLAN podľa ID
	- `show vlan name student` - podrobné info o VLAN podľa mena
	- `show vlan summary` - súhrnné info o počte a type konfigurovaných VLAN
	- `show interfaces fa0/18` - info o rozhraní
	- `show interfaces fa0/18 switchport` - podrobné info o rozhraní vrátane VLAN/trunk nastavení
	- `show interfaces vlan 20` - stav VLAN (up/down) a ďalšie podrobnosti
- **odstránenie VLAN:**
	- `no vlan 100` - odstráni VLAN 100; pozor, pred odstránením treba jej porty presunúť do inej VLAN, inak nebudú funkčné
	- `delete flash:vlan.dat` - odstráni info o všetkých definovaných VLAN


## Súvisiace
- [[komunikacia]]
- [[school/2it/iot/protokoly]]
- [[spojenia]]
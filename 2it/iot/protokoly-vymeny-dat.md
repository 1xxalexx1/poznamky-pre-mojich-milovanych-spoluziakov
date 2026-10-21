# Protokoly výmeny dát v IoT
- v IoT si zariadenia posielajú dáta
- výmena prebieha cez ľahké dátové formáty ktoré sú čitateľné pre stroje aj ľudí
- cieľ: efektívne prenášať dáta s minimálnou záťažou siete

## CSV
- comma separated values
- jednoduchý textový formát kde sú hondoty oddelené čiarkou
- používa sa na tabuľkové dáta
- **výhody:**
	- veľmi ľahký formát - nízka dátová veľkosť
	- jednoduchý na spracovanie
- **nevýhody:**
	- neobsahuje štruktúru ani hierarchiu dát
	- nevýhodný pre zložité alebo vnorené dáta

## XML
- extensible markup language
- značkový jazyk podobný HTML
- používa sa na štruktúrované a hierarchické dáta
- **výhody:**
	- dáta sú jasne šturktúrované pomocou značiek
	- prenositeľnosť a univerzálnosť - podporovaný v monohých systémoch
- **nevýhody**:
	- veľký objem dát - obsahuje veľa značiek
	- pomaľšie spracovanie oproti CSV/JSON

## JSON
- javascript object notation
- ľahký dátový formát veľmi rozšírený v IoT a webových aplikáciách
- dáta sú uložené v pároch kľúč - hodnota, často v podobe objektov
- **výhody:**
	- ľahko čitateľný a kompaktný
	- výborný pre zložité a vnorené dáta
	- podpora v mnohých programovacích jazykoch
- **nevýhody:**
	- väčší ako CSV ale menší ako XML

## HTML
- hypertext markup language
- primárne jazyk na zobrazovanie webových stránok
- v IoT sa používa na prezentáciu dát, nie priamo na ich výmenu
- **výhody:**
	- jednoduchá vyzualizácia dát pre použivateľov
	- možno kombinovať s JavaScriptom na živé zobrazenie IoT dát
- **nevýhody:**
	- veľký a zbytočne zložitý pre samotný prenos dát

## MQTT
- štandard komunikácie v IoT
- efektívny prenos malý objemov dát
- malá dátová režia
- rýchly a efektívny - nízka odozva - latency
- asynchrónna komunikácia - zariadenia nemusia byť pripojené stále
- podpora zabezpečenia - TSL/SSL autentifikácia
- jednoduchá integrácia do rôznych IoT zariadení
- základom MQTT je model publish/subscribe
- publisher - vydavateľ - zariadenie ktoré dáta **odosiela**
- subscriber - odoberateľ - zariadenie ktoré sa zaujíma o určitý typ dát
- broker - centrálny sprostredkovateľ, prjíma všetky správy od pub. a dáva ich subs.
- zariadenia medzi sebou nekomunikujú priamo ale cez brokera
- každá správa má priradenú tému - podobné ako _??????????_ -  dom/kuchyňa/teplota
- subscriber môže odoberať presnú tému alebo používať wildcardy
	- dom/+/ teplota - odoberá teplotu zo všetkých miestností
	- dom/# - všetky dáta domu
### MQTT - QOS
- quality of service
- 0 - at most one - správa sa doručí najviac raz
- 1 - at least one - minimálne raz
- 2 - exactly one - doručí práve raz pomocou zložitého potvrdenia
# Zadania pkrim 2024

Zadania a artefakty vychádzajú z dvoch case-study príkladov na incident. Cieľom cvičenia je spojiť
všetky doteraz získané vedomosti a vykonať forenznú analýzu incidentu.

## Inicident

Zamestnanec firmy AVF s.r.o. dostal do svojej schránky mail. Javil sa ako oficiálny mail od firemenj účtovníčky
a obsahoval text: 

>Predmet: Dôležité: Aktualizácia informácií o výplatnej páske
>
>Dobrý deň Peter,
>
>Som Eva, manažérka oddelenia ľudských zdrojov v našej spoločnosti. Rád by som vás informovala o dôležitej aktualizácii týkajúcej sa vašej výplatnej pásky.
>
>Prosím, pozrite si pripojený súbor (Výplatná_páska_2024-02.pdf), ktorý obsahuje podrobné informácie o vašej aktuálnej výplatnej páske za obdobie február 2024. Je dôležité, aby ste si overili správnosť údajov uvedených v tomto dokumente.
>
>Ak máte akékoľvek otázky alebo potrebujete ďalšiu pomoc, neváhajte ma kontaktovať.
>
>S pozdravom,
> 
>Eva Nováková, Manažérka Oddelenia Ľudských Zdrojov
> 
>AVF. s.r.o
> 
>eva.novak@AVF.sk

### Zadanie 1 (prvá fáza IR)

Link: https://drive.google.com/drive/folders/1WjCEuDrglKi_TyjEvPrynwUu0MfuQYzE?usp=sharing

Readme
~~~ 
Pri práci analytika je potrebné vedieť udalosti nie len správne analyzovať ale aj zachytiť dôkazy. Vašou úlohou v tomto zadaní je využiť AcessData FTK Imager na zachytenie triage obrazu disku ľubovoľného zariadenia s operačným systémom Windows (Váš ntb, virtuálka...). Následne je potrebné vykonať rovnaký postup na zaradení s operačným systémom linux za pomoci nástroja príkazového riadku dcfldd. Následne pomocou zvoleného nástroja vytvorte hash zachytených dôkazov pred aj po analýze aby ste sa ubezpečili, že dôkazy neboli modifikované.

Výstup zadania:
Dokument, ktorý bude obsahovať

	- Popis použitého nástroja a stručný popis na akom zariadení ste údaje získavali (Pre obidva operačné systémy)
	- Podrobne zdokumentujte ako ste postupovali pri zachytávaní digitálnych dôkazov a pri vytváraní kontrolého hashu
	- Zo zachteného triage obrazu sa pokúste zistiť základné systémové údaje o zariadení (OS + verzia, používatelia, timezone ...)
	- Porovnanie postupu zachytávania triage obrazov pre Linux a Windows

Pokúste sa v dokumente popísať rozdiely, ktoré ste si všimli v procese zachytávania obrazu aj pri získavaní systémových údajov 

FTK Imager: https://www.exterro.com/ftk-imager
Pofidérny zdroj ale funkčný bez vypĺňania formulára: https://iowin.net/en/ftk-imager/
dcfldd: https://www.kali.org/tools/dcfldd/
~~~

### Zadanie 2 
Link: https://drive.google.com/drive/folders/1-hJkNU4Ju5Rn8pQ9qd99JZfgzvAp3WYZ?usp=sharing

Readme
~~~
Analyzujte priloženú hlavičku, do reportu uveďte nie len technické detaily z Vašej analýzy ale aj Vaše poznatky z pohľadu analytika.
Pri písaní forenznej analýzy je potrebné nie len správne zhrnúť technický postup a použité nástroje ale aj manažérske zhnutie celého vyšetrovania. 
Uveďte Vaše závery z analýzy, čo ste zistili, aké sú vaše predpoklady, prípadne v čom sa vyskytol pri analýze problém (nedostatok informácií, zdrojov ...)
~~~

### Zadanie 3

Link: https://drive.google.com/drive/folders/1RTtSR-9j5YGeie6qesaydm9V_SqIr_I2?usp=drive_link

Readme
~~~
Príloha vyplatna_paska_Feb24.pdf obsahuje podozrivú prílohu vo forme pdf súboru. Analyzujte tento pdf súbor a spíšte Vaše zistenia:

- strušný popis nástrojoc ktoré ste použili
- základné údaje o súbore
- podrobne popíšte čo podozrivé ste objavili v pdf súbore 
- poskúste sa odhaliť aká zraniťeľnosť bola použitá a ako sa tomu dalo predísť

súbor analyzujte výhradne v Kali!
heslo: infected
~~~

### Zadanie 4

Link: https://drive.google.com/drive/folders/1ZdTgcqZjULM6791h7ngPhDiCtrgk8Dxh?usp=sharing

~~~
Našťastie máte zapnuté monitorovanie siete a zachytili ste premávku v čase kedy máte podozrenie na aktivitu útočníka. 
Pokúste sa analyzovať priložený súbor traffic.pcapng a popíšte čo vidíte v záznamoch. 
Pokúste sa identifikovať podozrivú aktivitu na zariadení a skontrolujte či nedošlo ku exfiltrácií dát.

Hint: podozrivé porty, adresa 192.168.137.106
~~~

### Zadanie 5

Link: https://drive.google.com/drive/folders/14XcqKqjdjjx045IUB_8A9joV12gYIIZw?usp=sharing

Readme
~~~
Zachytili ste vzorku kódu, ktorú útočník nahral a spustil na zariadení, naštastie sa jedná pravdepodobne o skript kiddie útočníka ktorý nenakódil škodlivý kód dobre.
Pokúste sa kód deobfuskovať a zistite čo sa na počítači vykonávalo. 
Viete však, že kód niečo zašifroval, naštastie už poznáte tajný kľúč: jZoGpdNx.

Spíšte postupy a zistenia z analýzy kódu. Reverzujte kód a odšifrujte priložený súbor flag.pkrim. Do reportu priložte aj deobfuskovaný kód.
~~~

### Zadanie 6

Link: https://drive.google.com/drive/folders/1OKjiAWMbuZD3zyf-NcS68DpCaxSvWpBX?usp=drive_link

Readme
~~~
Na anlýzu ste dostali .pcap súbor jeného z firemných počítačov. Pokúste sa z tejto komunikácie zistiť základné systémové informácie aj to či neprebehla podozrivá komunikácia.
Pokúste sa zistiť: 
	- Názov počítača z ktorého prebehla podozrivá komunikácia 
	- IP a MAC adresu tohto počítača (vieme, že sa používajú IP z range-u 192.168.1.0/16)
	- Pomocou akého protokolu prebehla podozrivá komunikácia
	- Nájdite informácie, ktoré unikli. (login, heslo, systémové údaje, adresy účastníkov)
	- Napíšte čas kedy k tomuto incidentu došlo 
~~~

### Zadanie 7

Link: https://drive.google.com/drive/folders/18NqZwUja-pX3ZTplEj6BN-oey12z8N-D?usp=drive_link

Readme
~~~
Dostali ste od firmy hlásenie, že ich počítač bol napadnutý. K dispozícií máme export Windows Events Logov v .xml formáte a .pcap súbor s odchytenou komunikáciou. Vašou úlohou je zistiť, čo sa počas incidentu dialo.
Úlohy: 
   -	Zistite ako útočník prenikol do systému. V priloženom .xml súbore nájdite korešpondujúci event, ktorý hovorí o prieniku do systému. Nájdite čas prvého 	prieniku a targetuser, vďaka ktorému útočník do systému prenikol.	
   -	Po tom ako sa mu podarilo prihlásiť, spustil v počítači malware, zistite jeho názov. 
   -	Útočník prenikol do systému cez telnet server pomocou brute-force útoku. Zistite z .pcap súboru meno používateľa a heslo, ktoré úhádol.
   - 	Po prihlásení útočník stiahol z internetu exploit, nájdite url stránky odkiaľ bol
	exploit stiahnutý
~~~

### Zadanie 8

Link: https://drive.google.com/drive/folders/1ejdvg3zxPE8fXr1JlUuX0Pb8jTOaM0O_?usp=drive_link

Readme
~~~
V priloženom priečinku máte k dispozícií .E01 záznam disku doménového radiča. Analyzujte tento súbor v programe Autopsy a odpovedzte na nasledujúce otázky, k odpovedi treba pripísať aj to kde ste danú informáciu našli.
Otázky: 
  Server
	- Akých používateľov viete v zariadení identifikovať
	- Aký je názov servera, operačný systém a detegovaná architektúra procesora
	- Skontrolujte históriu prehliadania a naájdite IP adresu, s ktorou prebehla podozrivá komunikácia
	- V počítači sa nachádza niekoľko súborov .txt, nájdite ich umiestnenie a ich obsah - NoJerry.txt, Beth_secret.txt
	- Súbor SECRET_beth.txt bol z počítača vymazaný, zistite jeho obsah
 	- Vyberte si ľubovoľný Autopsy plugin a demoštrujte jeho použitie

*3rd party plugins: https://wiki.sleuthkit.org/index.php?title=Autopsy_3rd_Party_Modules
~~~

### Zadanie 9

Link: https://drive.google.com/drive/folders/1bNxIDB4Rx7Own5kU1n14o52w08ptbJjH?usp=drive_link

Readme
~~~
Na anlýzu ste dostalo obraz pamäte počítača. Analyzujte ho pomocou nástroja volatility a odpovedte na nasledovné otázky:

- aký operačný systém (profil) má daný dump
- vylistujte procesy a uvedte názov a PID podozrivého procesu a taktiež jeho rodiča
- uveďte IP adresu zariadenia
- nájdite adresu útočníka na základe znalosti PID podozrivého procesu
- pokúste sa vydumpovať daný proces a uveďte jeho md5 hash (môžete pozdieť VirusTotal, Alienvault...)
- zistite aký používateľ sa na počítači nachádzal a zistite hash jeho hesla
- vieme že pomocou príkazového riadka bol spustný .vbs skript, uveďte jeho názov
- vydumpujte proces notepad.exe (zistite jeho pid) a pokúste sa zistit čo v ňom bolo napísané (hint: strings)

V zadaní uveďte aj postup (príkazy) a vaše závery. 
~~~
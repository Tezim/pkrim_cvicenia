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

https://drive.google.com/drive/folders/1WjCEuDrglKi_TyjEvPrynwUu0MfuQYzE?usp=sharing


### Zadanie 2 

Peter je zamestnanec AVF s.r.o. (Akože Vymyslená Firma), ktorá poskytuje malým klientom a podnikateľom reklamné služby. Táto firma je zopovedná za rozosielanie
aktuálnych ponúk a akcií týchto firiem. Peter pôsobí ako pomocná sila pri správe ich databázy klientov, ktorá obsahuje ich reklamné emailové schránky, heslá a zoznamy klientov. 
https://drive.google.com/drive/folders/1-hJkNU4Ju5Rn8pQ9qd99JZfgzvAp3WYZ?usp=sharing


### Zadanie 3
Peter si všimol nevinnú chybu v texte avšak neprikladal tomu význam. Mail sa javil ako oficiálna správa, ktorú síce zvyčajne nedostáva
avšak daná pracovníčka mu je známa tak prílohu stiahol a otvoril.

#### <span style="color:red;">Artefakt #3</span>
>PDF Výplatná_páska_2024-02.pdf - analýza pdf ktoré obsahuje autorun akciu, javasript, v komentári flag-fake, pravý flag v JS
>
> <span style="color:green;">
> Kompletná analýza metadát akomentárov - fake flag
> popísať autorun akcie - okienko, ktoré vypýta rodné číslo akože zaheslované ale posiela data
> </span>

### Zadanie 4
Kód v PDF stiahol z github repozitára škodlivý kód, analyzujte kód a popíšte čo vykonával
#### <span style="color:red;">Artefakt #4</span>

> Malicious kód stiahnutý z githubu
> Tu domyslieť že čo bude ten kód robiť - komunikácia s iným PC? bruteforce prihlásenie na DB server

### Zadanie 5
Útočník pomocou skriptu vykonal brute-force útok na DB serve, bohžial admin používal slabé heslo a dostal sa tam
#### <span style="color:red;">Artefakt #5</span>
> Linux logy ? databázové logy? niečo čo bude ukazovať exfiltráciu

### Zadanie 6
Zistili sme kam sa odosielalo info, bol to počítač jedného z kolegov vo firme 
Zachytili sme obraz systému aj daného zamestnanca, skúste analyzoavť všeobecne či nájdete niečo zaujímavé v pamäti
#### <span style="color:red;">Artefakt #5</span>
> Tu by som použila už jedno zo zadaní z minulého roka na anlýzu pomocou volatility
> 
> 
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

- vytvoriť image systému Windows pomocou FTK imagera, Spísať inventár artefaktov + hashe (vyslúšať si klasický postup pri zachytávaní dôkazov)
- tu by som možno pridala image nejakého USB
- nejakeho programu - vyskúšať si certutil
#### <span style="color:red;">Artefakt #1</span>
> Image systému + usb napríklad
> výsledkom má byť zoznam zachytených dôkazov 
> analýza systému - zákldané údaje a čo kde hľadať (doplním)


### Zadanie 2 

Peter je zamestnanec AVF s.r.o. (Akože Vymyslená Firma), ktorá poskytuje malým klientom a podnikateľom reklamné služby. Táto firma je zopovedná za rozosielanie
aktuálnych ponúk a akcií týchto firiem. Peter pôsobí ako pomocná sila pri správe ich databázy klientov, ktorá obsahuje ich reklamné emailové schránky, heslá a zoznamy klientov. 
#### <span style="color:red;">Artefakt #2</span>
> Falošný email - analýza hlavičiek - niekde skryť flag?
> Použitie OSINT na odhalenie neopatrného pćhateľa
> 
> <span style="color:green;">
> Nesprávne vytvorená hlavička - útočník zabudol a ponechal aj svoje súkromné údaje
> OSINT part - zistenie kto je útočník - fejkové socials s flagom, možno ľahký github page
> </span>

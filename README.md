# Avans-ATLS.github.io

## Eiwit peptide coverage visualisatie
Een interactieve tool die peptide coverage op een eiwit sequentie visualiseert.

### Input
De volgende input is nodig voor de visualisatie:
- FASTA bestand met volledige eiwit sequentie
```txt
>voorbeeld_eiwit_1
AVANSATLSMVMKLAVANSATLSMVMKLLKMVMSLTASNAVA
```
- Excel bestand met peptide lijst in eerste sheet, header "Sequence" in A1, peptides in A2+
```txt
# Excel bestand met 1 sheet
Sequence
AVANS
MVMK
LAVA
TAS
BIRGIT
```
> Pro tip: De lijst kan een andere header hebben, typ deze dan in het "Peptide header Excel" vak

### Output
Als de juiste input is aangegeven wordt de coverage gevisualiseerd na het klikken op "Visualiseer coverage".

Zie onderstaande afbeelding voor een voorbeeld:
<img width="1031" height="743" alt="image" src="https://github.com/user-attachments/assets/6e842689-3148-45ce-a672-49111d82c1df" />
- Bovenaan staat de naam van het eiwit uit de FASTA, samen met de lengte
- De tweede rij bevat algemene statistieken:
  - Het percentage van het eiwit dat gedekt is door de peptides
  - Het aantal eiwit-residuen van het totale aantal eiwit-residuen dat gedekt is door de peptides
  - Het aantal peptiden van het totale aantal peptiden dat op het eiwit gemapped is
  - Het aantal peptiden dat **niet** op het eiwit gemapped is
- De derde rij bevat een grafische weergave van het percentage coverage
- Het vierde gedeelte laat alle aminozuren van het eiwit zien in de volgorde uit de FASTA, waarbij gedekte aminozuren groen gekleurd zijn
  - Het vijfde gedeelte laat de legenda van bovenstaande figuur zien
- Het laatste gedeelte geeft een overzicht van de statistieken per gevonden/niet gevonden peptide

### Bonus
- De tool staat standaard op dark-modus, zet light-modus aan met de knop rechtsboven!
  <img width="1035" height="748" alt="image" src="https://github.com/user-attachments/assets/60edb7c4-09d4-4289-adf5-5c242d5f5efb" />
- Exporteer de per-peptide statistieken naar CSV met de knop rechtsonder!
  ```txt
  Peptide,Lengte,Start (1-based),Eind (1-based),Status
  AVANS,5,1,5,Gevonden
  AVANS,5,15,19,Gevonden
  MVMK,4,10,13,Gevonden
  MVMK,4,24,27,Gevonden
  LAVA,4,14,17,Gevonden
  TAS,3,36,38,Gevonden
  BIRGIT,6,,,Niet gemapped
  ```
- Pas lengte van de rijen in de visualisatie aan door een andere waarde te kiezen bij "Residuen per rij"!
- Voer een nieuwe analyse uit zonder te re-loaden door op de "Reset" knop te klikken!

  

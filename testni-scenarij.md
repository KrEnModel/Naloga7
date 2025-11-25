# Testni scenariji

## 1. Pametno upravljanje nalog

**Funkcionalnost:**  
Samodejno razvrščanje nalog po prioriteti, roku in tipu.

**Koraki izvedbe testa:**
1. Odpri aplikacijo.
2. Dodaj 3 naloge:
   - Naloga A: rok danes, visoka prioriteta, tip "Šola".
   - Naloga B: rok čez 3 dni, srednja prioriteta, tip "Osebno".
   - Naloga C: rok čez 1 dan, nizka prioriteta, tip "Delo".
3. Shrani vse naloge.
4. Osveži pogled seznama nalog (npr. povlek navzdol ali ponovni zagon aplikacije).
5. Preveri vrstni red prikaza nalog na glavnem seznamu.

**Pričakovan rezultat testa:**
- Naloge so razvrščene tako, da je najprej prikazana naloga z najvišjo prioriteto in najbližjim rokom.  
  Pričakovani vrstni red:
  1. Naloga A (visoka prioriteta, rok danes)  
  2. Naloga C (nizka prioriteta, rok čez 1 dan)  
  3. Naloga B (srednja prioriteta, rok čez 3 dni)  
- Tip naloge (Šola/Delo/Osebno) ne spremeni logike razvrščanja, le filtriranje/označevanje.


---

## 2. Sinhronizacija med napravami

**Funkcionalnost:**  
Takojšnja sinhronizacija nalog in opomnikov med telefonom, tablico in računalnikom.

**Koraki izvedbe testa:**
1. Prijavi se v aplikacijo na telefonu in na računalniku z istim uporabniškim računom.
2. Na telefonu dodaj novo nalogo z naslovom "Test sinhronizacije" in rokom danes.
3. Preveri, ali se na telefonu naloga prikaže na glavnem seznamu.
4. Odpri aplikacijo na računalniku (ali jo osveži, če je že odprta).
5. Počakaj nekaj sekund in preveri seznam nalog na računalniku.
6. Na računalniku uredi isto nalogo (spremeni naslov v "Test sinhronizacije – urejeno").
7. Ponovno preveri seznam nalog na telefonu.

**Pričakovan rezultat testa:**
- Naloga "Test sinhronizacije" se po dodajanju na telefonu samodejno pojavi tudi na računalniku brez ročnega ponovnega vnosa.
- Sprememba naslova naloge na računalniku se v kratkem času odrazi tudi na telefonu.
- Ni podvojenih nalog, podatki (naslov, rok, status) so enaki na obeh napravah.


---

## 3. Glasovni vnosi

**Funkcionalnost:**  
Dodajanje naloge z glasovnim ukazom brez tipkanja.

**Koraki izvedbe testa:**
1. Odpri aplikacijo na telefonu.
2. Na glavnem zaslonu izberi možnost "Dodaj nalogo" preko glasovnega vnosa (npr. ikona mikrofona).
3. Izgovori stavek: "Dodaj nalogo: Kupiti mleko jutri ob 17:00."
4. Počakaj, da aplikacija zaključi prepoznavanje govora in ustvari nalogo.
5. Preveri podrobnosti nove naloge v seznamu nalog.

**Pričakovan rezultat testa:**
- Aplikacija pravilno prepozna govor in ustvari novo nalogo z naslovom "Kupiti mleko" (ali zelo podobnim).
- Rok naloge je nastavljen na naslednji dan ob 17:00.
- Naloga je vidna v glavnem seznamu nalog, kot da bi bila dodana ročno (možno jo je urejati, brisati, označiti kot dokončano).

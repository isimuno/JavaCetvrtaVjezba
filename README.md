# JavaCetvrtaVjezba
4.1. TEMA VJEŽBE

Svrha laboratorijske vježbe je korištenje zbirki iz skupina listi, setova
i mapa te zamjena svih polja u aplikaciji sa zbirkama. U sklopu vježbe je
također sve skupine konstanti potrebno zamijeniti enumeracijama.
Također se u vježbi implementira i algoritam prema kojim se sortiraju
objekti unutar zbirki.
4.2. ZADATAK ZA PRIPREMU
Proširiti rješenje treće laboratorijske vježbe na način da se kopira
rješenje te preimenuje u naziv koji sadrži indeks „4“, umjesto „3“. Osim
same mape s projektom, potrebno je promijeniti i naziv projekta unutar
IntelliJ-a korištenjem opcije „Refactor->Rename“. Program je potrebno
proširiti na sljedeći način:
1. Na svim mjestima u aplikaciji gdje se koriste polja osoba potrebno je
polje zamijeniti listom. Umjesto polja u kojima se nalaze županije,
simptomi i bolesti je potrebno koristiti zbirke iz tipa set.
2. Nadjačati „equals“ i „hashCode“ metode za klase „Bolest“, „Osoba“,
„Simptom“, „Virus“ i „Zupanija“ korištenjem opcije IntelliJ-a opisane
na sljedećem linku: „https://www.jetbrains.com/help/idea/generateequals-and-hashcode-wizard.html“.
3. Umjesto definiranja fiksnog broja županija, osoba, simptoma, bolesti
i virusa, potrebno je od korisnika zatražiti unos podatka o količinama
objekata koje će korisnik unositi.
4. Kreirati novi paket „hr.java.covidportal.enumeracija“.
5. U paket „hr.java.covidportal.enumeracija“ dodati enumeraciju koja će
zamijeniti konstante koje predstavljaju vrijednosti simptoma (npr. za
vrijednosti „RIJETKO“, „SREDNJE“ ili „CESTO“). Enumeracija mora imati
svoj konstruktor (koji prima String s kojim se definira vrijednost 
simptoma „RIJETKO“, „SREDNJE“ ili „ČESTO“) te „getter“ metode za
vrijednost simptoma.
6. Metodu „main“ u glavnoj klasi proširiti zbirkom iz tipa mapa koja će
za ključ imati objekt klase „Virus“ ili „Bolest“, a za vrijednost listu
osoba koje boluju od određene bolesti ili su zaražene određenim
virusom. Na kraju programa ispisati informacije o osobama i virusima
kojima su zaražene te bolestima od kojih boluju.
7. Klasu „Zupanija“ proširiti podatkom o broju zaraženih osoba tipa
„Integer“. Prilikom unosa podataka o županijama potrebno je od
korisnika zatražiti unos podataka o broju zaraženih osoba, uz podatak
od broju stanovnika.
8. Kreirati novi paket „hr.java.covidportal.sortiranje“.
9. Unutar paketa „hr.java.covidportal.sortiranje“ kreirati klasu
„CovidSorter“ koja implementira sučelje „Comparator“ te unutar
metoda „compare“ implementira algoritam koji sortira podatke o
županijama po postotku zaraženosti
10. Na kraju programa ispisati podatak o županiji u kojoj je najveći i
najmanji postotak zaraženih osoba.
Primjer izvođenja programa:
Unesite broj županija koje želite unijeti: 3
Unesite podatke o 3 županije:
Unesite naziv županije: GRAD ZAGREB
Unesite broj stanovnika: asb
Pogreška u formatu podataka, molimo ponovite unos!
Unesite broj stanovnika: 1000000
Unesite broj zaraženih stanovnika: 20000
Unesite naziv županije: MEĐIMURSKA
Unesite broj stanovnika: 100000
Unesite broj zaraženih stanovnika: 500
Unesite naziv županije: VARAŽDINSKA
Unesite broj stanovnika: 200000
Unesite broj zaraženih stanovnika: 10000
Unesite broj simptoma koje želite unijeti: 3
Unesite podatke o 3 simptoma:
Unesite naziv simptoma: VISOKA TEMPERATURA
Unesite vrijednost simptoma (RIJETKO, SREDNJE ILI ČESTO): ČESTO
Unesite naziv simptoma: GLAVOBOLJA
Unesite vrijednost simptoma (RIJETKO, SREDNJE ILI ČESTO): SREDNJE
Unesite naziv simptoma: GRLOBOLJA
Unesite vrijednost simptoma (RIJETKO, SREDNJE ILI ČESTO): RIJETKO
Unesite broj bolesti koje želite unijeti: 2
Unesite broj virusa koje želite unijeti: 2
Unesite podatke o 4 bolesti ili virusa:
Unosite li bolest ili virus?
1) BOLEST
2) VIRUS
ODABIR >> 1
Unesite naziv bolesti ili virusa: HERPES
Unesite broj simptoma: 1
Odaberite 1. simptom:
1. VISOKA TEMPERATURA ČESTO
2. GLAVOBOLJA SREDNJE
3. GRLOBOLJA RIJETKO
Odabir: 3
Unosite li bolest ili virus?
1) BOLEST
2) VIRUS
ODABIR >> 2
Unesite naziv bolesti ili virusa: Covid
Unesite broj simptoma: 1
Odaberite 1. simptom:
1. VISOKA TEMPERATURA ČESTO
2. GLAVOBOLJA SREDNJE
3. GRLOBOLJA RIJETKO
Odabir: 3
Pogrešan unos, već ste unijeli bolest ili virus s istim simptomima. Molimo
ponovite unos.
Unesite naziv bolesti ili virusa: Covid
Unesite broj simptoma: 1
Odaberite 1. simptom:
1. VISOKA TEMPERATURA ČESTO
2. GLAVOBOLJA SREDNJE
3. GRLOBOLJA RIJETKO
Odabir: 1
Unosite li bolest ili virus?
1) BOLEST
2) VIRUS
ODABIR >> 2
Unesite naziv bolesti ili virusa: Gripa
Unesite broj simptoma: 1
Odaberite 1. simptom:
1. VISOKA TEMPERATURA ČESTO
2. GLAVOBOLJA SREDNJE
3. GRLOBOLJA RIJETKO
Odabir: 2
Unosite li bolest ili virus?
1) BOLEST
2) VIRUS
ODABIR >> 2
Unesite naziv bolesti ili virusa: KONJUKTIVITIS
Unesite broj simptoma: 1
Odaberite 1. simptom:
1. VISOKA TEMPERATURA ČESTO
2. GLAVOBOLJA SREDNJE
3. GRLOBOLJA RIJETKO
Odabir: 2
Unesite 1. ime osobe: Pero
Unesite prezime osobe: Perić
Unesite starost osobe: 88
Unesite županiju prebivališta osobe: 
1. GRAD ZAGREB
2. MEĐIMURSKA
3. VARAŽDINSKA
Odabir: 1
Unesite bolest ili virus osobe:
1. HERPES
2. Covid
3. Gripa
4. KONJUKTIVITIS
Odabir: 4
Unesite 2. ime osobe: Janko
Unesite prezime osobe: Janić
Unesite starost osobe: 77
Unesite županiju prebivališta osobe:
1. GRAD ZAGREB
2. MEĐIMURSKA
3. VARAŽDINSKA
Odabir: 2
Unesite bolest ili virus osobe:
1. HERPES
2. Covid
3. Gripa
4. KONJUKTIVITIS
Odabir: 2
Unesite broj osoba koje su bile u kontaktu s tom osobom: 2
Neispravan unos, možete odabrani maksimalno 1 osobu.
Unesite broj osoba koje su bile u kontaktu s tom osobom: 1
Unesite osobe koje su bile u kontaktu s tom osobom:
Odaberite 1. osobu:
1. Pero Perić
Odabir: 1
Unesite 3. ime osobe: Marica
Unesite prezime osobe: Ždrerić
Unesite starost osobe: 44
Unesite županiju prebivališta osobe: 
1. GRAD ZAGREB
2. MEĐIMURSKA
3. VARAŽDINSKA
Odabir: 3
Unesite bolest ili virus osobe:
1. HERPES
2. Covid
3. Gripa
4. KONJUKTIVITIS
Odabir: 3
Unesite broj osoba koje su bile u kontaktu s tom osobom: 2
Unesite osobe koje su bile u kontaktu s tom osobom:
Odaberite 1. osobu:
1. Pero Perić
2. Janko Janić
Odabir: 2
Odaberite 2. osobu:
1. Pero Perić
2. Janko Janić
Odabir: 2
Odabrana osoba se već nalazi među kontaktiranim osobama. Molimo Vas da
odaberete neku drugu osobu.
Odaberite 2. osobu:
1. Pero Perić
2. Janko Janić
Odabir: 1
Popis osoba:
Ime i prezime: Pero Perić
Starost: 88
Županija prebivališta: GRAD ZAGREB
Zaražen bolešću: Gripa
Kontaktirane osobe:
Nema kontaktiranih osoba.
Ime i prezime: Janko Janić
Starost: 77
Županija prebivališta: MEĐIMURSKA
Zaražen bolešću: Gripa
Kontaktirane osobe:
Pero Perić
Ime i prezime: Marica Ždrerić
Starost: 44
Županija prebivališta: VARAŽDINSKA
Zaražen bolešću: Gripa
Kontaktirane osobe:
Pero Perić
Janko Janić
Od virusa Gripa boluju: Pero Perić, Janko Jankić, Marica Žderić
Najviše zaraženih osoba ima u županiji VARAŽDINSKA: 5%.
Najmanje zaraženih osoba ima u županiji MEĐIMURSKA: 0,5%

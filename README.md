# Masinsko ucenje, pojam, cilj, zadatak, okviri ucenja, faze resavanja problema

**pojam**:

Masinsko ucenje se bavi resavanjem problema za koje je tesko dati formalnu
specifikaciju, ali je dostupna velika kolicina podataka
koji na neki nacin ilustruju resenja pojedinacnih instanci problema.

**zadatak**:

Zadatak masinskog ucenja je da u pruzenim podacima uoce relativne zakonitosti
i da ih formulisu u vidu nekog matematickog modela.

**cilj**:

Cilj masinskog ucenja je kreiranje modela koji ce biti korisni u resavanju
buducih instanci problema.

**faze resavanja problema**:

- Modelovanje problema
- Resavanje problema, odnosno treniranje modela
- Evaluacija dobijenog resenja, odnosno modela

**okviri ucenja**:

- Nadgledano ucenje (supervised learning)
- Nenadgledano ucenje (unsupervised learning)
- Ucenje potkrepljavanjem (reinforcement learning)

# Faze resavanja problema u masinskom ucenju - opis

**Modelovanje problema** je polazni deo procesa masinskog ucenja
i on cesto zahteva najvise znanja i inventivnosti.

- Uocavanje opsteg okvira ucenja adekvatnog za dati problem,
  koji je pre svega uslovljen vrstom informacije datih u
  primerima iz kojih se uci
- Izbor reprezentacije podataka iz kojih se uci
- Izbor forme modela zakonitosti u podacima,
  odnosno skupa dopustivih modela
- Izbor funkcije greske koja meri koliko model odgovara podacima
  na kojima se vrsi trening


# Podaci i karakteristike

**Podaci** su skup objekata i njihovih atributa.

**Atributi** su svojstvo ili karakteristika objekta.

Skup atributa opisuje objekat.

Vrednost atributa su brojevi ili simboli
koji su pridruzeni atributu.

Razlika izmedju atributa i njihovih vrednosti je sto
isti atributi mogu da budu preslikani u razlicite vrednosti atributa

Razliciti atributi mogu da budu preslikani u isti skup vrednosti,
pri cemu osobine vrednosti atributa mogu da budu razlicite.

Diskretni atributi imaju konacan skup vrednosti
(cesto su celi brojevi, a binarni atribudi su specijalan slucaj
diskretnih atributa)

Kontinualni (neprekidni) atributi su realni brojevi.

Asimetricni atributi su binarni atributi kod kojih su bitne ne-nula vrednosti.

**karakteristike podataka**:

- Razliciti formati
- Multidimenzioni format - razlicita polja u podacima odgovaraju
  razlicitim merljivim osobinama koje se nazivaju i karakteristike,
  atributi ili dimenzije
- Medjusobno nezavisni podaci - najcesce multidimenzioni ili tekstualni
- Medjusobno zavisni podaci - implicitna ili eksplicitna zavisnost izmedju podataka 


# Priprema podataka

- Razliciti izvori i formati podataka
- Nedostajuci i nekonzistentni podaci, greske
- Podatke je potrebno pripremiti za proces izstrazivanja podataka

### Preprocesiranje podataka

1. izdvajanje karakteristika
  - izdvajanje karakteristika iz ravnih/nestruktuiranih podataka
  - karakteristika koja se izdvaja zavisi od aplikacije
  - podaci mogu da sadrze heterogene tipove
2. prenosivost tipova podataka
  - neke karakteristike onemogucuju primenu gotovih alata
  - pojedini algoritmi rade samo sa odredjenim tipovima podataka
  - potrebna je promena tipa nekog podataka
  - moguce je gubljenje informacija
  - najcesca transformacija u numericke podatke
3. prenosivost podataka izmedju tipova
  - diskretizacija - neprekidni u kategoricke atribute
  - binarizacija - kategoricki u numericke atribute
  - tekstualni atributi u numericke
  - podaci iz vremenskih serija u diskretne niske
  - podaci iz vremenskih serija u numericke podatke
  - diskretne niske u numericke podatke
4. ciscenje
  1. rad sa nedostajucim podacima
    - razlozi za pojavu
	  - informacije nisu prikupljenje
	  - atributi nisu promenljivi u svim slucajevima
	- rukovanje nedostajucim vrednostima
	  - kompletni slogovi (ceo objekat) koji sadrze takav podatak se brisu
	  - nedostajuca vrednost se procenjuje i unosi (imputacija)
	  - algoritam moze da obradjuje i atribute/slogove sa nedostajucim podacima
	  - zamena sa mogucim vrednostima
  2. rad sa nekorektnim podacima
    - otkrivanje nekonzistentnosti
	- domenskon znanje
	- metoda orijentisana ka podacima
  3. rad sa dupliranim podacima
    - najcesce se javljaju kod spajanja podataka iz heterogenih izvora
	- najcesce se eliminisu iz materijala
  4. skaliranje i normalizacija
    - Transformacija promenljive oznacava transformaciju koja se primenjuje na sve vrednosti te promenljive
	- za svaki objekat, transformacija se primenjuje na vrednost promenljive za taj objekat
	- potreba za normalizacijom - vise atributa koji su razlicito skalirani
5. redukcija podataka
  Manja kolicina podataka - efikasnija primena algoritma
  - agregacija
  - uzimanje uzoraka
  - izbor karakteristika
  - redukcija podataka pomocu rotacije osa
  - ostale metode dimenzione redukcije

# Nadgledano ucenje - modeli i atributi

# Problemi nenadgledanog ucenja - klasifikacija i regresija

# Model funkcija greske i rizik

# Preprilagodjavanje i regularizacija

# Linearni modeli - linearna regresija

# Logisticka regresija

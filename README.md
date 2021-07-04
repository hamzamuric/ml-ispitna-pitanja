---
title: Masinsko ucenje - ispitna pitanja
geometry: margin=2cm
output: pdf_document
---

# Masinsko ucenje, pojam, cilj, zadatak, okviri ucenja, faze resavanja problema

**Pojam**:

Masinsko ucenje se bavi resavanjem problema za koje je tesko dati formalnu
specifikaciju, ali je dostupna velika kolicina podataka
koji na neki nacin ilustruju resenja pojedinacnih instanci problema.

**zadatak**:

Zadatak masinskog ucenja je da u pruzenim podacima uoce relativne zakonitosti
i da ih formulisu u vidu nekog matematickog modela.

**Cilj**:

Cilj masinskog ucenja je kreiranje modela koji ce biti korisni u resavanju
buducih instanci problema.

**Faze resavanja problema**:

- Modelovanje problema
- Resavanje problema, odnosno treniranje modela
- Evaluacija dobijenog resenja, odnosno modela

**Okviri ucenja**:

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

**Karakteristike podataka**:

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

1. Izdvajanje karakteristika
	- izdvajanje karakteristika iz ravnih/nestruktuiranih podataka
	- karakteristika koja se izdvaja zavisi od aplikacije
	- podaci mogu da sadrze heterogene tipove
2. Prenosivost tipova podataka
	- neke karakteristike onemogucuju primenu gotovih alata
	- pojedini algoritmi rade samo sa odredjenim tipovima podataka
	- potrebna je promena tipa nekog podataka
	- moguce je gubljenje informacija
	- najcesca transformacija u numericke podatke
3. Prenosivost podataka izmedju tipova
	- diskretizacija - neprekidni u kategoricke atribute
	- binarizacija - kategoricki u numericke atribute
	- tekstualni atributi u numericke
	- podaci iz vremenskih serija u diskretne niske
	- podaci iz vremenskih serija u numericke podatke
	- diskretne niske u numericke podatke
4. Ciscenje
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
5. Redukcija podataka

  Manja kolicina podataka - efikasnija primena algoritma
	- agregacija
	- uzimanje uzoraka
	- izbor karakteristika
	- redukcija podataka pomocu rotacije osa
	- ostale metode dimenzione redukcije

# Nadgledano ucenje - modeli i atributi

Nadgledano masinsko ucenje karakterise se time da su za sve
unapred raspolozive podatke poznate vrednosti ciljne promenljive.

Svakom ulaznom podatku $x$ je pridruzena zeljena izlazna vrednost $y$
koju algoritam treba da predvidi.

**Atributi**:

U klasicnom masinskom ucenju rucno se specificiraju atributi.
Svaki podatak se predstavlja kao vektor atributa.
Svaki od izabranih atributa moze imati vrednost koja pripada nekom
unapred zadatom skupu. Te vrednosti su nekad numericke a nekad kategoricke.
U dubokom masinskom ucenju, model je u stanju da sam pronadje relevantne odlike.

**Model**:

- potrebno je ustanoviti odnos izmedju atributa $x$ i ciljne promenljive $y$
- problemi koje danas razmatramo su cesto previse kompleksni, stoga se
  pomenuti odnos cesto aproksimira na osnovu uzorka
- zavisnosti izmedju promenljivih se modeluju funkcijom koja se naziva model
- cilj masinskog ucenja je da se dobije model koji ce davati dobre
  rezultate ne samo nad podacima nad kojima je ucenje vrseno
  vec i nad nekim novim podacima. ova sposobnost se zove **generalizacija**

# Problemi nenadgledanog ucenja - klasifikacija i regresija

Standardni problemi nenadgledanog ucenja su
klasifikacija (ciljna promenljiva je kategoricka) i 
regresija (ciljna promenljiva je neprekidna)

**Klasifikacija**:

- klasifikacija se sastoji u razvrstavanju nepoznate instance u jednu
  od unapred ponujenih kategorija (klasa)
- svakoj instanci je pridruzena vrednost klase kao i neke druge osobine.
  problem klasifikacije sastoji se onda u odredjivanju vrednosti klase
  na osnovu preostalih svojstava instance
- ciljna promenljiva ima diskretnu vrednost i nije joj moguce dodeliti
  neku numericku vrednost smisleno. klasa ciju je vrednost potrebno
  odrediti, kategoricko je svojstvo

**Regresija**:

Problem regresije predstavlja problem u kojem pored vrednosti svojstava
svakoj instanci odgovara i neka neprekidna numericka vrednost koju je potrebno predvideti.

# Model funkcija greske i rizik

Matematicke reprezentacije zavisnosti medju promenljivim nazivamo modelima.

Primer linearni model:
$$
f(x) = w_1x_1 + w_2x_2 + w_0
$$

Funkcija greske (loss) je razlika izmedju predvidjenih i
stvarnih vrednosti ciljne promenljive
$$
L(y, f(x))
$$
Nisu sve kombinacije vrednosti atributa i ciljne promenljive
podjednako vazne.

Odnos atributa x i ciljne promenljive y dat je verovatnocom p(x, y).

Vaznija je greska nastala na verovatnijim kombinacijama.

Funkcional rizika (stvarni rizik) R:
$$
R(f) = \int{L(y, f(x))p(x, y)dxdy}
$$

**Minimizacija rizika**:

Problem teorijskog nadgledanog ucenja je pronaci $\displaystyle \min_fR(f)$

Minimizacija po skupu svih funkcija na minimizaciju po skupu svih vrednosti i
parametara: $\displaystyle \min_wR(f_w(x))$ ili $\displaystyle \min_wR(w)$

Usled nedostatka gustine raspodele $p(x, y)$, rizik se zamenjuje empirijskim
rizikom (prosecnom greskom) $$E(w) = \frac{1}{N} \sum_1^NL(y_i, f_w(x))$$.

Minimizacija rizika ce se aproksimirati minimizacijom prosecne greske.

**Minimizacija greske u slucaju regresije**:

Jednoj vrednosti atributa u modelu ne mora uvek da odgovara jedna ciljna vrednost.
Moze se izabrati prosecna vrednost.

Regresiona funkcija $r(f) = \int yp(y|x)dy$

Ako vazi $r(x)=f_w(x)$ za neko $w$, tada se funkcija greske moze racunati
$$L(y, f_w(x)) = (f_w(x) - y)$$

Minimizacija greske
$$\displaystyle \min_w\frac{1}{N}\sum_1^N(y_i - f_w(x))^2$$

**Minimizacija greske u slucaju klasifikacije**:

Model je bolji ukoliko pravi manje greske pri klasifikaciji.

Indikatorska funkcija
$$
I(f) = \left\{
	\begin{array}{l}
	1, \text{ako vazi} f\\
	0, \text{ako ne vazi} f
	\end{array}
\right.
$$

Minimizacija greske
$$\displaystyle \min_w\frac{1}{N}\sum_1^NI(y_i\ne f_w(x))$$

# Preprilagodjavanje i regularizacija

**Preprilagodjavanje**:

Dobra prilagodjenost modela trening podacima ne obezbedjuje dobru regularizaciju.

Uzrok problema je prevelika prilagodljivost modela.

Osnovna prepreka dobroj aproksimaciji optimalnih vrednosti parametara,
a time i uspesnoj generalizaciji je preterano bogatstvo skupa dopustivi modela.

Sto je skup dostupnih modela bogatiji, to je potrebno vise podataka za uspesno ucenje.

Ogranicavanje bogatstva skupa dopustivih modela (linearni model).

Modifikovati funkciju koja minimizuje tako da veliki broj modela
ima visoku vrednost te funkcije.

**Regularizacija**:

Siromasan skup funkcija mozda ne sadrzi model sa malom prosecnom greskom
pa nema ni dobre generalizacije.

Bogat skup funkcija sadrzi model koji dobro generalizuje ali ga je tesko pronaci.

Zato se umesto minimizacije greske vrzi minimizacija regularizovane greske.
$$\displaystyle \min_w\frac{1}{N}\sum_1^NL(y_i, f_w(x_i))+\lambda \Omega (w)$$

Regularizacioni izraz $\Omega(w)$:
$$\Omega(w) = \parallel w\parallel_2^2 = \sum_{i=1}^Nw_i^2$$

Regularizacioni parametar $\lambda$.

Regularizacioni izraz kaznjava visoke apsolutne vrednosti parametara,
cineci model manje prilagodljivim.

Regularizacioni parametar sluzi za podesavanje prilagodljivosti modela.

Regularizacijom se naziva bilo koja modifikacija optimizacionog problema
koja ogranicava prilagodljivost modela i cini ga manje podloznim preprilagodjavanju.

# Linearni modeli - linearna regresija

Pretpostavka: Veza izmedju svojstva i ciljne promenljive se modeluje linearnim modelom
uz neku nelinearnu transformaciju:
$$f_w(x) = g(wx) = g(\sum_{i = 1}{k}w_ik_i)$$

Funkcija $g$ zavisi od konkretne primene.

**Linearna regresija**:

Linearna regresija predstavlja jedan od najjednostavnijih i najcesce
koriscenih modela masinskog ucenja.

Kod nje ne postoji transformacija to jeste $g = 1$.

$$f_w(x) = wx = \sum_{i = 1}{k}w_ix_i$$

Zadatak linearne regresije je odredjivanje vrednosti parametara $w$
koji najbolje odgovaraju trening podacima, tj. najbolje odgovaraju opazanjima iz iskustva.

Dizajn algoritama **probabilistickih** modela masinskog ucenja se zasniva
na definisanju raspodele verovatnoce koju je potrebno oceniti iz podataka.

**Linearni modeli**:

Linearna regresija je korisna i za ustanovljavanje jaine uticaja
nekog svojstva na vrednost ciljne promenljive.
Vece apsolutne vrednosti koeficijenta $w_i$ oznacavaju jaci uticaj
svojstva $x_i$ uz koji stoje.

Prilikom ocene parametara probabilistickih modela, tipicno se koristi
metod maksimalne verodostojnosti. Potrebno je odrediti parametre za koje
su dostupni podaci najverovatniji.

# Logisticka regresija

Dok linearna regresija predstavlja regresioni model,
logisticka regresija, uprkos svom nazivu, predstavlja model binarne klasifikacije.

$y \in {0, 1}$, sa diskretnom funkcijom raspodele $p(x|y)$:
$$p(x|y)=\left\{
\begin{array}{l}
\mu, y = 1\\
1 - \mu, y = 0
\end{array}
\right.$$

Cilj je modelovanje ove verovatnoce
$$p(y=1|x)=f_w(x),p(y=0|x)=1 - f_w(x)$$
$$p(y|x) = f_w(x)^y(1 - f_w(x))^{1 - y}$$



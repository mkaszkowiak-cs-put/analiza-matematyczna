Markdown jest dostosowany pod [Obsidian](https://obsidian.md/), więc w podglądzie Githuba część rzeczy może się psuć

---

### Granice
Granica w punkcie istnieje, gdy granice obustronne sa sobie rowne

#### 1^oo
lim n->oo (1+1/n)^n = e

#### 0/0
**lim x->0**
arc/sin/h oraz arc/tan/h:
 sinx / x = 1 

(e^x - 1) / x --> 1
(a^x - 1) / x --> ln a

#### oo - oo
Wspólny czynnik, przed nawias, delopital

### Pochodne
f'(x0) = lim d->0 (f(x0 + d) - f(x0)) / d

![[X Pochodne.png]]

#### Przybliżanie różniczką
f(x0 + dx) ~= f(x0) + dx \* f'(x0)

#### Asymptoty
Asymptoty pionowe x = a: 
lim x->a f(x) = +-oo

Asymptota ukośna y = Ax + B
lim x->+-oo f(x) - Ax - B = 0

Aby znaleźć współczynniki:
A = lim x->+-oo f(x) / x
B = lim x->+-oo f(x) - Ax

#### Taylor i Maclaurin
![[X Taylor i Maclaurin.png]]

#### Ekstrema lokalne
f'(x) = 0 => ekstremum lokalne

f'(x) = 0 oraz f''(x) > 0 => minimum lokalne
f'(x) = 0 oraz f''(x) < 0 => maksimum lokalne

#### Wypukłość i wklęsłość
f''(x) > 0 => wypukła w X
f''(x) < 0 => wklęsła w X

przykład funkcji wypukłej: x^2

f''(x) = 0 => punkt przegięcia

#### Schemat badania funkcji
- dziedzina
- granice na końcu dziedziny
- asymptoty
- punkty stacjonarne, ekstrema, przedziały monotoniczności
- tabela zmienności funkcji

### Całki nieoznaczone

#### Podstawienia Eulera
Dla całek postaci 1/sqrt(ax2 + bx + c)

A>0: sqrt() = t + sqrt(a)x 
C>0: sqrt() = tx + sqrt(c)

#### Przez rozkład na ułamki proste
Piszę aby pamiętać że istnieje

#### Metoda współczynników nieoznaczonych
Calka z Wn(x)/sqrt(ax2+bx+c) = Wn-1(x)sqrt(...) + A\*calka z 1/sqrt(...)

Następnie obustronna pochodna 
Wn-1(x) to po prostu np Ax+B bez podstawiania pod współczynniki 

#### Podstawienia trygonometryczne 
$tg \frac{x}{2} = t$ 
$tg x = t$

#### Wzory 
$\int \frac{1}{x^2 + a^2}dx = \frac{1}{a} * arctg(\frac{x}{a})$
$\int \frac{1}{\sqrt{a^2 + x^2}}dx = ln|x + \sqrt{a^2 + x^2}| + C$
$\int \frac{1}{\sqrt{a^2 - x^2}}dx = arcsin \frac{x}{a} + C$

##### Długość łuku 
$L = \int \sqrt{1 + f'(x)^2}dx$

##### Obrót dookoła Ox
$V = \pi * \int_a^b f(x)^2dx$
$Pp = 2\pi * \int_a^b f(x) * \sqrt{1 + f'(x)^2}dx$

##### Obrót dookoła Oy
$V = 2\pi * \int_a^b x*f(x)dx$
$Pp = 2\pi * \int_a^b x * \sqrt{1 + f'(x)^2}dx$

### Szeregi liczbowe
Warunek konieczny zbieżności szeregu:
$\lim_{n \to \infty} a_n = 0$

#### Dla szeregów o wyrazach nieujemnych (>= 0):

##### Kryterium d'Alemberta
$\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = g$
szereg jest zbieżny gdy g < 1, rozbieżny dla g > 1, nie wiadomo i należy zbadać dla g == 1

##### Kryterium Cauchy'ego
$\lim_{n \to \infty} \sqrt[n]{a_n} = g$
szereg jest zbieżny gdy g < 1, rozbieżny dla g > 1, nie wiadomo i należy zbadać dla g == 1

##### Kryterium porównawcze
Tworzymy drugi szereg (b\_n) o wyrazach mniejszych lub większych.

Jeśli b\_n > a\_n oraz b\_n jest zbieżny, to a\_n również jest zbieżny.
Jeśli b\_n < a\_n oraz b\_n jest rozbieżny, to a\_n również jest rozbieżny.

##### Kryterium całkowe
**Funkcja musi być nierosnąca!**

szereg  $\sum_{n_0}^{\infty} f(n)$ jest zbieżny wtedy, i tylko wtedy, gdy całka$\int_{n_0}^{\infty} f(x)dx$ jest zbieżna.

##### DEFINICJA: Szereg Dirichleta
Szereg z wyrazami postaci 1/n^p. Jest zbieżny dla p > 1, natomiast rozbieżny dla p <= 1.

#### Dla szeregów o wyrazach dowolnych

##### Kryterium bezwzględne
Jeśli szereg abs(a\_n) jest zbieżny, to szereg a\_n jest również zbieżny. 

##### Kryterium Leibniza
Jeśli szereg naprzemienny:
- a\_n > 0 (a_n dodatnie)
- a\_n >= a\_(n+1) (a_n nierosnące)
- lim n->oo a\_n = 0 (spełnione kryterium zbieżności)

Wówczas szereg naprzemienny jest zbieżny.
Zachodzi również nierówność przydatna do oszacowania błędu bezwględnego:

abs(S - S\_n) <= a\_(n+1)

##### DEFINICJA: Szereg naprzemienny
Szeregiem naprzemiennym nazywamy szereg postaci
(-1)^(n+1) \* a\_n, gdzie a\_n > 0.

##### DEFINICJA: Zbieżność bezwzględna i warunkowa
Szereg a\_n nazywamy bezwzględnie zbieżnym, jeśli szereg abs(a\_n) jest zbieżny.

Szereg zbieżny a\_n nazywamy warunkowo zbieżnym, jeśli szereg abs(a\_n) jest rozbieżny.

### Szeregi potęgowe

##### DEFINICJA: Szereg potęgowy
Szeregiem potęgowym nazywamy szereg o postaci:
$\sum_{n=0}^{\infty} a_n * (x - x_0)^n$

##### DEFINICJA: Promień zbieżności
Promieniem zbieżności szeregu potęgowego nazywamy największy bezwzględny X, dla którego szereg jest zbieżny.

Można obliczyć promień jednym ze wzorów:
1. $r = \lim_{n \to \infty} |\frac{a_n}{a_n + 1}|$
2. $r = lim_{n \to \infty} \frac{1}{\sqrt[n]{|a_n|}}$
Uwaga: To są odwrócone wzory z kryterium d'Alemberta i Cauchy'ego (z dodatkową wartością bezwzględną).

##### DEFINICJA: Przedział zbieżności
Przedziałem zbieżności nazywamy zbiór x, dla których szereg jest zbieżny. 

Szereg jest zbieżny w każdym punkcie otwartego przedziału (x\_0 - r, x\_0 + r). Krańce przedziału należy dodatkowo zbadać.

### Funkcje dwóch zmiennych
Pochodne drugiego stopnia zapisujemy jako d^2f/dx^2, czyli delta do potęgi wyłącznie przy funkcji.

d^2f/dxdy oznacza że dx jest liczone z dy - tj. najpierw obliczamy dy.

d2f/dxdy == d2f/dydx - są wyjątki, ale działa dla wszystkich przypadków na egzaminie z analizy.


#### Różniczka dwóch zmiennych
Przybliżanie:

f(x0 + dx, y0 + dy) ~= f(x0, y0) + df/dx(x0, y0) \* dx + df/dy(x0, y0) \* dy

Czyli analogiczny schemat = funkcja w x+delta ma aproksymacyjnie f(x) + delta razy tempo wzrostu w x

#### Ekstremum lokalne
1. Pochodne cząstkowe df/dx i df/dy muszą być równe 0 w punkcie x0, y0.
2. Wyznacznik macierzy musi być > 0. 
Na głównej przekątnej leżą df/dx^2 oraz df/dy^2.
Na drugiej przekątnej leżą df/dxdy.

Jeśli tak jest, istnieje ekstremum lokalne.
Maksimum dla df/dx^2 > 0, minimum dla < 0.



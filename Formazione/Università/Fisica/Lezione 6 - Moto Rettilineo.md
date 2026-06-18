# Moto di un proiettile

## Definizione

Il **moto di un proiettile** è un caso particolare di **moto in un piano**.

Un proiettile è un corpo lanciato con una velocità iniziale che possiede almeno una componente orizzontale.

Il moto del proiettile fu studiato da **Galileo**.

Nel caso generale, un proiettile può essere lanciato con una certa inclinazione rispetto al terreno.

In questa parte studiamo il caso più semplice:

> proiettile lanciato orizzontalmente da un'altezza $h$, con velocità iniziale orizzontale $v_0$.

---

# Lancio orizzontale

## Caratteristiche principali

Nel **lancio orizzontale**, il corpo parte con velocità solo orizzontale.

Quindi all'inizio:

$$
v_x = v_0
$$

$$
v_y = 0
$$

Il moto va separato in due direzioni:

- lungo l'asse $x$: moto rettilineo uniforme;
- lungo l'asse $y$: moto uniformemente accelerato per effetto della gravità.

---

# Moto lungo l'asse x

Lungo l'asse orizzontale non agisce accelerazione.

Quindi:

$$
a_x = 0
$$

La velocità orizzontale resta costante:

$$
v_x = v_0
$$

La legge oraria lungo $x$ è:

$$
x = x_0 + v_0t
$$

Se scegliamo l'origine nel punto di lancio:

$$
x_0 = 0
$$

allora:

$$
x = v_0t
$$

Da questa formula possiamo ricavare il tempo:

$$
t = \frac{x}{v_0}
$$

---

# Moto lungo l'asse y

Lungo l'asse verticale agisce l'accelerazione di gravità.

Se scegliamo il verso positivo verso il basso, allora:

$$
a_y = g
$$

La posizione verticale è:

$$
y = \frac{1}{2}gt^2
$$

Questa formula indica lo spazio verticale percorso durante la caduta.

Se invece scegliamo il verso positivo verso l'alto, allora:

$$
a_y = -g
$$

e la legge oraria diventa:

$$
y = y_0 - \frac{1}{2}gt^2
$$

> [!important]
> Il segno di $g$ dipende dal verso scelto per l'asse verticale.
>
> Se il basso è positivo:
>
> $$
> y = \frac{1}{2}gt^2
> $$
>
> Se l'alto è positivo:
>
> $$
> y = y_0 - \frac{1}{2}gt^2
> $$

---

# Traiettoria del proiettile

Nel lancio orizzontale abbiamo:

$$
x = v_0t
$$

e:

$$
y = \frac{1}{2}gt^2
$$

Dalla prima formula ricaviamo il tempo:

$$
t = \frac{x}{v_0}
$$

Sostituiamo questo valore nella formula di $y$:

$$
y = \frac{1}{2}g\left(\frac{x}{v_0}\right)^2
$$

quindi:

$$
y = \frac{1}{2}g\frac{x^2}{v_0^2}
$$

Questa è l'equazione della traiettoria.

> [!important]
> La traiettoria del proiettile è una parabola.
>
> Per questo si parla di **moto parabolico**.

---

# Tempo di caduta da un'altezza h

Se il proiettile parte da un'altezza $h$, il tempo di caduta si ricava dal moto verticale.

Usiamo:

$$
h = \frac{1}{2}gt^2
$$

Ricaviamo $t$:

$$
2h = gt^2
$$

$$
t^2 = \frac{2h}{g}
$$

$$
t = \sqrt{\frac{2h}{g}}
$$

> [!important]
> Il tempo di caduta dipende solo dall'altezza $h$ e dalla gravità $g$.
>
> Non dipende dalla velocità orizzontale $v_0$.

---

# Gittata

La **gittata** è la distanza orizzontale percorsa dal proiettile prima di toccare terra.

Lungo l'asse $x$ vale:

$$
x = v_0t
$$

Sostituendo il tempo di caduta:

$$
t = \sqrt{\frac{2h}{g}}
$$

otteniamo:

$$
x_g = v_0 \sqrt{\frac{2h}{g}}
$$

dove:

- $x_g$ è la gittata;
- $v_0$ è la velocità iniziale orizzontale;
- $h$ è l'altezza iniziale;
- $g$ è l'accelerazione di gravità.

---

# Velocità all'impatto

Durante il moto, la velocità orizzontale resta costante:

$$
v_x = v_0
$$

La velocità verticale aumenta per effetto della gravità:

$$
v_y = gt
$$

Se il verso positivo è verso l'alto, allora:

$$
v_y = -gt
$$

La velocità totale all'impatto si calcola con Pitagora:

$$
v = \sqrt{v_x^2 + v_y^2}
$$

quindi:

$$
v = \sqrt{v_0^2 + (gt)^2}
$$

---

# Angolo di impatto

L'angolo con cui il proiettile arriva al suolo si calcola usando le componenti della velocità.

La tangente dell'angolo è:

$$
\tan\phi = \frac{v_y}{v_x}
$$

quindi:

$$
\phi = \arctan\left(\frac{v_y}{v_x}\right)
$$

Se il proiettile sta scendendo e scegliamo l'asse $y$ positivo verso l'alto, allora $v_y$ è negativa.

In quel caso:

$$
\phi < 0
$$

Il segno negativo indica che l'angolo è rivolto verso il basso rispetto all'orizzontale.

---

# Schema per risolvere gli esercizi

## 1. Scrivere i dati

Di solito vengono dati:

$$
h
$$

$$
v_0
$$

$$
g = 9.8 \ m/s^2
$$

oppure:

$$
g = 9.81 \ m/s^2
$$

---

## 2. Separare il moto

Asse $x$:

$$
v_x = v_0
$$

$$
a_x = 0
$$

Asse $y$:

$$
v_y = gt
$$

$$
a_y = g
$$

oppure, con asse positivo verso l'alto:

$$
v_y = -gt
$$

$$
a_y = -g
$$

---

## 3. Calcolare il tempo di caduta

$$
t = \sqrt{\frac{2h}{g}}
$$

---

## 4. Calcolare la gittata

$$
x_g = v_0t
$$

oppure direttamente:

$$
x_g = v_0\sqrt{\frac{2h}{g}}
$$

---

## 5. Calcolare la velocità verticale finale

$$
v_y = gt
$$

oppure:

$$
v_y = -gt
$$

a seconda del verso scelto.

---

## 6. Calcolare la velocità totale finale

$$
v = \sqrt{v_x^2 + v_y^2}
$$

---

## 7. Calcolare l'angolo di impatto

$$
\phi = \arctan\left(\frac{v_y}{v_x}\right)
$$

---

# Formule da ricordare

## Moto orizzontale

$$
x = v_0t
$$

$$
t = \frac{x}{v_0}
$$

---

## Moto verticale

$$
y = \frac{1}{2}gt^2
$$

---

## Traiettoria

$$
y = \frac{1}{2}g\left(\frac{x}{v_0}\right)^2
$$

oppure:

$$
y = \frac{1}{2}g\frac{x^2}{v_0^2}
$$

---

## Tempo di caduta

$$
t = \sqrt{\frac{2h}{g}}
$$

---

## Gittata

$$
x_g = v_0t
$$

oppure:

$$
x_g = v_0\sqrt{\frac{2h}{g}}
$$

---

## Velocità verticale

$$
v_y = gt
$$

oppure:

$$
v_y = -gt
$$

---

## Velocità totale

$$
v = \sqrt{v_x^2 + v_y^2}
$$

---

## Angolo di impatto

$$
\phi = \arctan\left(\frac{v_y}{v_x}\right)
$$

---

# Collegamento con gli esercizi precedenti

Negli esercizi visti prima si usano proprio queste formule.

## Esercizio con $h = 100 \ m$ e $v_0 = 50 \ m/s$

Tempo di caduta:

$$
t = \sqrt{\frac{2h}{g}}
$$

$$
t = \sqrt{\frac{2 \cdot 100}{9.8}}
$$

$$
t \approx 4.5 \ s
$$

Velocità verticale finale:

$$
v_y = -gt
$$

$$
v_y = -9.8 \cdot 4.5
$$

$$
v_y \approx -44 \ m/s
$$

Angolo di impatto:

$$
\phi = \arctan\left(\frac{-44}{50}\right)
$$

$$
\phi \approx -41^\circ
$$

Quindi il proiettile arriva con inclinazione di circa:

$$
\boxed{41^\circ}
$$

sotto l'orizzontale.

---

## Esercizio con $h = 25 \ m$ e $v_0 = 200 \ m/s$

Tempo di caduta:

$$
t = \sqrt{\frac{2h}{g}}
$$

$$
t = \sqrt{\frac{2 \cdot 25}{9.81}}
$$

$$
t \approx 2.26 \ s
$$

Gittata:

$$
x_g = v_0t
$$

$$
x_g = 200 \cdot 2.26
$$

$$
x_g \approx 452 \ m
$$

Velocità verticale finale:

$$
v_y = gt
$$

$$
v_y = 9.81 \cdot 2.26
$$

$$
v_y \approx 22.15 \ m/s
$$

Velocità totale finale:

$$
v = \sqrt{v_x^2 + v_y^2}
$$

$$
v = \sqrt{200^2 + 22.15^2}
$$

$$
v \approx 201.22 \ m/s
$$

Quindi:

$$
\boxed{x_g \approx 452 \ m}
$$

$$
\boxed{v \approx 201.22 \ m/s}
$$

---

# Riassunto rapido

Nel moto di un proiettile lanciato orizzontalmente:

- il moto orizzontale è uniforme;
- il moto verticale è uniformemente accelerato;
- la traiettoria è una parabola;
- il tempo di caduta dipende solo dall'altezza;
- la gittata dipende sia dall'altezza sia dalla velocità iniziale;
- la velocità finale si calcola componendo $v_x$ e $v_y$.

La formula più importante è:

$$
t = \sqrt{\frac{2h}{g}}
$$

perché da questa si ricavano quasi tutti gli altri risultati.


# Quiz fisica - Cinematica

## 1. Velocità media

Formula:

$$
v = \frac{s}{t}
$$

Se il risultato è in m/s e serve in km/h:

$$
km/h = m/s \cdot 3.6
$$

### Esempio

Carl Lewis percorre 188 m in 15 s.

$$
v = \frac{188}{15} = 12.53 \ m/s
$$

$$
12.53 \cdot 3.6 = 45.12 \ km/h
$$

Risposta:

$$
\boxed{45.12 \ km/h}
$$

---

## 2. Lancio verticale verso l’alto

Formula utile:

$$
v^2 = v_0^2 - 2gh
$$

Si usa quando un corpo viene lanciato verso l’alto e voglio sapere la velocità a una certa altezza.

### Esempio

Palla lanciata con:

$$
v_0 = 35 \ m/s
$$

alla quota:

$$
h = 30 \ m
$$

$$
v^2 = 35^2 - 2 \cdot 9.8 \cdot 30
$$

$$
v^2 = 1225 - 588 = 637
$$

$$
v = \sqrt{637} = 25.2 \ m/s
$$

Risposta:

$$
\boxed{25.2 \ m/s}
$$

> La massa non serve.

---

## 3. Velocità iniziale per raggiungere un’altezza

Nel punto più alto:

$$
v = 0
$$

Formula:

$$
v_0 = \sqrt{2gh}
$$

### Esempio

Altezza massima:

$$
h = 50 \ m
$$

$$
v_0 = \sqrt{2 \cdot 9.8 \cdot 50}
$$

$$
v_0 = \sqrt{980} = 31.3 \ m/s
$$

Risposta:

$$
\boxed{31.3 \ m/s}
$$

---

## 4. Caduta libera da ferma

Se un corpo viene lasciato cadere:

$$
v_0 = 0
$$

Formula:

$$
h = \frac{1}{2}gt^2
$$

### Esempio

Tempo di caduta:

$$
t = 5.5 \ s
$$

$$
h = \frac{1}{2} \cdot 9.8 \cdot 5.5^2
$$

$$
h = 4.9 \cdot 30.25 = 148.2 \ m
$$

Risposta:

$$
\boxed{148 \ m}
$$

---

## 5. Accelerazione media

Formula:
$$
a = \frac{\Delta v}{\Delta t}
$$
Prima di calcolare, se le velocità sono in km/h, convertirle in m/s:
$$
m/s = \frac{km/h}{3.6}
$$
### Esempio

Velocità da 54 km/h a 108 km/h in 20 s.

$$
54 \ km/h = 15 \ m/s
$$

$$
108 \ km/h = 30 \ m/s
$$

$$
\Delta v = 30 - 15 = 15 \ m/s
$$

$$
a = \frac{15}{20} = 0.75 \ m/s^2
$$

Risposta:

$$
\boxed{0.75 \ m/s^2}
$$

---

## 6. Moto uniforme

Nel moto uniforme la velocità è costante.

Formula:

$$
s = vt
$$

Le distanze percorse sono proporzionali agli intervalli di tempo.

### Esempio

Treno a 300 km/h per 15 minuti.

Convertiamo il tempo in ore:

$$
15 \ min = \frac{15}{60} = 0.25 \ h
$$

$$
s = 300 \cdot 0.25 = 75 \ km
$$

Risposta:

$$
\boxed{75 \ km}
$$

---

## 7. Definizione di moto uniforme

Si ha moto uniforme se:

$$
v = costante
$$

quindi:

$$
s = vt
$$

Risposta corretta:

$$
\boxed{\text{Le distanze percorse sono proporzionali agli intervalli di tempo}}
$$

---

## 8. Newton

Il Newton, simbolo:

$$
N
$$

è l’unità di misura della forza.

Formula:

$$
F = ma
$$

Unità:

$$
1N = 1kg \cdot \frac{m}{s^2}
$$

Risposta corretta:

$$
\boxed{\text{È l’unità di misura della forza}}
$$

---

# Formule da ricordare

## Velocità

$$
v = \frac{s}{t}
$$

## Spazio nel moto uniforme

$$
s = vt
$$

## Accelerazione media

$$
a = \frac{\Delta v}{\Delta t}
$$

## Caduta libera

$$
h = \frac{1}{2}gt^2
$$

## Lancio verticale

$$
v^2 = v_0^2 - 2gh
$$

## Velocità iniziale per arrivare a quota h

$$
v_0 = \sqrt{2gh}
$$

## Conversioni

$$
km/h \div 3.6 = m/s
$$

$$
m/s \cdot 3.6 = km/h
$$

## Gravità

$$
g = 9.8 \ m/s^2
$$
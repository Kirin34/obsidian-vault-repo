## Punti di equilibrio

In questa lezione si studiano sistemi dinamici in cui può comparire un **moto armonico semplice**, in particolare:

- corpo collegato a una **molla** su piano orizzontale senza attrito;
- **pendolo semplice**.

Un corpo è in equilibrio quando, se lasciato fermo in quella posizione, non tende a muoversi.

Le posizioni di equilibrio possono essere:

### Equilibrio stabile
Se il corpo viene spostato di poco, tende a tornare verso la posizione iniziale.

Esempio: corpo attaccato a una molla vicino alla posizione di riposo.

### Equilibrio indifferente
Se il corpo viene spostato di poco, resta nella nuova posizione.

### Equilibrio instabile
Se il corpo viene spostato di poco, tende ad allontanarsi sempre di più dalla posizione iniziale.

---

## Legge di Hooke

Consideriamo un blocco su un piano orizzontale senza attrito, collegato a una molla fissata a una parete.

La molla ha una posizione di riposo, cioè una posizione in cui non è né compressa né allungata.

Se la molla viene deformata, esercita sul corpo una **forza elastica** che tende a riportarlo verso l’equilibrio.

La forza elastica segue la **legge di Hooke**:

$$
F = -kx
$$

dove:

- $F$ è la forza elastica;
- $k$ è la costante elastica della molla;
- $x$ è lo spostamento dalla posizione di equilibrio;
- il segno meno indica che la forza è sempre opposta allo spostamento.

Più grande è $k$, più la molla è rigida.

---

## Forza elastica e moto armonico

Applicando la seconda legge di Newton:

$$
F = ma
$$

e sapendo che:

$$
F = -kx
$$

si ottiene:

$$
m \frac{d^2x}{dt^2} = -kx
$$

## Pendolo semplice

Il **pendolo semplice** è formato da una massa appesa a un filo inestensibile di lunghezza $l$, fissato in alto.

La posizione verticale verso il basso è una posizione di **equilibrio stabile**: se la massa viene spostata di poco, tende a tornare verso il basso e inizia a oscillare.

Le forze agenti sono:

- il **peso** $mg$, diretto verso il basso;
- la **tensione** del filo $\tau$, diretta lungo il filo.

Si scompone il moto in:

- direzione **tangenziale**, responsabile dell’oscillazione;
- direzione **normale/radiale**, legata alla tensione del filo.

La componente tangenziale della forza peso è:

$$
F_T = ma_T = -mg \sin \theta
$$

Poiché lo spostamento lungo l’arco è:

$$
s = l\theta
$$

allora:

$$
a_T = l \frac{d^2\theta}{dt^2}
$$

Quindi:

$$
ml\frac{d^2\theta}{dt^2} = -mg\sin\theta
$$

---

## Piccole oscillazioni

Per piccoli angoli vale l’approssimazione:

$$
\sin\theta \approx \theta
$$

quindi l’equazione diventa:

$$
\frac{d^2\theta}{dt^2} = -\frac{g}{l}\theta
$$

Questa è l’equazione di un **moto armonico semplice**.

La soluzione è:

$$
\theta(t) = \theta_0 \cos(\omega t + \varphi)
$$

dove:

$$
\omega = \sqrt{\frac{g}{l}}
$$

Quindi il pendolo semplice, per piccole oscillazioni, si comporta come un oscillatore armonico.

---

## Periodo del pendolo

Il periodo del pendolo semplice è:

$$
T = 2\pi \sqrt{\frac{l}{g}}
$$

Il periodo:

- dipende dalla lunghezza del filo $l$;
- dipende dall’accelerazione di gravità $g$;
- **non dipende dalla massa** del corpo.

Un filo più lungo produce oscillazioni più lente, quindi periodo maggiore.

---

## Stima di $g$ tramite il pendolo

Dato che:

$$
T = 2\pi \sqrt{\frac{l}{g}}
$$

si può ricavare $g$ misurando il periodo $T$ e la lunghezza $l$:

$$
g = \frac{4\pi^2 l}{T^2}
$$

Quindi il pendolo può essere usato sperimentalmente per stimare l’accelerazione di gravità.

---

## Velocità e tensione massima

La velocità del pendolo è massima nel punto più basso della traiettoria, cioè quando:

$$
\theta = 0
$$

In quel punto anche la tensione del filo è massima, perché alla tensione deve contribuire anche la forza centripeta necessaria al moto curvilineo.

La tensione massima è:

$$
\tau_{max} = mg + m\frac{v^2}{l}
$$

Per piccole oscillazioni si può scrivere circa:

$$
\tau_{max} = mg(1+\theta_0^2)
$$

dove $\theta_0$ è l’ampiezza angolare iniziale.

## Esercizi - Pendolo e molla

### Esercizio 1: pendolo semplice

Un pendolo ha massa:

$$
m = 60.0\,g
$$

e angolo descritto da:

$$
\theta(t) = (0.0800\,rad)\cos[(4.43\,rad/s)t+\phi]
$$

Quindi:

$$
\theta_0 = 0.0800\,rad
$$

$$
\omega = 4.43\,rad/s
$$

Per il pendolo semplice:

$$
\omega = \sqrt{\frac{g}{l}}
$$

Da cui:

$$
l = \frac{g}{\omega^2}
$$

Sostituendo:

$$
l = \frac{9.8}{(4.43)^2} \approx 0.50\,m
$$

La velocità massima si ha nel punto più basso della traiettoria:

$$
v_{max} = \omega l \theta_0
$$

quindi:

$$
v_{max} = 4.43 \cdot 0.50 \cdot 0.0800 \approx 0.177\,m/s
$$

Risultati:

$$
l \approx 0.50\,m
$$

$$
v_{max} \approx 0.177\,m/s
$$

---

### Esercizio 2: molla verticale

Una molla verticale si allunga di:

$$
\Delta y = 9.6\,cm = 0.096\,m
$$

quando viene appesa una massa:

$$
m = 1.3\,kg
$$

Nel nuovo equilibrio vale:

$$
k\Delta y = mg
$$

quindi:

$$
k = \frac{mg}{\Delta y}
$$

Sostituendo:

$$
k = \frac{1.3 \cdot 9.8}{0.096} \approx 132.7\,N/m
$$

Se il corpo viene tirato verso il basso di altri:

$$
A = 5.0\,cm = 0.05\,m
$$

e lasciato da fermo, il moto è armonico attorno alla nuova posizione di equilibrio.

La pulsazione è:

$$
\omega = \sqrt{\frac{k}{m}}
$$

Il periodo è:

$$
T = 2\pi \sqrt{\frac{m}{k}}
$$

Sostituendo:

$$
T \approx 0.62\,s
$$

La frequenza è:

$$
f = \frac{1}{T}
$$

quindi:

$$
f \approx 1.6\,Hz
$$

La velocità massima è:

$$
v_{max} = \omega A
$$

quindi:

$$
v_{max} \approx 0.51\,m/s
$$

Risultati:

$$
k = 132.7\,N/m
$$

$$
T = 0.62\,s
$$

$$
f = 1.6\,Hz
$$

$$
A = 0.05\,m
$$

$$
v_{max} = 0.51\,m/s
$$

---

## Quesiti finali

### Q1. Legge di Hooke

La forza elastica è:

$$
F = -kx
$$

dove:

- $k$ è la costante elastica;
- $x$ è lo spostamento dalla posizione di riposo;
- il segno meno indica che la forza è opposta allo spostamento.

---

### Q2. Periodo massa-molla

Per una massa $m$ collegata a una molla di costante elastica $k$:

$$
T = 2\pi \sqrt{\frac{m}{k}}
$$

Il periodo aumenta se aumenta la massa e diminuisce se aumenta la rigidità della molla.

---

### Q3. Periodo del pendolo semplice

Per un pendolo di lunghezza $l$:

$$
T = 2\pi \sqrt{\frac{l}{g}}
$$

Il periodo dipende dalla lunghezza del filo e da $g$, ma non dalla massa.
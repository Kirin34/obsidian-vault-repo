# Lezione 11 — Le leggi della dinamica: esempi di forze

In questa lezione si applicano le leggi della dinamica a casi pratici, analizzando le forze che agiscono su un corpo. In particolare si studiano il **piano inclinato**, la **tensione di un filo** e la **macchina di Atwood**. L’obiettivo è capire come scomporre le forze e scrivere correttamente le equazioni del moto.

## Piano inclinato

Il piano inclinato è un sistema classico usato per studiare il moto di un corpo soggetto alla forza peso. Si considera un corpo di massa `m` che scivola senza attrito su un piano inclinato di angolo `θ`.

La forza peso è:

$$
F_g = mg
$$

Questa forza viene scomposta in due componenti:

- una componente **parallela al piano**, che fa scivolare il corpo;
- una componente **perpendicolare al piano**, che viene bilanciata dalla reazione normale.

Le componenti della forza peso sono:

$$
F_{g,\parallel} = F_g \sin \theta = mg \sin \theta
$$

$$
F_{g,\perp} = -F_g \cos \theta = -mg \cos \theta
$$

Il segno meno indica che la componente perpendicolare della forza peso è diretta verso il piano.


![[Pasted image 20260618233918.png]]

## Reazione normale

Sul corpo agisce anche la reazione vincolare del piano, detta **forza normale**:

$$
F_N
$$

Poiché il corpo non si muove nella direzione perpendicolare al piano, in quella direzione l’accelerazione è nulla. Quindi:

$$
-F_g \cos \theta + F_N = 0
$$

Da cui:

$$
F_N = F_g \cos \theta = mg \cos \theta
$$

La forza normale quindi non è sempre uguale a `mg`, ma dipende dall’inclinazione del piano.

## Moto lungo il piano inclinato

L’unica forza che produce movimento lungo il piano è la componente parallela della forza peso:

$$
F_{g,\parallel} = mg \sin \theta
$$

Applicando la seconda legge della dinamica:

$$
F = ma
$$

si ottiene:

$$
mg \sin \theta = ma
$$

semplificando la massa:

$$
a = g \sin \theta
$$

Quindi l’accelerazione del corpo lungo il piano inclinato dipende solo da `g` e dall’angolo `θ`.

## Legge oraria nel sistema cartesiano

Se il moto viene studiato con assi cartesiani orizzontale `x` e verticale `y`, l’accelerazione lungo il piano può essere scomposta nelle due direzioni.

Dato che:

$$
a = g \sin \theta
$$

le componenti dell’accelerazione sono:

$$
a_x = g \sin \theta \cos \theta
$$

$$
a_y = -g \sin^2 \theta
$$

oppure, usando le derivate seconde:

$$
\frac{d^2x}{dt^2} = g \sin \theta \cos \theta
$$

$$
\frac{d^2y}{dt^2} = -g \sin^2 \theta
$$

Se il corpo parte da fermo da `x = 0` e altezza iniziale `y_0`, allora:

$$
x(t) = \frac{1}{2} g \sin \theta \cos \theta \ t^2
$$

$$
y(t) = y_0 - \frac{1}{2} g \sin^2 \theta \ t^2
$$

Il segno meno in `y(t)` indica che il corpo scende verso il basso.

## Idea fondamentale

Sul piano inclinato la forza peso non agisce tutta nella direzione del moto. Va scomposta:

- la componente `mg sinθ` fa muovere il corpo lungo il piano;
- la componente `mg cosθ` viene compensata dalla reazione normale;
- l’accelerazione lungo il piano è:

$$
a = g \sin \theta
$$

Più il piano è inclinato, maggiore è `sinθ`, quindi maggiore è l’accelerazione.

## La tensione

Nei problemi di dinamica si usa spesso un **filo ideale**, cioè:

- **inestensibile**, quindi la lunghezza non cambia;
- di **massa trascurabile**, quindi non altera il moto;
- capace di trasmettere una forza ai corpi collegati.

Quando un filo è in tensione, ogni sua parte è tirata da forze uguali e opposte. La forza trasmessa dal filo si chiama **tensione** e si indica con:

$$
T
$$

La tensione ha sempre:

- direzione **parallela al filo**;
- verso diretto **verso l’interno del filo**;
- verso opposto sui due corpi collegati.

Se il filo è ideale, la tensione ha lo stesso valore in ogni punto del filo.

## Puleggia

La **puleggia** serve a cambiare la direzione della tensione.

Se la puleggia è ideale, cioè senza massa e senza attrito, allora cambia solo la direzione della forza, ma non il suo modulo.

Quindi, nei due lati del filo, la tensione resta la stessa:

$$
T
$$

Questo permette di collegare corpi che si muovono in direzioni diverse.

![[Pasted image 20260618234239.png]]
## Macchina di Atwood

La **macchina di Atwood** è un sistema formato da due masse `m_1` e `m_2` collegate da un filo ideale che passa su una puleggia ideale.

Sulle due masse agiscono:

- il peso:

$$
P_1 = m_1 g
$$

$$
P_2 = m_2 g
$$

- la tensione del filo:

$$
T
$$

La tensione è diretta verso l’alto per entrambe le masse, mentre il peso è diretto verso il basso.

Le equazioni del moto sono:

$$
m_1 a = T - m_1 g
$$

$$
-m_2 a = T - m_2 g
$$

Il segno meno nella seconda equazione dipende dalla scelta del verso positivo. Le due masse si muovono in versi opposti: se una sale, l’altra scende.

Risolvendo il sistema si ottiene l’accelerazione:

$$
a = \frac{m_2 - m_1}{m_1 + m_2}g
$$

e la tensione del filo:

$$
T = \frac{2m_1m_2}{m_1 + m_2}g
$$

![[Pasted image 20260618234316.png]]
## Interpretazione fisica

Se:

$$
m_2 > m_1
$$

allora l’accelerazione è positiva: `m_2` scende e `m_1` sale.

Se invece:

$$
m_1 > m_2
$$

allora l’accelerazione è negativa rispetto al verso scelto: `m_1` scende perché ha peso maggiore.

La macchina di Atwood è utile perché, scegliendo masse molto vicine tra loro, si può ottenere un’accelerazione piccola, anche se su ogni massa agisce la gravità.

## Idee fondamentali

La tensione è la forza trasmessa da un filo.

Un filo ideale trasmette la stessa tensione lungo tutta la sua lunghezza.

Una puleggia ideale cambia la direzione della tensione, ma non il suo valore.

Nella macchina di Atwood il moto dipende dalla differenza tra le due masse:

$$
a = \frac{m_2 - m_1}{m_1 + m_2}g
$$

Se le masse sono uguali, il sistema è in equilibrio:

$$
m_1 = m_2 \Rightarrow a = 0
$$


## Esercizio — Due casse a contatto su piano senza attrito

Due casse sono poste a contatto su un piano orizzontale privo di attrito.

Dati:

$$
m_1 = 2.4 \ kg
$$

$$
m_2 = 3.6 \ kg
$$

Una forza esterna agisce sulla prima cassa:

$$
F = 12 \ N
$$

Bisogna trovare:

- la forza di contatto tra le due casse;
- l’accelerazione del sistema.

---

## Idea fisica

Le due casse sono a contatto, quindi si muovono insieme con la stessa accelerazione `a`.

La forza esterna `F` spinge `m_1`, che a sua volta spinge `m_2`.

Tra le due casse nasce una forza di contatto:

$$
F_c
$$

Le due forze di contatto sono uguali in modulo e opposte in verso:

$$
F_{12} = F_{21} = F_c
$$

---

## Equazioni del moto

Per la seconda cassa `m_2`, l’unica forza orizzontale è la forza di contatto:

$$
F_c = m_2 a
$$

Per la prima cassa `m_1`, agiscono la forza esterna `F` in avanti e la forza di contatto `F_c` all’indietro:

$$
F - F_c = m_1 a
$$

Quindi il sistema è:

$$
\begin{cases}
F_c = m_2 a \\
F - F_c = m_1 a
\end{cases}
$$

---

## Calcolo dell’accelerazione

Considerando le due casse come un unico sistema, la massa totale è:

$$
m_1 + m_2 = 2.4 + 3.6 = 6 \ kg
$$

Quindi:

$$
F = (m_1 + m_2)a
$$

Da cui:

$$
a = \frac{F}{m_1 + m_2}
$$

Sostituendo:

$$
a = \frac{12}{6}
$$

$$
a = 2.0 \ m/s^2
$$

---

## Calcolo della forza di contatto

Usiamo:

$$
F_c = m_2 a
$$

Sostituendo:

$$
F_c = 3.6 \cdot 2.0
$$

$$
F_c = 7.2 \ N
$$

Equivalentemente:

$$
F_c = \frac{m_2}{m_1 + m_2}F
$$

$$
F_c = \frac{3.6}{2.4 + 3.6} \cdot 12 = 7.2 \ N
$$

---

## Risultato finale

L’accelerazione delle due casse è:

$$
\boxed{a = 2.0 \ m/s^2}
$$

La forza di contatto tra le casse è:

$$
\boxed{F_c = 7.2 \ N}
$$

Nota importante: la forza di contatto non è uguale alla forza esterna `F`, perché `F` deve accelerare entrambe le masse, mentre `F_c` serve solo ad accelerare la seconda cassa.



## Esercizio — Massa sospesa spinta dal vento

Un corpo di massa:

$$
m = 3 \cdot 10^{-4} \ kg
$$

è sospeso a un filo. Un vento orizzontale lo spinge fino a far formare al filo un angolo:

$$
\theta = 37^\circ
$$

rispetto alla verticale.

Il corpo è in equilibrio, quindi la somma delle forze è nulla.

Le forze agenti sono:

- il peso:

$$
P = mg
$$

- la tensione del filo:

$$
T
$$

- la spinta orizzontale del vento:

$$
F
$$

Scomponiamo la tensione:

- componente orizzontale:

$$
T \sin\theta
$$

- componente verticale:

$$
T \cos\theta
$$

Le condizioni di equilibrio sono:

$$
-F + T\sin\theta = 0
$$

$$
T\cos\theta - mg = 0
$$

Dalla seconda:

$$
T = \frac{mg}{\cos\theta}
$$

Sostituendo i valori:

$$
T = \frac{3 \cdot 10^{-4} \cdot 9.8}{\cos37^\circ}
$$

$$
T \approx 3.7 \cdot 10^{-3} \ N
$$

Per la forza del vento:

$$
F = T\sin\theta
$$

oppure direttamente:

$$
F = mg \tan\theta
$$

Sostituendo:

$$
F = 3 \cdot 10^{-4} \cdot 9.8 \cdot \tan37^\circ
$$

$$
F \approx 2.2 \cdot 10^{-3} \ N
$$

Risultati:

$$
\boxed{F \approx 2.2 \cdot 10^{-3} \ N}
$$

$$
\boxed{T \approx 3.7 \cdot 10^{-3} \ N}
$$

---

## Esercizio — Cassa su piano inclinato spinta orizzontalmente

Una cassa di massa:

$$
m = 100 \ kg
$$

viene fatta salire a velocità costante su un piano inclinato di angolo:

$$
\theta = 30^\circ
$$

La forza applicata è orizzontale, cioè parallela al terreno.

Poiché la velocità è costante:

$$
a = 0
$$

quindi la risultante delle forze è nulla.

La forza orizzontale `F` va scomposta rispetto al piano inclinato:

- componente parallela al piano:

$$
F \cos\theta
$$

- componente perpendicolare al piano:

$$
F \sin\theta
$$

Anche il peso si scompone:

- componente parallela al piano:

$$
mg \sin\theta
$$

- componente perpendicolare al piano:

$$
mg \cos\theta
$$

Lungo il piano:

$$
F\cos\theta - mg\sin\theta = 0
$$

Da cui:

$$
F\cos\theta = mg\sin\theta
$$

$$
F = mg \tan\theta
$$

Sostituendo:

$$
F = 100 \cdot 9.8 \cdot \tan30^\circ
$$

$$
F \approx 566 \ N
$$

Per la reazione normale del piano:

$$
F_N - F\sin\theta - mg\cos\theta = 0
$$

quindi:

$$
F_N = F\sin\theta + mg\cos\theta
$$

Sostituendo:

$$
F_N = 566\sin30^\circ + 100 \cdot 9.8 \cos30^\circ
$$

$$
F_N \approx 1130 \ N
$$

Risultati:

$$
\boxed{F \approx 566 \ N}
$$

$$
\boxed{F_N \approx 1130 \ N}
$$

Nota: la forza normale è maggiore del solo `mg cosθ` perché la forza orizzontale applicata schiaccia ulteriormente la cassa contro il piano.

---

## Esercizio — Quattro blocchi collegati da funi

Quattro blocchi `B1`, `B2`, `B3`, `B4` sono collegati da funi e trascinati da una tensione esterna:

$$
T_4 = 222 \ N
$$

Sono note le masse:

$$
m_{B1} = 12 \ kg
$$

$$
m_{B3} = 15 \ kg
$$

$$
m_{B4} = 20 \ kg
$$

e una tensione interna:

$$
T_{2-3} = 111 \ N
$$

Bisogna trovare la massa di `B2`.

Tutti i blocchi si muovono con la stessa accelerazione `a`.

Considerando il sistema intero:

$$
T_4 = (m_{B1}+m_{B2}+m_{B3}+m_{B4})a
$$

Per trovare `a`, consideriamo solo i blocchi `B3` e `B4`.

Per `B4`:

$$
m_{B4}a = T_4 - T_{3-4}
$$

Per `B3`:

$$
m_{B3}a = T_{3-4} - T_{2-3}
$$

Sommando le due equazioni, la tensione interna `T_{3-4}` si elimina:

$$
(m_{B4}+m_{B3})a = T_4 - T_{2-3}
$$

Da cui:

$$
a = \frac{T_4 - T_{2-3}}{m_{B4}+m_{B3}}
$$

Sostituendo:

$$
a = \frac{222 - 111}{20+15}
$$

$$
a = \frac{111}{35}
$$

$$
a \approx 3.17 \ m/s^2
$$

Ora usiamo la relazione del sistema intero:

$$
T_4 = (m_{B1}+m_{B2}+m_{B3}+m_{B4})a
$$

Da cui:

$$
m_{B2} = \frac{T_4}{a} - (m_{B1}+m_{B3}+m_{B4})
$$

Sostituendo:

$$
m_{B2} = \frac{222}{3.17} - (12+15+20)
$$

$$
m_{B2} \approx 70 - 47
$$

$$
m_{B2} \approx 23 \ kg
$$

Risultato:

$$
\boxed{m_{B2} = 23 \ kg}
$$

Idea importante: quando più corpi sono collegati, hanno la stessa accelerazione. Le tensioni interne si possono eliminare scegliendo bene il sistema da considerare.

## Esercizio — Discesa lungo un piano inclinato senza attrito

In questo esercizio si studia il moto di una cassa che scende lungo un piano inclinato senza attrito.

Dalla geometria del piano inclinato si ricava la base:

$$
b = \sqrt{\ell^2 - h^2}
$$

Dalla slide:

$$
b = 6.5 \ m
$$

dove:

- `\ell` è la lunghezza del piano inclinato;
- `h` è l’altezza del piano;
- `b` è la base orizzontale.

---

## Reazione normale del piano

La reazione vincolare del piano non è uguale a `mg`, ma alla componente del peso perpendicolare al piano.

Dalla geometria del piano:

$$
\cos\theta = \frac{b}{\ell}
$$

quindi:

$$
N = mg \cos\theta
$$

e quindi:

$$
N = \frac{b}{\ell}mg
$$

Dalla slide:

$$
N = 36 \ N
$$

---

## Accelerazione lungo il piano

Sul corpo agisce la componente del peso parallela al piano:

$$
mg\sin\theta
$$

Applicando la seconda legge della dinamica:

$$
ma = mg\sin\theta
$$

semplificando la massa:

$$
a = g\sin\theta
$$

Poiché:

$$
\sin\theta = \frac{h}{\ell}
$$

allora:

$$
a = g\frac{h}{\ell}
$$

---

## Tempo di discesa

Il moto lungo il piano è uniformemente accelerato.

Partendo da fermo:

$$
\ell = \frac{1}{2}at^2
$$

Da cui:

$$
t = \sqrt{\frac{2\ell}{a}}
$$

Sostituendo:

$$
a = g\frac{h}{\ell}
$$

si ottiene:

$$
t = \sqrt{\frac{2\ell}{g\frac{h}{\ell}}}
$$

$$
t = \sqrt{\frac{2\ell^2}{gh}}
$$

$$
t = \ell \sqrt{\frac{2}{gh}}
$$

Dalla slide:

$$
t = 1.7 \ s
$$

---

## Velocità finale

La velocità finale si calcola con:

$$
v = at
$$

Sostituendo le formule:

$$
v = g\frac{h}{\ell} \cdot \ell \sqrt{\frac{2}{gh}}
$$

semplificando:

$$
v = \sqrt{2gh}
$$

Dalla slide:

$$
v = 8.6 \ m/s
$$

---

## Osservazione importante

La velocità finale non dipende dalla lunghezza del piano inclinato né dalla sua pendenza.

Dipende solo dall’altezza `h` da cui parte il corpo:

$$
v = \sqrt{2gh}
$$

Questa è la stessa velocità che avrebbe il corpo se cadesse liberamente dalla stessa altezza `h`.

Quindi il piano inclinato cambia il tempo di discesa e l’accelerazione, ma non la velocità finale se non c’è attrito.

---

# Quesiti

## Q1 — Che direzione e modulo ha la reazione vincolare di un piano qualsiasi?

La reazione vincolare ha sempre direzione normale alla superficie del piano.

Il suo modulo non è fisso: dipende dalle altre forze presenti nella direzione perpendicolare alla superficie.

In generale, la reazione vincolare è uguale in modulo e opposta in verso alla risultante delle forze che spingono il corpo contro il piano.

Esempio:

$$
N = mg\cos\theta
$$

per un corpo su piano inclinato senza altre forze perpendicolari.

---

## Q2 — Che direzione ha la tensione di un filo ai suoi estremi?

La tensione ha direzione parallela al filo.

Il suo verso è sempre diretto verso l’interno del filo.

Se il filo è ideale, cioè inestensibile e di massa trascurabile, il modulo della tensione è uguale ai due estremi.

Quindi:

$$
T_1 = T_2 = T
$$

I versi però sono opposti, perché il filo tira i corpi verso di sé.
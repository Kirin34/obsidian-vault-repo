
## Impulso di una forza

Consideriamo una forza $\vec{F}$ che agisce su un corpo di massa $m$ per un intervallo di tempo molto piccolo $dt$.

Si definisce **impulso istantaneo** della forza:

$$
d\vec{J} = \vec{F} \, dt
$$

Se la forza non è costante nel tempo, l'impulso totale tra due istanti $t_1$ e $t_2$ si calcola con l'integrale:

$$
\vec{J} = \int_{t_1}^{t_2} \vec{F}(t) \, dt
$$

Quindi l'impulso dipende dall'andamento della forza nel tempo.

Se invece la forza è costante:

$$
\vec{J} = \vec{F} \Delta t
$$

L'impulso è una **grandezza vettoriale**, perché deriva da una forza vettoriale.

Unità di misura:

$$
[\vec{J}] = N \cdot s
$$

---

## Teorema dell'impulso

Dal secondo principio della dinamica:

$$
\vec{F} = m \vec{a}
$$

Sapendo che:

$$
\vec{a} = \frac{d\vec{v}}{dt}
$$

si può scrivere:

$$
\vec{F} = m \frac{d\vec{v}}{dt}
$$

Moltiplicando entrambi i membri per $dt$:

$$
\vec{F}dt = m d\vec{v}
$$

Ma $\vec{F}dt$ è l'impulso infinitesimo, quindi:

$$
d\vec{J} = m d\vec{v}
$$

Integrando tra $t_1$ e $t_2$:

$$
\vec{J} = \int_{t_1}^{t_2} \vec{F}dt
= \int_{\vec{v}(t_1)}^{\vec{v}(t_2)} m d\vec{v}
$$

Se la massa è costante:

$$
\vec{J} = m\vec{v}(t_2) - m\vec{v}(t_1)
$$

---

## Quantità di moto

La grandezza vettoriale:

$$
\vec{p} = m\vec{v}
$$

si chiama **quantità di moto** o **momento lineare**.

Dove:

- $m$ è la massa del corpo
- $\vec{v}$ è la velocità
- $\vec{p}$ ha la stessa direzione e verso della velocità

Unità di misura:

$$
[\vec{p}] = kg \frac{m}{s}
$$

che è equivalente a:

$$
N \cdot s
$$

---

## Enunciato del teorema dell'impulso

L'impulso della forza agente su un punto materiale in un intervallo di tempo è uguale alla variazione della quantità di moto del punto materiale nello stesso intervallo.

In formula:

$$
\vec{J} = \Delta \vec{p}
$$

cioè:

$$
\vec{J} = \vec{p}_2 - \vec{p}_1
$$

oppure:

$$
\vec{J} = m\vec{v}_2 - m\vec{v}_1
$$

---

## Idea chiave

Una forza applicata per un certo tempo modifica la velocità del corpo, quindi modifica la sua quantità di moto.

Più grande è la forza o più lungo è il tempo di applicazione, maggiore sarà l'impulso:

$$
\vec{J} = \vec{F}\Delta t
$$

e quindi maggiore sarà la variazione della quantità di moto:

$$
\vec{J} = \Delta \vec{p}
$$

## Sistemi a massa variabile

La quantità di moto è:

$$
\vec{p} = m\vec{v}
$$

Se la massa è costante, la seconda legge della dinamica si scrive:

$$
\vec{F} = \frac{d\vec{p}}{dt}
$$

Però esistono sistemi in cui la massa cambia nel tempo, ad esempio un razzo che consuma combustibile.

Se non agiscono forze esterne e la quantità di moto si conserva:

$$
\frac{d\vec{p}}{dt} = 0
$$

allora:

$$
\frac{d(m\vec{v})}{dt} = 0
$$

Applicando la derivata del prodotto:

$$
\frac{dm}{dt}\vec{v} + m\frac{d\vec{v}}{dt} = 0
$$

Da cui:

$$
\frac{d\vec{v}}{dt} = -\frac{1}{m}\frac{dm}{dt}\vec{v}
$$

Questa relazione mostra che, se la massa varia, può variare anche la velocità.

---

## Sistema globale

Nel caso dei razzi, il sistema completo da considerare è:

$$
\text{razzo} + \text{combustibile espulso}
$$

Anche se la massa del razzo diminuisce, la massa totale del sistema globale si conserva, perché il combustibile non sparisce: viene espulso.

---

## Razzo a massa variabile

Il razzo si muove perché espelle combustibile ad alta velocità.

Consideriamo un sistema inerziale nello spazio libero, trascurando:

- gravità
- attrito
- resistenza dell’aria

All’istante $t$ il razzo ha:

$$
m = \text{massa}
$$

$$
\vec{v} = \text{velocità}
$$

All’istante successivo $t + dt$:

$$
m \rightarrow m - dm
$$

$$
\vec{v} \rightarrow \vec{v} + d\vec{v}
$$

La massa diminuisce perché una quantità $dm$ di combustibile viene espulsa.

---

## Quantità di moto del sistema razzo-combustibile

La massa espulsa $dm$, con velocità $\vec{V}$, contribuisce alla quantità di moto con:

$$
dm \vec{V}
$$

Per conservazione della quantità di moto:

$$
m\vec{v} = (m - dm)(\vec{v} + d\vec{v}) + dm\vec{V}
$$

Sviluppando e trascurando il prodotto infinitesimo $dm \, d\vec{v}$:

$$
m\vec{v} = m\vec{v} + m d\vec{v} - dm\vec{v} + dm\vec{V}
$$

Semplificando:

$$
m d\vec{v} = dm(\vec{v} - \vec{V})
$$

Indicando con $\vec{u}$ la velocità relativa del combustibile espulso rispetto al razzo:

$$
\vec{u} = \vec{v} - \vec{V}
$$

si ottiene:

$$
m\frac{d\vec{v}}{dt} = -\frac{dm}{dt}\vec{u}
$$

Questa è la forma della spinta del razzo.

---

## Idea chiave

Un razzo accelera perché espelle massa in verso opposto al moto.

La quantità di moto totale del sistema si conserva:

$$
\vec{p}_{tot} = costante
$$

quindi, se il combustibile viene espulso all’indietro, il razzo riceve una spinta in avanti.

Formula importante:

$$
m\frac{d\vec{v}}{dt} = -\frac{dm}{dt}\vec{u}
$$

## Velocità relativa del combustibile

Nel modello del razzo, $\vec{u}$ indica la **velocità relativa del combustibile espulso rispetto al razzo**.

Dalla slide:

$$
\vec{u} = \vec{V} - (\vec{v} + d\vec{v})
$$

dove:

- $\vec{V}$ è la velocità del combustibile espulso rispetto al sistema inerziale
- $\vec{v} + d\vec{v}$ è la velocità del razzo dopo l’espulsione
- $\vec{u}$ è la velocità del combustibile vista dal razzo

La **spinta** del razzo dipende da due fattori:

- quanto combustibile viene espulso ogni secondo
- con quale velocità relativa viene espulso

La relazione fondamentale è:

$$
m\frac{d\vec{v}}{dt} = -\frac{dm}{dt}\vec{u}
$$

---

## Andamento della velocità del razzo

Se il tasso di espulsione della massa è costante, si può scrivere:

$$
m = M_0 - ct
$$

dove:

- $M_0$ è la massa iniziale del razzo
- $c$ è il tasso costante di perdita di massa
- $t$ è il tempo

Partendo da:

$$
m\frac{dv}{dt} = -\frac{dm}{dt}u
$$

si ottiene:

$$
dv = -u \frac{dm}{m}
$$

Integrando:

$$
\int_{v_0}^{v} dv = -u \int_{M_0}^{m} \frac{dm}{m}
$$

si arriva a:

$$
v = v_0 + u \ln \left(\frac{M_0}{M_0 - ct}\right)
$$

Questa formula mostra che la velocità del razzo aumenta man mano che la massa diminuisce.

---

## Formula finale del razzo

La velocità del razzo in funzione del tempo è:

$$
v = v_0 + u \ln \left(\frac{M_0}{M_0 - ct}\right)
$$

Quindi il razzo accelera perché espelle massa: più combustibile viene espulso, più aumenta la velocità del razzo.

---
## Idea chiave

Il razzo non accelera perché “spinge sull’aria”, ma perché espelle combustibile in verso opposto.

Per conservazione della quantità di moto:

$$
\text{combustibile indietro} \Rightarrow \text{razzo avanti}
$$

## Esercizio di ripasso 1 - Colline e attrito

### Traccia

Due colline si trovano ai lati opposti di una valle, con altezze:

$$
H = 850 \, m
$$

$$
h = 750 \, m
$$

Il percorso totale tra le due cime è:

$$
L = 3.2 \, km = 3200 \, m
$$

La pendenza media è:

$$
\theta = 30^\circ
$$

Un blocco parte da fermo dalla cima più alta e scende senza attrito.

Si chiede:

1. con quale velocità raggiunge l’altra cima;
2. quale coefficiente di attrito dinamico servirebbe per farlo fermare esattamente sulla cima opposta.

---

### Punto (a) - Caso senza attrito

Senza attrito si conserva l’energia meccanica:

$$
E_i = E_f
$$

All’inizio il blocco è fermo, quindi ha solo energia potenziale:

$$
E_i = mgH
$$

Alla fine, sulla cima opposta, ha energia potenziale più energia cinetica:

$$
E_f = mgh + \frac{1}{2}mv^2
$$

Quindi:

$$
mgH = mgh + \frac{1}{2}mv^2
$$

Semplificando la massa:

$$
gH = gh + \frac{1}{2}v^2
$$

$$
v = \sqrt{2g(H-h)}
$$

Sostituendo:

$$
v = \sqrt{2 \cdot 9.8 \cdot (850-750)}
$$

$$
v = \sqrt{1960}
$$

$$
v \approx 44.3 \, m/s
$$

---

### Punto (b) - Caso con attrito

Per fermarsi sulla cima opposta, il blocco deve arrivare con velocità finale nulla.

Quindi l’energia persa deve essere uguale al lavoro negativo dell’attrito.

La variazione di energia meccanica è:

$$
\Delta E = mg(h-H)
$$

Il lavoro dell’attrito dinamico lungo il percorso è:

$$
L_{attrito} = -\mu mg \cos \theta \, L
$$

Uguagliando:

$$
mg(h-H) = -\mu mgL\cos \theta
$$

Semplificando $mg$:

$$
h-H = -\mu L\cos \theta
$$

Da cui:

$$
\mu = \frac{H-h}{L\cos \theta}
$$

Sostituendo:

$$
\mu = \frac{850-750}{3200 \cos 30^\circ}
$$

$$
\mu = \frac{100}{3200 \cdot 0.866}
$$

$$
\mu \approx 0.036
$$

---

### Risultati

$$
v \approx 44.3 \, m/s
$$

$$
\mu \approx 0.036
$$

---

## Esercizio di ripasso 2 - Pista con attrito

### Traccia

Un punto materiale scorre su una pista composta da:

- un tratto piano centrale;
- due estremità simmetriche curve e rialzate.

Le estremità curve sono lisce, quindi senza attrito.

Il tratto piano ha:

$$
L = 40 \, cm
$$

$$
\mu = 0.20
$$

Il punto parte da fermo da un’altezza:

$$
h = \frac{L}{2}
$$

rispetto al tratto piano.

Si chiede in quale punto si fermerà.

---

### Energia iniziale

Il punto parte da fermo, quindi ha solo energia potenziale:

$$
E_0 = mgh
$$

Dato che:

$$
h = \frac{L}{2}
$$

allora:

$$
E_0 = mg\frac{L}{2}
$$

---

### Energia persa per attrito

Ogni volta che il punto attraversa il tratto piano, perde energia a causa dell’attrito.

Il lavoro dell’attrito sul tratto piano è:

$$
\Delta E_{attr} = -\mu mgL
$$

Quindi a ogni attraversamento completo del piano perde:

$$
\mu mgL
$$

---

### Numero di attraversamenti

Per capire dopo quanti attraversamenti si ferma, confrontiamo energia iniziale ed energia persa a ogni passaggio:

$$
n = \frac{mg\frac{L}{2}}{\mu mgL}
$$

Semplificando:

$$
n = \frac{1}{2\mu}
$$

Sostituendo:

$$
n = \frac{1}{2 \cdot 0.20}
$$

$$
n = \frac{1}{0.40}
$$

$$
n = 2.5
$$

Serve quindi l’intero subito maggiore:

$$
n = 3
$$

---

### Interpretazione

Dopo 2 attraversamenti completi del tratto piano, il corpo non ha ancora perso tutta l’energia.

Al terzo attraversamento si fermerà prima di completare tutto il tratto piano.

Energia iniziale:

$$
E_0 = mg\frac{L}{2}
$$

Energia persa nei primi 2 attraversamenti:

$$
2\mu mgL = 2 \cdot 0.20 mgL = 0.40mgL
$$

Energia rimasta:

$$
mg\frac{L}{2} - 0.40mgL = 0.10mgL
$$

Durante il terzo attraversamento, l’attrito dissipa energia:

$$
\mu mgx = 0.10mgL
$$

Semplificando:

$$
\mu x = 0.10L
$$

$$
x = \frac{0.10L}{0.20}
$$

$$
x = \frac{L}{2}
$$

---

### Risultato

Il punto materiale si ferma al terzo passaggio sul tratto piano, a metà del tratto piano:

$$
x = \frac{L}{2}
$$

Dato che:

$$
L = 40 \, cm
$$

allora:

$$
x = 20 \, cm
$$

Quindi si ferma a metà del tratto piano.

## Esercizio - Rimbalzo contro una parete

### Traccia

Un punto materiale di massa:

$$
m = 0.165 \, kg
$$

si muove con velocità:

$$
v = 2.00 \, m/s
$$

e urta una parete con angolo:

$$
\theta_1 = 30^\circ
$$

rispetto alla normale alla parete.

Dopo il rimbalzo:

- la componente della velocità normale alla parete si inverte;
- la componente parallela alla parete resta invariata.

Si chiede:

1. la direzione dopo il rimbalzo;
2. la variazione della quantità di moto.

---

### Soluzione

Scomponiamo la velocità in due componenti:

$$
\vec{v}_1 = (v \sin \theta_1, v \cos \theta_1)
$$

Dopo il rimbalzo, la componente parallela resta uguale, mentre quella normale cambia segno:

$$
\vec{v}_2 = (v \sin \theta_1, -v \cos \theta_1)
$$

Quindi l’angolo dopo il rimbalzo ha lo stesso valore in modulo:

$$
\theta_2 = \theta_1 = 30^\circ
$$

ma si trova dal lato opposto della normale.

---

### Variazione della quantità di moto

La quantità di moto è:

$$
\vec{p} = m\vec{v}
$$

La variazione è:

$$
\Delta \vec{p} = m(\vec{v}_2 - \vec{v}_1)
$$

Poiché cambia solo la componente normale:

$$
\Delta \vec{p} = (0, -2mv\cos 30^\circ)
$$

Modulo:

$$
|\Delta \vec{p}| = 2mv\cos 30^\circ
$$

Sostituendo:

$$
|\Delta \vec{p}| = 2 \cdot 0.165 \cdot 2.00 \cdot \cos 30^\circ
$$

$$
|\Delta \vec{p}| \approx 0.57 \, kg \frac{m}{s}
$$

La variazione della quantità di moto è diretta lungo la normale alla parete, verso il verso negativo.

---

## Esercizio - Razzo con gravità

### Traccia

Un razzo ha massa iniziale:

$$
m_0 = 10^6 \, kg
$$

brucia carburante con tasso:

$$
c = 1.2 \cdot 10^3 \, kg/s
$$

I gas vengono espulsi con velocità relativa:

$$
u = 3 \cdot 10^4 \, m/s
$$

Il razzo parte da fermo in verticale, in presenza di gravità.

Si chiede la velocità dopo:

$$
t = 100 \, s
$$

---

### Soluzione

Per un razzo a massa variabile, senza altre forze, vale:

$$
v = v_0 + u \ln \left( \frac{M_0}{M_0 - ct} \right)
$$

Poiché il razzo si muove verso l’alto, la gravità agisce verso il basso, quindi bisogna sottrarre il termine:

$$
gt
$$

La formula diventa:

$$
v = v_0 + u \ln \left( \frac{M_0}{M_0 - ct} \right) - gt
$$

Il razzo parte da fermo:

$$
v_0 = 0
$$

Sostituiamo i dati:

$$
v(100) = 3 \cdot 10^4 \ln \left( \frac{10^6}{10^6 - 1.2 \cdot 10^3 \cdot 100} \right) - 9.8 \cdot 100
$$

Calcoliamo la massa rimasta:

$$
M_0 - ct = 10^6 - 1.2 \cdot 10^3 \cdot 100
$$

$$
M_0 - ct = 880000 \, kg
$$

Quindi:

$$
v(100) = 3 \cdot 10^4 \ln \left( \frac{10^6}{880000} \right) - 980
$$

$$
v(100) \approx 2855 \, m/s
$$

---

### Risultato

$$
v(100) \approx 2855 \, m/s
$$

---

## Quesiti

### Q.1 Come è definita la quantità di moto di un punto materiale?

La quantità di moto è una grandezza vettoriale definita come il prodotto tra massa e velocità:

$$
\vec{p} = m\vec{v}
$$

---

### Q.2 Cosa afferma il teorema dell’impulso?

Il teorema dell’impulso afferma che l’impulso di una forza agente su un punto materiale in un certo intervallo di tempo è uguale alla variazione della quantità di moto:

$$
\vec{J} = \Delta \vec{p}
$$

cioè:

$$
\vec{J} = \vec{p}_2 - \vec{p}_1
$$

---

### Q.3 A quanto equivale la spinta di un razzo a massa variabile?

La spinta è la forza generata dall’espulsione del combustibile ad alta velocità.

Vale:

$$
F = u \frac{dm}{dt}
$$

dove:

- $u$ è la velocità relativa del materiale espulso rispetto al razzo;
- $\frac{dm}{dt}$ è il tasso di espulsione della massa.

In forma vettoriale, dalla relazione vista prima:

$$
m\frac{d\vec{v}}{dt} = -\frac{dm}{dt}\vec{u}
$$
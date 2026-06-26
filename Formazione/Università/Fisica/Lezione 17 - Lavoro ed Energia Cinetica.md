## Energia

L’energia è una grandezza fisica fondamentale, difficile da definire in modo “operativo” unico.

In meccanica, l’energia è una proprietà associata allo stato di un corpo, cioè può dipendere da:

- moto;
- posizione;
- configurazione del sistema.

Un principio fondamentale della fisica è la **conservazione dell’energia**: l’energia non si crea né si distrugge, ma si trasforma o si trasferisce tra sistemi.

Uno dei principali modi con cui un sistema scambia energia con l’ambiente è il **lavoro**.

---

## Lavoro elementare

Il **lavoro elementare** compiuto da una forza $\vec{F}$ su un punto materiale che si sposta di un tratto infinitesimo $d\vec{s}$ è:

$$
dL = \vec{F} \cdot d\vec{s}
$$

oppure:

$$
dL = |\vec{F}| \ |d\vec{s}| \cos \theta
$$

dove $\theta$ è l’angolo tra la forza e lo spostamento.

Il lavoro è una **grandezza scalare**, perché deriva da un prodotto scalare.

Unità di misura:

$$
1J = 1Nm = 1 \frac{kg \ m^2}{s^2}
$$

Il joule misura quindi il lavoro compiuto da una forza di $1N$ che sposta un corpo di $1m$ nella stessa direzione della forza.

---

## Significato dell’angolo

Conta solo la componente della forza parallela allo spostamento.

- Se la forza è nella stessa direzione dello spostamento:

$$
\theta = 0^\circ \Rightarrow \cos \theta = 1
$$

il lavoro è massimo e positivo.

- Se la forza è perpendicolare allo spostamento:

$$
\theta = 90^\circ \Rightarrow \cos \theta = 0
$$

il lavoro è nullo.

- Se la forza è opposta allo spostamento:

$$
\theta = 180^\circ \Rightarrow \cos \theta = -1
$$

il lavoro è negativo.

In generale:

- angolo acuto → lavoro positivo;
- angolo retto → lavoro nullo;
- angolo ottuso → lavoro negativo.

---

## Idea chiave

Il lavoro misura quanta energia una forza trasferisce a un corpo durante uno spostamento.

Non basta che ci sia una forza: deve esserci anche uno spostamento e una componente della forza lungo lo spostamento.

## Lavoro su una traiettoria

Se un punto materiale si sposta dal punto $A$ al punto $B$, il lavoro totale è la somma di tutti i lavori elementari lungo la traiettoria.

Nel limite in cui gli spostamenti infinitesimi diventano sempre più piccoli:

$$
L_{AB} = \int_A^B \vec{F} \cdot d\vec{s}
$$

Quindi il lavoro è un **integrale di linea** lungo la traiettoria percorsa.

---

## Lavoro di una forza costante

Se la forza è costante e parallela allo spostamento:

$$
L = F \cdot s
$$

Più in generale:

$$
L = F s \cos \theta
$$

dove $\theta$ è l’angolo tra forza e spostamento.

Se il moto avviene lungo l’asse $s$, tra due posizioni $s_1$ e $s_2$:

$$
L = F(s_2 - s_1)
$$

Dal punto di vista grafico, il lavoro di una forza costante coincide con l’**area del rettangolo** sotto il grafico forza-spostamento.

---

## Lavoro di una forza variabile

Se la forza non è costante, il lavoro si calcola come area sotto la curva $F(x)$.

Si divide l’intervallo da $x_i$ a $x_f$ in tanti piccoli intervalli $\Delta x$, nei quali la forza può essere considerata circa costante.

Il lavoro totale è la somma dei piccoli lavori:

$$
L \approx \sum F_i \Delta x
$$

Nel limite in cui $\Delta x \to 0$:

$$
L = \int_{x_i}^{x_f} F(x) \ dx
$$

Quindi:

> il lavoro di una forza variabile è l’area sottesa dalla curva forza-spostamento.

---

## Lavoro di più forze

Se su un punto materiale agiscono più forze:

$$
\vec{F}_1, \vec{F}_2, ..., \vec{F}_N
$$

la risultante è:

$$
\vec{F} = \vec{F}_1 + \vec{F}_2 + ... + \vec{F}_N
$$

Il lavoro della risultante è uguale alla somma dei lavori delle singole forze:

$$
L_{AB} = L_{AB,1} + L_{AB,2} + ... + L_{AB,N}
$$

---

## Casi semplici di lavoro

| Angolo | Formula | Segno | Tipo di lavoro |
|---|---|---|---|
| $0^\circ$ | $L = Fs$ | positivo | motore |
| $90^\circ$ | $L = 0$ | nullo | nullo |
| $180^\circ$ | $L = -Fs$ | negativo | resistente |

- **Lavoro motore**: la forza favorisce il movimento.
- **Lavoro nullo**: la forza è perpendicolare allo spostamento.
- **Lavoro resistente**: la forza si oppone al movimento.

---

## Idea chiave

Il lavoro dipende da:

1. intensità della forza;
2. spostamento;
3. angolo tra forza e spostamento;
4. eventuale variazione della forza lungo la traiettoria.

Se la forza è variabile, il lavoro si calcola con un integrale.


## Energia cinetica

Riprendendo il lavoro elementare:

$$
dL = \vec{F} \cdot d\vec{s}
$$

usando la seconda legge della dinamica:

$$
\vec{F} = m\vec{a}
$$

e la definizione di velocità:

$$
\vec{v} = \frac{d\vec{s}}{dt}
$$

si ottiene che il lavoro compiuto dalla forza risultante è legato alla variazione della velocità del corpo.

Il risultato finale è:

$$
L_{AB} = \frac{1}{2}mv_B^2 - \frac{1}{2}mv_A^2
$$

Si definisce quindi **energia cinetica**:

$$
K = \frac{1}{2}mv^2
$$

L’energia cinetica è l’energia posseduta da un corpo a causa del suo movimento.

Dipende da:

- massa del corpo;
- quadrato della velocità.

Ha le stesse dimensioni del lavoro e si misura in joule:

$$
[J]
$$

---

## Energia e lavoro

L’energia è una grandezza scalare associata allo **stato** di un corpo.

Le forme principali viste in meccanica sono:

- **energia cinetica**: energia dovuta al movimento;
- **energia potenziale**: energia dovuta alla posizione;
- **energia meccanica**: somma di energia cinetica e potenziale.

$$
E_m = K + U
$$

Il lavoro rappresenta un processo di trasferimento di energia.

---

## Teorema dell’energia cinetica

Il lavoro compiuto dalla risultante delle forze agenti su un punto materiale è uguale alla variazione della sua energia cinetica:

$$
L_{AB} = K_B - K_A
$$

oppure:

$$
L_{AB} = \Delta K
$$

Questo prende il nome di **teorema dell’energia cinetica** o **teorema delle forze vive**.

Significato fisico:

- se $L > 0$, l’energia cinetica aumenta;
- se $L < 0$, l’energia cinetica diminuisce;
- se $L = 0$, l’energia cinetica resta costante.

Quindi una forza che compie lavoro positivo accelera il corpo, mentre una forza che compie lavoro negativo tende a rallentarlo.

---

## Idea chiave

L’energia cinetica è una proprietà del corpo legata al suo moto, mentre il lavoro è il modo con cui una forza trasferisce energia al corpo o la sottrae.

In formula:

$$
\text{lavoro della risultante} = \text{variazione di energia cinetica}
$$## Verifica del teorema delle forze vive

Consideriamo un caso semplice:

- forza $\vec{F}$ costante;
- massa $m$;
- moto rettilineo;
- forza parallela allo spostamento;
- corpo inizialmente fermo.

Dalla cinematica del moto uniformemente accelerato:

$$
l = \frac{1}{2}at^2
$$

e:

$$
v = at
$$

Da cui:

$$
t = \frac{v}{a}
$$

Sostituendo nella legge oraria:

$$
l = \frac{1}{2}a \left(\frac{v}{a}\right)^2
$$

quindi:

$$
l = \frac{v^2}{2a}
$$

Poiché dalla seconda legge della dinamica:

$$
F = ma
$$

allora:

$$
a = \frac{F}{m}
$$

Sostituendo:

$$
l = \frac{v^2}{2 \frac{F}{m}}
$$

Moltiplicando per $F$:

$$
Fl = \frac{1}{2}mv^2
$$

Il primo membro rappresenta il **lavoro della forza**, perché il moto è rettilineo e la forza è parallela allo spostamento:

$$
L = Fl
$$

Il secondo membro rappresenta l’**energia cinetica finale**:

$$
K = \frac{1}{2}mv^2
$$

Dato che il corpo parte da fermo:

$$
K_i = 0
$$

quindi:

$$
L = K_f - K_i
$$

cioè:

$$
L = \Delta K
$$

---

## Idea chiave

In questo esempio si verifica il teorema dell’energia cinetica:

$$
\text{lavoro della forza risultante} = \text{variazione di energia cinetica}
$$

Se il corpo parte da fermo, tutto il lavoro compiuto dalla forza diventa energia cinetica finale.

## Potenza istantanea

La **potenza istantanea** misura quanto rapidamente viene compiuto lavoro in un istante.

È definita come:

$$
W = \frac{dL}{dt}
$$

dove:

- $dL$ è il lavoro elementare;
- $dt$ è l’intervallo di tempo infinitesimo.

La potenza è una **grandezza scalare**.

Unità di misura:

$$
1W = 1 \frac{J}{s} = 1 \frac{kg \ m^2}{s^3}
$$

---

## Potenza media

La **potenza media** è il rapporto tra il lavoro totale compiuto e il tempo impiegato:

$$
\overline{W} = \frac{L_{AB}}{\Delta t_{AB}}
$$

La potenza indica quindi la rapidità con cui un sistema compie lavoro.

A parità di lavoro:

- minore è il tempo impiegato;
- maggiore è la potenza.

---

## Potenza come prodotto forza-velocità

Partendo dalla definizione:

$$
W = \frac{dL}{dt}
$$

e sapendo che:

$$
dL = \vec{F} \cdot d\vec{s}
$$

si ottiene:

$$
W = \frac{\vec{F} \cdot d\vec{s}}{dt}
$$

Poiché:

$$
\vec{v} = \frac{d\vec{s}}{dt}
$$

allora:

$$
W = \vec{F} \cdot \vec{v}
$$

Quindi la potenza istantanea è il prodotto scalare tra forza e velocità.

---

## Calcolo del lavoro

Il lavoro di una forza si calcola tramite un **integrale di linea**.

Nel caso generale, la forza può avere tre componenti che dipendono dalla posizione:

$$
\vec{F} = F_x(x,y,z)\vec{i} + F_y(x,y,z)\vec{j} + F_z(x,y,z)\vec{k}
$$

Il lavoro lungo la traiettoria da $A$ a $B$ è:

$$
L_{AB} = \int_A^B \left[ F_x(x,y,z)dx + F_y(x,y,z)dy + F_z(x,y,z)dz \right]
$$

---

## Traiettoria parametrizzata

Se la traiettoria dipende da un solo parametro $p$:

$$
\vec{s} = [x(p), y(p), z(p)]
$$

allora il lavoro diventa:

$$
L_{AB} =
\int_A^B
\left[
F_x(x(p),y(p),z(p))\frac{dx}{dp}
+
F_y(x(p),y(p),z(p))\frac{dy}{dp}
+
F_z(x(p),y(p),z(p))\frac{dz}{dp}
\right]dp
$$

---

## Idea chiave

La potenza dice **quanto velocemente** viene trasferita energia tramite il lavoro.

Il lavoro invece dipende dalla forza e dallo spostamento lungo la traiettoria:

$$
L = \int \vec{F} \cdot d\vec{s}
$$

Se la forza è espressa in componenti, il prodotto scalare diventa una somma dei contributi lungo $x$, $y$ e $z$.

## Lavoro della gravità

Consideriamo la forza peso durante lo spostamento di un punto materiale da $A$ a $B$.

La forza peso è:

$$
\vec{P} = m\vec{g}
$$

diretta verticalmente verso il basso.

Il lavoro della gravità è:

$$
L_{AB} = \int_A^B \vec{F} \cdot d\vec{s}
$$

Poiché la forza peso agisce solo lungo l’asse verticale:

$$
L_{AB} = \int_A^B -mg \ dy
$$

quindi:

$$
L_{AB} = -mg y_B + mg y_A
$$

cioè:

$$
L_{AB} = mg(y_A - y_B)
$$

Se il punto finale è più in basso del punto iniziale:

$$
y_B < y_A
$$

allora il lavoro della gravità è positivo.

La gravità è una forza particolare: il suo lavoro dipende solo dalla posizione iniziale e finale, non dalla traiettoria percorsa.

---

## Lavoro nel pendolo semplice

Nel pendolo semplice agiscono due forze:

- la forza peso;
- la tensione del filo.

La tensione del filo non compie lavoro, perché è sempre perpendicolare allo spostamento.

Quindi il lavoro è dovuto solo alla forza peso.

La posizione del pendolo può essere descritta con:

$$
\vec{s} = [l \sin \theta, -l \cos \theta]
$$

Se il pendolo parte da un angolo iniziale $\theta_0$ e arriva nel punto più basso, dove $\theta = 0$, il lavoro della gravità è:

$$
L_{AB} = mgl(1 - \cos \theta_0)
$$

Questo risultato coincide con la formula generale:

$$
L_{AB} = mg(y_A - y_B)
$$

perché:

$$
y_A = -l \cos \theta_0
$$

e:

$$
y_B = -l
$$

---

## Velocità massima del pendolo

Nel punto più basso del moto, il pendolo ha velocità massima.

Se parte da fermo da un angolo $\theta_0$, il lavoro della gravità diventa energia cinetica:

$$
\frac{1}{2}mv_{max}^2 = mgl(1 - \cos \theta_0)
$$

Semplificando la massa:

$$
v_{max} = \sqrt{2gl(1 - \cos \theta_0)}
$$

Per piccoli angoli si può usare l’approssimazione:

$$
\cos \theta_0 \approx 1 - \frac{\theta_0^2}{2}
$$

quindi:

$$
v_{max} \approx \theta_0 \sqrt{gl}
$$

Poiché nel pendolo semplice:

$$
\omega = \sqrt{\frac{g}{l}}
$$

si può anche scrivere:

$$
v_{max} = l\theta_0 \omega
$$

---

## Idea chiave

La gravità compie lavoro positivo quando il corpo scende e negativo quando sale.

Nel pendolo, la tensione non compie lavoro: l’energia cinetica nel punto più basso deriva dal lavoro della forza peso.


## Lavoro della forza elastica

Per una molla vale la legge di Hooke:

$$
F = -kx
$$

dove:

- $k$ è la costante elastica della molla;
- $x$ è lo spostamento rispetto alla posizione di riposo;
- il segno meno indica che la forza elastica è sempre diretta verso la posizione di equilibrio.

Il lavoro della forza elastica da una posizione $A$ a una posizione $B$ è:

$$
L_{AB} = \int_A^B \vec{F} \cdot d\vec{s}
$$

Nel caso monodimensionale lungo l’asse $x$:

$$
L_{AB} = \int_{x_A}^{x_B} -kx \ dx
$$

quindi:

$$
L_{AB} = -\frac{1}{2}kx_B^2 + \frac{1}{2}kx_A^2
$$

oppure:

$$
L_{AB} = \frac{1}{2}k(x_A^2 - x_B^2)
$$

Il lavoro è positivo se il corpo si avvicina alla posizione di riposo della molla, cioè se:

$$
|x_A| > |x_B|
$$

In questo caso la forza elastica favorisce il movimento.

---

## Lavoro della forza d’attrito

La forza d’attrito radente è sempre opposta al moto.

Se il corpo si muove su un piano orizzontale, la forza d’attrito ha modulo:

$$
F_a = \mu mg
$$

Il lavoro dell’attrito lungo una traiettoria da $A$ a $B$ è:

$$
L_{AB} = \int_A^B \vec{F} \cdot d\vec{s}
$$

Poiché l’attrito è sempre opposto allo spostamento:

$$
L_{AB} = -\mu mg \int_A^B ds

$$
## Lavoro della forza elastica

Per una molla vale la legge di Hooke:

$$
F = -kx
$$

dove:

- $k$ è la costante elastica della molla;
- $x$ è lo spostamento rispetto alla posizione di riposo;
- il segno meno indica che la forza elastica è sempre diretta verso la posizione di equilibrio.

Il lavoro della forza elastica da una posizione $A$ a una posizione $B$ è:

$$
L_{AB} = \int_A^B \vec{F} \cdot d\vec{s}
$$

Nel caso monodimensionale lungo l’asse $x$:

$$
L_{AB} = \int_{x_A}^{x_B} -kx \ dx
$$

quindi:

$$
L_{AB} = -\frac{1}{2}kx_B^2 + \frac{1}{2}kx_A^2
$$

oppure:

$$
L_{AB} = \frac{1}{2}k(x_A^2 - x_B^2)
$$

Il lavoro è positivo se il corpo si avvicina alla posizione di riposo della molla, cioè se:

$$
|x_A| > |x_B|
$$

In questo caso la forza elastica favorisce il movimento.

---

## Lavoro della forza d’attrito

La forza d’attrito radente è sempre opposta al moto.

Se il corpo si muove su un piano orizzontale, la forza d’attrito ha modulo:

$$
F_a = \mu mg
$$

Il lavoro dell’attrito lungo una traiettoria da $A$ a $B$ è:

$$
L_{AB} = \int_A^B \vec{F} \cdot d\vec{s}
$$

Poiché l’attrito è sempre opposto allo spostamento:

$$
L_{AB} = -\mu mg \int_A^B ds
$$

$$
L_{AB} = -\mu mg s_{AB}
$$

dove $s_{AB}$ è la lunghezza effettiva della traiettoria percorsa.

L’attrito compie sempre lavoro negativo, quindi è una forza resistente.

A differenza della gravità e della forza elastica, il lavoro dell’attrito dipende dalla traiettoria percorsa, non solo dal punto iniziale e finale.

---

## Idea chiave

- La **forza elastica** può compiere lavoro positivo o negativo, a seconda che il corpo si avvicini o si allontani dalla posizione di equilibrio.
- La **forza d’attrito** compie sempre lavoro negativo.
- L’attrito sottrae energia cinetica al corpo, quindi tende a diminuire la velocità.

## Esercizio: lavoro di una forza variabile

Una forza agisce lungo l’asse $x$ con intensità:

$$
F(x)=10e^{-x/2}
$$

Bisogna trovare il lavoro compiuto nello spostamento da:

$$
x=0 \quad \text{a} \quad x=2m
$$

Il lavoro si calcola con l’integrale:

$$
L_{AB}=\int_0^2 F(x)dx
$$

quindi:

$$
L_{AB}=\int_0^2 10e^{-x/2}dx
$$

Integrando:

$$
L_{AB}=\left[-20e^{-x/2}\right]_0^2
$$

$$
L_{AB}=-20e^{-1}+20
$$

$$
L_{AB}=20\left(1-\frac{1}{e}\right)
$$

Risultato:

$$
L_{AB} \approx 12.6J
$$

---

## Quesiti finali

### Q.1 Lavoro elementare

Il lavoro elementare compiuto da una forza $\vec{F}$ durante uno spostamento infinitesimo $d\vec{s}$ è:

$$
dL=\vec{F}\cdot d\vec{s}
$$

È un prodotto scalare.

---

### Q.2 Teorema dell’energia cinetica

Il lavoro totale svolto dalla risultante delle forze su un punto materiale è uguale alla variazione della sua energia cinetica:

$$
L_{AB}=K_B-K_A
$$

oppure:

$$
L=\Delta K
$$

---

### Q.3 Potenza media

La potenza media è il lavoro totale diviso per il tempo impiegato:

$$
\overline{W}=\frac{L}{\Delta t}
$$

Indica quanto rapidamente viene compiuto lavoro.

---

### Q.4 Lavoro della gravità verso l’alto

Se un corpo si sposta verso l’alto, il lavoro della forza di gravità è negativo, perché la forza peso è diretta verso il basso.

$$
L=-mg\Delta h
$$

---

### Q.5 Lavoro della forza elastica

Per una molla:

$$
F=-kx
$$

Il lavoro della forza elastica da $x_A$ a $x_B$ è:

$$
L_{AB}=\frac{1}{2}k(x_A^2-x_B^2)
$$

Il lavoro è positivo se il corpo si avvicina alla posizione di equilibrio.

---

### Q.6 Lavoro dell’attrito

Il lavoro dell’attrito ha sempre segno negativo, perché l’attrito si oppone sempre allo spostamento:

$$
L=-\mu mg s
$$

Il lavoro dell’attrito dipende dalla lunghezza della traiettoria percorsa, non solo dalla posizione iniziale e finale.

---

## Idea chiave finale

- Il lavoro trasferisce energia.
- Il lavoro della risultante modifica l’energia cinetica.
- La potenza misura la rapidità con cui viene compiuto lavoro.
- Gravità e forza elastica dipendono solo da posizione iniziale e finale.
- L’attrito dipende dal percorso ed è sempre resistente.
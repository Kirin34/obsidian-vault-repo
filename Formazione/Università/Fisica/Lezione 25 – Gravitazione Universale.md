## Teoria della gravitazione

Newton formulò la **legge di gravitazione universale** partendo dalle osservazioni di Keplero sul moto dei pianeti.

La teoria permette di spiegare:
- il moto dei pianeti intorno al Sole;
- l'interazione gravitazionale tra corpi dotati di massa;
- la forza di gravità terrestre;
- più in generale, le orbite di pianeti e satelliti.

---

## Il campo in fisica

Un **campo** è una regione dello spazio nella quale ad ogni punto è associato il valore di una determinata **grandezza fisica**.

Il campo deve essere generato da una **sorgente**.

A seconda della grandezza associata ai punti dello spazio possiamo avere:

- **campo scalare** → ad ogni punto è associato un numero;
- **campo vettoriale** → ad ogni punto è associato un vettore.

Il **campo gravitazionale** è un campo vettoriale, perché in ogni punto è caratterizzato da **intensità, direzione e verso**.

---

## Linee di forza

Un campo vettoriale può essere rappresentato graficamente attraverso le **linee di forza**.

Una linea di forza è una linea che, in ogni suo punto, ha come **tangente la direzione del vettore campo** presente in quel punto.

Quindi dalle linee di forza possiamo ricavare:

- **direzione** del campo → tangente alla linea;
- **verso** → indicato dalle frecce;
- **intensità** → indicata dalla densità delle linee.

### Convenzione di Faraday

Il numero di linee di forza che attraversano una superficie unitaria posta perpendicolarmente alle linee è proporzionale all'**intensità del campo**.

Quindi:

**linee più fitte → campo più intenso**

**linee più distanti → campo meno intenso**

---

## Proprietà delle linee di forza

1. Per ogni punto dello spazio passa **una e una sola linea di forza**.
2. Due linee di forza **non possono mai intersecarsi**.
3. Le linee sono orientate nello **stesso verso del campo**.
4. La tangente alla linea in un punto indica la **direzione del campo**.
5. La densità delle linee indica l'**intensità del campo**.

> Due linee non possono intersecarsi perché, se lo facessero, nello stesso punto il campo avrebbe due direzioni diverse, cosa impossibile.

## Legge di gravitazione universale

Due corpi di masse $m_1$ e $m_2$, posti a distanza $r$, si attraggono reciprocamente con una forza gravitazionale di intensità:

$$
F = G\frac{m_1m_2}{r^2}
$$

dove:

- $m_1$, $m_2$ = masse dei due corpi;
- $r$ = distanza tra i due corpi;
- $G$ = **costante di gravitazione universale**.

Il suo valore è:

$$
G = 6.67 \cdot 10^{-11}\ \frac{m^3}{kg\,s^2}
$$

### Cosa ci dice la formula?

La forza gravitazionale:

- aumenta all'aumentare delle masse $m_1$ e $m_2$;
- diminuisce con il **quadrato della distanza**.

Quindi, ad esempio, se la distanza raddoppia:

$$
r \rightarrow 2r
$$

allora:

$$
F \rightarrow \frac{F}{4}
$$

---

## Forma vettoriale

Definiamo $\vec{u}_r$ come il versore diretto dal corpo $1$ al corpo $2$.

La forza esercitata dalla massa $1$ sulla massa $2$ è:

$$
\vec{F}_{12} = -G\frac{m_1m_2}{r^2}\vec{u}_r
$$

Il segno **$-$** indica che la forza è **attrattiva**, quindi diretta verso la massa $1$.

Viceversa, la forza esercitata dalla massa $2$ sulla massa $1$ è:

$$
\vec{F}_{21} = G\frac{m_1m_2}{r^2}\vec{u}_r
$$

Per il **principio di azione e reazione**:

$$
\vec{F}_{12} = -\vec{F}_{21}
$$

Le due forze hanno quindi:

- stesso modulo;
- stessa direzione;
- verso opposto.

> **Da ricordare:** la gravitazione è sempre attrattiva e la sua intensità segue una legge dell'inverso del quadrato della distanza: $F \propto 1/r^2$.


## Campo gravitazionale

La forza gravitazionale è un'interazione **a distanza**: non richiede contatto diretto tra le masse.

Una massa $M$ genera attorno a sé un **campo gravitazionale**. Se una massa di prova $m$ si trova a distanza $r$, il campo vale:

$$
\vec{G}(r)=\frac{\vec{F}_g}{m}
$$

quindi:

$$
\vec{G}(r)=-\frac{GM}{r^2}\vec{u}_r
$$

Il segno $-$ indica che il campo è diretto verso la massa $M$, quindi è **attrattivo**.

> Il campo gravitazionale dipende dalla massa sorgente $M$ e dalla distanza $r$, ma non dalla massa di prova $m$.

---

## Campo gravitazionale come campo conservativo

Il campo gravitazionale è **conservativo**: il lavoro compiuto dalla forza gravitazionale dipende solo dalla posizione iniziale e finale.

Per uno spostamento da $A$ a $B$:

$$
L_{A\to B}=\int_A^B \vec{F}_g\cdot d\vec{s}
$$

Sostituendo la forza gravitazionale:

$$
L_{A\to B}
=
Gm_1m_2
\left(
\frac{1}{r_B}
-
\frac{1}{r_A}
\right)
$$

Essendo una forza conservativa:

$$
L_{A\to B}=-(U_B-U_A)
$$

---

## Energia potenziale gravitazionale

Ponendo l'energia potenziale uguale a zero a distanza infinita:

$$
U(\infty)=0
$$

l'energia potenziale gravitazionale di una massa $m$ nel campo generato da $M$ è:

$$
U(r)=-\frac{GMm}{r}
$$

L'energia potenziale è **negativa** perché l'interazione gravitazionale è attrattiva.

La forza si ricava dall'energia potenziale tramite:

$$
\vec{F}(r)
=
-\frac{dU}{dr}\vec{u}_r
$$

ottenendo:

$$
\vec{F}(r)
=
-\frac{GMm}{r^2}\vec{u}_r
$$

> All'aumentare di $r$, $U$ aumenta e tende a $0$.

---

## Distribuzione di masse

Per più masse vale il **principio di sovrapposizione**: la forza totale è la somma vettoriale delle singole forze.

$$
\vec{F}_{tot}
=
\vec{F}_{10}
+
\vec{F}_{20}
+
\dots
+
\vec{F}_{N0}
$$

Lo stesso principio vale anche per il campo gravitazionale.

### Distribuzione sferica uniforme

Una massa $M$ distribuita uniformemente in una sfera genera, per un punto esterno, lo stesso campo che si avrebbe considerando tutta la massa concentrata nel **centro della sfera**.

Se:

- $R$ = raggio della sfera;
- $h$ = altezza rispetto alla superficie;

la distanza dal centro è:

$$
r=R+h
$$

e la forza gravitazionale sulla massa $m$ è:

$$
\vec{F}
=
-\frac{GMm}{(R+h)^2}\vec{u}_r
$$

> Quindi, all'esterno di un corpo sferico uniforme, possiamo trattarlo come una massa puntiforme posta nel suo centro.

## Campo gravitazionale terrestre

La Terra può essere approssimata come una **sfera di massa $M_T$**.

Sulla superficie terrestre, una massa $m$ subisce:

$$
\vec{F}_g=-m\frac{GM_T}{R_T^2}\vec{u}_r
$$

dove $R_T$ è il raggio terrestre.

Confrontando con la forza peso:

$$
\vec{F}_g=m\vec{g}
$$

si ottiene il campo gravitazionale terrestre:

$$
\vec{g}=-\frac{GM_T}{R_T^2}\vec{u}_r
$$

Il campo è diretto **verso il centro della Terra** e, vicino alla superficie:

$$
g \approx 9.81\ m/s^2
$$

---

## Variazione di $g$ con l'altezza

Allontanandosi dalla superficie terrestre, l'accelerazione di gravità **diminuisce**.

A un'altezza $h$:

$$
g(h)=\frac{GM_T}{(R_T+h)^2}
$$

con raggio medio terrestre:

$$
R_T=6.37\cdot10^6\ m
$$

Rispetto al valore sulla superficie:

$$
\frac{g(h)}{g}
=
\frac{R_T^2}{(R_T+h)^2}
=
\frac{1}{\left(1+\frac{h}{R_T}\right)^2}
$$

Per $h \ll R_T$, la variazione è molto piccola e possiamo considerare:

$$
g \approx 9.81\ m/s^2
$$

costante.

> Quindi l'approssimazione di $g$ costante funziona bene vicino alla superficie terrestre.

---

## Velocità di fuga

La **velocità di fuga** è la velocità minima che deve avere un corpo per riuscire ad allontanarsi indefinitamente da un pianeta senza ricadere sulla sua superficie.

Si ricava dalla **conservazione dell'energia meccanica**.

Alla superficie terrestre:

$$
E_i=\frac{1}{2}mv^2-\frac{GM_Tm}{R_T}
$$

Nel caso limite di fuga, a distanza infinita:

$$
U(\infty)=0
$$

e la velocità finale può essere considerata nulla:

$$
v(\infty)=0
$$

Quindi imponiamo:

$$
\frac{1}{2}mv_f^2-\frac{GM_Tm}{R_T}=0
$$

da cui:

$$
\boxed{v_f=\sqrt{\frac{2GM_T}{R_T}}}
$$

La massa $m$ del corpo si semplifica: **la velocità di fuga non dipende dalla massa dell'oggetto lanciato**.

Per la Terra:

$$
\boxed{v_f\approx11.2\ km/s}
$$

> La formula vale in generale per qualsiasi corpo celeste sostituendo la sua massa $M$ e il suo raggio $R$:

$$
v_f=\sqrt{\frac{2GM}{R}}
$$

## Le leggi di Keplero

Keplero descrisse il moto dei pianeti attraverso **tre leggi fondamentali**.

### 1ª legge di Keplero
I pianeti si muovono su **orbite ellittiche**, con il Sole posto in uno dei due fuochi.

### 2ª legge di Keplero
Il raggio vettore che unisce il Sole al pianeta **spazza aree uguali in tempi uguali**.

Quindi la velocità areolare è costante.

> Il pianeta si muove più velocemente quando è vicino al Sole e più lentamente quando è lontano.

### 3ª legge di Keplero
Il rapporto tra il quadrato del periodo orbitale $T$ e il cubo del semiasse maggiore $a$ è costante:

$$
\frac{T^2}{a^3}=\text{costante}
$$

Per un'orbita circolare $a=r$, quindi:

$$
T^2 \propto r^3
$$

---

## Satelliti artificiali in orbita circolare

Un satellite di massa $m$ che orbita attorno alla Terra compie un **moto circolare uniforme**.

L'accelerazione centripeta è:

$$
a_c=\frac{v^2}{r}
$$

ed è diretta verso il centro della Terra.

La forza gravitazionale fornisce proprio la forza centripeta:

$$
F_g=\frac{GM_Tm}{r^2}
$$

Applicando $F=ma$:

$$
a_c=\frac{GM_T}{r^2}
$$

Quindi:

$$
\frac{v^2}{r}=\frac{GM_T}{r^2}
$$

da cui si ricava la **velocità orbitale**:

$$
\boxed{v=\sqrt{\frac{GM_T}{r}}}
$$

> Maggiore è il raggio dell'orbita, minore è la velocità orbitale.

---

## Periodo orbitale

Nel moto circolare uniforme:

$$
a_c=\omega^2r=\frac{4\pi^2r}{T^2}
$$

Uguagliandola all'accelerazione gravitazionale:

$$
\frac{4\pi^2r}{T^2}=\frac{GM_T}{r^2}
$$

si ottiene:

$$
\boxed{T^2=\frac{4\pi^2r^3}{GM_T}}
$$

Questa relazione rappresenta, per un'orbita circolare, la **terza legge di Keplero**.

---

## Altezza delle orbite

In teoria un satellite potrebbe orbitare anche molto vicino alla superficie terrestre.

Nella realtà, però, l'**attrito atmosferico** rallenta il satellite e rende instabili le orbite troppo basse.

L'orbita più bassa possibile è quindi circa:

$$
h \approx 150\ km
$$

---

## Orbita geosincrona e geostazionaria

Un'orbita è **geosincrona** quando il periodo del satellite coincide con quello di rotazione terrestre:

$$
T=24\ h=8.64\cdot10^4\ s
$$

Dalla relazione del periodo:

$$
r=\sqrt[3]{\frac{GMT^2}{4\pi^2}}
$$

si ottiene:

$$
r\approx4.22\cdot10^7\ m
$$

Poiché $r$ è misurato dal **centro della Terra**, l'altezza dalla superficie è:

$$
h=r-R_T
$$

quindi:

$$
\boxed{h\approx35800\ km}
$$

A questa altezza la velocità orbitale è circa:

$$
v\approx3.1\ km/s
$$

### Orbita geostazionaria

Un'orbita geosincrona diventa **geostazionaria** se:

- si trova sul piano dell'equatore;
- il satellite ruota nello stesso verso della Terra.

In questo modo il satellite appare **fermo sopra lo stesso punto della superficie terrestre**, caratteristica molto utile per i satelliti per telecomunicazioni.

> **Da ricordare:** geosincrona = stesso periodo della Terra; geostazionaria = stesso periodo + orbita equatoriale + stesso verso di rotazione.

## Esercizio 1 – Seconda legge di Keplero

### Traccia
Ricavare la **seconda legge di Keplero** usando la conservazione del momento angolare.

### Soluzione
La forza gravitazionale è diretta lungo la congiungente Sole-pianeta, quindi è una **forza centrale**.

Il momento della forza rispetto al Sole vale:

$$
\vec{M}=\vec{r}\times\vec{F}=0
$$

Quindi:

$$
\frac{d\vec{L}}{dt}=0
$$

e il momento angolare si conserva:

$$
\vec{L}=\vec{r}\times m\vec{v}=\text{costante}
$$

L'area infinitesima spazzata dal raggio vettore è:

$$
dA=\frac{1}{2}|\vec{r}\times d\vec{s}|
$$

Dividendo per $dt$:

$$
\frac{dA}{dt}
=
\frac{1}{2}|\vec{r}\times\vec{v}|
$$

Poiché:

$$
L=m|\vec{r}\times\vec{v}|
$$

si ha:

$$
\boxed{\frac{dA}{dt}=\frac{L}{2m}=\text{costante}}
$$

Quindi il raggio vettore **spazza aree uguali in tempi uguali**: è la seconda legge di Keplero.

---

## Esercizio 2 – Periodo di rivoluzione di Giove

### Traccia
La distanza media di Giove dal Sole è $5.205$ volte quella della Terra. Calcolare il suo periodo di rivoluzione.

### Soluzione
Dalla terza legge di Keplero:

$$
\frac{T_T^2}{T_G^2}
=
\frac{r_T^3}{r_G^3}
$$

quindi:

$$
T_G
=
T_T
\left(
\frac{r_G}{r_T}
\right)^{3/2}
$$

Sapendo che:

$$
\frac{r_G}{r_T}=5.205
$$

e:

$$
T_T=1\ anno
$$

si ottiene:

$$
T_G=(5.205)^{3/2}
$$

$$
\boxed{T_G\approx11.87\ anni}
$$

---

## Esercizio 3 – Dimostrazione della terza legge di Keplero

### Traccia
Dimostrare la terza legge di Keplero considerando l'orbita del pianeta circolare.

### Soluzione
Per un pianeta di massa $m$ in orbita circolare di raggio $R$, la forza gravitazionale coincide con la forza centripeta:

$$
\frac{GMm}{R^2}=m\omega^2R
$$

Semplificando $m$:

$$
\frac{GM}{R^2}=\omega^2R
$$

Con:

$$
\omega=\frac{2\pi}{T}
$$

si ha:

$$
\frac{GM}{R^2}
=
\frac{4\pi^2}{T^2}R
$$

Riordinando:

$$
\boxed{\frac{R^3}{T^2}=\frac{GM}{4\pi^2}}
$$

Poiché il termine a destra è costante:

$$
\boxed{\frac{T^2}{R^3}=\text{costante}}
$$

che è la **terza legge di Keplero**.

---

## Esercizio 4 – Raggio e velocità orbitale di un pianeta

### Traccia
Un pianeta impiega $300$ giorni terrestri per orbitare attorno a una stella di massa:

$$
M=6.0\cdot10^{30}\ kg
$$

Calcolare:

1. il raggio dell'orbita;
2. la velocità orbitale.

### Soluzione

Convertiamo il periodo:

$$
T=300\cdot24\cdot3600
$$

Dalla terza legge di Keplero:

$$
\frac{GM}{4\pi^2}=\frac{R^3}{T^2}
$$

da cui:

$$
R=
\sqrt[3]{
\frac{GMT^2}{4\pi^2}
}
$$

Si ottiene:

$$
\boxed{R\approx1.9\cdot10^{11}\ m}
$$

La velocità orbitale vale:

$$
v=\frac{2\pi R}{T}
$$

quindi:

$$
\boxed{v\approx45.9\ km/s}
$$

---

## Quesiti finali

### Q1 – Legge di gravitazione universale

Due masse $M$ e $m$, poste a distanza $r$, si attraggono con una forza:

$$
\boxed{F=G\frac{Mm}{r^2}}
$$

diretta lungo la congiungente dei due corpi.

La costante di gravitazione universale vale:

$$
G=6.67\cdot10^{-11}\ \frac{m^3}{kg\,s^2}
$$

---

### Q2 – Tre leggi di Keplero

**Prima legge:** i pianeti si muovono su orbite ellittiche con il Sole in uno dei fuochi.

**Seconda legge:** il raggio vettore Sole-pianeta spazza aree uguali in tempi uguali.

**Terza legge:**

$$
\boxed{\frac{T^2}{a^3}=\text{costante}}
$$

## Energia nei sistemi di punti materiali

In un sistema di punti materiali, su ogni punto possono agire:

- **forze esterne** $\vec{R}_i^{(e)}$
- **forze interne** $\vec{R}_i^{(i)}$, dovute all'interazione con gli altri punti del sistema.

Il lavoro elementare sul punto $i$ è quindi:

\[ dW_i = \vec{F}_i \cdot d\vec{r}_i = \vec{R}_i^{(e)} \cdot d\vec{r}_i + \vec{R}_i^{(i)} \cdot d\vec{r}_i \]

ovvero:

\[ dW_i = dW_i^{(e)} + dW_i^{(i)} \]

### Lavoro delle forze interne

A differenza di quanto accade con la **quantità di moto**, i contributi delle forze interne al lavoro **non si annullano necessariamente**.

Considerando due punti $i$ e $j$, per il principio di azione e reazione:

\[ \vec{F}_{ji}=-\vec{F}_{ij} \]

Il lavoro complessivo della coppia di forze interne è:

\[ \vec{F}_{ij}\cdot d\vec{r}_j+ \vec{F}_{ji}\cdot d\vec{r}_i \]

da cui:

\[ =\vec{F}_{ij}\cdot(d\vec{r}_j-d\vec{r}_i) =\vec{F}_{ij}\cdot d\vec{r}_{ij} \]

> [!important]  
> Il lavoro delle forze interne dipende quindi dalla **variazione della distanza relativa tra i punti** e non è, in generale, nullo.

---

## Teorema dell'energia cinetica per un sistema

Il lavoro totale compiuto dalle **forze esterne e interne** è uguale alla variazione dell'energia cinetica totale del sistema:

\[ W^{(e)}+W^{(i)}=E_{c,B}-E_{c,A} \]

oppure:

\[ W^{(e)}+W^{(i)}=\Delta E_c \]

Se tutte le forze, interne ed esterne, sono **conservative**, si conserva l'energia meccanica:

\[ E_m=E_c+E_p=\text{costante} \]

Se invece sono presenti **forze non conservative**, il loro lavoro determina la variazione dell'energia meccanica:

\[ W_{nc}=\Delta E_m \]

---

# Gli urti

Un **urto** è un'interazione tra due punti materiali che avviene in un intervallo di tempo molto breve.

Durante l'urto agiscono forze interne molto intense, dette **forze impulsive**, che provocano una variazione della quantità di moto dei singoli corpi.

Tuttavia, essendo queste forze **interne al sistema**, in assenza di forze esterne la quantità di moto totale si conserva:

\[ \vec{P}_{iniziale}=\vec{P}_{finale} \]

cioè:

\[ \sum_i m_i\vec{v}_{i}=\sum_i m_i\vec{v}_{i}' \]

### Perché spesso si trascurano le forze esterne?

L'urto avviene in un intervallo $\Delta t$ molto piccolo. L'impulso delle forze interne durante l'urto è quindi generalmente molto maggiore di quello prodotto dalle forze esterne:

\[ \vec{F}_{int}\,dt \gg \vec{F}_{ext}\,dt \]

Per questo, salvo indicazioni diverse, negli esercizi sugli urti si considera il sistema **isolato durante l'urto**.

---

## Urti elastici e anelastici

La **quantità di moto totale** si conserva negli urti di un sistema isolato, indipendentemente dal tipo di urto.

La differenza riguarda invece l'**energia cinetica**.

### Urto elastico

Nell'urto elastico si conserva anche l'energia cinetica:

\[ E_{c,i}=E_{c,f} \]

Quindi valgono contemporaneamente:

\[ \begin{cases} \vec{P}_i=\vec{P}_f\\ E_{c,i}=E_{c,f} \end{cases} \]

### Urto anelastico

Nell'urto anelastico la quantità di moto si conserva, ma **l'energia cinetica no**:

\[ E_{c,f}<E_{c,i} \]

Parte dell'energia cinetica viene trasformata in altre forme di energia, ad esempio deformazione, calore o energia interna.

> [!important]  
> **Da ricordare per gli esercizi:**
> 
> - Urto elastico → si conservano **quantità di moto + energia cinetica**.
> - Urto anelastico → si conserva la **quantità di moto**, ma non necessariamente l'energia cinetica.
> - Le forze interne non modificano la quantità di moto totale, ma **possono compiere lavoro e modificare l'energia cinetica del sistema**.

## Urti e sistemi di riferimento

Un urto può essere studiato sia nel **sistema di riferimento del laboratorio** sia nel **sistema del centro di massa (CM)**.

Le velocità nei due sistemi sono legate da:

$$
\vec{v}_1 = \vec{v}_1' + \vec{v}_{CM}
$$

$$
\vec{v}_2 = \vec{v}_2' + \vec{v}_{CM}
$$

dove $\vec{v}_1'$ e $\vec{v}_2'$ sono le velocità misurate rispetto al centro di massa.

### Quantità di moto nel sistema del centro di massa

Nel riferimento del centro di massa, la quantità di moto totale è sempre nulla:

$$
m_1\vec{v}_1' + m_2\vec{v}_2' = 0
$$

quindi:

$$
m_1\vec{v}_1' = -m_2\vec{v}_2'
$$

I due corpi hanno quindi **quantità di moto uguali in modulo e opposte in verso**.

Durante l'urto, nel sistema del CM:
- i corpi si avvicinano con quantità di moto opposte;
- avviene l'urto;
- si allontanano mantenendo quantità di moto uguali e opposte, anche se le velocità possono essere diverse da quelle iniziali.

L'energia cinetica totale rispetto al centro di massa è:

$$
K_{tot} = \frac{1}{2}m_1v_1'^2 + \frac{1}{2}m_2v_2'^2
$$

> [!important]
> Nel sistema del centro di massa vale sempre $\vec{P}_{tot}=0$. Questo rende spesso più semplice lo studio degli urti.

---

## Urti elastici

In un **urto elastico** le forze interne sono conservative: durante il contatto i corpi possono deformarsi elasticamente, ma successivamente ritornano alla configurazione iniziale.

Si conservano contemporaneamente:

### 1. Quantità di moto

$$
\vec{P}_{in} = \vec{P}_{fin}
$$

### 2. Energia cinetica

$$
K_{in} = K_{fin}
$$

In tre dimensioni la conservazione della quantità di moto fornisce **3 equazioni** (una per ogni componente), mentre la conservazione dell'energia cinetica ne fornisce un'altra.

In generale queste equazioni, da sole, non sono sufficienti a determinare tutte le velocità finali: servono quindi ulteriori informazioni sul problema.

### Caso unidimensionale

Il caso più semplice è l'**urto elastico unidimensionale**.

Conoscendo masse e velocità iniziali, le incognite sono solamente le due velocità finali $v_{1f}$ e $v_{2f}$.

Si hanno esattamente due equazioni:

**Conservazione della quantità di moto:**

$$
m_1v_{1i} + m_2v_{2i}
=
m_1v_{1f} + m_2v_{2f}
$$

**Conservazione dell'energia cinetica:**

$$
\frac{1}{2}m_1v_{1i}^2 + \frac{1}{2}m_2v_{2i}^2
=
\frac{1}{2}m_1v_{1f}^2 + \frac{1}{2}m_2v_{2f}^2
$$

> [!important]
> Nell'**urto elastico unidimensionale**, conoscendo le condizioni iniziali, le due leggi di conservazione permettono di ricavare completamente le **due velocità finali**.

## Urto elastico unidimensionale

Consideriamo due corpi di masse $m_1$ e $m_2$, con velocità iniziali $v_{1,in}$ e $v_{2,in}$.

In un urto elastico devono conservarsi **quantità di moto** ed **energia cinetica**.

### Conservazione della quantità di moto

$$
m_1v_{1,in}+m_2v_{2,in}
=
m_1v_{1,fin}+m_2v_{2,fin}
$$

Inoltre la quantità di moto totale può essere scritta tramite la velocità del centro di massa:

$$
m_1v_{1,in}+m_2v_{2,in}=(m_1+m_2)v_{CM}
$$

### Conservazione dell'energia cinetica

$$
\frac{1}{2}m_1v_{1,in}^2+\frac{1}{2}m_2v_{2,in}^2
=
\frac{1}{2}m_1v_{1,fin}^2+\frac{1}{2}m_2v_{2,fin}^2
$$

---

### Nel sistema del centro di massa

Nel riferimento del centro di massa la quantità di moto totale è nulla:

$$
m_1v'_{1,in}=-m_2v'_{2,in}
$$

e dopo l'urto:

$$
m_1v'_{1,fin}=-m_2v'_{2,fin}
$$

Combinando conservazione della quantità di moto e dell'energia cinetica si ottiene:

$$
v'_{1,fin}=-v'_{1,in}
$$

$$
v'_{2,fin}=-v'_{2,in}
$$

> [!important]
> In un urto elastico unidimensionale, visto dal centro di massa, i due corpi dopo l'urto **invertono semplicemente il verso delle loro velocità**, mantenendone il modulo.

---

### Velocità finali nel sistema del laboratorio

Tornando al sistema di riferimento del laboratorio si ottengono le formule generali:

$$
v_{1,fin}
=
\frac{m_1-m_2}{m_1+m_2}v_{1,in}
+
\frac{2m_2}{m_1+m_2}v_{2,in}
$$

$$
v_{2,fin}
=
\frac{2m_1}{m_1+m_2}v_{1,in}
+
\frac{m_2-m_1}{m_1+m_2}v_{2,in}
$$

Queste formule permettono di trovare direttamente le velocità finali conoscendo **masse e velocità iniziali**.

---

## Sistema proiettile-bersaglio

Un caso molto comune è quello di un **proiettile** di massa $m_1$ che urta elasticamente un **bersaglio** di massa $m_2$ inizialmente fermo.

In questo caso:

$$
v_{2,in}=0
$$

Le formule precedenti diventano:

$$
v_{1,fin}
=
\frac{m_1-m_2}{m_1+m_2}v_{1,in}
$$

$$
v_{2,fin}
=
\frac{2m_1}{m_1+m_2}v_{1,in}
$$

### Casi particolari

#### 1. Masse uguali: $m_1=m_2$

Si ottiene:

$$
v_{1,fin}=0
$$

$$
v_{2,fin}=v_{1,in}
$$

Il proiettile **si ferma** e il bersaglio parte con la velocità che aveva inizialmente il proiettile.

> Quantità di moto ed energia cinetica vengono completamente trasferite dal primo corpo al secondo.

#### 2. Proiettile molto più pesante: $m_1 \gg m_2$

Approssimativamente:

$$
v_{1,fin}\approx v_{1,in}
$$

$$
v_{2,fin}\approx 2v_{1,in}
$$

Il proiettile continua quasi indisturbato, mentre il bersaglio viene spinto con una velocità circa **doppia** rispetto a quella iniziale del proiettile.

#### 3. Proiettile molto più leggero: $m_1 \ll m_2$

Approssimativamente:

$$
v_{1,fin}\approx -v_{1,in}
$$

$$
v_{2,fin}\approx 0
$$

Il proiettile **rimbalza all'indietro** quasi con la stessa velocità, mentre il bersaglio pesante si muove pochissimo.

> [!important]
> **Schema da ricordare:**
>
> - $m_1=m_2$ → il primo si ferma e il secondo prende la sua velocità.
> - $m_1\gg m_2$ → il primo continua quasi uguale, il secondo parte a circa $2v_1$.
> - $m_1\ll m_2$ → il primo rimbalza indietro, il secondo rimane quasi fermo.

## Esercizio 1 – Carro e fanciullo

### Traccia

Un carro di massa $m_1 = 350\,kg$ si muove con velocità $v_1 = 7.2\,m/s$.

Un fanciullo di massa $m_2 = 43\,kg$ corre incontro al carro con velocità $v_2 = 3.7\,m/s$, quindi in verso opposto.

Il fanciullo salta sul carro e rimane sopra di esso. Determinare la velocità finale comune $v$.

### Soluzione

Poiché dopo l'urto carro e fanciullo rimangono uniti, si tratta di un **urto completamente anelastico**.

Si conserva la quantità di moto:

$$
m_1v_1 - m_2v_2 = (m_1+m_2)v
$$

Da cui:

$$
v = \frac{m_1v_1-m_2v_2}{m_1+m_2}
$$

Sostituendo:

$$
v=
\frac{350\cdot7.2-43\cdot3.7}{350+43}
$$

$$
v \approx 6.0\,m/s
$$

> [!important]
> Il segno meno davanti a $m_2v_2$ dipende dal fatto che il fanciullo corre in verso opposto rispetto al carro.

---

## Esercizio 2 – Urto elastico con bersaglio fermo

### Traccia

Un punto materiale di massa:

$$
m_1 = 4.2\,kg
$$

si muove con velocità:

$$
v_1 = 5.2\,m/s
$$

e urta elasticamente un secondo punto materiale inizialmente fermo, di massa $m_2$.

Studiare le velocità finali dei due corpi al variare di $m_2$.

### Soluzione

Per un urto elastico unidimensionale valgono:

$$
m_1v_1+m_2v_2=m_1V_1+m_2V_2
$$

e la relazione:

$$
v_1-v_2=V_2-V_1
$$

Le velocità finali generali sono:

$$
V_1=
\frac{(m_1-m_2)v_1+2m_2v_2}{m_1+m_2}
$$

$$
V_2=
\frac{(m_2-m_1)v_2+2m_1v_1}{m_1+m_2}
$$

Poiché il secondo corpo è inizialmente fermo:

$$
v_2=0
$$

si ottiene:

$$
V_1=
\frac{m_1-m_2}{m_1+m_2}v_1
$$

$$
V_2=
\frac{2m_1}{m_1+m_2}v_1
$$

### Discussione dei risultati

Il secondo corpo si muove sempre nello stesso verso iniziale di $m_1$.

Per il primo corpo:

- se $m_2<m_1$, allora $V_1>0$ e continua nello stesso verso;
- se $m_2=m_1$, allora $V_1=0$ e il primo corpo si ferma;
- se $m_2>m_1$, allora $V_1<0$ e il primo corpo rimbalza indietro.

Nel caso limite:

$$
m_2\gg m_1
$$

si ha:

$$
V_1\approx -v_1
$$

$$
V_2\approx0
$$

quindi è come urtare una parete: il corpo leggero rimbalza indietro quasi con la stessa velocità.

> [!important]
> Il segno di $V_1$ dipende dal confronto tra $m_1$ e $m_2$.

---

## Esercizio 3 – Urto completamente anelastico

### Traccia

Due punti materiali hanno:

$$
m_1=3.5\,kg
$$

$$
m_2=4.2\,kg
$$

e si muovono lungo la stessa retta e nello stesso verso con:

$$
v_1=5.4\,m/s
$$

$$
v_2=3.4\,m/s
$$

Dopo l'urto rimangono attaccati.

Determinare:

1. la velocità finale comune;
2. l'energia dissipata nell'urto.

### 1. Velocità finale

Poiché i corpi rimangono attaccati:

$$
V_1=V_2=V
$$

Si conserva la quantità di moto:

$$
m_1v_1+m_2v_2=(m_1+m_2)V
$$

Quindi:

$$
V=
\frac{m_1v_1+m_2v_2}{m_1+m_2}
$$

Sostituendo:

$$
V=
\frac{3.5\cdot5.4+4.2\cdot3.4}{3.5+4.2}
$$

$$
V\approx4.3\,m/s
$$

### 2. Energia dissipata

L'energia cinetica iniziale è:

$$
K_i=
\frac{1}{2}m_1v_1^2+
\frac{1}{2}m_2v_2^2
$$

L'energia cinetica finale è:

$$
K_f=
\frac{1}{2}(m_1+m_2)V^2
$$

L'energia dissipata vale:

$$
E_d=K_i-K_f
$$

quindi:

$$
E_d=
\frac{1}{2}m_1v_1^2+
\frac{1}{2}m_2v_2^2-
\frac{1}{2}(m_1+m_2)V^2
$$

Risultato:

$$
E_d\approx3.8\,J
$$

> [!important]
> Negli urti completamente anelastici si conserva la **quantità di moto**, ma non l'energia cinetica.
> La differenza $K_i-K_f$ rappresenta l'energia trasformata in deformazioni, calore, suono, ecc.

## Quesiti finali

### Q.1 Quali sono le grandezze conservate in un urto elastico?

In un **urto elastico** si conservano:

- la quantità di moto totale;
- l'energia cinetica totale.

Quindi:

$$
\vec{P}_{in}=\vec{P}_{fin}
$$

$$
K_{in}=K_{fin}
$$

---

### Q.2 Come viene descritto un urto elastico nel sistema di riferimento del centro di massa?

Nel sistema del **centro di massa** la quantità di moto totale è nulla.

I due corpi:

- si avvicinano con quantità di moto uguali e opposte;
- urtano in corrispondenza dell'origine;
- si allontanano ancora con quantità di moto uguali e opposte.

In un urto elastico unidimensionale, nel sistema del centro di massa, le velocità cambiano solo verso:

$$
v'_{1,fin}=-v'_{1,in}
$$

$$
v'_{2,fin}=-v'_{2,in}
$$

---

### Q.3 Quali sono le grandezze conservate in un urto anelastico?

In un **urto anelastico** si conserva la quantità di moto totale:

$$
\vec{P}_{in}=\vec{P}_{fin}
$$

L'energia cinetica invece **non si conserva**:

$$
K_{fin}<K_{in}
$$

La differenza viene trasformata in altre forme di energia.

---

### Q.4 Cos'è il coefficiente di restituzione?

Il **coefficiente di restituzione** $e$ misura quanto un urto è elastico.

Nel sistema del centro di massa può essere visto come il rapporto tra la quantità di moto dopo e prima dell'urto:

$$
e=\frac{|p_{fin}|}{|p_{in}|}
$$

Equivalentemente, negli urti unidimensionali:

$$
e=
\frac{\text{velocità relativa di allontanamento}}
{\text{velocità relativa di avvicinamento}}
$$

con:

$$
0\le e\le1
$$

- $e=1$ → urto elastico;
- $0<e<1$ → urto anelastico;
- $e=0$ → urto completamente anelastico.

---

### Q.5 Quando un urto si definisce completamente anelastico?

Un urto è **completamente anelastico** quando i due corpi, dopo l'urto, rimangono uniti e si muovono con la stessa velocità finale:

$$
v_{1,fin}=v_{2,fin}=v_f
$$

Si conserva la quantità di moto:

$$
m_1v_1+m_2v_2=(m_1+m_2)v_f
$$

ma si ha la **massima perdita possibile di energia cinetica** compatibile con la conservazione della quantità di moto.

## Esercizio – Proiettile e blocco con attrito

### Traccia

Un proiettile di massa:

$$
m_1 = 12.0\,g
$$

viene sparato contro un blocco di legno di massa:

$$
m_2 = 100\,g
$$

inizialmente fermo su una superficie orizzontale.

Il proiettile rimane conficcato nel blocco e, dopo l'urto, il sistema scivola per:

$$
L = 7.50\,m
$$

prima di fermarsi.

Il coefficiente di attrito dinamico tra blocco e superficie è:

$$
\mu_d = 0.650
$$

Determinare la **velocità $v_1$ del proiettile prima dell'urto**.

---

### Soluzione

Il problema si divide in **due fasi**:

1. urto completamente anelastico tra proiettile e blocco;
2. scivolamento del sistema fino all'arresto per effetto dell'attrito.

Conviene risolvere il problema partendo dalla **seconda fase**.

### 1. Scivolamento con attrito

Subito dopo l'urto, proiettile e blocco si muovono insieme con velocità $v_2$.

Durante lo scivolamento, l'attrito dissipa tutta l'energia cinetica fino a fermare il sistema.

Applichiamo il teorema dell'energia cinetica:

$$
\Delta K = W_{attrito}
$$

Poiché alla fine il sistema è fermo:

$$
0-\frac{1}{2}(m_1+m_2)v_2^2
=
f_dL\cos(180^\circ)
$$

Essendo:

$$
\cos(180^\circ)=-1
$$

si ha:

$$
-\frac{1}{2}(m_1+m_2)v_2^2=-f_dL
$$

La forza di attrito dinamico vale:

$$
f_d=\mu_dN
$$

Sul piano orizzontale:

$$
N=(m_1+m_2)g
$$

quindi:

$$
\frac{1}{2}(m_1+m_2)v_2^2
=
\mu_d(m_1+m_2)gL
$$

Semplificando $(m_1+m_2)$:

$$
\frac{1}{2}v_2^2=\mu_dgL
$$

da cui:

$$
v_2=\sqrt{2\mu_dgL}
$$

Sostituendo:

$$
v_2=
\sqrt{2(0.650)(9.8)(7.50)}
$$

$$
v_2=9.77\,m/s
$$

---

### 2. Urto proiettile-blocco

Il proiettile rimane conficcato nel blocco, quindi si tratta di un **urto completamente anelastico**.

Durante l'urto si conserva la quantità di moto:

$$
m_1v_1=(m_1+m_2)v_2
$$

Ricaviamo $v_1$:

$$
v_1=
\frac{m_1+m_2}{m_1}v_2
$$

Sostituendo:

$$
v_1=
\frac{12.0+100}{12.0}\cdot9.77
$$

$$
v_1=
\frac{112}{12.0}\cdot9.77
$$

$$
\boxed{v_1=91.2\,m/s}
$$

> [!important]
> **Metodo da ricordare:** il problema si risolve andando a ritroso.
>
> 1. Dallo spazio di arresto $L$ ricaviamo la velocità $v_2$ subito dopo l'urto tramite il **lavoro dell'attrito**.
> 2. Da $v_2$ risaliamo alla velocità iniziale $v_1$ del proiettile tramite la **conservazione della quantità di moto**.
>
> Durante l'urto **non si conserva l'energia cinetica**, perché l'urto è completamente anelastico.

## Esercizio – Secondo urto dopo il rimbalzo su una parete

### Traccia

Un punto materiale di massa $m_1=0.30\,kg$ si muove lungo l'asse $x$ con velocità:

$$
v=2.0\,m/s
$$

e urta elasticamente, nel punto $x=0$, un secondo punto di massa:

$$
m_2=0.40\,kg
$$

inizialmente fermo.

La massa $m_2$ raggiunge una parete posta a:

$$
x=70\,cm=0.70\,m
$$

e rimbalza senza perdere velocità.

Determinare **in quale posizione i due corpi si urtano nuovamente**.

### Soluzione

Dopo il primo urto elastico, con $m_2$ inizialmente fermo:

$$
v_1=
\frac{m_1-m_2}{m_1+m_2}v
$$

$$
v_2=
\frac{2m_1}{m_1+m_2}v
$$

Sostituendo:

$$
v_1=
\frac{0.30-0.40}{0.30+0.40}\cdot2.0
\approx -0.29\,m/s
$$

$$
v_2=
\frac{2(0.30)}{0.30+0.40}\cdot2.0
\approx1.71\,m/s
$$

La massa $m_1$ quindi torna verso sinistra, mentre $m_2$ va verso la parete.

### Tempo impiegato da $m_2$ per tornare all'origine

La massa $m_2$ percorre $0.70\,m$ fino alla parete e altri $0.70\,m$ per tornare all'origine:

$$
t_0=\frac{2L}{v_2}
$$

$$
t_0=\frac{2(0.70)}{1.71}\approx0.82\,s
$$

Nel frattempo $m_1$ si trova in:

$$
x_0=v_1t_0
$$

$$
x_0=(-0.29)(0.82)\approx-0.24\,m
$$

Da questo istante $m_2$ parte dall'origine verso sinistra, mentre $m_1$ continua a muoversi verso sinistra più lentamente.

Le loro posizioni sono:

$$
x_2=-v_2t
$$

$$
x_1=x_0+v_1t
$$

Quando si incontrano:

$$
-v_2t=x_0+v_1t
$$

da cui:

$$
t=-\frac{x_0}{v_1+v_2}
$$

La posizione dell'urto è:

$$
x=-v_2t
$$

e quindi:

$$
\boxed{x\approx-0.29\,m}
$$

> [!important]
> Il secondo urto avviene **29 cm a sinistra dell'origine**.

---

## Esercizio – Pendolo che urta elasticamente un blocco

### Traccia

Una palla di massa:

$$
m_1=0.500\,kg
$$

è appesa a un filo lungo:

$$
L=70.0\,cm=0.70\,m
$$

La palla viene lasciata cadere dalla posizione in cui il filo è orizzontale.

Nel punto più basso della traiettoria urta elasticamente un blocco fermo di massa:

$$
m_2=2.50\,kg
$$

posto su un piano orizzontale senza attrito.

Determinare:

1. la velocità della palla dopo l'urto;
2. la velocità del centro di massa.

### 1. Velocità prima dell'urto

La palla scende di un'altezza pari alla lunghezza del filo:

$$
h=L=0.70\,m
$$

Per la conservazione dell'energia meccanica:

$$
m_1gh=\frac{1}{2}m_1v_0^2
$$

da cui:

$$
v_0=\sqrt{2gh}
$$

$$
v_0=\sqrt{2(9.8)(0.70)}
\approx3.70\,m/s
$$

### 2. Velocità della palla dopo l'urto

Il blocco è inizialmente fermo e l'urto è elastico, quindi:

$$
v_1=
\frac{m_1-m_2}{m_1+m_2}v_0
$$

Sostituendo:

$$
v_1=
\frac{0.500-2.50}{0.500+2.50}\cdot3.70
$$

$$
\boxed{v_1\approx-2.47\,m/s}
$$

Il segno negativo indica che la palla **rimbalza indietro**.

### 3. Velocità del centro di massa

La velocità del centro di massa vale:

$$
v_{CM}=
\frac{m_1v_0+m_2v_{2,0}}{m_1+m_2}
$$

Poiché il blocco è inizialmente fermo:

$$
v_{2,0}=0
$$

quindi:

$$
v_{CM}=
\frac{m_1v_0}{m_1+m_2}
$$

$$
v_{CM}=
\frac{0.500\cdot3.70}{0.500+2.50}
$$

$$
\boxed{v_{CM}\approx0.62\,m/s}
$$

---

## Esercizio – Urto tra masse uguali con guida vincolante

### Traccia

Un punto materiale di massa $m$ si muove lungo una guida rettilinea senza attrito con velocità $v$.

Un secondo punto, anch'esso di massa $m$, si muove con la stessa velocità $v$ lungo una direzione **perpendicolare alla guida**.

Il secondo punto urta il primo e vi rimane attaccato.

Determinare:

1. il moto del centro di massa prima e dopo l'urto;
2. la reazione media esercitata dalla guida durante l'urto.

### Soluzione

L'urto è **completamente anelastico**, perché le due masse rimangono unite.

La guida impedisce il moto nella direzione perpendicolare, quindi lungo la direzione della guida si conserva la quantità di moto.

Prima dell'urto:

$$
p_x=mv
$$

Dopo l'urto la massa totale è $2m$:

$$
mv=2mV
$$

da cui:

$$
V=\frac{v}{2}
$$

---

### 1. Velocità del centro di massa

Indichiamo con $\hat{i}$ la direzione della guida e con $\hat{k}$ la direzione perpendicolare.

Prima dell'urto:

$$
\vec{v}_{CM,i}
=
\frac{mv\hat{i}+mv\hat{k}}{2m}
$$

quindi:

$$
\boxed{
\vec{v}_{CM,i}
=
\frac{v}{2}\hat{i}
+
\frac{v}{2}\hat{k}
}
$$

Dopo l'urto, le due masse sono vincolate a muoversi lungo la guida:

$$
\boxed{
\vec{v}_{CM,f}
=
\frac{v}{2}\hat{i}
}
$$

> [!note]
> La componente perpendicolare della velocità del centro di massa scompare perché la **guida esercita un impulso esterno** sul sistema.

---

### 2. Reazione della guida

Prima dell'urto la seconda massa possiede, nella direzione perpendicolare alla guida, quantità di moto:

$$
p_{\perp}=mv
$$

Dopo l'urto questa componente diventa nulla.

La guida deve quindi fornire un impulso di modulo:

$$
J=mv
$$

Essendo:

$$
J=R_{media}\Delta t
$$

si ottiene:

$$
\boxed{
R_{media}=\frac{mv}{\Delta t}
}
$$

dove $\Delta t$ è la durata dell'urto.

> [!important]
> In questo esercizio la quantità di moto totale **non si conserva in tutte le direzioni**, perché la guida esercita una forza esterna.
>
> Si conserva soltanto la componente della quantità di moto **lungo la guida**.


## Esercizio – Urto tra due blocchi

### Traccia

Un blocco di massa:

$$
m_1=5.0\,kg
$$

si muove con velocità:

$$
v_{1,i}=3.0\,m/s
$$

e urta un secondo blocco di massa:

$$
m_2=10\,kg
$$

che si muove nella stessa direzione con velocità:

$$
v_{2,i}=2.0\,m/s
$$

Dopo l'urto, il blocco più grande procede con velocità:

$$
v_{2,f}=2.5\,m/s
$$

Determinare:

1. la velocità finale del blocco più piccolo;
2. la variazione dell'energia cinetica totale del sistema.

---

### 1. Velocità finale del blocco piccolo

Si conserva la quantità di moto:

$$
m_1v_{1,i}+m_2v_{2,i}
=
m_1v_{1,f}+m_2v_{2,f}
$$

Ricaviamo $v_{1,f}$:

$$
v_{1,f}
=
v_{1,i}
+
\frac{m_2}{m_1}(v_{2,i}-v_{2,f})
$$

Sostituendo:

$$
v_{1,f}
=
3.0+
\frac{10}{5}(2.0-2.5)
$$

$$
\boxed{v_{1,f}=2.0\,m/s}
$$

---

### 2. Variazione dell'energia cinetica

La variazione dell'energia cinetica totale è:

$$
\Delta K=K_f-K_i
$$

quindi:

$$
\Delta K
=
\frac{1}{2}m_1(v_{1,f}^2-v_{1,i}^2)
+
\frac{1}{2}m_2(v_{2,f}^2-v_{2,i}^2)
$$

Sostituendo:

$$
\Delta K
=
\frac{1}{2}(5)(2.0^2-3.0^2)
+
\frac{1}{2}(10)(2.5^2-2.0^2)
$$

$$
\boxed{\Delta K=-1.25\,J}
$$

> [!important]
> Il valore negativo indica che l'energia cinetica totale **diminuisce** durante l'urto.
>
> Quindi l'urto è **anelastico** e vengono dissipati:
>
> $$
> 1.25\,J
> $$


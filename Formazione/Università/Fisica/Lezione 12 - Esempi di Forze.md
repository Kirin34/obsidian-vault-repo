## Lezione 12 — Sistemi non inerziali e ascensore in caduta libera

### Sistemi inerziali e non inerziali

Le leggi della dinamica valgono direttamente nei **sistemi di riferimento inerziali**.

Un sistema di riferimento è **inerziale** quando è fermo oppure si muove di **moto rettilineo uniforme** rispetto a un altro sistema inerziale.

Un sistema è invece **non inerziale** quando si muove con accelerazione oppure ruota rispetto a un sistema inerziale.

Esempi di sistemi non inerziali:

- un ascensore che accelera o scende;
- un’automobile che frena;
- una giostra che ruota;
- un sistema in caduta libera.

Nei sistemi non inerziali possono comparire delle forze che sembrano agire sul corpo, ma che non derivano da una vera interazione fisica. Queste sono dette **forze apparenti** o **forze fittizie**.

---

### Passaggio da sistema inerziale a sistema non inerziale

Nel sistema inerziale vale la seconda legge della dinamica:

$$
\vec{F} = m\vec{a}
$$

Nel passaggio a un sistema non inerziale, l’accelerazione può essere scritta come somma di più contributi:

$$
\vec{a} = \vec{a}^{\,\prime} + \vec{a}_t + \vec{a}_c
$$

dove:

- $\vec{a}$ è l’accelerazione vista dal sistema inerziale;
- $\vec{a}^{\,\prime}$ è l’accelerazione vista dal sistema non inerziale;
- $\vec{a}_t$ è l’accelerazione di trascinamento;
- $\vec{a}_c$ è l’accelerazione di Coriolis.

Sostituendo nella seconda legge di Newton:

$$
\vec{F} = m\vec{a}^{\,\prime} + m\vec{a}_t + m\vec{a}_c
$$

Portando gli ultimi due termini dall’altra parte:

$$
m\vec{a}^{\,\prime} = \vec{F} - m\vec{a}_t - m\vec{a}_c
$$

Quindi, nel sistema non inerziale:

$$
\vec{F}^{\,\prime} = m\vec{a}^{\,\prime} = \vec{F} + \vec{F}_t + \vec{F}_c
$$

dove:

$$
\vec{F}_t = -m\vec{a}_t
$$

$$
\vec{F}_c = -m\vec{a}_c
$$

Le forze $\vec{F}_t$ e $\vec{F}_c$ sono **forze apparenti**.

Non sono forze reali, perché non nascono da un’interazione tra due corpi. Compaiono solo perché stiamo osservando il moto da un sistema di riferimento accelerato o rotante.

---

## Ascensore in caduta libera

Il caso dell’ascensore è utile per capire cosa succede in un sistema non inerziale.

Immaginiamo un corpo di massa $m$ poggiato su una bilancia dentro un ascensore.

La bilancia misura la **reazione vincolare** $R$, cioè la forza normale esercitata dalla bilancia sul corpo.

Questa forza è anche detta **peso apparente**, perché indica quanto “sembra pesare” il corpo dentro l’ascensore.

---

### Ascensore fermo

Se l’ascensore è fermo, il corpo è in equilibrio.

Sul corpo agiscono due forze:

- il peso $mg$, diretto verso il basso;
- la reazione della bilancia $R$, diretta verso l’alto.

In equilibrio:

$$
R = mg
$$

Quindi la bilancia misura il peso normale del corpo.

---

### Ascensore accelerato verso l’alto

Se l’ascensore accelera verso l’alto con accelerazione $a_R$, il corpo sembra pesare di più.

La bilancia deve esercitare una reazione maggiore per sostenere il corpo e farlo accelerare verso l’alto.

La bilancia misura:

$$
R = m(g + a_R)
$$

Quindi:

$$
R > mg
$$

In questo caso il peso apparente aumenta.

Esempio: quando un ascensore parte verso l’alto, per un attimo ci sentiamo più “schiacciati” verso il pavimento.

---

### Ascensore accelerato verso il basso con $a_R < g$

Se l’ascensore accelera verso il basso con accelerazione $a_R$ minore di $g$, il corpo sembra pesare di meno.

La bilancia misura:

$$
R = m(g - a_R)
$$

Quindi:

$$
R < mg
$$

In questo caso il peso apparente diminuisce.

Esempio: quando l’ascensore inizia a scendere, per un attimo ci sentiamo più leggeri.

---

### Ascensore in caduta libera

Il caso limite si ha quando l’ascensore cade liberamente.

In caduta libera:

$$
a_R = g
$$

Sostituendo nella formula:

$$
R = m(g - g)
$$

quindi:

$$
R = 0
$$

La bilancia misura un peso nullo.

Questo non significa che la forza di gravità sia scomparsa. La gravità continua ad agire, ma ascensore, bilancia e corpo cadono tutti insieme con la stessa accelerazione.

Per questo motivo il corpo non preme più sulla bilancia.

Si parla quindi di **assenza apparente di peso**.

---

### Caso con accelerazione verso il basso maggiore di $g$

Se l’ascensore accelerasse verso il basso con accelerazione maggiore di $g$, cioè:

$$
a_R > g
$$

allora la forza apparente sarebbe più intensa del peso.

Nel sistema dell’ascensore il corpo sembrerebbe accelerare verso l’alto rispetto all’ascensore.

La risultante apparente sarebbe:

$$
F^{\,\prime} = m(a_R - g)
$$

Questo caso indica che il corpo perderebbe il contatto con la bilancia, perché la bilancia non può esercitare una reazione negativa.

---

## Riassunto finale

Nei sistemi inerziali vale direttamente:

$$
\vec{F} = m\vec{a}
$$

Nei sistemi non inerziali, invece, bisogna aggiungere le **forze apparenti** per descrivere correttamente il moto.

Nel caso dell’ascensore:

- se è fermo, la bilancia misura il peso normale:

$$
R = mg
$$

- se accelera verso l’alto, il corpo sembra pesare di più:

$$
R = m(g + a_R)
$$

- se accelera verso il basso con $a_R < g$, il corpo sembra pesare di meno:

$$
R = m(g - a_R)
$$

- se è in caduta libera, la bilancia misura zero:

$$
R = 0
$$

Il concetto fondamentale è che la bilancia non misura direttamente la forza peso, ma misura la reazione vincolare $R$, cioè il peso apparente del corpo.

## Forza centrifuga

La **forza centrifuga** è una forza apparente o fittizia che si manifesta quando ci troviamo in un sistema di riferimento **rotante**, quindi non inerziale.

Consideriamo una massa $m$ ferma sul bordo di una piattaforma circolare di raggio $R$, che ruota con velocità angolare costante $\omega$.

Per un osservatore solidale con la piattaforma, cioè che ruota insieme ad essa, la massa appare ferma.  
Quindi, nel sistema rotante:

$$
\vec{a}^{\,\prime} = 0
$$

e anche la velocità relativa è nulla.

Tuttavia, rispetto a un sistema inerziale esterno, la massa sta compiendo un moto circolare. Per rimanere sulla traiettoria circolare deve esserci una forza reale diretta verso il centro: la **forza centripeta**.

La forza centripeta vale:

$$
F_c = m \omega^2 R
$$

ed è diretta verso il centro della circonferenza.

---

### Interpretazione nel sistema rotante

Nel sistema solidale con la piattaforma, la massa è ferma.  
Se è ferma, la risultante delle forze deve essere nulla.

Per ottenere equilibrio nel sistema rotante, oltre alla forza centripeta reale diretta verso il centro, bisogna introdurre una forza apparente diretta verso l’esterno: la **forza centrifuga**.

La forza centrifuga ha modulo:

$$
F_{cf} = m \omega^2 R
$$

ed è diretta radialmente verso l’esterno.

In forma vettoriale:

$$
\vec{F}_{cf} = m \omega^2 \vec{r}^{\,\prime}
$$

dove $\vec{r}^{\,\prime}$ è il vettore radiale diretto dal centro verso l’esterno.

---

### Equilibrio nel sistema rotante

Nel sistema rotante la massa è ferma, quindi:

$$
\vec{a}^{\,\prime} = 0
$$

Per questo la forza centripeta reale e la forza centrifuga apparente si annullano:

$$
\vec{F}_{centripeta} + \vec{F}_{centrifuga} = 0
$$

La forza centripeta tira il corpo verso il centro, mentre la forza centrifuga apparente sembra spingerlo verso l’esterno.

---

## Idea fondamentale

La **forza centrifuga** non è una forza reale: compare solo perché stiamo osservando il moto da un sistema di riferimento rotante.

Nel sistema inerziale esterno si vede solo la forza centripeta, che mantiene il corpo in moto circolare.

Nel sistema rotante, invece, siccome il corpo sembra fermo, dobbiamo introdurre una forza apparente verso l’esterno per spiegare l’equilibrio.

In sintesi:

- la **forza centripeta** è reale ed è diretta verso il centro;
- la **forza centrifuga** è apparente ed è diretta verso l’esterno;
- nel sistema rotante le due forze si bilanciano;
- la forza centrifuga nasce dal fatto che il sistema di riferimento è non inerziale.

## La forza di Coriolis

La **forza di Coriolis** è una forza apparente che compare quando osserviamo il moto di un corpo da un sistema di riferimento **rotante**, come la Terra.

È una forza fittizia perché non nasce da una vera interazione fisica, ma dal fatto che il sistema di riferimento ruota.

La forza di Coriolis diventa importante quando un corpo si muove rispetto al sistema rotante.

---

## Formula della forza di Coriolis

Se un corpo ha velocità relativa $\vec{v}^{\,\prime}$ rispetto al sistema rotante, allora compare una forza apparente detta forza di Coriolis.

Come accelerazione apparente:

$$
\vec{a}_c = -2(\vec{\omega} \times \vec{v}^{\,\prime})
$$

Come forza:

$$
\vec{F}_c = -2m(\vec{\omega} \times \vec{v}^{\,\prime})
$$

dove:

- $m$ è la massa del corpo;
- $\vec{\omega}$ è la velocità angolare di rotazione del sistema;
- $\vec{v}^{\,\prime}$ è la velocità del corpo rispetto al sistema rotante;
- $\times$ indica il prodotto vettoriale.

Il segno e la direzione della forza dipendono dal prodotto vettoriale tra $\vec{\omega}$ e $\vec{v}^{\,\prime}$.

---

## Significato fisico

La forza di Coriolis non cambia direttamente il modulo della velocità del corpo, ma devia la sua traiettoria.

Questo effetto è particolarmente evidente sulla Terra, perché la Terra ruota.

Quindi un corpo che si muove sulla superficie terrestre non segue esattamente una traiettoria rettilinea rispetto alla superficie, ma tende a deviare.

---

## Corpo in caduta verso il centro della Terra

Se un corpo cade verso il centro della Terra, quindi ha una velocità diretta circa verso il basso, la forza di Coriolis lo devia verso Est.

Questo accade perché il corpo conserva parte della velocità dovuta alla rotazione terrestre.

Quindi, durante la caduta, il corpo non cade perfettamente lungo la verticale, ma subisce una piccola deviazione.

---

## Moto lungo un meridiano

Se un corpo si muove lungo un meridiano, cioè in direzione Nord-Sud o Sud-Nord, la forza di Coriolis provoca una deviazione laterale.

Nell’emisfero boreale, cioè nell’emisfero Nord, i corpi in movimento vengono deviati verso destra rispetto al loro verso di moto.

Nell’emisfero australe, cioè nell’emisfero Sud, i corpi vengono deviati verso sinistra rispetto al loro verso di moto.

Quindi:

- nell’emisfero Nord: deviazione verso destra;
- nell’emisfero Sud: deviazione verso sinistra.

---

## Effetto sui venti

La forza di Coriolis influenza il movimento delle masse d’aria.

Per questo motivo i venti non si muovono semplicemente in linea retta dalle zone di alta pressione alle zone di bassa pressione, ma vengono deviati.

A causa della rotazione terrestre:

- nell’emisfero Nord i venti deviano verso destra;
- nell’emisfero Sud i venti deviano verso sinistra.

Questo effetto è molto importante nella formazione dei grandi sistemi atmosferici.

---

## Effetto sulle correnti marine

La forza di Coriolis influenza anche la circolazione delle correnti marine.

Le correnti oceaniche vengono deviate dalla rotazione terrestre e tendono a formare grandi circolazioni.

Per questo motivo l’effetto di Coriolis è una delle cause che determinano il senso della circolazione delle correnti marine.

---

## Riassunto finale

La forza di Coriolis è una forza apparente che compare nei sistemi rotanti quando un corpo si muove rispetto al sistema.

Sulla Terra è importante perché la Terra ruota.

La sua espressione è:

$$
\vec{F}_c = -2m(\vec{\omega} \times \vec{v}^{\,\prime})
$$

Essa provoca una deviazione della traiettoria dei corpi in movimento.

Gli effetti principali sono:

- deviazione dei corpi in caduta;
- deviazione dei venti;
- deviazione delle correnti marine;
- deviazione verso destra nell’emisfero Nord;
- deviazione verso sinistra nell’emisfero Sud.

La cosa fondamentale da ricordare è che la forza di Coriolis non è una forza reale, ma una forza apparente dovuta al fatto che osserviamo il moto da un sistema rotante.

## La forza di Coriolis

La **forza di Coriolis** è una forza apparente che compare quando osserviamo il moto di un corpo da un sistema di riferimento **rotante**, come la Terra.

È una forza fittizia perché non nasce da una vera interazione fisica, ma dal fatto che il sistema di riferimento ruota.

La forza di Coriolis diventa importante quando un corpo si muove rispetto al sistema rotante.

---

## Formula della forza di Coriolis

Se un corpo ha velocità relativa $\vec{v}^{\,\prime}$ rispetto al sistema rotante, allora compare una forza apparente detta forza di Coriolis.

Come accelerazione apparente:

$$
\vec{a}_c = -2(\vec{\omega} \times \vec{v}^{\,\prime})
$$

Come forza:

$$
\vec{F}_c = -2m(\vec{\omega} \times \vec{v}^{\,\prime})
$$

dove:

- $m$ è la massa del corpo;
- $\vec{\omega}$ è la velocità angolare di rotazione del sistema;
- $\vec{v}^{\,\prime}$ è la velocità del corpo rispetto al sistema rotante;
- $\times$ indica il prodotto vettoriale.

Il segno e la direzione della forza dipendono dal prodotto vettoriale tra $\vec{\omega}$ e $\vec{v}^{\,\prime}$.

---

## Significato fisico

La forza di Coriolis non cambia direttamente il modulo della velocità del corpo, ma devia la sua traiettoria.

Questo effetto è particolarmente evidente sulla Terra, perché la Terra ruota.

Quindi un corpo che si muove sulla superficie terrestre non segue esattamente una traiettoria rettilinea rispetto alla superficie, ma tende a deviare.

---

## Corpo in caduta verso il centro della Terra

Se un corpo cade verso il centro della Terra, quindi ha una velocità diretta circa verso il basso, la forza di Coriolis lo devia verso Est.

Questo accade perché il corpo conserva parte della velocità dovuta alla rotazione terrestre.

Quindi, durante la caduta, il corpo non cade perfettamente lungo la verticale, ma subisce una piccola deviazione.

---

## Moto lungo un meridiano

Se un corpo si muove lungo un meridiano, cioè in direzione Nord-Sud o Sud-Nord, la forza di Coriolis provoca una deviazione laterale.

Nell’emisfero boreale, cioè nell’emisfero Nord, i corpi in movimento vengono deviati verso destra rispetto al loro verso di moto.

Nell’emisfero australe, cioè nell’emisfero Sud, i corpi vengono deviati verso sinistra rispetto al loro verso di moto.

Quindi:

- nell’emisfero Nord: deviazione verso destra;
- nell’emisfero Sud: deviazione verso sinistra.

---

## Effetto sui venti

La forza di Coriolis influenza il movimento delle masse d’aria.

Per questo motivo i venti non si muovono semplicemente in linea retta dalle zone di alta pressione alle zone di bassa pressione, ma vengono deviati.

A causa della rotazione terrestre:

- nell’emisfero Nord i venti deviano verso destra;
- nell’emisfero Sud i venti deviano verso sinistra.

Questo effetto è molto importante nella formazione dei grandi sistemi atmosferici.

---

## Effetto sulle correnti marine

La forza di Coriolis influenza anche la circolazione delle correnti marine.

Le correnti oceaniche vengono deviate dalla rotazione terrestre e tendono a formare grandi circolazioni.

Per questo motivo l’effetto di Coriolis è una delle cause che determinano il senso della circolazione delle correnti marine.

---

## Riassunto finale

La forza di Coriolis è una forza apparente che compare nei sistemi rotanti quando un corpo si muove rispetto al sistema.

Sulla Terra è importante perché la Terra ruota.

La sua espressione è:

$$
\vec{F}_c = -2m(\vec{\omega} \times \vec{v}^{\,\prime})
$$

Essa provoca una deviazione della traiettoria dei corpi in movimento.

Gli effetti principali sono:

- deviazione dei corpi in caduta;
- deviazione dei venti;
- deviazione delle correnti marine;
- deviazione verso destra nell’emisfero Nord;
- deviazione verso sinistra nell’emisfero Sud.

La cosa fondamentale da ricordare è che la forza di Coriolis non è una forza reale, ma una forza apparente dovuta al fatto che osserviamo il moto da un sistema rotante.

## Esercizi — Sistemi non inerziali

---

# Esercizio 1 — Corpo rotante con due fili

Un corpo di massa:

$$
m = 1{,}34 \, kg
$$

ruota intorno a un asse verticale ed è collegato a un’asta tramite due fili senza massa lunghi:

$$
L = 1{,}70 \, m
$$

I due fili formano con l’asta un triangolo equilatero.

La tensione del filo superiore è:

$$
T_1 = 35 \, N
$$

Bisogna trovare la **forza centrifuga** sperimentata nel sistema solidale con il corpo.

---

## Dati importanti

Poiché il triangolo è equilatero, l’angolo considerato nelle formule è:

$$
\theta = 30^\circ
$$

quindi:

$$
\sin\theta = 0{,}5
$$

e

$$
\cos\theta \simeq 0{,}866
$$

---

## Equilibrio verticale

Il corpo non accelera verticalmente, quindi la somma delle forze verticali deve essere nulla.

Le componenti verticali delle due tensioni sono opposte:

- la componente verticale di $T_1$ è verso l’alto;
- la componente verticale di $T_2$ è verso il basso;
- il peso $mg$ è verso il basso.

L’equazione verticale è:

$$
(T_1 - T_2)\sin\theta - mg = 0
$$

Da cui:

$$
(T_1 - T_2)\sin\theta = mg
$$

Isoliamo $T_2$:

$$
T_2 = T_1 - \frac{mg}{\sin\theta}
$$

Sostituendo i valori:

$$
T_2 = 35 - \frac{1{,}34 \cdot 9{,}8}{0{,}5}
$$

$$
T_2 = 35 - 26{,}26
$$

$$
T_2 = 8{,}74 \, N
$$

---

## Forza centripeta e forza centrifuga

Le componenti orizzontali delle due tensioni sono entrambe dirette verso l’asse di rotazione.

Queste componenti forniscono la **forza centripeta**:

$$
F_{centripeta} = (T_1 + T_2)\cos\theta
$$

Sostituendo:

$$
F_{centripeta} = (35 + 8{,}74)\cdot 0{,}866
$$

$$
F_{centripeta} \simeq 37{,}9 \, N
$$

Nel sistema solidale con il corpo, cioè nel sistema rotante, si introduce una **forza centrifuga apparente** uguale in modulo e opposta alla forza centripeta.

Quindi:

$$
F_{centrifuga} = 37{,}9 \, N
$$

---

## Risultato esercizio 1

$$
\boxed{F_{centrifuga} = 37{,}9 \, N}
$$

La forza centrifuga è diretta verso l’esterno rispetto all’asse di rotazione.

---

# Esercizio 2 — Cassa su un furgone che frena

Un osservatore $O'$ si trova su un furgone che inizialmente viaggia a velocità costante.

Nel furgone c’è una cassa di massa:

$$
m = 0{,}25 \, kg
$$

La cassa può scorrere senza attrito sul pavimento.

A un certo punto il furgone frena con decelerazione costante:

$$
a = 2{,}8 \, m/s^2
$$

---

## Punto di vista dell’osservatore esterno

L’osservatore esterno, fermo rispetto alla strada, si trova in un sistema di riferimento inerziale.

Poiché sulla cassa non agisce attrito, non c’è una forza orizzontale reale che la faccia frenare insieme al furgone.

Quindi l’osservatore esterno vede la cassa continuare a muoversi di moto rettilineo uniforme, con la velocità che aveva prima della frenata.

In pratica:

- il furgone rallenta;
- la cassa continua ad avanzare;
- quindi rispetto al furgone la cassa sembra muoversi in avanti.

---

## Punto di vista dell’osservatore sul furgone

L’osservatore $O'$ è solidale con il furgone.

Quando il furgone frena, il sistema di riferimento del furgone è **non inerziale**, perché sta accelerando, in questo caso decelerando.

Per spiegare il moto della cassa dentro il furgone, l’osservatore $O'$ introduce una **forza fittizia**.

Questa forza è diretta nel verso del moto iniziale del furgone, cioè in avanti.

Il modulo della forza fittizia è:

$$
F' = ma
$$

Sostituendo:

$$
F' = 0{,}25 \cdot 2{,}8
$$

$$
F' = 0{,}7 \, N
$$

---

## Risultato esercizio 2

$$
\boxed{F' = 0{,}7 \, N}
$$

La forza fittizia è diretta in avanti, cioè nella direzione del moto del furgone prima della frenata.

---

## Riassunto concettuale

Nel primo esercizio, il corpo ruota: nel sistema rotante compare una **forza centrifuga apparente** diretta verso l’esterno.

Nel secondo esercizio, il furgone frena: nel sistema del furgone compare una **forza fittizia** diretta in avanti.

In entrambi i casi le forze fittizie non sono forze reali, ma servono per descrivere il moto in un sistema di riferimento non inerziale.


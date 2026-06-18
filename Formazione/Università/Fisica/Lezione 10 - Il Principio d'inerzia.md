La **seconda legge della dinamica**, detta anche **legge di Newton**, mette in relazione la forza applicata a un corpo con l'accelerazione che esso subisce.

La formula fondamentale è:

$$
F = ma
$$

dove:

- $F$ è la forza applicata;
- $m$ è la massa del corpo;
- $a$ è l'accelerazione prodotta dalla forza.

Questa legge significa che una forza applicata a un corpo genera un'accelerazione proporzionale alla forza stessa e inversamente collegata alla massa del corpo.

Se la forza è nulla, anche l'accelerazione è nulla:

$$
F = 0 \Rightarrow a = 0
$$

Quindi il corpo mantiene il suo stato di quiete o di moto rettilineo uniforme, come stabilito dal principio di inerzia.

La massa è una grandezza scalare, mentre la forza è una grandezza vettoriale: infatti una forza ha modulo, direzione e verso.

### Unità di misura della forza

Nel Sistema Internazionale, la forza si misura in **Newton**, indicato con il simbolo **N**.

Un Newton è la forza necessaria per imprimere a un corpo di massa $1 \ kg$ un'accelerazione di $1 \ m/s^2$.

$$
1 \ N = 1 \ kg \cdot m/s^2
$$

Le dimensioni fisiche della forza sono:

$$
[F] = [M L T^{-2}]
$$

Questo deriva dal fatto che:

$$
F = ma
$$

quindi:

- la massa ha dimensione $[M]$;
- l'accelerazione ha dimensione $[L T^{-2}]$;
- la forza ha dimensione $[M L T^{-2}]$.

## Risultante delle forze

Poiché la forza è una **grandezza vettoriale**, quando su un corpo agiscono più forze non si può sommarle come semplici numeri, ma bisogna fare la **somma vettoriale**.

Se su un punto materiale agiscono più forze:

$$
\vec{F}_1, \vec{F}_2, \dots, \vec{F}_N
$$

la forza complessiva che produce il moto si chiama **risultante delle forze**:

$$
\vec{R} = \sum_i \vec{F}_i
$$

La seconda legge della dinamica, nel caso generale di più forze applicate, diventa:

$$
\vec{R} = \sum_i \vec{F}_i = m \sum_i \vec{a}_i = m\vec{a}
$$

Questo significa che ogni forza contribuisce all'accelerazione del corpo e il moto finale dipende dalla **somma vettoriale** di tutte le forze applicate.

In pratica, invece di studiare separatamente ogni forza, possiamo sostituire tutte le forze con una sola forza equivalente: la **risultante**.

---

## Equilibrio statico

Se la risultante delle forze è nulla:

$$
\vec{R} = 0
$$

allora anche l'accelerazione è nulla:

$$
\vec{a} = 0
$$

Se il corpo era inizialmente fermo, rimane fermo. In questo caso si dice che il corpo è in **equilibrio statico**.

Quindi la condizione di equilibrio statico è:

$$
\sum_i \vec{F}_i = 0
$$

---

## Somma vettoriale delle forze

Con le forze si possono fare le stesse operazioni che si fanno con i vettori.

### Forze con direzioni diverse

Se due forze hanno direzioni diverse, si usa la **regola del parallelogramma**.

Date due forze:

$$
\vec{F}_1
$$

e

$$
\vec{F}_2
$$

si costruisce un parallelogramma avente come lati i due vettori forza. La diagonale del parallelogramma rappresenta la risultante:

$$
\vec{F}_r = \vec{F}_1 + \vec{F}_2
$$

---

## Caso particolare: forze perpendicolari

Se le due forze sono **perpendicolari**, cioè formano un angolo di 90°, il modulo della risultante si calcola con il teorema di Pitagora:

$$
F_r = \sqrt{(F_1)^2 + (F_2)^2}
$$

Questo perché le due forze rappresentano i cateti di un triangolo rettangolo, mentre la risultante rappresenta l'ipotenusa.

---

## Somma di tre forze

Per sommare tre forze si applica più volte la regola del parallelogramma.

Date tre forze:

$$
\vec{F}_1, \vec{F}_2, \vec{F}_3
$$

si procede così:

1. si sommano prima due forze, ad esempio:

$$
\vec{F}_{12} = \vec{F}_1 + \vec{F}_2
$$

2. poi si somma la risultante ottenuta con la terza forza:

$$
\vec{F}_r = \vec{F}_{12} + \vec{F}_3
$$

## Dinamica e legge oraria del moto

La **seconda legge della dinamica** collega la dinamica con la cinematica, perché permette di determinare l'accelerazione di un corpo a partire dalle forze che agiscono su di esso.

La dinamica studia le **cause del moto**, cioè le forze.

La cinematica studia il moto senza preoccuparsi delle sue cause.

La seconda legge di Newton:

$$
\vec{F} = m\vec{a}
$$

permette quindi di passare dalle forze all'accelerazione e, conoscendo l'accelerazione, si può poi ricavare la legge oraria del moto.

Poiché la forza e l'accelerazione sono grandezze vettoriali, la legge può essere scomposta lungo gli assi cartesiani:

$$
\frac{d^2x}{dt^2} = \frac{\sum_i F_{x,i}(t)}{m}
$$

$$
\frac{d^2y}{dt^2} = \frac{\sum_i F_{y,i}(t)}{m}
$$

$$
\frac{d^2z}{dt^2} = \frac{\sum_i F_{z,i}(t)}{m}
$$

Queste formule dicono che l'accelerazione lungo ogni asse dipende dalla somma delle componenti delle forze lungo quello stesso asse.

In pratica:

- se conosco le forze e la massa, posso trovare l'accelerazione;
- se conosco l'accelerazione, posso studiare il moto;
- se conosco la legge oraria del moto, posso risalire alla dinamica del problema e quindi alle forze coinvolte.

---

## Terzo principio della dinamica: azione e reazione

Il **terzo principio della dinamica** afferma che, in un sistema inerziale, se un corpo A esercita una forza su un corpo B, allora il corpo B esercita una forza sul corpo A uguale in modulo e direzione, ma opposta in verso.

La relazione è:

$$
\vec{F}_{B-A} = -\vec{F}_{A-B}
$$

Questo principio è detto anche **principio di azione e reazione**.

La frase classica è:

> A ogni azione corrisponde una reazione uguale e contraria.

Le due forze:

- hanno lo stesso modulo;
- hanno la stessa direzione;
- hanno verso opposto;
- agiscono sulla stessa retta di applicazione;
- agiscono però su corpi diversi.

Questo ultimo punto è fondamentale: azione e reazione non si annullano tra loro perché non sono applicate allo stesso corpo.

Esempio: se un corpo A spinge un corpo B, anche B spinge A con una forza uguale e opposta.

---

## Riassunto dei principi della dinamica

Nel caso dei **sistemi inerziali**, i tre principi della dinamica sono:

### 1. Primo principio della dinamica

Se la risultante delle forze è nulla, il corpo mantiene velocità costante:

$$
\vec{F} = 0 \Longleftrightarrow \vec{v} = costante
$$

Questo è il **principio di inerzia**.

Significa che un corpo fermo resta fermo e un corpo in moto continua a muoversi di moto rettilineo uniforme, se non agiscono forze risultanti su di esso.

---

### 2. Secondo principio della dinamica

Se la risultante delle forze è diversa da zero, il corpo subisce un'accelerazione:

$$
\vec{F} \neq 0 \Rightarrow \vec{F} = m\vec{a}
$$

La forza risultante è proporzionale alla massa e all'accelerazione.

Questa è la legge fondamentale della dinamica.

---

### 3. Terzo principio della dinamica

Se un corpo A esercita una forza su un corpo B, allora B esercita su A una forza uguale e opposta:

$$
\vec{F}_{AB} = -\vec{F}_{BA}
$$

Questo è il **principio di azione e reazione**.

---

## Importanza delle leggi di Newton

I principi della dinamica sono anche chiamati **leggi di Newton**.

Sono principi fondamentali perché non si dimostrano matematicamente a partire da altre leggi, ma derivano dall'esperienza e dall'osservazione dei fenomeni fisici.

Essi costituiscono la base della **meccanica classica**, valida per corpi di dimensioni maggiori rispetto a quelle atomiche e che si muovono a velocità molto più piccole rispetto alla velocità della luce.

## La reazione vincolare

Quando un corpo è soggetto a una risultante non nulla di forze, per farlo rimanere fermo è necessario che intervenga un dispositivo fisso capace di esercitare una forza uguale e opposta alla forza applicata.

Questo dispositivo prende il nome di **vincolo**.

La forza esercitata dal vincolo sul corpo si chiama **reazione vincolare**.

In questo modo si ristabiliscono le condizioni di equilibrio statico, perché la somma delle forze agenti sul corpo diventa nulla.

Un esempio classico è un oggetto appoggiato su un tavolo.

Sul corpo agisce la forza peso:

$$
\vec{P}
$$

diretta verso il basso.

Il tavolo esercita invece una forza verso l’alto, detta reazione vincolare:

$$
\vec{R}_v
$$

Affinché il corpo sia in equilibrio, deve valere:

$$
\vec{R}_v + \vec{P} = 0
$$

Quindi:

$$
\vec{R}_v = -\vec{P}
$$

Le due forze hanno stesso modulo e direzione, ma verso opposto.

![[Pasted image 20260618231947.png]]

---

## Esempi di reazione vincolare

Un esempio tipico di reazione vincolare è quella esercitata da un tavolo su un oggetto appoggiato sopra di esso.

L’oggetto, a causa della gravità, tende a muoversi verso il basso. Il tavolo però impedisce questo movimento e applica sull’oggetto una forza verso l’alto.

In questo caso l’oggetto resta fermo perché la forza peso e la reazione del tavolo si bilanciano.

Un altro esempio è quello di un corpo appeso a un filo fissato a una parete.

Il corpo subisce la forza di gravità verso il basso, ma il filo esercita una forza opposta, impedendo al corpo di cadere.

Anche in questo caso il vincolo produce una forza che si oppone al moto che il corpo avrebbe sotto l’azione delle altre forze.

Il concetto di reazione vincolare viene introdotto per descrivere situazioni di equilibrio statico, ma può essere esteso anche a situazioni dinamiche.

---

## Massa inerziale e massa gravitazionale

Attraverso la seconda legge della dinamica:

$$
\vec{F} = m\vec{a}
$$

è possibile definire la massa come una grandezza scalare legata al rapporto tra forza applicata e accelerazione prodotta.

Infatti:

$$
m = \frac{F}{a}
$$

Questa definizione descrive la **massa inerziale**.

La massa inerziale rappresenta la resistenza che un corpo oppone alla variazione del proprio stato di moto.

A parità di forza applicata:

- se la massa è maggiore, l’accelerazione prodotta è minore;
- se la massa è minore, l’accelerazione prodotta è maggiore.

Quindi maggiore è la massa di un corpo, maggiore è la sua **inerzia**, cioè la sua tendenza a opporsi alle variazioni del moto.

In altre parole, un corpo molto massiccio è più difficile da accelerare o da frenare rispetto a un corpo meno massiccio.

---

## Definizione operativa di forza

La forza può essere misurata tramite un **dinamometro a deformazione**.

Il dinamometro funziona associando l’allungamento di una molla alla forza applicata.

Maggiore è la forza applicata, maggiore sarà la deformazione della molla.

In questo modo è possibile misurare la forza in maniera operativa, cioè attraverso un effetto osservabile.


## Esercizio — Moto con forza costante

Un punto materiale di massa:

$$
m = 2 \ kg
$$

parte dall’origine con velocità iniziale:

$$
v_0 = 5 \ m/s
$$

diretta lungo l’asse $y$.  
Sul corpo agisce una forza costante:

$$
F = 4 \ N
$$

diretta lungo l’asse $x$.

Per la seconda legge della dinamica:

$$
F = ma
$$

quindi l’accelerazione lungo $x$ è:

$$
a_x = \frac{F}{m} = \frac{4}{2} = 2 \ m/s^2
$$

Il moto lungo $x$ è uniformemente accelerato:

$$
x = \frac{1}{2}a_xt^2
$$

quindi:

$$
x = t^2
$$

Il moto lungo $y$ è uniforme:

$$
y = v_0t = 5t
$$

Ricavando il tempo da $x = t^2$:

$$
t = \sqrt{x}
$$

e sostituendo in $y = 5t$:

$$
y = 5\sqrt{x}
$$

La traiettoria del punto è quindi:

$$
y = 5\sqrt{x}
$$

---

## Quesiti teorici

### Q.1 — Seconda legge della dinamica

La forza totale applicata a un corpo è uguale al prodotto tra massa e accelerazione:

$$
\vec{F} = m\vec{a}
$$

---

### Q.2 — Relatività galileiana

La seconda legge è valida in tutti i sistemi inerziali.  
Se due sistemi si muovono di moto rettilineo uniforme uno rispetto all’altro, l’accelerazione resta la stessa:

$$
\vec{a}' = \vec{a}
$$

Poiché anche la massa non cambia:

$$
\vec{F}' = m\vec{a}' = m\vec{a} = \vec{F}
$$

Quindi la legge di Newton è invariata.

---

### Q.3 — Terza legge della dinamica

Se un corpo A esercita una forza su un corpo B, allora B esercita su A una forza uguale e opposta:

$$
\vec{F}_{A-B} = -\vec{F}_{B-A}
$$

Questo è il principio di azione e reazione.
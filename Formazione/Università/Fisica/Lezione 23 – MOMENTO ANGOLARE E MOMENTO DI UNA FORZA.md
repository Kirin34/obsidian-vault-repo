## Momento di un vettore

Dato un vettore $\vec{v}$ applicato nel punto $P$, il **momento del vettore rispetto al polo $O$** è:

$$
\vec{M}_O = \overrightarrow{OP} \times \vec{v}
$$

Il momento è perpendicolare al piano formato da $\overrightarrow{OP}$ e $\vec{v}$.

Il suo modulo vale:

$$
M_O = OP \cdot v \sin\theta
$$

Definendo $h$ come il **braccio del momento**, cioè la distanza perpendicolare tra il polo $O$ e la retta d'azione del vettore:

$$
M_O = h \cdot v
$$

> Il momento dipende sia dal vettore sia dalla distanza della sua retta d'azione dal polo.

Cambiando polo da $O$ a $O'$:

$$
\vec{M}_O = \overrightarrow{OO'} \times \vec{v} + \vec{M}_{O'}
$$

Quindi, in generale, il momento dipende dal polo scelto.

---

## Momento angolare

Per un punto materiale di massa $m$, posizione $\vec{r}$ rispetto al polo $O$ e velocità $\vec{v}$, il **momento angolare** è:

$$
\boxed{\vec{L} = \vec{r} \times m\vec{v}}
$$

Poiché la quantità di moto è:

$$
\vec{p} = m\vec{v}
$$

si può anche scrivere:

$$
\vec{L} = \vec{r} \times \vec{p}
$$

### Moto curvilineo

La velocità può essere scomposta in:

$$
\vec{v} = \vec{v}_r + \vec{v}_\theta
$$

La componente radiale $\vec{v}_r$ è parallela a $\vec{r}$, quindi:

$$
\vec{r} \times m\vec{v}_r = 0
$$

Contribuisce quindi solo la componente trasversale:

$$
\vec{L} = \vec{r} \times m\vec{v}_\theta
$$

In modulo:

$$
L = mr^2\frac{d\theta}{dt}
$$

Poiché:

$$
\omega = \frac{d\theta}{dt}
$$

nel moto circolare:

$$
\boxed{L = mr^2\omega}
$$

---

## Teorema del momento angolare

Partendo da:

$$
\vec{L} = \vec{r} \times m\vec{v}
$$

deriviamo rispetto al tempo:

$$
\frac{d\vec{L}}{dt}
=
\frac{d\vec{r}}{dt} \times m\vec{v}
+
\vec{r} \times m\frac{d\vec{v}}{dt}
$$

Dato che:

$$
\frac{d\vec{r}}{dt} = \vec{v}
$$

il primo termine diventa:

$$
\vec{v} \times m\vec{v} = 0
$$

Quindi:

$$
\frac{d\vec{L}}{dt}
=
\vec{r} \times m\vec{a}
$$

Usando:

$$
\vec{F} = m\vec{a}
$$

si ottiene:

$$
\boxed{\frac{d\vec{L}}{dt} = \vec{r} \times \vec{F} = \vec{M}}
$$

> **Teorema del momento angolare:** la derivata temporale del momento angolare è uguale al momento della forza risultante rispetto allo stesso polo.

---

## Conservazione del momento angolare

Dal teorema:

$$
\frac{d\vec{L}}{dt} = \vec{M}
$$

Se il momento risultante delle forze è nullo:

$$
\vec{M} = 0
$$

allora:

$$
\frac{d\vec{L}}{dt} = 0
$$

e quindi:

$$
\boxed{\vec{L} = \text{costante}}
$$

Il momento angolare si conserva anche quando $\vec{r}$ e $\vec{F}$ sono paralleli, perché:

$$
\vec{r} \times \vec{F} = 0
$$

---

## Formule da ricordare

$$
\boxed{\vec{L} = \vec{r} \times m\vec{v}}
$$

$$
\boxed{L = mr^2\omega}
$$

$$
\boxed{\frac{d\vec{L}}{dt} = \vec{M}}
$$

$$
\boxed{\vec{M} = 0 \Rightarrow \vec{L} = \text{costante}}
$$

## Momento angolare di un sistema di punti

Per un sistema formato da più punti materiali, il **momento angolare totale** rispetto a un polo $O$ è la somma dei momenti angolari dei singoli punti:

$$
\vec L = \sum_i \vec r_i \times m_i \vec v_i
$$

Derivando rispetto al tempo:

$$
\frac{d\vec L}{dt}
=
\sum_i \frac{d\vec r_i}{dt}\times m_i\vec v_i
+
\sum_i \vec r_i \times m_i\frac{d\vec v_i}{dt}
$$

Se il polo $O$ si muove con velocità $\vec v_O$:

$$
\frac{d\vec r_i}{dt} = \vec v_i - \vec v_O
$$

Considerando sia le **forze esterne** sia le **forze interne**, si arriva a:

$$
\frac{d\vec L}{dt}
=
\vec M^{(e)}+\vec M^{(i)}
-
\vec v_O\times M\vec v_{CM}
$$

dove:

- $\vec M^{(e)}$ = momento totale delle forze esterne
- $\vec M^{(i)}$ = momento totale delle forze interne
- $M$ = massa totale del sistema
- $\vec v_{CM}$ = velocità del centro di massa

---

## Teorema del momento angolare per un sistema

Il momento totale delle **forze interne** è nullo:

$$
\vec M^{(i)}=0
$$

Se il polo $O$:

- è fisso in un sistema inerziale;
- oppure coincide con il centro di massa;

allora:

$$
\boxed{\frac{d\vec L}{dt}=\vec M^{(e)}}
$$

> La variazione del momento angolare totale del sistema è determinata soltanto dal momento delle forze esterne.

---

## Conservazione del momento angolare

Dal teorema:

$$
\frac{d\vec L}{dt}=\vec M^{(e)}
$$

quindi il momento angolare si conserva quando:

$$
\vec M^{(e)}=0
$$

e quindi:

$$
\boxed{\vec L=\text{costante}}
$$

Questo può avvenire in due casi principali:

1. **Sistema isolato**, cioè senza forze esterne:

$$
\vec R^{(e)}=0
$$

In questo caso si conserva anche la quantità di moto.

2. Le forze esterne sono presenti, ma il loro **momento risultante rispetto a un determinato polo è nullo**:

$$
\vec M^{(e)}=0
$$

> In questo secondo caso la scelta del polo è fondamentale, perché il momento delle forze può essere nullo rispetto a un polo ma non rispetto a un altro.

---

## Momento angolare rispetto al centro di massa

Consideriamo il momento angolare rispetto all'origine di un sistema inerziale.

La posizione e la velocità di ogni punto possono essere scritte come:

$$
\vec r_i=\vec r_i' + \vec r_{CM}
$$

$$
\vec v_i=\vec v_i' + \vec v_{CM}
$$

Sostituendo nella definizione del momento angolare:

$$
\vec L=\sum_i \vec r_i\times m_i\vec v_i
$$

si ottiene:

$$
\boxed{
\vec L=\vec L' + \vec r_{CM}\times M\vec v_{CM}
}
$$

dove $\vec L'$ è il momento angolare del sistema calcolato rispetto al centro di massa.

Questa relazione è analoga al **teorema di König**.

Il momento angolare totale può quindi essere visto come somma di:

- momento angolare del sistema rispetto al centro di massa;
- momento angolare dovuto al moto del centro di massa:

$$
\boxed{
\vec L
=
\vec L_{CM}
+
\vec r_{CM}\times M\vec v_{CM}
}
$$

> In pratica: il sistema può ruotare attorno al proprio centro di massa mentre, contemporaneamente, il centro di massa si muove nello spazio.

---

## Formule da ricordare

$$
\boxed{
\vec L=\sum_i \vec r_i\times m_i\vec v_i
}
$$

$$
\boxed{
\frac{d\vec L}{dt}=\vec M^{(e)}
}
$$

$$
\boxed{
\vec M^{(e)}=0
\Rightarrow
\vec L=\text{costante}
}
$$

$$
\boxed{
\vec L=\vec L' + \vec r_{CM}\times M\vec v_{CM}
}
$$

## Equazioni cardinali della dinamica dei sistemi

Le due relazioni fondamentali che descrivono il moto complessivo di un sistema di punti sono dette **equazioni cardinali della dinamica**.

### 1. Teorema del moto del centro di massa

$$
\boxed{\frac{d\vec P}{dt} = \vec R^{(e)}}
$$

dove:

- $\vec P$ = quantità di moto totale del sistema
- $\vec R^{(e)}$ = risultante delle forze esterne

Quindi la variazione della quantità di moto totale dipende solo dalle **forze esterne**.

---

### 2. Teorema del momento angolare

$$
\boxed{\frac{d\vec L}{dt} = \vec M^{(e)}}
$$

dove:

- $\vec L$ = momento angolare totale
- $\vec M^{(e)}$ = momento risultante delle forze esterne

Anche in questo caso le **forze interne non compaiono**, perché il loro contributo complessivo si annulla.

Le equazioni cardinali permettono quindi di studiare la dinamica globale del sistema senza analizzare necessariamente il moto di ogni singolo punto.

---

## Lavoro e momenti nel moto circolare

Nel moto circolare, solo la componente **tangenziale** della forza compie lavoro.

Il lavoro elementare è:

$$
dW = F_t\,ds
$$

Poiché lungo una circonferenza:

$$
ds = r\,d\theta
$$

si ha:

$$
dW = F_t r\,d\theta
$$

Ma il momento della forza rispetto al centro della traiettoria vale:

$$
M = rF_t
$$

quindi:

$$
dW = M\,d\theta
$$

Integrando tra due posizioni angolari $\theta_A$ e $\theta_B$:

$$
\boxed{
W = \int_{\theta_A}^{\theta_B} M\,d\theta
}
$$

> Nel moto rotatorio, il momento $M$ svolge un ruolo analogo a quello della forza nel moto traslatorio.

Se il momento è costante:

$$
\boxed{
W = M(\theta_B-\theta_A)
}
$$

ovvero:

$$
\boxed{
W = M\Delta\theta
}
$$

con $\Delta\theta$ espresso in **radianti**.

---

## Formule da aggiungere a quelle da ricordare

$$
\boxed{\frac{d\vec P}{dt} = \vec R^{(e)}}
$$

$$
\boxed{\frac{d\vec L}{dt} = \vec M^{(e)}}
$$

$$
\boxed{dW = M\,d\theta}
$$

$$
\boxed{W = \int M\,d\theta}
$$

Se $M$ è costante:

$$
\boxed{W = M\Delta\theta}
$$

## Esercizi sul momento angolare

### Esercizio 1 – Due masse collegate da una sbarretta telescopica

**Traccia**

Due punti materiali di ugual massa $m$ sono collegati da una sbarretta di massa trascurabile e ruotano senza attrito su un piano orizzontale attorno al centro della sbarretta.

Inizialmente:

- lunghezza totale della sbarretta: $2r_1$
- velocità angolare: $\omega_1$

Successivamente la sbarretta si allunga fino a:

- lunghezza totale: $2r_2$, con $r_2>r_1$

Calcolare la nuova velocità angolare $\omega_2$.

### Soluzione

Le forze esterne verticali, peso e reazione vincolare, si bilanciano.

La tensione della sbarretta è una **forza interna**, quindi rispetto al centro non produce momento esterno.

Di conseguenza:

$$
\vec M^{(e)}=0
$$

e quindi si conserva il momento angolare:

$$
L_1=L_2
$$

Per ciascuna massa:

$$
L=mr^2\omega
$$

Essendoci due masse:

$$
L_1=2mr_1^2\omega_1
$$

$$
L_2=2mr_2^2\omega_2
$$

Imponendo la conservazione:

$$
2mr_1^2\omega_1=2mr_2^2\omega_2
$$

Semplificando:

$$
r_1^2\omega_1=r_2^2\omega_2
$$

quindi:

$$
\boxed{\omega_2=\omega_1\frac{r_1^2}{r_2^2}}
$$

Dato che $r_2>r_1$:

$$
\boxed{\omega_2<\omega_1}
$$

> Aumentando la distanza delle masse dall'asse di rotazione, la velocità angolare diminuisce.

---

### Esercizio 2 – Momento della forza sui pedali

**Traccia**

La pedivella di una bicicletta ha lunghezza:

$$
r=0.15\,m
$$

Sul pedale viene applicata una forza:

$$
F=100\,N
$$

Calcolare il modulo del momento della forza quando l'angolo tra pedivella e forza è:

- $\theta=30^\circ$
- $\theta=90^\circ$
- $\theta=180^\circ$

### Soluzione

Il modulo del momento di una forza è:

$$
M=rF\sin\theta
$$

#### Caso $\theta=30^\circ$

$$
M=0.15\cdot100\cdot\sin30^\circ
$$

Poiché:

$$
\sin30^\circ=0.5
$$

si ha:

$$
\boxed{M=7.5\,N\,m}
$$

#### Caso $\theta=90^\circ$

$$
M=0.15\cdot100\cdot1
$$

$$
\boxed{M=15\,N\,m}
$$

Il momento è massimo quando forza e braccio sono perpendicolari.

#### Caso $\theta=180^\circ$

$$
\sin180^\circ=0
$$

quindi:

$$
\boxed{M=0}
$$

> Se la forza è parallela alla pedivella, non produce alcun effetto rotatorio.

---

### Esercizio 3 – Momento angolare rispetto a due poli diversi

**Traccia**

Un punto materiale di massa:

$$
m=2.0\,kg
$$

si muove nel piano con velocità:

$$
v_x=30\,m/s
$$

$$
v_y=60\,m/s
$$

e passa per il punto:

$$
P=(3.0,-4.0)\,m
$$

Calcolare il momento angolare:

1. rispetto all'origine $O=(0,0)$;
2. rispetto al punto $O'=(-2.0,-2.0)\,m$.

---

### 1. Momento angolare rispetto all'origine

La definizione è:

$$
\vec L=\vec r\times m\vec v
$$

Nel piano $xy$ il momento angolare è diretto lungo l'asse $z$ e vale:

$$
L_z=m(xv_y-yv_x)
$$

Con:

$$
x=3,\qquad y=-4
$$

si ottiene:

$$
L_z=2[3(60)-(-4)(30)]
$$

$$
L_z=2(180+120)
$$

$$
\boxed{L_z=600\,kg\,m^2/s}
$$

---

### 2. Momento angolare rispetto a $O'$

La posizione relativa al nuovo polo è:

$$
\vec r'=\vec r-\vec r_{O'}
$$

quindi:

$$
x'=3-(-2)=5
$$

$$
y'=-4-(-2)=-2
$$

Perciò:

$$
\vec r'=(5,-2)\,m
$$

Il momento angolare diventa:

$$
L'_z=m(x'v_y-y'v_x)
$$

$$
L'_z=2[5(60)-(-2)(30)]
$$

$$
L'_z=2(300+60)
$$

$$
\boxed{L'_z=720\,kg\,m^2/s}
$$

> Il momento angolare dipende dal polo rispetto al quale viene calcolato.

---

## Formule utili per gli esercizi

Momento angolare di un punto:

$$
\boxed{\vec L=\vec r\times m\vec v}
$$

Nel piano $xy$:

$$
\boxed{L_z=m(xv_y-yv_x)}
$$

Momento di una forza:

$$
\boxed{M=rF\sin\theta}
$$

Conservazione del momento angolare:

$$
\boxed{L_i=L_f}
$$

Per masse che ruotano a distanza $r$:

$$
\boxed{L=mr^2\omega}
$$
## Quesiti

### Q1. Come è definito il momento angolare di un punto materiale?

Il **momento angolare** $\vec L$ di un punto materiale di massa $m$, che si trova in posizione $\vec r$ rispetto a un polo $O$ e si muove con velocità $\vec v$, è definito come:

$$
\boxed{\vec L=\vec r\times m\vec v}
$$

Poiché:

$$
\vec p=m\vec v
$$

si può anche scrivere:

$$
\boxed{\vec L=\vec r\times\vec p}
$$

> È quindi il prodotto vettoriale tra il vettore posizione e la quantità di moto.

---

### Q2. Come è definito il momento di una forza?

Il **momento di una forza** $\vec F$ rispetto a un polo $O$ è definito come:

$$
\boxed{\vec M=\vec r\times\vec F}
$$

dove $\vec r$ è il vettore che va dal polo $O$ al punto di applicazione della forza.

Il suo modulo è:

$$
\boxed{M=rF\sin\theta}
$$

oppure, usando il braccio $h$:

$$
\boxed{M=Fh}
$$

> Il momento misura l'effetto rotatorio prodotto dalla forza rispetto al polo scelto.


### Q3. Cosa afferma il teorema del momento angolare per un sistema di punti materiali?

Il **teorema del momento angolare** afferma che, se il polo è:

- fisso in un sistema di riferimento inerziale;
- oppure coincide con il centro di massa;

allora la variazione nel tempo del momento angolare totale del sistema è uguale al momento risultante delle forze esterne:

$$
\boxed{\frac{d\vec L}{dt}=\vec M^{(e)}}
$$

> Quindi sono le **forze esterne** a determinare la variazione del momento angolare totale del sistema.
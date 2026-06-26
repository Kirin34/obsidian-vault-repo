

## Proiezione del moto circolare uniforme

Riprendiamo il **moto circolare uniforme**: un punto materiale si muove con velocità di modulo costante lungo una circonferenza di raggio $R$, centrata nell’origine degli assi.

Se consideriamo la proiezione della posizione del punto sull’asse $x$, otteniamo un moto rettilineo periodico.

La legge oraria della proiezione è:

$$
x(t) = R \cos(\omega t + \theta_0)
$$

dove:

- $R$ è il raggio della circonferenza;
- $\omega$ è la pulsazione;
- $\theta_0$ è la fase iniziale;
- $\omega t + \theta_0$ rappresenta l’angolo descritto dal punto nel tempo.

Quindi il moto circolare uniforme, se osservato solo lungo un asse, diventa un moto avanti e indietro: questo è alla base del **moto armonico semplice**.

---

## Periodo, frequenza e pulsazione

Nel moto periodico si definiscono:

- **periodo** $T$: tempo necessario per completare un’oscillazione;
- **frequenza** $\nu$: numero di oscillazioni al secondo;
- **pulsazione** $\omega$: grandezza legata alla rapidità dell’oscillazione.

Le relazioni sono:

$$
T = \frac{1}{\nu}
$$

e

$$
T = \frac{2\pi}{\omega}
$$

quindi:

$$
\omega = \frac{2\pi}{T}
$$

e anche:

$$
\omega = 2\pi \nu
$$

---

## Moto armonico semplice

Il **moto armonico semplice** è un moto rettilineo periodico descritto da una legge del tipo:

$$
x(t) = A \cos(\omega t + \varphi)
$$

dove:

- $x(t)$ è la posizione al tempo $t$;
- $A$ è l’ampiezza del moto;
- $\omega$ è la pulsazione;
- $\varphi$ è la fase iniziale;
- $\omega t + \varphi$ è la fase del moto.

L’ampiezza $A$ rappresenta la massima distanza dalla posizione centrale di equilibrio.

Poiché il coseno varia tra $-1$ e $1$, la posizione varia tra:

$$
-A \leq x(t) \leq A
$$

Quindi il corpo oscilla tra due estremi: $-A$ e $A$.

---

## Equazione caratteristica del moto armonico

Il moto armonico semplice è caratterizzato dalla relazione:

$$
\frac{d^2x}{dt^2} = -\omega^2 x
$$
## Posizione, velocità e accelerazione nel moto armonico

Nel moto armonico semplice, posizione, velocità e accelerazione sono tutte grandezze periodiche.

Partendo dalla legge oraria:

$$
x(t) = A \cos(\omega t + \varphi)
$$

si ricavano:

$$
v(t) = \dot{x}(t) = -A\omega \sin(\omega t + \varphi)
$$

$$
a(t) = \ddot{x}(t) = -A\omega^2 \cos(\omega t + \varphi)
$$

Poiché:

$$
x(t) = A \cos(\omega t + \varphi)
$$

allora l’accelerazione può essere scritta anche come:

$$
a(t) = -\omega^2 x(t)
$$

Questa è una relazione fondamentale: l’accelerazione è sempre proporzionale alla posizione, ma ha verso opposto.

---

## Caso con fase iniziale nulla

Se la fase iniziale è nulla:

$$
\varphi = 0
$$

allora la legge oraria diventa:

$$
x(t) = A \cos(\omega t)
$$

La velocità diventa:

$$
v_x(t) = -A\omega \sin(\omega t)
$$

L’accelerazione diventa:

$$
a_x(t) = -A\omega^2 \cos(\omega t)
$$

oppure:

$$
a_x(t) = -\omega^2 x(t)
$$

---

## Sfasamento tra posizione, velocità e accelerazione

I grafici di posizione, velocità e accelerazione sono tutti periodici, ma non raggiungono massimi e minimi nello stesso istante.

Sono sfasati tra loro.

### Posizione e velocità

La velocità è sfasata di un quarto di periodo rispetto alla posizione.

Quando la posizione è massima:

$$
x = A
$$

la velocità è nulla:

$$
v = 0
$$

Quando il corpo passa per la posizione centrale:

$$
x = 0
$$

la velocità è massima in modulo.

Quindi:

- agli estremi dell’oscillazione la velocità è zero;
- al centro dell’oscillazione la velocità è massima.

---

### Posizione e accelerazione

L’accelerazione è opposta alla posizione:

$$
a(t) = -\omega^2 x(t)
$$

Quindi posizione e accelerazione sono in opposizione di fase.

Quando:

$$
x = A
$$

allora:

$$
a = -\omega^2 A
$$

Quando:

$$
x = -A
$$

allora:

$$
a = +\omega^2 A
$$

Quando:

$$
x = 0
$$

allora:

$$
a = 0
$$

Questo significa che l’accelerazione è massima agli estremi dell’oscillazione e nulla al centro.

---

## Interpretazione fisica

Nel moto armonico semplice il corpo oscilla tra due estremi:

$$
-A \quad \text{e} \quad A
$$

Se parte da fermo nella posizione di massima ampiezza:

$$
x = A
$$

allora:

- la velocità iniziale è nulla;
- l’accelerazione è massima e diretta verso il centro;
- il corpo comincia a muoversi verso la posizione di equilibrio.

Dopo un quarto di periodo:

$$
t = \frac{T}{4}
$$

il corpo passa per il centro:

$$
x = 0
$$

Qui:

- la velocità è massima;
- l’accelerazione è nulla.

Dopo mezzo periodo:

$$
t = \frac{T}{2}
$$

il corpo arriva all’altro estremo:

$$
x = -A
$$

Qui:

- la velocità torna nulla;
- l’accelerazione è massima ma diretta nel verso opposto;
- il corpo riparte verso il centro.

---

## Schema riassuntivo

| Posizione del corpo | Posizione $x$ | Velocità $v$ | Accelerazione $a$ |
|---|---:|---:|---:|
| Estremo destro | $A$ | $0$ | massima verso sinistra |
| Centro | $0$ | massima | $0$ |
| Estremo sinistro | $-A$ | $0$ | massima verso destra |
| Centro di ritorno | $0$ | massima in verso opposto | $0$ |

---

## Idea chiave

Nel moto armonico semplice:

- la posizione segue una funzione coseno;
- la velocità è sfasata di un quarto di periodo rispetto alla posizione;
- l’accelerazione è opposta alla posizione;
- agli estremi la velocità è nulla e l’accelerazione è massima;
- al centro la velocità è massima e l’accelerazione è nulla.

La relazione più importante resta:

$$
a(t) = -\omega^2 x(t)
$$
## Accelerazione nel moto armonico

Nel moto armonico semplice l’accelerazione è proporzionale alla posizione, ma ha verso opposto:

$$
a(t) = -\omega^2 x(t)
$$

Quindi l’accelerazione punta sempre verso la posizione di equilibrio.

È massima agli estremi del moto, dove $x = \pm A$, e nulla al centro, dove $x = 0$.

$$
|a|_{max} = \omega^2 A
$$

## Moto armonico e dinamica

Nel moto armonico semplice vale:

$$
a(t)=\ddot{x}(t)=-\omega^2 x(t)
$$

Quindi ogni sistema in cui la forza risultante è proporzionale allo spostamento, ma diretta in verso opposto, genera un moto armonico.

Caso tipico:

$$
F=-cx
$$

Applicando il secondo principio:

$$
m\ddot{x}=-cx
$$

$$
\ddot{x}=-\frac{c}{m}x
$$

Confrontando con:

$$
\ddot{x}=-\omega^2x
$$

si ottiene:

$$
\omega^2=\frac{c}{m}
$$

quindi:

$$
\omega=\sqrt{\frac{c}{m}}
$$

---

## Moto armonico smorzato

Se è presente una forza resistente viscosa, il moto armonico si smorza nel tempo.

Nel caso oscillatorio smorzato:

$$
x(t)=Ae^{-\frac{b}{2m}t}\cos\left(\frac{\sqrt{-\Delta}}{2m}t+\varphi\right)
$$

oppure:

$$
x(t)=ae^{-\frac{t}{\tau}}\cos(\omega t+\varphi)
$$

L’ampiezza diminuisce progressivamente a causa del termine esponenziale.

Più piccola è la costante di tempo $\tau$, più rapidamente il moto si smorza.

---

## Moto armonico forzato

Se al sistema smorzato aggiungiamo una forza esterna periodica:

$$
F_0\sin(\omega t)
$$

l’equazione diventa:

$$
m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+cx=F_0\sin(\omega t)
$$

Per tempi lunghi, l’oscillazione naturale si attenua e rimane il moto imposto dalla forza esterna:

$$
x(t)=A\sin(\omega t+\varphi)
$$

L’ampiezza $A$ e la fase $\varphi$ dipendono dal sistema fisico e dalla frequenza della forza esterna.

---

## Risonanza

Nel moto armonico forzato, a regime:

$$
x(t)=A\sin(\omega t+\varphi)
$$

con:

$$
A=\frac{F_0/m}{\sqrt{(\omega_0^2-\omega^2)^2+4\gamma^2\omega^2}}
$$

dove:

$$
\gamma=\frac{b}{2m}
$$

e $\omega_0$ è la pulsazione naturale del sistema.

Per smorzamenti piccoli, l’ampiezza diventa massima quando la frequenza esterna è vicina alla frequenza naturale:

$$
\omega \approx \omega_0
$$

Questa condizione si chiama **risonanza**.

In assenza di smorzamento, l’ampiezza tenderebbe a crescere indefinitamente.

Esempio: un ponte può oscillare molto se viene sollecitato con una frequenza vicina alla sua frequenza naturale.

## Esercizi – Moto armonico semplice

### Esercizio 1: differenza di fase

Due punti si muovono di moto armonico semplice con stessa ampiezza $A$ e stessa pulsazione $\omega$:

$$
x_1(t)=A\cos(\omega t+\varphi_1)
$$

$$
x_2(t)=A\cos(\omega t+\varphi_2)
$$

Si incontrano quando lo spostamento vale metà ampiezza:

$$
x=\frac{A}{2}
$$

quindi:

$$
\cos(\omega t+\varphi)=\frac{1}{2}
$$

Perciò:

$$
\omega t+\varphi=\pm \frac{\pi}{3}
$$

Poiché nell’istante dell’incontro le velocità sono opposte:

$$
v_1=-v_2
$$

si ottiene:

$$
\varphi_1-\varphi_2=\frac{2\pi}{3}
$$

**Risultato:**

$$
\Delta \varphi=\frac{2\pi}{3}
$$

---

### Esercizio 2: oggetto su pistone oscillante

Un pistone si muove verticalmente di moto armonico.  
L’oggetto si separa dal pistone quando l’accelerazione massima del moto armonico supera $g$.

Condizione limite:

$$
\omega^2 A = g
$$

Sapendo che:

$$
\omega=\frac{2\pi}{T}
$$

si ricava:

$$
A=g\left(\frac{T}{2\pi}\right)^2
$$

Con $T=1s$:

$$
A \approx 0.25\,m
$$

Se invece $A=5cm=0.05m$, la massima frequenza ammessa è:

$$
(2\pi \nu)^2A=g
$$


$$
\nu=\frac{1}{2\pi}\sqrt{\frac{g}{A}}
$$

$$
\nu \approx 2.2\,Hz
$$

---

### Esercizio 3: membrana di un altoparlante

Dati:

$$
\nu=440\,Hz
$$

$$
A=0.75\,mm=7.5\cdot10^{-4}m
$$

Pulsazione:

$$
\omega=2\pi\nu
$$

$$
\omega=2.76\cdot10^3\,rad/s
$$

Velocità massima:

$$
v_{max}=\omega A
$$

$$
v_{max}=2.07\,m/s
$$

Accelerazione massima:

$$
a_{max}=\omega^2A
$$

$$
a_{max}=5.71\cdot10^3\,m/s^2
$$

---

# Quesiti

## Q.1 Condizione per avere moto armonico semplice

Una forza genera moto armonico semplice se è proporzionale allo spostamento e diretta in verso opposto:

$$
F=-cx
$$

Applicando Newton:

$$
m\ddot{x}=-cx
$$

$$
\ddot{x}=-\frac{c}{m}x
$$

Quindi:

$$
\omega^2=\frac{c}{m}
$$

---

## Q.2 Moto armonico smorzato

Nel moto armonico smorzato alle oscillazioni naturali si sovrappone un termine esponenziale decrescente.

Forma tipica:

$$
x(t)=Ae^{-\frac{t}{\tau}}\cos(\omega t+\varphi)
$$

Il termine:

$$
e^{-\frac{t}{\tau}}
$$

fa diminuire progressivamente l’ampiezza delle oscillazioni nel tempo.
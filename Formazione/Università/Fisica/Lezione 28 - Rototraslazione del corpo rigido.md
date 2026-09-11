## Rototraslazione del corpo rigido

La dinamica di un corpo rigido è governata dalle **due equazioni cardinali**:

$$
\vec F = \frac{d\vec P}{dt} = M\vec a_{CM}
$$

$$
\vec M = \frac{d\vec L}{dt}
$$

- La prima descrive il **moto traslatorio** del centro di massa.
- La seconda descrive il **moto rotatorio**.

In generale il moto di un corpo rigido può essere visto come la composizione di:

1. traslazione del centro di massa;
2. rotazione attorno ad un asse istantaneo.

---

# Puro rotolamento

Il caso più semplice di rototraslazione è il **rotolamento senza strisciamento**.

Per una ruota di raggio $R$:

$$
s = R\theta
$$

dove:

- $s$ = spazio percorso dal centro di massa;
- $R$ = raggio;
- $\theta$ = angolo ruotato.

Derivando rispetto al tempo:

$$
v_{CM} = R\frac{d\theta}{dt}
$$

quindi:

$$
\boxed{v_{CM}=R\omega}
$$

Questa è la condizione fondamentale del **puro rotolamento**.

---

## Punto di contatto con il terreno

Nel puro rotolamento il punto $P$ della ruota a contatto con il terreno è, istantaneamente, fermo rispetto al terreno.

La sua velocità è:

$$
\vec v_P = \vec v_C + \vec\omega\times\vec r
$$

Essendo:

$$
\vec v_P=0
$$

si ha:

$$
\boxed{\vec v_C=-\vec\omega\times\vec r}
$$

Per le accelerazioni:

$$
\boxed{a_C=\alpha R}
$$

dove $\alpha$ è l'accelerazione angolare.

### Relazioni da ricordare

$$
\boxed{v_{CM}=\omega R}
$$

$$
\boxed{a_{CM}=\alpha R}
$$

---

# Energia cinetica nel rotolamento

Durante il puro rotolamento il moto possiede contemporaneamente:

- energia cinetica di **traslazione**;
- energia cinetica di **rotazione**.

Considerando il punto di contatto $P$ come centro istantaneo di rotazione:

$$
K=\frac12 I_P\omega^2
$$

Per il teorema di Huygens-Steiner:

$$
I_P=I_{CM}+MR^2
$$

quindi:

$$
K=\frac12(I_{CM}+MR^2)\omega^2
$$

ossia:

$$
K=\frac12I_{CM}\omega^2+\frac12MR^2\omega^2
$$

Dato che:

$$
v_{CM}=R\omega
$$

otteniamo:

$$
\boxed{
K=
\frac12Mv_{CM}^2+
\frac12I_{CM}\omega^2
}
$$

Quindi l'energia cinetica totale è:

> energia traslatoria del centro di massa + energia rotatoria attorno al centro di massa.

---

# Dinamica del rotolamento

Consideriamo una ruota su un piano orizzontale e una forza $\vec F$ applicata al centro di massa.

Per ottenere il rotolamento è necessaria una **forza di attrito statico**.

Sulla ruota agiscono:

- forza applicata $F$;
- peso $Mg$;
- reazione normale $N$;
- attrito statico $f_s$.

L'equazione traslatoria è:

$$
M\vec a_C=\vec F+M\vec g+\vec N+\vec f_s
$$

Verticalmente:

$$
N=Mg
$$

quindi rimane solamente la componente orizzontale:

$$
\boxed{Ma_C=F-f_s}
$$

---

## Equazione dei momenti

Calcoliamo i momenti rispetto al centro di massa.

La forza $F$, il peso e la normale non producono momento rispetto al centro di massa.

Il momento è prodotto dall'attrito:

$$
M=I\alpha=R f_s
$$

Utilizzando:

$$
\alpha=\frac{a_C}{R}
$$

otteniamo:

$$
I\frac{a_C}{R}=Rf_s
$$

quindi:

$$
f_s=\frac{Ia_C}{R^2}
$$

Mettendo questa relazione insieme a:

$$
Ma_C=F-f_s
$$

si ottiene:

$$
\boxed{
a_C=
\frac{F}
{M\left(1+\frac{I}{MR^2}\right)}
}
$$

e:

$$
\boxed{
f_s=
\frac{F}
{1+\frac{MR^2}{I}}
}
$$

---

# Attrito nel rotolamento

Perché continui ad esserci **puro rotolamento**, l'attrito statico necessario non deve superare il massimo attrito statico disponibile:

$$
f_s\leq\mu_sN
$$

Dato che:

$$
N=Mg
$$

si ha:

$$
\boxed{f_s\leq\mu_sMg}
$$

Poiché:

$$
f_s=
\frac{F}
{1+\frac{MR^2}{I}}
$$

la forza applicata deve rispettare:

$$
\boxed{
F\leq
\mu_sMg
\left(
1+\frac{MR^2}{I}
\right)
}
$$

Superato questo limite la ruota inizia a **strisciare**.

---

## Lavoro dell'attrito statico

Nel puro rotolamento il punto di contatto con il terreno è istantaneamente fermo.

Per questo motivo l'attrito statico:

$$
\boxed{L_{attrito}=0}
$$

e, in condizioni ideali, si conserva l'energia meccanica.

---

# Attrito volvente

Nel caso reale ruota e terreno possono deformarsi nella zona di contatto.

Compare quindi una resistenza chiamata **attrito volvente**.

Può essere rappresentata tramite un momento resistente:

$$
\boxed{M_a=hmg}
$$

dove $h$ è il **coefficiente di attrito volvente**.

A differenza del coefficiente di attrito statico, $h$ ha le dimensioni di una **lunghezza**.

---

# Precessione del giroscopio

Un **giroscopio** è un corpo rigido in rotazione con un punto fisso opportunamente vincolato.

Un esempio è una trottola.

La trottola ruota attorno al proprio asse con velocità angolare $\omega$.

Il peso produce un momento rispetto al punto di appoggio $O$:

$$
\vec M=\vec r\times M\vec g
$$

Dalla seconda equazione cardinale:

$$
\vec M=\frac{d\vec L}{dt}
$$

La variazione del momento angolare è perpendicolare a $\vec L$ e ne modifica principalmente la **direzione**.

Si genera quindi il moto di **precessione**.

Definiamo la velocità angolare di precessione $\vec\Omega$:

$$
\frac{d\vec L}{dt}
=
\vec\Omega\times\vec L
$$

Poiché:

$$
L=I\omega
$$

si ricava:

$$
\boxed{
\Omega=
\frac{Mgr}{I\omega}
}
$$

### Da ricordare

La precessione è la rotazione dell'asse del giroscopio attorno alla verticale.

---

# Esercizio 1 – Ruota trascinata da una forza

## Traccia

Una forza orizzontale costante:

$$
F=10\,N
$$

è applicata al centro di massa di una ruota avente:

$$
M=10\,kg
$$

$$
R=0.30\,m
$$

La ruota rotola senza strisciare e l'accelerazione del centro di massa è:

$$
a=0.60\,m/s^2
$$

Determinare:

1. intensità e direzione della forza di attrito;
2. momento d'inerzia della ruota.

---

## 1. Forza di attrito

L'equazione traslatoria è:

$$
F-f_s=Ma
$$

quindi:

$$
f_s=F-Ma
$$

Sostituendo:

$$
f_s=10-(10)(0.60)
$$

$$
\boxed{f_s=4\,N}
$$

La forza di attrito è diretta nel **verso opposto alla forza applicata**.

---

## 2. Momento d'inerzia

Il momento prodotto dall'attrito è:

$$
f_sR=I\alpha
$$

Nel rotolamento:

$$
\alpha=\frac{a}{R}
$$

quindi:

$$
f_sR=I\frac{a}{R}
$$

da cui:

$$
I=\frac{f_sR^2}{a}
$$

Sostituendo:

$$
I=
\frac{4(0.30)^2}{0.60}
$$

$$
\boxed{I=0.60\,kg\,m^2}
$$

---

# Esercizio 2 – Urto anelastico contro un'asta

## Traccia

Una particella di massa:

$$
m=50\,g
$$

scivola senza attrito da un'altezza:

$$
h=20\,cm
$$

e urta in modo perfettamente anelastico l'estremità inferiore di un'asta omogenea.

L'asta ha:

$$
M=100\,g
$$

$$
d=40\,cm
$$

ed è incernierata all'estremità superiore.

Determinare l'angolo massimo $\theta$ raggiunto dal sistema.

---

## 1. Momento d'inerzia dell'asta

La densità lineare è:

$$
\lambda=\frac{M}{d}
$$

Il momento d'inerzia dell'asta rispetto al perno è:

$$
I_0=
\lambda\int_0^d x^2dx
$$

quindi:

$$
I_0=\frac13Md^2
$$

Numericamente:

$$
\boxed{
I_0=5.3\cdot10^{-3}\,kg\,m^2
}
$$

---

## 2. Momento d'inerzia dopo l'urto

La particella rimane attaccata all'estremità dell'asta.

Il nuovo momento d'inerzia è:

$$
I=I_0+md^2
$$

quindi:

$$
\boxed{
I=1.33\cdot10^{-2}\,kg\,m^2
}
$$

---

## 3. Velocità della particella prima dell'urto

Durante la discesa si conserva l'energia meccanica:

$$
mgh=\frac12mv^2
$$

da cui:

$$
v=\sqrt{2gh}
$$

Numericamente:

$$
\boxed{v=1.98\,m/s}
$$

---

## 4. Velocità angolare dopo l'urto

Durante l'urto utilizziamo la conservazione del momento angolare rispetto al perno:

$$
mvd=I\omega_0
$$

quindi:

$$
\omega_0=\frac{mvd}{I}
$$

Numericamente:

$$
\boxed{\omega_0=2.98\,rad/s}
$$

---

## 5. Angolo massimo

Dopo l'urto il sistema ruota verso l'alto.

L'energia cinetica rotazionale iniziale viene trasformata in energia potenziale gravitazionale:

$$
\frac12I\omega_0^2
=
\left(
m+\frac{M}{2}
\right)
gd(1-\cos\theta)
$$

Da cui:

$$
\theta=
\arccos
\left[
1-
\frac{\omega_0^2I}
{2gd\left(m+\frac{M}{2}\right)}
\right]
$$

Numericamente:

$$
\boxed{\theta=31.8^\circ}
$$

---

# Esercizio 3 – Cilindro con una lenza

## Traccia

Una lenza è avvolta attorno ad un cilindro omogeneo di:

$$
M=10\,kg
$$

$$
R=10\,cm=0.10\,m
$$

La lenza viene tirata dalla parte superiore con una forza:

$$
F=12\,N
$$

Il cilindro rotola senza strisciare.

Determinare:

1. accelerazione del centro di massa;
2. accelerazione angolare;
3. forza di attrito.

---

## 1. Accelerazione del centro di massa

Le equazioni sono:

$$
F-f_s=Ma_{CM}
$$

e:

$$
(F+f_s)R=I\alpha
$$

Nel puro rotolamento:

$$
\alpha=\frac{a_{CM}}{R}
$$

quindi:

$$
F+f_s=
\frac{I}{R^2}a_{CM}
$$

Sommando le due equazioni:

$$
2F=
\left(
M+\frac{I}{R^2}
\right)a_{CM}
$$

Per un cilindro omogeneo:

$$
I=\frac12MR^2
$$

quindi:

$$
2F=
\frac32Ma_{CM}
$$

da cui:

$$
a_{CM}=\frac{4F}{3M}
$$

Sostituendo:

$$
a_{CM}
=
\frac{4(12)}{3(10)}
$$

$$
\boxed{a_{CM}=1.6\,m/s^2}
$$

---

## 2. Accelerazione angolare

$$
\alpha=\frac{a_{CM}}{R}
$$

quindi:

$$
\alpha=
\frac{1.6}{0.10}
$$

$$
\boxed{\alpha=16\,rad/s^2}
$$

---

## 3. Forza di attrito

Dalla prima equazione:

$$
F-f_s=Ma_{CM}
$$

$$
12-f_s=(10)(1.6)
$$

$$
f_s=-4\,N
$$

Il segno negativo indica che il verso ipotizzato inizialmente per l'attrito era sbagliato.

Quindi:

$$
\boxed{|f_s|=4\,N}
$$

e la forza di attrito è diretta **nel verso del moto**.

---

# Quesito

## Quanto vale l'energia cinetica di una ruota in puro rotolamento?

L'energia cinetica è composta da un contributo traslatorio e uno rotatorio:

$$
\boxed{
K=
\frac12Mv_{CM}^2+
\frac12I_{CM}\omega^2
}
$$

---

# Formule fondamentali della lezione

### Puro rotolamento

$$
\boxed{v_{CM}=\omega R}
$$

$$
\boxed{a_{CM}=\alpha R}
$$

### Energia cinetica

$$
\boxed{
K=
\frac12Mv_{CM}^2+
\frac12I_{CM}\omega^2
}
$$

### Dinamica

$$
\boxed{Ma_C=F-f_s}
$$

$$
\boxed{I\alpha=Rf_s}
$$

$$
\boxed{
a_C=
\frac{F}
{M\left(1+\frac{I}{MR^2}\right)}
}
$$

$$
\boxed{
f_s=
\frac{F}
{1+\frac{MR^2}{I}}
}
$$

### Limite per il puro rotolamento

$$
\boxed{f_s\leq\mu_sMg}
$$

### Precessione

$$
\boxed{
\Omega=\frac{Mgr}{I\omega}
}
$$

---

# Concetti chiave

- La rototraslazione combina **traslazione + rotazione**.
- Nel puro rotolamento il punto di contatto con il terreno è istantaneamente fermo.
- La condizione fondamentale è:

$$
v_{CM}=\omega R
$$

- L'attrito che permette il puro rotolamento è **statico**.
- L'attrito statico nel puro rotolamento ideale **non compie lavoro**.
- L'energia cinetica totale contiene una parte traslatoria e una rotatoria.
- Nel rotolamento reale compare anche l'**attrito volvente**.
- Nel giroscopio il momento della forza peso modifica la direzione del momento angolare producendo la **precessione**.
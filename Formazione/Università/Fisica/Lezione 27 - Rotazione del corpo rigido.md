## 1. Rotazione di un corpo rigido

Un **corpo rigido** può compiere:
- un moto di **traslazione**;
- un moto di **rotazione** attorno a un asse.

Durante una rotazione tutti i punti del corpo hanno la **stessa velocità angolare** $\omega$, ma velocità lineari diverse a seconda della distanza $r$ dall'asse.

La velocità tangenziale di un punto è:

$$
v = \omega r
$$

Quindi:
- maggiore è la distanza dall'asse → maggiore è $v$;
- sull'asse di rotazione $r=0$ → $v=0$.

---

## 2. Momento d'inerzia

Nel moto rotatorio il **momento d'inerzia $I$** svolge un ruolo analogo a quello della massa nel moto traslatorio.

L'energia cinetica di un corpo rigido in rotazione è:

$$
K_R = \frac{1}{2}I\omega^2
$$

Per un sistema discreto di punti:

$$
I = \sum_i m_i r_i^2
$$

dove $r_i$ è la distanza della massa $m_i$ dall'asse di rotazione.

Per un corpo continuo:

$$
I = \int r^2\,dm
$$

Se è nota la densità $\rho$:

$$
I = \int \rho r^2\,dV
$$

> [!important]
> Il momento d'inerzia non dipende solo dalla massa totale, ma soprattutto da **come la massa è distribuita rispetto all'asse di rotazione**.
>
> Più massa è lontana dall'asse → maggiore è $I$.

---

## 3. Teorema di Huygens-Steiner

Permette di calcolare il momento d'inerzia rispetto a un asse quando conosciamo quello rispetto a un **asse parallelo passante per il centro di massa**.

$$
I_h = I_C + Mh^2
$$

dove:
- $I_C$ = momento d'inerzia rispetto all'asse passante per il centro di massa;
- $M$ = massa totale;
- $h$ = distanza tra i due assi;
- $I_h$ = momento d'inerzia rispetto al nuovo asse.

### Significato

Allontanando l'asse di rotazione dal centro di massa, il momento d'inerzia aumenta della quantità:

$$
Mh^2
$$

> [!important]
> Il teorema vale tra **assi paralleli**.

---

## 4. Momenti d'inerzia notevoli

### Guscio cilindrico rispetto al proprio asse

$$
I = mr^2
$$

### Cilindro pieno rispetto al proprio asse

$$
I = \frac{1}{2}mr^2
$$

### Sfera piena rispetto a un diametro

$$
I = \frac{2}{5}mr^2
$$

### Asta sottile rispetto a un asse perpendicolare passante per il centro

$$
I = \frac{1}{12}ml^2
$$

### Guscio cilindrico rispetto a un diametro passante per il centro

$$
I = \frac{1}{2}mr^2+\frac{1}{12}ml^2
$$

### Cilindro pieno rispetto a un diametro passante per il centro

$$
I = \frac{1}{4}mr^2+\frac{1}{12}ml^2
$$

---

## 5. Momento angolare del corpo rigido

Per un punto materiale il momento angolare rispetto a un polo $O$ è:

$$
\vec L = \vec r \times \vec p
$$

con:

$$
\vec p = m\vec v
$$

Per un elemento infinitesimo di massa $dm$:

$$
d\vec L = \vec r \times (dm\,\vec v)
$$

In un corpo rigido che ruota attorno a un **asse di simmetria**, le componenti del momento angolare perpendicolari all'asse si annullano tra loro.

Rimane quindi solamente la componente parallela all'asse di rotazione.

Poiché:

$$
v=\omega h
$$

integrando i contributi di tutti gli elementi del corpo:

$$
L = \omega\int h^2\,dm
$$

ma:

$$
I=\int h^2\,dm
$$

quindi:

$$
\boxed{L=I\omega}
$$

In forma vettoriale, nel caso considerato:

$$
\boxed{\vec L=I\vec\omega}
$$

> [!important]
> $L=I\omega$ è l'analogo rotazionale della quantità di moto:
>
> $$p=mv$$

---

## 6. Conservazione del momento angolare

Se il **momento risultante delle forze esterne è nullo**:

$$
\sum \vec M_{ext}=0
$$

allora il momento angolare si conserva:

$$
\vec L=\text{costante}
$$

Poiché:

$$
L=I\omega
$$

si ha:

$$
I_{in}\omega_{in}=I_{fin}\omega_{fin}
$$

### Conseguenza

Se il momento d'inerzia diminuisce:

$$
I\downarrow \quad\Rightarrow\quad \omega\uparrow
$$

Se il momento d'inerzia aumenta:

$$
I\uparrow \quad\Rightarrow\quad \omega\downarrow
$$

### Esempio

Un pattinatore che raccoglie le braccia avvicina la propria massa all'asse:

$$
I\downarrow \Rightarrow \omega\uparrow
$$

e quindi ruota più velocemente.

---

## 7. Variazione del momento angolare

La variazione del momento angolare è causata dal **momento delle forze esterne**:

$$
\vec M_{ext}=\frac{d\vec L}{dt}
$$

Per un corpo rigido che ruota attorno a un asse fisso, $I$ è costante.

Dato che:

$$
L=I\omega
$$

allora:

$$
M_{ext}=\frac{dL}{dt}
=I\frac{d\omega}{dt}
$$

Definendo l'accelerazione angolare:

$$
\alpha=\frac{d\omega}{dt}
$$

otteniamo:

$$
\boxed{M_{ext}=I\alpha}
$$

Questa è l'equazione fondamentale della dinamica rotazionale, analoga alla seconda legge di Newton:

$$
F=ma
$$

---

## 8. Lavoro nel moto rotatorio

L'energia cinetica rotazionale è:

$$
K_R=\frac{1}{2}I\omega^2
$$

Il lavoro compiuto dal momento delle forze esterne è uguale alla variazione dell'energia cinetica rotazionale:

$$
L=K_{fin}-K_{in}
$$

quindi:

$$
L=\frac{1}{2}I\omega_{fin}^2-\frac{1}{2}I\omega_{in}^2
$$

In forma infinitesima:

$$
dL=M\,d\theta
$$

e quindi:

$$
\boxed{L=\int M\,d\theta}
$$

Se il momento è costante:

$$
\boxed{L=M\Delta\theta}
$$

Il concetto è analogo al moto traslatorio:

$$
dL=\vec F\cdot d\vec s
$$

mentre nella rotazione:

$$
dL=\vec M\cdot d\vec\theta
$$

---

## 9. Traslazione e rotazione: analogie

| Moto traslatorio | Moto rotatorio |
|---|---|
| Massa $m$ | Momento d'inerzia $I$ |
| Velocità $v$ | Velocità angolare $\omega$ |
| Quantità di moto $p=mv$ | Momento angolare $L=I\omega$ |
| $K=\frac12mv^2$ | $K_R=\frac12I\omega^2$ |
| $\sum F=ma$ | $\sum M=I\alpha$ |
| $F=\frac{dp}{dt}$ | $M=\frac{dL}{dt}$ |
| $p=$ costante se $\sum F=0$ | $L=$ costante se $\sum M=0$ |
| $P=Fv$ | $P=M\omega$ |

---

## Formule fondamentali da ricordare

$$
\boxed{v=\omega r}
$$

$$
\boxed{I=\sum_i m_i r_i^2}
$$

$$
\boxed{I=\int r^2\,dm}
$$

$$
\boxed{K_R=\frac12I\omega^2}
$$

$$
\boxed{I_h=I_C+Mh^2}
$$

$$
\boxed{L=I\omega}
$$

$$
\boxed{I_{in}\omega_{in}=I_{fin}\omega_{fin}}
$$

$$
\boxed{M_{ext}=\frac{dL}{dt}=I\alpha}
$$

$$
\boxed{dL=M\,d\theta}
$$

### Idea chiave della lezione

Gran parte della dinamica della rotazione è analoga alla dinamica traslatoria:

$$
\boxed{
m\leftrightarrow I,\qquad
v\leftrightarrow\omega,\qquad
p\leftrightarrow L,\qquad
F\leftrightarrow M,\qquad
a\leftrightarrow\alpha
}
$$

Il **momento d'inerzia $I$** indica quanto un corpo si oppone alla variazione del proprio moto rotatorio, proprio come la massa $m$ rappresenta l'inerzia nel moto traslatorio.

# Lezione 28 - Calcolo dei momenti d'inerzia

## 1. Momento d'inerzia di un disco omogeneo

Consideriamo un disco omogeneo di:
- massa $M$;
- raggio $R$;
- densità superficiale costante $\sigma$.

La densità superficiale è:

$$
\sigma = \frac{M}{S} = \frac{M}{\pi R^2}
$$

Per calcolare il momento d'inerzia rispetto all'asse perpendicolare al disco e passante per il centro, dividiamo il disco in corone circolari di raggio $r$ e spessore $dr$.

L'area infinitesima della corona è:

$$
dS = 2\pi r\,dr
$$

La massa infinitesima vale:

$$
dm = \sigma dS = \sigma 2\pi r\,dr
$$

Il momento d'inerzia è:

$$
I = \int r^2\,dm
$$

quindi:

$$
I = \int_0^R r^2\sigma 2\pi r\,dr
$$

$$
I = 2\pi\sigma\int_0^R r^3\,dr
$$

$$
I = 2\pi\sigma\frac{R^4}{4}
$$

Sostituendo:

$$
\sigma = \frac{M}{\pi R^2}
$$

si ottiene:

$$
\boxed{I=\frac{1}{2}MR^2}
$$

---

## 2. Teorema di Huygens-Steiner applicato al disco

Il teorema di Huygens-Steiner è:

$$
I = I_C + Md^2
$$

Per un asse parallelo a quello centrale e passante per il bordo del disco:

$$
d=R
$$

quindi:

$$
I = \frac{1}{2}MR^2 + MR^2
$$

$$
\boxed{I=\frac{3}{2}MR^2}
$$

> [!warning]
> Nella slide compare $I'=MR^2$, ma applicando Huygens-Steiner al disco il risultato corretto è:
>
> $$
> I'=\frac{3}{2}MR^2
> $$

---

## 3. Momenti d'inerzia comuni

### Sfera piena

Rispetto a un asse passante per il centro:

$$
\boxed{I=\frac{2}{5}MR^2}
$$

### Sfera cava

$$
\boxed{I=\frac{2}{3}MR^2}
$$

### Cilindro pieno

Rispetto al proprio asse centrale:

$$
\boxed{I=\frac{1}{2}MR^2}
$$

### Anello rispetto a un diametro

$$
\boxed{I=\frac{1}{2}MR^2}
$$

### Anello rispetto all'asse centrale perpendicolare al piano

$$
\boxed{I=MR^2}
$$

---

# Esercizio 1 - Satellite cilindrico

## Traccia

Un satellite di forma cilindrica ha:

- diametro $d=1.21\,m$;
- altezza $h=1.75\,m$;
- massa $M=1210\,kg$;
- velocità angolare $\omega=1.52\,rad/s$.

Il satellite ruota attorno al proprio asse.

Calcolare:

1. il momento d'inerzia;
2. l'energia cinetica rotazionale.

---

## Soluzione

Il raggio è:

$$
R=\frac{d}{2}=\frac{1.21}{2}=0.605\,m
$$

Per un cilindro pieno:

$$
I=\frac{1}{2}MR^2
$$

quindi:

$$
I=\frac{1}{2}(1210)(0.605)^2
$$

$$
\boxed{I\approx221\,kg\,m^2}
$$

L'energia cinetica rotazionale è:

$$
K_R=\frac{1}{2}I\omega^2
$$

$$
K_R=\frac{1}{2}(221)(1.52)^2
$$

$$
\boxed{K_R\approx256\,J}
$$

> [!warning]
> Nella slide compare circa $10^4\,J$, ma usando i dati riportati il risultato è circa $256\,J$.

---

# Esercizio 2 - Parallelepipedo omogeneo

## Traccia

Un parallelepipedo omogeneo ha:

$$
M=0.172\,kg
$$

e lati:

$$
3.5\,cm,\qquad 8.4\,cm,\qquad 1.4\,cm
$$

Calcolare il momento d'inerzia rispetto a un asse passante per uno dei suoi spigoli più corti.

---

## Soluzione

Convertiamo le dimensioni in metri.

$$
3.5\,cm=0.035\,m
$$

$$
8.4\,cm=0.084\,m
$$

$$
1.4\,cm=0.014\,m
$$

Per l'asse indicato nella figura, le distanze dall'asse dipendono dai lati:

$$
b=0.084\,m
$$

$$
c=0.035\,m
$$

La densità del parallelepipedo è:

$$
\rho=\frac{M}{V}
$$

con:

$$
V=abc
$$

quindi:

$$
\rho=\frac{M}{abc}
$$

Il momento d'inerzia si calcola mediante:

$$
I=\int r^2\,dm
$$

con:

$$
r^2=x^2+y^2
$$

e:

$$
dm=\rho\,dV
$$

Integrando sull'intero volume si ottiene:

$$
I=\frac{1}{3}M(b^2+c^2)
$$

Sostituendo:

$$
I=\frac{1}{3}(0.172)\left[(0.084)^2+(0.035)^2\right]
$$

$$
\boxed{I\approx4.75\cdot10^{-4}\,kg\,m^2}
$$

---

## Formula utile per un parallelepipedo

Per un parallelepipedo di massa $M$, rispetto a un asse coincidente con uno spigolo, se $b$ e $c$ sono i lati perpendicolari all'asse:

$$
\boxed{I=\frac{1}{3}M(b^2+c^2)}
$$

---

# Formule da ricordare

Disco o cilindro pieno:

$$
\boxed{I=\frac{1}{2}MR^2}
$$

Sfera piena:

$$
\boxed{I=\frac{2}{5}MR^2}
$$

Sfera cava:

$$
\boxed{I=\frac{2}{3}MR^2}
$$

Anello, asse centrale:

$$
\boxed{I=MR^2}
$$

Anello rispetto a un diametro:

$$
\boxed{I=\frac{1}{2}MR^2}
$$

Huygens-Steiner:

$$
\boxed{I=I_C+Md^2}
$$

Energia cinetica rotazionale:

$$
\boxed{K_R=\frac{1}{2}I\omega^2}
$$

## Idea chiave

Il calcolo del momento d'inerzia parte sempre da:

$$
I=\int r^2\,dm
$$

La difficoltà consiste nel determinare correttamente:
- come è distribuita la massa;
- la distanza $r$ di ogni elemento dall'asse;
- l'asse rispetto al quale viene richiesto il momento d'inerzia.
# Esercizio 3 - Momento d'inerzia di una ruota

## Traccia

Calcolare il momento d'inerzia di una ruota che possiede:

- energia cinetica $K = 24400\,J$;
- velocità di rotazione $n = 602\,giri/min$.

---

## Soluzione

Prima dobbiamo convertire i giri al minuto in giri al secondo:

$$
\nu = \frac{602}{60} \approx 10.03\,Hz
$$

La velocità angolare vale:

$$
\omega = 2\pi\nu
$$

quindi:

$$
\omega = 2\pi(10.03) \approx 63\,rad/s
$$

Utilizziamo ora l'energia cinetica rotazionale:

$$
K=\frac{1}{2}I\omega^2
$$

Ricaviamo il momento d'inerzia:

$$
I=\frac{2K}{\omega^2}
$$

Sostituendo:

$$
I=\frac{2(24400)}{63^2}
$$

$$
\boxed{I\approx12.3\,kg\,m^2}
$$

> [!important]
> Quando la velocità è data in $giri/min$, prima di usare le formule della rotazione bisogna convertirla:
>
> $$
> \boxed{\omega=2\pi\frac{n}{60}}
> $$
>
> con $n$ espresso in $giri/min$.


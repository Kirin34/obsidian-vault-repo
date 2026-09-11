## Formule principali da ricordare

### Momento angolare
Per un corpo rigido che ruota attorno a un asse:

$$
L = I\omega
$$

Se il momento risultante delle forze esterne è nullo:

$$
L_i = L_f
$$

quindi:

$$
I_i\omega_i = I_f\omega_f
$$

---

### Momento delle forze

$$
M = I\alpha
$$

Per una forza perpendicolare al braccio:

$$
M = Fr
$$

---

### Energia cinetica di rotazione

$$
E_c = \frac{1}{2}I\omega^2
$$

---

### Teorema di Huygens-Steiner

Se conosciamo il momento d'inerzia rispetto al centro di massa:

$$
I = I_{CM} + md^2
$$

dove $d$ è la distanza tra il centro di massa e il nuovo asse di rotazione.

---

# Sessione di studio 0

## Esercizio 1 – Pattinatrice

### Traccia

Una pattinatrice ruota attorno ad un asse passante per il proprio baricentro con:

- $\omega_1 = 2.4\ rad/s$
- $\omega_2 = 3.5\ rad/s$
- $I_1 = 5.2\ kg\,m^2$

Portando le braccia lungo il corpo aumenta la propria velocità angolare.

Determinare il momento d'inerzia finale $I_2$.

---

### Svolgimento

Il momento delle forze esterne rispetto al centro di massa è nullo.

Di conseguenza si conserva il momento angolare:

$$
L_1=L_2
$$

quindi:

$$
I_1\omega_1=I_2\omega_2
$$

Ricaviamo $I_2$:

$$
I_2=\frac{\omega_1}{\omega_2}I_1
$$

$$
I_2=\frac{2.4}{3.5}\cdot5.2
$$

$$
\boxed{I_2\simeq3.6\ kg\,m^2}
$$

### Concetto chiave

Quando la pattinatrice porta le braccia verso il corpo:

- $I$ diminuisce;
- $\omega$ aumenta;
- $L$ rimane costante.

---

## Esercizio 2 – Satellite cilindrico

### Traccia

Un satellite cilindrico ha:

- $r=4.5\ m$
- $m=5.4\cdot10^3\ kg$
- $\omega=3.5\ rad/s$
- $\Delta t=360\ s$

Il satellite parte da fermo e viene fatto ruotare mediante **due propulsori tangenziali**.

Determinare:

1. la forza $F$ esercitata da ciascun propulsore;
2. l'energia cinetica finale.

---

### 1. Forza dei propulsori

L'equazione della dinamica rotazionale è:

$$
M=I\alpha
$$

Poiché parte da fermo:

$$
\alpha=\frac{\omega}{\Delta t}
$$

Per un cilindro:

$$
I=\frac{1}{2}mr^2
$$

I due propulsori producono entrambi momento:

$$
M=2Fr
$$

quindi:

$$
2Fr=\frac{1}{2}mr^2\frac{\omega}{\Delta t}
$$

semplificando:

$$
F=\frac{mr\omega}{4\Delta t}
$$

Sostituendo:

$$
\boxed{F\simeq59\ N}
$$

---

### 2. Energia cinetica finale

$$
E_c=\frac{1}{2}I\omega^2
$$

Sostituendo:

$$
E_c=
\frac{1}{2}
\left(\frac{1}{2}mr^2\right)\omega^2
$$

$$
E_c=\frac{1}{4}mr^2\omega^2
$$

$$
\boxed{E_c\simeq3.4\cdot10^5\ J}
$$

---

# Sessione di studio 1

## Esercizio 3 – Energia cinetica della Terra

Determinare l'energia cinetica della Terra:

1. nella rotazione attorno al proprio asse;
2. nella rivoluzione attorno al Sole.

---

## 1. Rotazione attorno al proprio asse

La Terra viene considerata una sfera con:

$$
I=\frac{2}{5}mr^2
$$

L'energia cinetica rotazionale è:

$$
E_{c1}=\frac{1}{2}I\omega^2
$$

La velocità angolare vale:

$$
\omega=\frac{2\pi}{T}
$$

dove $T$ è un giorno.

Quindi:

$$
E_{c1}
=
\frac{1}{2}
\frac{2}{5}mr^2
\left(\frac{2\pi}{T}\right)^2
$$

$$
E_{c1}
=
\frac{4\pi^2}{5}\frac{mr^2}{T^2}
$$

Secondo le slide:

$$
\boxed{E_{c1}=2.56\cdot10^{29}\ J}
$$

---

## 2. Rivoluzione attorno al Sole

In questo caso la Terra viene approssimata come un **punto materiale**.

La velocità orbitale è:

$$
v=\frac{2\pi d}{T_1}
$$

quindi:

$$
E_{c2}=\frac{1}{2}mv^2
$$

$$
E_{c2}
=
\frac{1}{2}m
\left(
\frac{2\pi d}{T_1}
\right)^2
$$

Nelle slide viene riportato:

$$
\boxed{E_{c2}=8.45\cdot10^{26}\ J}
$$

> [!warning]
> Riporto qui il valore esattamente come presente nelle slide.

---

# Esercizio 4 – Sfera che rotola su un piano inclinato

## Traccia

Una sfera parte da ferma dalla cima di un piano inclinato scabro.

Dati:

- $m=24\ kg$
- $h=3.5\ m$
- $\theta=23^\circ$
- $\mu_s=0.30$

La sfera rotola senza strisciare.

Determinare:

1. velocità in fondo al piano;
2. forza di attrito statico;
3. inclinazione massima che consente il rotolamento senza strisciamento.

---

## 1. Velocità finale

L'unica forza che compie lavoro è la forza peso.

Si conserva quindi l'energia meccanica:

$$
E_{p,i}=E_{c,f}
$$

Per calcolare l'energia cinetica si considera la rotazione attorno al punto di contatto.

Utilizziamo Steiner:

$$
I=I_G+mr^2
$$

Per una sfera:

$$
I_G=\frac{2}{5}mr^2
$$

quindi:

$$
I=
\frac{2}{5}mr^2+mr^2
$$

$$
I=\frac{7}{5}mr^2
$$

Poiché nel puro rotolamento:

$$
v_G=r\omega
$$

nelle slide viene utilizzata la relazione:

$$
E_c=\frac{7}{5}mv_G^2
$$

La conservazione dell'energia diventa:

$$
mgh=\frac{7}{5}mv_G^2
$$

Da cui:

$$
v_G=\sqrt{\frac{5}{7}gh}
$$

e quindi:

$$
\boxed{v_G\simeq5.0\ m/s}
$$

> [!warning]
> Nelle slide compare $E_c=\frac{7}{5}mv^2$. Partendo invece dalla formula generale $E_c=\frac12I\omega^2$ compare un fattore $1/2$: quindi questo passaggio delle slide merita di essere controllato separatamente.

---

## 2. Forza di attrito statico

Le forze sulla sfera sono:

- peso $mg$;
- reazione normale $N$;
- attrito statico $F_s$.

Lungo il piano:

$$
mg\sin\theta-F_s=ma_G
$$

Per la rotazione rispetto al punto di appoggio:

$$
mgr\sin\theta=I\alpha
$$

utilizzando:

$$
I=\frac{7}{5}mr^2
$$

e:

$$
r\alpha=a_G
$$

otteniamo:

$$
mgr\sin\theta=
\frac{7}{5}mr^2\alpha
$$

da cui:

$$
a_G=\frac{5}{7}g\sin\theta
$$

Torniamo quindi all'equazione traslazionale:

$$
F_s=mg\sin\theta-ma_G
$$

$$
F_s=
mg\sin\theta-
\frac{5}{7}mg\sin\theta
$$

$$
\boxed{F_s=\frac{2}{7}mg\sin\theta}
$$

---

## 3. Massima inclinazione

Il massimo attrito statico disponibile è:

$$
F_s^{max}=\mu_sN
$$

con:

$$
N=mg\cos\theta
$$

quindi:

$$
F_s^{max}=\mu_smg\cos\theta
$$

Nelle slide viene riportato:

$$
F_s^{max}=26\ N
$$

Perché non avvenga strisciamento:

$$
F_s\leq F_s^{max}
$$

quindi:

$$
\frac{2}{7}mg\sin\theta
\leq
\mu_smg\cos\theta
$$

Semplificando:

$$
\frac{2}{7}\tan\theta\leq\mu_s
$$

$$
\tan\theta\leq\frac{7}{2}\mu_s
$$

Pertanto:

$$
\theta_{max}
=
\arctan\left(\frac{7}{2}\mu_s\right)
$$

$$
\boxed{\theta_{max}\simeq46^\circ}
$$

---

# Sessione di studio 2

## Esercizio 5 – Asta soggetta a forza e attrito

### Traccia

Un'asta inizialmente ferma ruota attorno ad una cerniera $O$.

Dati:

- $m=0.4\ kg$
- $l=0.80\ m$
- $F=100\ N$
- $M_A=30\ Nm$
- $I_{CM}=\frac{1}{12}ml^2$

La forza $F$ rimane sempre perpendicolare all'asta.

Determinare la velocità angolare quando l'asta ha ruotato di:

$$
180^\circ
$$

---

## Momento della forza

Poiché $F$ è sempre perpendicolare:

$$
M_F=Fl
$$

$$
M_F=100\cdot0.8
$$

$$
M_F=80\ Nm
$$

Il momento d'attrito è opposto al moto:

$$
M_{TOT}=M_F-M_A
$$

$$
M_{TOT}=80-30
$$

$$
\boxed{M_{TOT}=50\ Nm}
$$

---

## Momento d'inerzia rispetto al perno

Bisogna trasformare $I_{CM}$ nel momento rispetto alla cerniera usando Steiner:

$$
I_O=I_{CM}+mr^2
$$

Nelle slide viene ottenuto:

$$
I_O=0.021+0.032
$$

$$
\boxed{I_O=0.053\ kg\,m^2}
$$

---

## Accelerazione angolare

$$
M_{TOT}=I_O\alpha
$$

quindi:

$$
\alpha=\frac{M_{TOT}}{I_O}
$$

$$
\boxed{\alpha=943.40\ rad/s^2}
$$

---

## Velocità angolare finale

Utilizziamo:

$$
\omega_f^2-\omega_i^2
=
2\alpha(\theta_f-\theta_i)
$$

L'asta parte da ferma:

$$
\omega_i=0
$$

e:

$$
\Delta\theta=180^\circ=\pi\ rad
$$

quindi:

$$
\omega_f=\sqrt{2\alpha\pi}
$$

$$
\boxed{\omega_f=76.97\ rad/s}
$$

> [!warning]
> Anche qui riporto i passaggi numerici delle slide. Il termine di Steiner indicato nella slide ($0.032\ kg\,m^2$) va eventualmente ricontrollato se vogliamo verificare l'esercizio matematicamente da zero.

---

# Sessione di studio 3

## Esercizio 6 – Asta che cade sotto l'effetto della gravità

### Traccia

Un'asta rigida è vincolata ad un perno liscio $P$ e viene lasciata cadere da ferma.

Dati:

- $m=200\ g=0.2\ kg$
- $l=60\ cm=0.60\ m$
- $I=\frac{ml^2}{3}$

Determinare la velocità quando passa per il punto di minimo.

---

## Conservazione dell'energia

Il sistema conserva l'energia meccanica.

Poniamo:

$$
U=0
$$

quando il centro di massa si trova nella posizione più bassa.

Dalla geometria della figura:

$$
h=
\frac{l}{2}
+
\frac{l}{2}\sin30^\circ
$$

L'energia potenziale iniziale è:

$$
U=mgh
$$

quindi:

$$
U=
mg
\left(
\frac{l}{2}
+
\frac{l}{2}\sin30^\circ
\right)
$$

Nelle slide:

$$
\boxed{U=0.88\ J}
$$

Quando l'asta raggiunge il punto più basso, tutta l'energia è cinetica rotazionale:

$$
K_R=\frac{1}{2}I\omega^2
$$

Per conservazione dell'energia:

$$
U=\frac{1}{2}I\omega^2
$$

da cui:

$$
\omega=\sqrt{\frac{2U}{I}}
$$

ottenendo:

$$
\boxed{\omega=8.56\ rad/s}
$$

> [!note]
> La traccia parla della velocità del punto $A$, mentre nelle slide la soluzione si ferma alla velocità angolare $\omega$.

---

## Esercizio 7 – Cilindro di ghiaccio secco

### Traccia

Un cilindro di ghiaccio secco ruota attorno al proprio asse.

Dati iniziali:

- $M_i=300\ g$
- $f_i=8\ Hz$

Dopo $10$ minuti:

- $M_f=270\ g$

Il raggio rimane invariato.

Determinare:

1. frequenza finale;
2. velocità angolare finale.

Il momento d'inerzia del cilindro è:

$$
I=\frac{1}{2}MR^2
$$

---

## Conservazione del momento angolare

L'evaporazione avviene uniformemente e gli attriti sono trascurabili.

Il momento angolare si conserva:

$$
L_i=L_f
$$

quindi:

$$
I_i\omega_i=I_f\omega_f
$$

Utilizziamo:

$$
\omega=2\pi f
$$

ottenendo:

$$
\frac{1}{2}M_iR^2(2\pi f_i)
=
\frac{1}{2}M_fR^2\omega_f
$$

Semplificando:

$$
\omega_f=
2\pi f_i\frac{M_i}{M_f}
$$

Sostituendo:

$$
\omega_f=
2\pi(8)\frac{300}{270}
$$

$$
\boxed{\omega_f=55.82\ rad/s}
$$

La frequenza finale vale:

$$
f_f=\frac{\omega_f}{2\pi}
$$

oppure direttamente:

$$
f_f=f_i\frac{M_i}{M_f}
$$

$$
f_f=
8\frac{300}{270}
$$

$$
\boxed{f_f\simeq8.89\ Hz}
$$

### Concetto chiave

Diminuendo la massa diminuisce il momento d'inerzia.

Poiché:

$$
L=I\omega=\text{costante}
$$

se $I$ diminuisce, $\omega$ deve aumentare.

---

# Concetti da ricordare dalla Lezione 29

1. **Conservazione del momento angolare**

$$
I_i\omega_i=I_f\omega_f
$$

utile quando il momento risultante delle forze esterne è nullo.

2. **Dinamica rotazionale**

$$
M=I\alpha
$$

è l'equivalente rotazionale di:

$$
F=ma
$$

3. **Energia cinetica rotazionale**

$$
E_c=\frac{1}{2}I\omega^2
$$

4. **Teorema di Steiner**

$$
I=I_{CM}+md^2
$$

serve quando cambia l'asse rispetto al quale viene calcolato il momento d'inerzia.

5. **Rotolamento senza strisciamento**

$$
v=r\omega
$$

e:

$$
a=r\alpha
$$

6. **Attrito statico nel rotolamento**

$$
F_s\leq\mu_sN
$$

Se l'attrito richiesto supera questo valore, il corpo inizia a strisciare.
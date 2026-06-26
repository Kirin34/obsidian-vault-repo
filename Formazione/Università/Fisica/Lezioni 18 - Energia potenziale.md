## Operatore gradiente

Il **gradiente** è un operatore vettoriale indicato con **nabla**:

$$
\nabla = \left(\frac{\partial}{\partial x}; \frac{\partial}{\partial y}; \frac{\partial}{\partial z}\right)
$$

Applicato a una funzione scalare, ad esempio l’energia potenziale $U(x,y,z)$ o una funzione $V(x,y,z)$, indica **come varia quella funzione nello spazio**.

Per un piccolo spostamento:

$$
d\vec{r} = (dx, dy, dz)
$$

vale:

$$
\nabla V \cdot d\vec{r}
=
\frac{\partial V}{\partial x}dx
+
\frac{\partial V}{\partial y}dy
+
\frac{\partial V}{\partial z}dz
=
dV
$$

Quindi il gradiente misura la variazione infinitesima della funzione lungo uno spostamento.

---

## Forze conservative ed energia potenziale

Per una **forza conservativa**, la forza è legata all’energia potenziale tramite:

$$
\vec{F} = - \nabla U
$$

Significa che la forza punta nella direzione in cui l’energia potenziale diminuisce più rapidamente.

In una dimensione:

$$
F_x = -\frac{dU}{dx}
$$

Il lavoro di una forza conservativa può essere scritto come:

$$
L_{AB} = -\Delta U
$$

cioè:

$$
L_{AB} = U_A - U_B
$$

Se la forza compie lavoro positivo, l’energia potenziale diminuisce.

---
## Esercizio 1 - Lavoro e potenza

### Traccia

Un oggetto di massa:

$$  
m = 2.0 , kg  
$$

accelera uniformemente da fermo fino alla velocità:

$$  
v_f = 10 , m/s  
$$

in un intervallo di tempo:

$$  
t = 3.0 , s  
$$

Si chiede:

1. quanto lavoro viene compiuto sull’oggetto;
    
2. con che potenza viene compiuto il lavoro al termine dell’intervallo;
    
3. con che potenza viene compiuto il lavoro alla metà dell’intervallo.
    

### Soluzione

Per il lavoro si usa il teorema dell’energia cinetica:

$$  
L = \Delta K  
$$

Poiché l’oggetto parte da fermo:

$$  
L = \frac{1}{2}mv_f^2  
$$

$$  
L = \frac{1}{2}(2.0)(10)^2 = 100 , J  
$$

Quindi:

$$  
L = 100 , J  
$$

L’accelerazione è:

$$  
a = \frac{v_f}{t} = \frac{10}{3} \approx 3.3 , m/s^2  
$$

La forza costante vale:

$$  
F = ma = 2.0 \cdot 3.3 = 6.6 , N  
$$

La potenza istantanea si calcola con:

$$  
P = Fv  
$$

Alla fine dell’intervallo:

$$  
P_f = 6.6 \cdot 10 = 66 , W  
$$

A metà intervallo la velocità è:

$$  
v = 5 , m/s  
$$

quindi:

$$  
P = 6.6 \cdot 5 = 33 , W  
$$

---

## Esercizio 2 - Lavoro tramite integrale

### Traccia

La forza:

$$  
\vec{F} = (cx - 3.00x^2)\hat{i}  
$$

con $c$ costante, agisce su un punto materiale che si muove lungo l’asse $x$.

Si sa che:

$$  
K(0) = 20.0 , J  
$$

e che in:

$$  
x = 3.00 , m  
$$

l’energia cinetica vale:

$$  
K(3.00) = 11.0 , J  
$$

Bisogna trovare la costante $c$.

### Soluzione

Dal teorema dell’energia cinetica:

$$  
L = \Delta K  
$$

quindi:

$$  
L = 11 - 20 = -9 , J  
$$

Il lavoro della forza si calcola integrando:

$$  
L = \int_0^3 (cx - 3x^2) dx  
$$

Svolgendo l’integrale:

$$  
L = \left[\frac{cx^2}{2} - x^3\right]_0^3  
$$

$$  
L = \frac{c \cdot 3^2}{2} - 3^3  
$$

$$  
L = 4.5c - 27  
$$

Ora uguagliamo il lavoro trovato con la variazione di energia cinetica:

$$  
4.5c - 27 = -9  
$$

$$  
4.5c = 18  
$$

$$  
c = 4 , N/m  
$$

Quindi:

$$  
c = 4 , N/m  
$$

## Esercizio 3 - Pendolo ed energia potenziale gravitazionale

### Traccia

Un pendolo semplice è formato da un filo inestensibile lungo:

$$  
l = 2.00 , m  
$$

fissato a un perno. Alla sua estremità è attaccata una massa:

$$  
m = 5.00 , kg  
$$

inizialmente in quiete nella posizione verticale.

La massa viene spostata lateralmente fino a formare un angolo:

$$  
\theta = 30^\circ  
$$

con la verticale, poi viene lasciata libera.

Durante il moto verso il punto più basso si chiede:

1. quanto lavoro compie la forza di gravità;
    
2. di quanto varia l’energia potenziale;
    
3. se $U = 0$ nel punto più basso, quanto valeva l’energia potenziale alla partenza;
    
4. cosa succede aumentando l’angolo $\theta$.
    

---

### Soluzione

Quando il pendolo scende verso il punto più basso, l’unica forza che compie lavoro è la **forza di gravità**.

La variazione di altezza è:

$$  
\Delta h = l(1 - \cos \theta)  
$$

Quindi il lavoro della forza peso è:

$$  
L = mg \Delta h  
$$

Sostituendo:

$$  
L = mg l(1 - \cos \theta)  
$$

$$  
L = 5.00 \cdot 9.8 \cdot 2.00 \cdot (1 - \cos 30^\circ)  
$$

$$  
L \approx 13.1 , J  
$$

Quindi:

$$  
L = 13.1 , J  
$$

---

### Variazione di energia potenziale

Per una forza conservativa vale:

$$  
L = -\Delta U  
$$

Quindi:

$$  
\Delta U = -L  
$$

$$  
\Delta U = -13.1 , J  
$$

L’energia potenziale diminuisce perché il corpo si muove verso il basso.

---

### Energia potenziale iniziale

Se nel punto più basso poniamo:

$$  
U_f = 0  
$$

allora:

$$  
\Delta U = U_f - U_i  
$$

$$  
-13.1 = 0 - U_i  
$$

quindi:

$$  
U_i = 13.1 , J  
$$

Alla partenza l’energia potenziale valeva quindi:

$$  
U_i = 13.1 , J  
$$

---

### Aumentando l’angolo $\theta$

Se aumenta l’angolo $\theta$, aumenta anche la differenza di altezza:

$$  
\Delta h = l(1 - \cos \theta)  
$$

Quindi aumentano:

- il lavoro compiuto dalla forza di gravità;
    
- l’energia potenziale iniziale.
    

In pratica, più il pendolo viene sollevato lateralmente, più energia potenziale possiede all’inizio.

## Esercizio 4 - Ascensore sollevato a velocità costante

### Traccia

Il motore di un ascensore solleva con **velocità costante** la cabina contenente quattro persone per un dislivello:

$$  
h = 45 , m  
$$

La massa complessiva della cabina e delle persone è:

$$  
m = 450 , kg  
$$

Determinare:

1. il lavoro compiuto dal motore;
    
2. il lavoro compiuto dalla forza peso.
    

---

### Soluzione

Poiché l’ascensore si muove con **velocità costante**, l’accelerazione è nulla:

$$  
a = 0  
$$

Quindi anche la risultante delle forze è nulla:

$$  
\sum F = 0  
$$

Il motore deve esercitare una forza verso l’alto uguale in modulo alla forza peso:

$$  
F = mg  
$$

Lo spostamento è verso l’alto ed è parallelo alla forza del motore, quindi il lavoro del motore è positivo:

$$  
L_{motore} = Fh  
$$

Sostituendo:

$$  
L_{motore} = mgh  
$$

$$  
L_{motore} = 450 \cdot 9.8 \cdot 45  
$$

$$  
L_{motore} \approx 2.0 \cdot 10^5 , J  
$$

Quindi:

$$  
L_{motore} = 2.0 \cdot 10^5 , J  
$$

---

### Lavoro della forza peso

La forza peso è diretta verso il basso, mentre lo spostamento dell’ascensore è verso l’alto.

Quindi forza peso e spostamento formano un angolo di:

$$  
180^\circ  
$$

Per questo il lavoro della forza peso è negativo:

$$  
L_{peso} = -mgh  
$$

$$  
L_{peso} = -2.0 \cdot 10^5 , J  
$$

---

### Interpretazione

Il lavoro del motore è positivo perché il motore aiuta il movimento.

Il lavoro della forza peso è negativo perché la gravità si oppone al sollevamento.

Poiché l’ascensore si muove a velocità costante, la variazione di energia cinetica è nulla:

$$  
\Delta K = 0  
$$

Infatti il lavoro totale è:

$$  
L_{tot} = L_{motore} + L_{peso}  
$$

$$  
L_{tot} = 2.0 \cdot 10^5 - 2.0 \cdot 10^5 = 0  
$$

Quindi il risultato è coerente con il teorema dell’energia cinetica:

$$  
L_{tot} = \Delta K = 0  
$$

---

## Esercizio 5 - Cassa trascinata con attrito

### Traccia

Una cassa di massa:

$$  
m = 75 , kg  
$$

viene spostata di:

$$  
s = 4.0 , m  
$$

su un pavimento orizzontale.

La cassa viene tirata tramite un filo applicato sulla sua sommità, che forma con l’orizzontale un angolo:

$$  
\alpha = 35^\circ  
$$

La tensione del filo vale:

$$  
T = 520 , N  
$$

Il coefficiente di attrito dinamico tra cassa e pavimento è:

$$  
\mu_d = 0.72  
$$

Determinare:

1. il lavoro del filo e il lavoro della forza di attrito;
    
2. quanto deve valere la tensione $T$ affinché la cassa si muova di moto uniforme.
    

---

### Soluzione del punto 1

La tensione del filo forma un angolo $\alpha$ con lo spostamento.

Il lavoro del filo si calcola con:

$$  
L_T = Ts \cos \alpha  
$$

Sostituendo:

$$  
L_T = 520 \cdot 4.0 \cdot \cos 35^\circ  
$$

$$  
L_T \approx 1.7 \cdot 10^3 , J  
$$

Quindi:

$$  
L_T = 1.7 \cdot 10^3 , J  
$$

Il lavoro è positivo perché la tensione favorisce lo spostamento della cassa.

---

### Calcolo della forza di attrito

Sulla cassa agiscono:

- il peso $mg$, verso il basso;
    
- la reazione normale $N$, verso l’alto;
    
- la tensione $T$, inclinata verso l’alto;
    
- l’attrito dinamico, opposto al moto.
    

Poiché non c’è movimento verticale, la risultante verticale deve essere nulla.

La componente verticale della tensione è:

$$  
T \sin \alpha  
$$

Quindi:

$$  
N + T \sin \alpha = mg  
$$

Da cui:

$$  
N = mg - T \sin \alpha  
$$

La forza di attrito dinamico vale:

$$  
F_d = \mu_d N  
$$

quindi:

$$  
F_d = \mu_d (mg - T \sin \alpha)  
$$

Sostituendo:

$$  
F_d = 0.72 \cdot (75 \cdot 9.8 - 520 \sin 35^\circ)  
$$

$$  
F_d \approx 3.1 \cdot 10^2 , N  
$$

---

### Lavoro della forza di attrito

L’attrito ha verso opposto allo spostamento, quindi il suo lavoro è negativo:

$$  
L_d = -F_d s  
$$

$$  
L_d = -\mu_d (mg - T \sin \alpha)s  
$$

Sostituendo:

$$  
L_d \approx -1.3 \cdot 10^3 , J  
$$

Quindi:

$$  
L_d = -1.3 \cdot 10^3 , J  
$$

---

### Soluzione del punto 2

Affinché la cassa si muova di **moto uniforme**, la velocità deve essere costante.

Quindi:

$$  
a = 0  
$$

e la risultante delle forze orizzontali deve essere nulla.

La componente orizzontale della tensione è:

$$  
T \cos \alpha  
$$

La forza di attrito è:

$$  
F_d = \mu_d (mg - T \sin \alpha)  
$$

Per il moto uniforme deve valere:

$$  
T \cos \alpha = \mu_d (mg - T \sin \alpha)  
$$

Portiamo i termini con $T$ insieme:

$$  
T \cos \alpha + \mu_d T \sin \alpha = \mu_d mg  
$$

Raccogliendo $T$:

$$  
T(\cos \alpha + \mu_d \sin \alpha) = \mu_d mg  
$$

Quindi:

$$  
T = \frac{\mu_d mg}{\cos \alpha + \mu_d \sin \alpha}  
$$

Sostituendo i dati:

$$  
T = \frac{0.72 \cdot 75 \cdot 9.8}{\cos 35^\circ + 0.72 \sin 35^\circ}  
$$

$$  
T \approx 4.3 \cdot 10^2 , N  
$$

Quindi, per avere moto uniforme, la tensione dovrebbe essere circa:

$$  
T \approx 430 , N  
$$

---

### Interpretazione

Nel primo caso la tensione data è:

$$  
T = 520 , N  
$$

ma per il moto uniforme basterebbe circa:

$$  
T = 430 , N  
$$

Quindi, con $520 , N$, la componente orizzontale della tensione è maggiore dell’attrito e la cassa tende ad accelerare.

L’attrito compie sempre lavoro negativo perché si oppone al moto.

## Esercizio 6 - Piano inclinato senza attrito

### Traccia

Un punto materiale di massa:

$$  
m = 18 , kg  
$$

scende lungo un piano inclinato di altezza:

$$  
h = 2.5 , m  
$$

Sapendo che parte da fermo e che **non sono presenti forze di attrito**, determinare:

1. il lavoro compiuto dalla forza peso quando il punto materiale arriva in fondo al piano inclinato;
    
2. il modulo della velocità finale.
    

---

### Soluzione

Durante la discesa lungo il piano inclinato, le forze che agiscono sul corpo sono:

- la forza peso $mg$;
    
- la reazione normale $N$ del piano.
    

La reazione normale è perpendicolare allo spostamento, quindi non compie lavoro.

L’unica forza che compie lavoro è la forza peso.

Il lavoro della forza peso dipende solo dalla variazione di altezza:

$$  
L_p = mgh  
$$

Infatti, indicando con $\ell$ la lunghezza del piano inclinato e con $\alpha$ l’angolo di inclinazione:

$$  
h = \ell \sin \alpha  
$$

quindi:

$$  
L_p = mg\ell \sin \alpha = mgh  
$$

Sostituendo i dati:

$$  
L_p = 18 \cdot 9.8 \cdot 2.5  
$$

$$  
L_p \approx 440 , J  
$$

Quindi:

$$  
L_p = 440 , J  
$$

---

### Velocità finale

Per trovare la velocità finale usiamo il teorema dell’energia cinetica:

$$  
L_{tot} = \Delta K  
$$

Il corpo parte da fermo, quindi:

$$  
K_i = 0  
$$

Non essendoci attrito, tutto il lavoro della forza peso diventa energia cinetica finale:

$$  
mgh = \frac{1}{2}mv^2  
$$

La massa si semplifica:

$$  
gh = \frac{1}{2}v^2  
$$

Da cui:

$$  
v = \sqrt{2gh}  
$$

Sostituendo:

$$  
v = \sqrt{2 \cdot 9.8 \cdot 2.5}  
$$

$$  
v = \sqrt{49}  
$$

$$  
v = 7.0 , m/s  
$$

Quindi la velocità finale è:

$$  
v = 7.0 , m/s  
$$

---

### Interpretazione

In assenza di attrito, l’energia potenziale gravitazionale persa dal corpo si trasforma completamente in energia cinetica.

Per questo la velocità finale dipende solo dall’altezza $h$, non dalla massa del corpo o dalla lunghezza del piano inclinato.

---

## Esercizio 7 - Piano inclinato con attrito dinamico

### Traccia

Un punto materiale di massa:

$$  
m = 18 , kg  
$$

scende lungo un piano inclinato di altezza:

$$  
h = 2.5 , m  
$$

e lunghezza:

$$  
\ell = 7.5 , m  
$$

Sapendo che parte da fermo e che la velocità finale in fondo al piano inclinato ha modulo:

$$  
v = 5.0 , m/s  
$$

determinare il modulo della forza di attrito radente dinamico presente tra il punto materiale e la superficie del piano inclinato.

---

### Soluzione

In questo caso ci sono due forze che compiono lavoro:

- la forza peso, che compie lavoro positivo;
    
- la forza di attrito dinamico, che compie lavoro negativo.
    

La reazione normale non compie lavoro perché è perpendicolare allo spostamento.

Il lavoro della forza peso è:

$$  
L_p = mgh

$$
Il lavoro dell’attrito dinamico è negativo perché l’attrito si oppone al moto:

$$
L_d = -F_d \ell
$$

Per il teorema dell’energia cinetica:

$$
L_p + L_d = \Delta K
$$

Poiché il corpo parte da fermo:

$$
\Delta K = \frac{1}{2}mv^2
$$

Quindi:

$$
mgh - F_d \ell = \frac{1}{2}mv^2
$$

Ora isoliamo $F_d$:

$$  
F_d \ell = mgh - \frac{1}{2}mv^2  
$$

$$  
F_d = \frac{mgh - \frac{1}{2}mv^2}{\ell}  
$$

Possiamo anche scriverla così:

$$  
F_d = \frac{m}{2\ell}(2gh - v^2)  
$$

Sostituendo i dati:

$$  
F_d = \frac{18}{2 \cdot 7.5}(2 \cdot 9.8 \cdot 2.5 - 5.0^2)  
$$

$$  
F_d = \frac{18}{15}(49 - 25)  
$$

$$  
F_d = 1.2 \cdot 24  
$$

$$  
F_d = 28.8 , N  
$$

Quindi:

$$  
F_d \approx 29 , N  
$$

---

### Interpretazione

Senza attrito, nell’esercizio precedente, la velocità finale sarebbe stata:

$$  
v = 7.0 , m/s  
$$

In questo esercizio, invece, la velocità finale è minore:

$$  
v = 5.0 , m/s  
$$

Questo succede perché una parte dell’energia meccanica viene dissipata dall’attrito.

La forza di attrito compie lavoro negativo e riduce l’energia cinetica finale del corpo.


## Esercizio 8 - Slitta trainata con velocità costante

### Traccia

Un bambino traina una slitta su un piano orizzontale applicando una forza di modulo:

$$  
F = 50 , N  
$$

La forza forma con l’orizzontale un angolo:

$$  
\alpha = 35^\circ  
$$

La slitta si muove con velocità costante:

$$  
v = 0.75 , m/s  
$$

per un tempo:

$$  
t = 12 , s  
$$

Determinare:

1. il lavoro fatto dalle forze agenti sulla slitta nel tempo $t = 12 , s$;
    
2. la potenza della forza $F$.
    

---

### Soluzione

Sulla slitta agiscono quattro forze:

- la forza peso $mg$, diretta verso il basso;
    
- la reazione normale $N$, diretta verso l’alto;
    
- la forza $F$ applicata dal bambino;
    
- la forza di attrito dinamico $F_a$, opposta al moto.
    

La forza peso e la reazione normale sono perpendicolari allo spostamento, quindi il loro lavoro è nullo:

$$  
L_{peso} = 0  
$$

$$  
L_N = 0  
$$

Lo spostamento della slitta si ricava da:

$$  
s = vt  
$$

Sostituendo:

$$  
s = 0.75 \cdot 12 = 9 , m  
$$

---

### Lavoro della forza del bambino

La forza $F$ non è parallela allo spostamento, ma forma un angolo $\alpha = 35^\circ$.

Quindi il lavoro della forza $F$ è:

$$  
L_F = Fs \cos \alpha  
$$

Poiché $s = vt$, possiamo scrivere:

$$  
L_F = Fvt \cos \alpha  
$$

Sostituendo:

$$  
L_F = 50 \cdot 0.75 \cdot 12 \cdot \cos 35^\circ  
$$

$$  
L_F \approx 370 , J  
$$

Quindi:

$$  
L_F = 370 , J  
$$

Il lavoro è positivo perché la componente orizzontale della forza aiuta il moto.

---

### Lavoro della forza di attrito

Dato che la slitta si muove con velocità costante:

$$  
a = 0  
$$

quindi la risultante delle forze deve essere nulla.

La componente orizzontale della forza del bambino è:

$$  
F \cos \alpha  
$$

L’attrito deve avere stesso modulo e verso opposto:

$$  
F_a = F \cos \alpha  
$$

Poiché l’attrito è opposto allo spostamento, il suo lavoro è negativo:

$$  
L_a = F_a s \cos 180^\circ  
$$

$$  
L_a = -F_a s  
$$

Dato che l’attrito compensa il lavoro della forza $F$:

$$  
L_a = -L_F  
$$

quindi:

$$  
L_a = -370 , J  
$$

---

### Lavoro totale

Il lavoro totale è:

$$  
L_{tot} = L_F + L_a + L_{peso} + L_N  
$$

$$  
L_{tot} = 370 - 370 + 0 + 0  
$$

$$  
L_{tot} = 0  
$$

Questo è coerente con il teorema dell’energia cinetica, perché la velocità è costante e quindi:

$$  
\Delta K = 0  
$$

---

### Potenza della forza $F$

La potenza media della forza $F$ è:

$$  
P = \frac{L_F}{t}  
$$

Sostituendo:

$$  
P = \frac{370}{12}  
$$

$$  
P \approx 31 , W  
$$

Quindi:

$$  
P = 31 , W  
$$

Si poteva calcolare anche direttamente con:

$$  
P = Fv \cos \alpha  
$$

---

## Esercizio 9 - Automobile accelerata da una forza costante

### Traccia

Un’automobile di massa:

$$  
m = 720 , kg  
$$

è sottoposta a una forza di modulo costante.

L’automobile accelera da una velocità iniziale:

$$  
v_1 = 3.5 , m/s  
$$

a una velocità finale:

$$  
v_2 = 12 , m/s  
$$

percorrendo uno spazio:

$$  
s = 30 , m  
$$

Determinare:

1. il modulo della forza esercitata dal motore e il lavoro da essa svolto;
    
2. la potenza erogata dal motore.
    

---

### Soluzione del punto 1

Per calcolare il lavoro si usa il teorema dell’energia cinetica:

$$  
L = \Delta K  
$$

quindi:

$$  
L = \frac{1}{2}m(v_2^2 - v_1^2)  
$$

Sostituendo:

$$  
L = \frac{1}{2} \cdot 720 \cdot (12^2 - 3.5^2)  
$$

$$  
L = 360 \cdot (144 - 12.25)  
$$

$$  
L = 360 \cdot 131.75  
$$

$$  
L \approx 4.7 \cdot 10^4 , J  
$$

Quindi il lavoro svolto dal motore è:

$$  
L = 4.7 \cdot 10^4 , J  
$$

---

### Calcolo della forza

Dato che la forza è costante e parallela allo spostamento, il lavoro può essere scritto come:

$$  
L = Fs  
$$

Da cui:

$$  
F = \frac{L}{s}  
$$

Sostituendo:

$$  
F = \frac{4.7 \cdot 10^4}{30}  
$$

$$  
F \approx 1.6 \cdot 10^3 , N  
$$

Quindi:

$$  
F = 1.6 \cdot 10^3 , N  
$$

> Nota: nella slide sembra comparire $1.6 , N$, ma il valore corretto è circa $1.6 \cdot 10^3 , N$.

---

### Soluzione del punto 2

Per trovare la potenza media serve il tempo impiegato.

Poiché la forza è costante, anche l’accelerazione è costante.

Usiamo la relazione:

$$  
v_2^2 = v_1^2 + 2as  
$$

Da cui:

$$  
a = \frac{v_2^2 - v_1^2}{2s}  
$$

Sostituendo:

$$  
a = \frac{12^2 - 3.5^2}{2 \cdot 30}  
$$

$$  
a = \frac{144 - 12.25}{60}  
$$

$$  
a \approx 2.2 , m/s^2  
$$

Ora troviamo il tempo:

$$  
v_2 = v_1 + at  
$$

quindi:

$$  
t = \frac{v_2 - v_1}{a}  
$$

$$  
t = \frac{12 - 3.5}{2.2}  
$$

$$  
t \approx 3.9 , s  
$$

La potenza media è:

$$  
P = \frac{L}{t}  
$$

Sostituendo:

$$  
P = \frac{4.7 \cdot 10^4}{3.9}  
$$

$$  
P \approx 1.2 \cdot 10^4 , W  
$$

Quindi:

$$  
P \approx 12 , kW  
$$

---

### Interpretazione

Il motore compie lavoro positivo perché aumenta l’energia cinetica dell’automobile.

La forza è costante, quindi il lavoro dipende dallo spazio percorso:

$$  
L = Fs  
$$

La potenza media indica quanto rapidamente viene svolto quel lavoro:

$$  
P = \frac{L}{t}  
$$

Più rapidamente il motore compie lo stesso lavoro, maggiore è la potenza.


### Soluzione del punto 2 - Potenza erogata dal motore

Poiché la forza è costante, il moto è **uniformemente accelerato**.

Nel moto uniformemente accelerato, la velocità media è:

$$  
v_m = \frac{v_1 + v_2}{2}  
$$

Lo spazio percorso si può quindi scrivere come:

$$  
s = v_m t  
$$

cioè:

$$  
s = \frac{v_1 + v_2}{2}t  
$$

Da questa formula ricaviamo il tempo:

$$  
t = \frac{2s}{v_1 + v_2}  
$$

Sostituendo i dati:

$$  
t = \frac{2 \cdot 30}{3.5 + 12}  
$$

$$  
t = \frac{60}{15.5}  
$$

$$  
t \approx 3.9 , s  
$$

La potenza media sviluppata dal motore è:

$$  
P = \frac{L}{t}  
$$

Il lavoro trovato prima era:

$$  
L = 4.7 \cdot 10^4 , J  
$$

Quindi:

$$  
P = \frac{4.7 \cdot 10^4}{3.9}  
$$

$$  
P \approx 1.2 \cdot 10^4 , W  
$$

Quindi:

$$  
P = 1.2 \cdot 10^4 , W  
$$

oppure:

$$  
P = 12 , kW  
$$

La slide riassume il calcolo in un’unica formula:

$$  
P = \frac{L}{t}

\frac{m}{4s}(v_2^2 - v_1^2)(v_1 + v_2)  
$$

Questa formula deriva dal fatto che:

$$  
L = \frac{1}{2}m(v_2^2 - v_1^2)  
$$

e:

$$  
t = \frac{2s}{v_1 + v_2}  
$$

Quindi il motore eroga una potenza media di circa:

$$  
P = 1.2 \cdot 10^4 , W  
$$

## Quesiti - Energia potenziale

### Q.1 Quali caratteristiche ha il lavoro svolto da forze conservative?

Il lavoro svolto da una **forza conservativa** dipende solo dalla posizione iniziale e dalla posizione finale del corpo.

Non dipende dal percorso seguito.

Quindi, se un corpo si sposta da un punto $A$ a un punto $B$, il lavoro della forza conservativa è sempre lo stesso, qualunque sia il cammino percorso.

$$  
L_{AB} = U_A - U_B  
$$

oppure:

$$  
L_{AB} = -\Delta U  
$$

dove $U$ è l’energia potenziale.

---

### Q.2 A quanto equivale il lavoro lungo un cammino chiuso in un campo di forze conservative?

In un **cammino chiuso**, il punto iniziale e il punto finale coincidono.

Quindi:

$$  
A = B  
$$

La variazione di energia potenziale è nulla:

$$  
\Delta U = 0  
$$

Perciò anche il lavoro della forza conservativa è nullo:

$$  
L = -\Delta U = 0  
$$

Quindi:

$$  
L_{chiuso} = 0  
$$

Questo è proprio uno dei modi per riconoscere una forza conservativa.

---

### Q.3 Che rapporto c’è tra una forza conservativa e l’energia potenziale associata?

A una forza conservativa si può associare una funzione scalare chiamata **energia potenziale** $U$.

La forza conservativa si ricava dall’energia potenziale tramite il **gradiente**:

$$  
\vec{F} = -\nabla U  
$$

Il segno meno indica che la forza punta nella direzione in cui l’energia potenziale diminuisce più rapidamente.

In coordinate cartesiane:

$$  
\nabla U =  
\left(  
\frac{\partial U}{\partial x},  
\frac{\partial U}{\partial y},  
\frac{\partial U}{\partial z}  
\right)  
$$

quindi:

 $$  
\vec{F}

\left(  
\frac{\partial U}{\partial x},  
\frac{\partial U}{\partial y},  
\frac{\partial U}{\partial z}  
\right)  
$$

In una sola dimensione diventa:

$$  
F_x = -\frac{dU}{dx}  
$$

---

### Riassunto veloce

- Le forze conservative hanno lavoro indipendente dal percorso.
    
- Il lavoro dipende solo da punto iniziale e finale.
    
- Su un cammino chiuso il lavoro è nullo:
    

$$  
L = 0  
$$

- Per una forza conservativa vale:
    

$$  
\vec{F} = -\nabla U  
$$

- Il lavoro è legato all’energia potenziale da:
    

$$  
L = -\Delta U  
$$


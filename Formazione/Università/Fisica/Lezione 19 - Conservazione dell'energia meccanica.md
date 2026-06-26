## Lavoro ed energia potenziale

Per una **forza conservativa**, il lavoro può essere espresso tramite la variazione di energia potenziale.

Il lavoro di una forza conservativa vale:

$$  
L = -\Delta U  
$$

cioè:

$$  
L = U_i - U_f  
$$

Se durante il moto agiscono **solo forze conservative**, l'energia meccanica si conserva:

$$  
E_m = K + U  
$$

quindi:

$$  
K_i + U_i = K_f + U_f  
$$

dove:

$$  
K = \frac{1}{2}mv^2  
$$

è l'energia cinetica, mentre nel caso gravitazionale:

$$  
U = mgh  
$$

è l'energia potenziale gravitazionale.

Quando un corpo cade sotto l'azione della sola forza peso, perde energia potenziale gravitazionale e acquista energia cinetica.

---

## Esercizio 1 - Massa lasciata cadere su una molla

### Traccia

Una massa di $700 \ g$ viene lasciata da ferma ad altezza $h_0$ sopra una molla di costante elastica:

$$  
k = 400 \ N/m  
$$

La massa rimane solidale con la molla e si arresta dopo averla compressa di:

$$  
\Delta y = 19.0 \ cm  
$$

Calcolare:

1. Il lavoro svolto dalla massa sulla molla.
    
2. Il lavoro svolto dalla molla sulla massa.
    
3. Il valore di $h_0$.
    
4. Se $h_0$ fosse doppio, quale sarebbe la massima compressione della molla?
    

---

### Dati

$$  
m = 700 \ g = 0.7 \ kg  
$$

$$  
k = 400 \ N/m  
$$

$$  
\Delta y = 19.0 \ cm = 0.19 \ m  
$$

---

### a) Lavoro svolto dalla massa sulla molla

Quando la massa comprime la molla, trasferisce energia alla molla.

L'energia elastica accumulata dalla molla è:

$$  
U_e = \frac{1}{2}k(\Delta y)^2  
$$

Sostituendo i dati:

$$  
U_e = \frac{1}{2} \cdot 400 \cdot (0.19)^2  
$$$$



U_e = 7.2 \ J  
$$

Quindi il lavoro svolto dalla massa sulla molla è:

$$  
L = 7.2 \ J  
$$

---

### b) Lavoro svolto dalla molla sulla massa

La molla esercita una forza opposta allo spostamento della massa.

Per questo motivo il lavoro ha segno negativo:

$$  
L = -7.2 \ J  
$$

---

### c) Calcolo di $h_0$

L'energia potenziale gravitazionale persa dalla massa viene trasformata in energia elastica della molla.

La massa scende complessivamente di:

$$  
h_0 + \Delta y  
$$

Quindi:

$$  
mg(h_0 + \Delta y) = \frac{1}{2}k(\Delta y)^2  
$$

Dato che:

$$  
\frac{1}{2}k(\Delta y)^2 = 7.2 \ J  
$$

allora:

$$  
0.7 \cdot 9.8 \cdot (h_0 + 0.19) = 7.2  
$$

$$  
6.86(h_0 + 0.19) = 7.2  
$$

$$  
h_0 + 0.19 = \frac{7.2}{6.86}  
$$

$$  
h_0 + 0.19 \approx 1.05  
$$

$$  
h_0 \approx 0.86 \ m  
$$

Risultato:

$$  
h_0 = 0.86 \ m  
$$

---

### d) Compressione se $h_0$ fosse doppio

Se l'altezza iniziale fosse doppia, avremmo:

$$  
2h_0  
$$

La massa scenderebbe complessivamente di:

$$  
2h_0 + \Delta y  
$$

Per conservazione dell'energia:

$$  
mg(2h_0 + \Delta y) = \frac{1}{2}k(\Delta y)^2  
$$

Questa è un'equazione di secondo grado nella nuova compressione $\Delta y$.

Risolvendo e prendendo la soluzione positiva si ottiene:

$$  
\Delta y = 0.26 \ m  
$$

Quindi la massima compressione della molla sarebbe:

$$  
\Delta y = 26 \ cm  
$$

---

## Esercizio 2 - Energia potenziale e forza

### Traccia

L'energia potenziale di un campo di forze conservativo è data da:

$$  
U(x,y,z) = x^2 - xy + z^2  
$$

Nel punto:

$$  
P = (1,0,0)  
$$

calcolare l'angolo formato dalla forza con l'asse $x$.

---

### Soluzione

Per un campo conservativo, la forza si ricava dall'energia potenziale tramite il gradiente.

In generale:

$$  
\vec{F} = -\nabla U  
$$

Nella slide vengono date le componenti della forza:

$$  
F_x = 2x + y  
$$

$$  
F_y = x  
$$

$$  
F_z = -2z  
$$

Nel punto $P = (1,0,0)$:

$$  
F_x = 2  
$$

$$  
F_y = 1  
$$

$$  
F_z = 0  
$$

Quindi la forza è:

$$  
\vec{F} = 2\vec{i} + \vec{j}  
$$

---

### Calcolo dell'angolo con l'asse $x$

L'asse $x$ ha versore $\vec{i}$.

Usiamo il prodotto scalare:

$$  
\vec{F} \cdot \vec{i} = |\vec{F}| |\vec{i}| \cos\theta  
$$

Poiché:

$$  
\vec{F} = 2\vec{i} + \vec{j}  
$$

il modulo della forza è:

$$  
|\vec{F}| = \sqrt{2^2 + 1^2}  
$$

$$  
|\vec{F}| = \sqrt{5}  
$$

Il prodotto scalare con $\vec{i}$ vale:

$$  
\vec{F} \cdot \vec{i} = 2  
$$

Quindi:

$$  
2 = \sqrt{5}\cos\theta  
$$

$$  
\cos\theta = \frac{2}{\sqrt{5}}  
$$

$$  
\theta = \arccos\left(\frac{2}{\sqrt{5}}\right)  
$$

$$  
\theta = 26.6^\circ  
$$

Risultato:

$$  
\theta = 26.6^\circ  
$$

---

## Nota

Per l'esame conviene seguire il procedimento mostrato nelle slide.  
La cosa importante da ricordare è che, quando è nota l'energia potenziale $U$, la forza si collega al gradiente di $U$.



## Conservazione dell'energia meccanica

Per una forza conservativa, il lavoro può essere scritto in due modi:

1. tramite la variazione di energia cinetica;
    
2. tramite la variazione di energia potenziale.
    

Il teorema dell'energia cinetica dice:

$$  
L_{AB} = K_B - K_A  
$$

Per una forza conservativa, invece:

$$  
L_{AB} = -\Delta U  
$$

cioè:

$$  
L_{AB} = U_A - U_B  
$$

Uguagliando le due espressioni:

$$  
K_B - K_A = U_A - U_B  
$$

Portando i termini dello stesso punto insieme:

$$  
K_A + U_A = K_B + U_B  
$$

Questa è la **conservazione dell'energia meccanica**.

L'energia meccanica totale è:

$$  
E_m = K + U  
$$

Se agiscono solo forze conservative:

$$  
E_m = costante  
$$

quindi:

$$  
K + U = E  
$$

Nel caso della forza peso:

$$  
K = \frac{1}{2}mv^2  
$$

$$  
U = mgy  
$$

perciò:

$$  
\frac{1}{2}mv^2 + mgy = E  
$$

Quindi, se un corpo si muove sotto l'azione della sola gravità, l'energia meccanica totale rimane costante.

---

## Caduta di un corpo sotto gravità

Quando un corpo cade sotto l'effetto della gravità:

- perde energia potenziale gravitazionale;
    
- acquista energia cinetica;
    
- l'energia meccanica totale resta costante.
    

Quindi durante la caduta non si crea né si distrugge energia: semplicemente si trasforma da energia potenziale a energia cinetica.

La relazione è:

$$  
K_i + U_i = K_f + U_f  
$$

oppure:

$$  
\frac{1}{2}mv_i^2 + mgy_i =  
\frac{1}{2}mv_f^2 + mgy_f  
$$

Se il corpo parte da fermo, allora:

$$  
v_i = 0  
$$

e quindi l'energia iniziale è solo potenziale.

---

## Sistema massa-molla senza attrito

Anche una massa collegata a una molla può conservare l'energia meccanica, se si muove su un piano orizzontale senza attrito.

In questo caso l'energia meccanica è data dalla somma di:

- energia cinetica;
    
- energia potenziale elastica.
    

L'energia cinetica è:

$$  
K = \frac{1}{2}mv^2  
$$

L'energia potenziale elastica è:

$$  
U_e = \frac{1}{2}kx^2  
$$

Quindi l'energia meccanica totale è:

$$  
E_m = \frac{1}{2}mv^2 + \frac{1}{2}kx^2  
$$

Se non ci sono attriti:

$$  
\frac{1}{2}mv^2 + \frac{1}{2}kx^2 = E  
$$

Durante le oscillazioni:

- quando la massa passa vicino alla posizione di equilibrio, la velocità è massima e quindi è massima l'energia cinetica;
    
- quando la molla è molto compressa o molto allungata, la velocità si annulla e l'energia è quasi tutta potenziale elastica.
    

Quindi l'energia continua a trasformarsi:

$$  
U_e \leftrightarrow K  
$$

ma la somma rimane costante.

---

## Forze non conservative

Se sono presenti anche forze non conservative, come l'attrito, l'energia meccanica non si conserva più.

Il teorema dell'energia cinetica rimane valido:

$$  
L_c + L_{nc} = K_B - K_A  
$$

dove:

- $L_c$ è il lavoro delle forze conservative;
    
- $L_{nc}$ è il lavoro delle forze non conservative.
    

Per le forze conservative:

$$  
L_c = U_A - U_B  
$$

Sostituendo:

$$  
U_A - U_B + L_{nc} = K_B - K_A  
$$

Da cui:

$$  
L_{nc} = K_B + U_B - (K_A + U_A)  
$$

Quindi:

$$  
L_{nc} = \Delta E_m  
$$

Questo significa che il lavoro delle forze non conservative è uguale alla variazione dell'energia meccanica.

Se c'è attrito, di solito:

$$  
L_{nc} < 0  
$$

quindi l'energia meccanica diminuisce.

In realtà l'energia totale del sistema non sparisce: viene trasformata in altre forme di energia, ad esempio energia termica dovuta all'attrito.

---

## Formula importante da ricordare

Se agiscono solo forze conservative:

$$  
E_{m,i} = E_{m,f}  
$$

cioè:

$$  
K_i + U_i = K_f + U_f  
$$

Se invece agiscono anche forze non conservative:

$$  
L_{nc} = \Delta E_m  
$$

cioè:

$$  
L_{nc} = E_{m,f} - E_{m,i}  
$$

## Definizione generale di potenza

La **potenza** indica la rapidità con cui un sistema trasferisce energia oppure converte energia da una forma a un'altra.

La potenza istantanea è:

$$  
P = \frac{dE}{dt}  
$$

dove $dE$ è la variazione infinitesima di energia e $dt$ l'intervallo infinitesimo di tempo.

In un intervallo finito $\Delta t$, si definisce invece la **potenza media**:

$$  
P_m = \frac{\Delta E}{\Delta t}  
$$

In pratica:

- se un sistema trasferisce molta energia in poco tempo, ha grande potenza;
    
- se trasferisce la stessa energia in più tempo, ha potenza minore.
    

---

## Equilibrio ed energia potenziale

Per una forza conservativa, l'energia potenziale dipende dalla posizione:

$$  
U = U(x,y,z)  
$$

Nel caso unidimensionale:

$$  
U = U(x)  
$$

La forza è legata alla derivata dell'energia potenziale:

$$  
F_x = -\frac{dU}{dx}  
$$

Un punto è di equilibrio quando la forza è nulla:

$$  
F_x = 0  
$$

quindi:

$$  
\frac{dU}{dx} = 0  
$$

Questo significa che i punti di equilibrio si trovano dove il grafico di $U(x)$ ha derivata nulla, cioè nei punti di massimo o minimo.

---

### Equilibrio stabile

Un punto di **minimo relativo** dell'energia potenziale è un punto di equilibrio stabile.

Se il corpo viene spostato leggermente da quel punto, la forza tende a riportarlo verso la posizione di equilibrio.

Esempio: nel punto $A$ della figura, l'energia potenziale ha un minimo.  
Quindi $A$ è un punto di equilibrio stabile.

---

### Equilibrio instabile

Un punto di **massimo relativo** dell'energia potenziale è un punto di equilibrio instabile.

Se il corpo viene spostato leggermente da quel punto, la forza tende ad allontanarlo ancora di più dalla posizione iniziale.

Esempio: nel punto $B$ della figura, l'energia potenziale ha un massimo.  
Quindi $B$ è un punto di equilibrio instabile.

---

## Esercizio - Piano inclinato, attrito e molla

### Traccia

Un punto materiale di massa:

$$  
m = 20 \ g  
$$

scende, partendo da fermo, lungo un piano inclinato liscio.

Alla fine del piano inclinato, esso scorre su un tratto orizzontale scabro con coefficiente di attrito:

$$  
\mu = 0.1  
$$

andando a urtare una molla di massa trascurabile fissata a una parete verticale.

La molla ha lunghezza a riposo:

$$  
l_0 = 10 \ cm  
$$

e costante elastica:

$$  
k = 2 \ N/m  
$$

La parete su cui è fissata la molla si trova a distanza:

$$  
d = 40 \ cm  
$$

dalla fine del piano inclinato.

Determinare l'altezza $h$ da cui deve partire il punto materiale per arrivare a toccare la parete dopo aver urtato la molla.

---

### Dati in unità SI

$$  
m = 0.02 \ kg  
$$

$$  
l_0 = 0.1 \ m  
$$

$$  
d = 0.4 \ m  
$$

$$  
\mu = 0.1  
$$

$$  
k = 2 \ N/m  
$$

---

### Idea fisica

Il corpo parte da fermo e arriva di nuovo fermo quando tocca la parete.

All'inizio ha solo energia potenziale gravitazionale:

$$  
E_i = mgh  
$$

Alla fine ha energia potenziale elastica nella molla compressa:

$$  
E_f = \frac{1}{2}kl_0^2  
$$

Sul tratto orizzontale agisce l'attrito, che compie lavoro negativo:

$$  
L_{attrito} = -\mu mgd  
$$

Dato che c'è una forza non conservativa, usiamo:

$$  
L_{nc} = \Delta E_m  
$$

cioè:

$$  
-\mu mgd = E_f - E_i  
$$

Sostituendo:

$$  
-\mu mgd = \frac{1}{2}kl_0^2 - mgh  
$$

Da cui:

$$  
mgh = \frac{1}{2}kl_0^2 + \mu mgd  
$$

e quindi:

$$  
h = \frac{\frac{1}{2}kl_0^2 + \mu mgd}{mg}  
$$

---

### Risultato

Nella slide viene riportato:

$$  
h = 91 \ mm  
$$

cioè:

$$  
h = 0.091 \ m  
$$

---

### Nota

La formula importante dell'esercizio è:

$$  
\frac{1}{2}kl_0^2 - mgh = -\mu mgd  
$$

oppure, in forma più comoda:

$$  
h = \frac{\frac{1}{2}kl_0^2 + \mu mgd}{mg}  
$$

Serve perché l'energia iniziale gravitazionale deve compensare sia l'energia elastica immagazzinata nella molla, sia l'energia persa per attrito.
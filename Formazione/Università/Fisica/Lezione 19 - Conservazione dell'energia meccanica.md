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

## Esercizio - Sasso lanciato verso l'alto

### Traccia

Un sasso viene lanciato verso l'alto a partire dall'altezza:

$$  
h_1 = 150 \ cm = 1.5 \ m  
$$

rispetto al suolo, con velocità iniziale:

$$  
v_1 = 8.5 \ m/s  
$$

Determinare:

1. l'altezza massima $H$ raggiunta;
    
2. il modulo della velocità $v_2$ quando il sasso si trova a quota $h_2 = 3.2 \ m$;
    
3. l'altezza $h_3$ alla quale il modulo della velocità vale $v_3 = 4.0 \ m/s$;
    
4. il modulo della velocità con cui il sasso cade a terra.
    

---

### Idea fisica

Sul sasso agisce solo la forza peso, che è conservativa.  
Quindi l'energia meccanica si conserva:

$$  
K_i + U_i = K_f + U_f  
$$

Nel caso della forza peso:

$$  
\frac{1}{2}mv^2 + mgh = costante  
$$

---

### 1) Altezza massima raggiunta

Nel punto più alto il sasso si ferma per un istante, quindi:

$$  
v = 0  
$$

L'energia iniziale è:

$$  
\frac{1}{2}mv_1^2 + mgh_1  
$$

Nel punto più alto l'energia è tutta potenziale:

$$  
mgH  
$$

Quindi:

$$  
\frac{1}{2}mv_1^2 + mgh_1 = mgH  
$$

Dividendo per $mg$:

$$  
H = h_1 + \frac{v_1^2}{2g}  
$$

Sostituendo:

$$  
H = 1.5 + \frac{(8.5)^2}{2 \cdot 9.8}  
$$

$$  
H \approx 5.2 \ m  
$$

Risultato:

$$  
H = 5.2 \ m  
$$

---

### 2) Velocità alla quota $h_2 = 3.2 \ m$

Usiamo ancora la conservazione dell'energia:

$$  
\frac{1}{2}mv_1^2 + mgh_1 =  
\frac{1}{2}mv_2^2 + mgh_2  
$$

Semplificando la massa e isolando $v_2$:

$$  
v_2 = \sqrt{v_1^2 - 2g(h_2 - h_1)}  
$$

Sostituendo:

$$  
v_2 = \sqrt{(8.5)^2 - 2 \cdot 9.8(3.2 - 1.5)}  
$$

$$  
v_2 \approx 6.2 \ m/s  
$$

Risultato:

$$  
v_2 = 6.2 \ m/s  
$$

Nota: questo è il **modulo** della velocità, quindi vale sia durante la salita sia durante la discesa alla stessa quota.

---

### 3) Altezza alla quale $v_3 = 4.0 \ m/s$

Di nuovo:

$$  
\frac{1}{2}mv_1^2 + mgh_1 =  
\frac{1}{2}mv_3^2 + mgh_3  
$$

Semplificando:

$$  
h_3 = h_1 + \frac{v_1^2 - v_3^2}{2g}  
$$

Sostituendo:

$$  
h_3 = 1.5 + \frac{(8.5)^2 - (4.0)^2}{2 \cdot 9.8}  
$$

$$  
h_3 \approx 4.4 \ m  
$$

Risultato:

$$  
h_3 = 4.4 \ m  
$$

---

### 4) Velocità con cui il sasso arriva a terra

Quando il sasso arriva a terra, l'altezza finale è:

$$  
h_f = 0  
$$

Quindi:

$$  
\frac{1}{2}mv_1^2 + mgh_1 = \frac{1}{2}mv^2  
$$

Semplificando:

$$  
v = \sqrt{v_1^2 + 2gh_1}  
$$

Sostituendo:

$$  
v = \sqrt{(8.5)^2 + 2 \cdot 9.8 \cdot 1.5}  
$$

$$  
v \approx 10 \ m/s  
$$

Risultato:

$$  
v = 10 \ m/s  
$$

---

## Esercizio - Sasso lanciato verso l'alto e molla

### Traccia

Un sasso di massa:

$$  
m = 2.4 \ kg  
$$

viene lanciato verso l'alto a partire dall'altezza:

$$  
h = 1.2 \ m  
$$

rispetto al suolo.

Dopo aver raggiunto l'altezza massima:

$$  
H = 5.6 \ m  
$$

il sasso ricade al suolo, dove comprime una molla di costante elastica:

$$  
k = 750 \ N/m  
$$

Determinare:

1. il modulo $v_0$ della velocità con cui il sasso è stato lanciato;
    
2. la deformazione $x$ della molla, trascurando l'altezza dal suolo quando la molla è compressa.
    

---

### 1) Velocità iniziale del sasso

Usiamo la conservazione dell'energia tra il punto iniziale e il punto di massima altezza.

All'inizio:

$$  
E_i = \frac{1}{2}mv_0^2 + mgh  
$$

Alla massima altezza la velocità è nulla, quindi:

$$  
E_f = mgH  
$$

Per conservazione dell'energia:

$$  
\frac{1}{2}mv_0^2 + mgh = mgH  
$$

Semplificando la massa:

$$  
\frac{1}{2}v_0^2 + gh = gH  
$$

Da cui:

$$  
v_0 = \sqrt{2g(H-h)}  
$$

Sostituendo:

$$  
v_0 = \sqrt{2 \cdot 9.8(5.6 - 1.2)}  
$$

$$  
v_0 \approx 9.3 \ m/s  
$$

Risultato:

$$  
v_0 = 9.3 \ m/s  
$$

---

### 2) Compressione della molla

Tra il punto di massima altezza e il punto in cui la molla è completamente compressa, l'energia potenziale gravitazionale diventa energia elastica.

Alla massima altezza:

$$  
E_i = mgH  
$$

Quando la molla è compressa, il sasso è fermo e l'energia è elastica:

$$  
E_f = \frac{1}{2}kx^2  
$$

Quindi:

$$  
mgH = \frac{1}{2}kx^2  
$$

Isoliamo $x$:

$$  
x = \sqrt{\frac{2mgH}{k}}  
$$

Sostituendo:

$$  
x = \sqrt{\frac{2 \cdot 2.4 \cdot 9.8 \cdot 5.6}{750}}  
$$

$$  
x \approx 0.35 \ m  
$$

Risultato:

$$  
x = 0.35 \ m = 35 \ cm  
$$

---

## Formule usate

Conservazione dell'energia meccanica:

$$  
K_i + U_i = K_f + U_f  
$$

Energia cinetica:

$$  
K = \frac{1}{2}mv^2  
$$

Energia potenziale gravitazionale:

$$  
U = mgh  
$$

Energia potenziale elastica:

$$  
U_e = \frac{1}{2}kx^2  
$$
## Esercizio - Piano inclinato con molla collegata al punto materiale

### Traccia

Un punto materiale di massa:

$$  
m = 4.5 \ kg  
$$

si trova inizialmente nel punto più alto di un piano inclinato di altezza:

$$  
h = 4.2 \ m  
$$

e lunghezza:

$$  
\ell = 10 \ m  
$$

Il punto viene spinto verso il basso con velocità iniziale:

$$  
v_0 = 12 \ m/s  
$$

Il punto materiale è collegato a una molla con lunghezza di equilibrio nulla. L'altro capo della molla è fissato nel vertice retto del piano inclinato.

Quando il punto materiale arriva nel punto più basso del piano inclinato, la sua velocità vale:

$$  
v = 2.0 \ m/s  
$$

Determinare:

1. la costante elastica $k$ della molla;
    
2. il lavoro compiuto dalla forza elastica.
    

---

### Idea fisica

Si usa la conservazione dell'energia meccanica.

Nel punto iniziale:

- il corpo ha energia cinetica;
    
- ha energia potenziale gravitazionale;
    
- la molla è allungata di $h$.
    

Nel punto finale:

- il corpo ha ancora energia cinetica;
    
- l'altezza è nulla;
    
- la molla è allungata di $b$.
    

Dal triangolo del piano inclinato:

$$  
b = \sqrt{\ell^2 - h^2}  
$$

---

### Conservazione dell'energia

L'energia iniziale è:

$$  
E_i = \frac{1}{2}mv_0^2 + mgh + \frac{1}{2}kh^2  
$$

L'energia finale è:

$$  
E_f = \frac{1}{2}mv^2 + \frac{1}{2}kb^2  
$$

Poiché $b^2 = \ell^2 - h^2$, si ha:

$$  
\frac{1}{2}mv_0^2 + mgh + \frac{1}{2}kh^2 =  
\frac{1}{2}mv^2 + \frac{1}{2}k(\ell^2 - h^2)  
$$

Isolando $k$:

$$  
k = \frac{m}{\ell^2 - 2h^2}(2gh + v_0^2 - v^2)  
$$

Sostituendo i dati:

$$  
k = 15 \ N/m  
$$

---

### Lavoro della forza elastica

Il lavoro compiuto dalla molla è uguale alla diminuzione della sua energia potenziale elastica:

$$  
L_{el} = U_{e,i} - U_{e,f}  
$$

quindi:

$$  
L_{el} = \frac{1}{2}kh^2 - \frac{1}{2}kb^2  
$$

Siccome $b^2 = \ell^2 - h^2$:

$$  
L_{el} = \frac{1}{2}kh^2 - \frac{1}{2}k(\ell^2 - h^2)  
$$

Dalla slide:

$$  
L_{el} = -\frac{1}{2}m(2gh + v_0^2 - v^2)  
$$

Risultato:

$$  
L_{el} = -500 \ J  
$$

Il segno negativo indica che la forza elastica compie lavoro contrario al moto del corpo.

---

## Esercizio - Corpo spinto da una molla su piano inclinato

### Traccia

Un corpo di massa:

$$  
m = 8.52 \ kg  
$$

si trova alla base di un piano inclinato privo di attrito, appoggiato a una molla di costante elastica:

$$  
k = 21.5 \ N/cm  
$$

La molla è compressa di:

$$  
x = 24.2 \ cm  
$$

Determinare:

1. il modulo $v$ della velocità del corpo appena si stacca dalla molla;
    
2. l'altezza massima a cui arriva il corpo.
    

---

### Dati in unità SI

$$  
k = 21.5 \ N/cm = 2150 \ N/m  
$$

$$  
x = 24.2 \ cm = 0.242 \ m  
$$

---

### 1) Velocità appena il corpo lascia la molla

Quando il corpo lascia la molla, tutta l'energia potenziale elastica è diventata energia cinetica.

Quindi:

$$  
\frac{1}{2}kx^2 = \frac{1}{2}mv^2  
$$

Semplificando:

$$  
v = x\sqrt{\frac{k}{m}}  
$$

Sostituendo:

$$  
v = 0.242 \sqrt{\frac{2150}{8.52}}  
$$

$$  
v = 3.84 \ m/s  
$$

Risultato:

$$  
v = 3.84 \ m/s  
$$

---

### 2) Altezza massima raggiunta

Dopo aver lasciato la molla, il corpo sale lungo il piano inclinato.

L'energia cinetica diventa energia potenziale gravitazionale:

$$  
\frac{1}{2}mv^2 = mgh  
$$

Ma siccome l'energia cinetica deriva dall'energia elastica, possiamo scrivere direttamente:

$$  
\frac{1}{2}kx^2 = mgh  
$$

Isolando $h$:

$$  
h = \frac{kx^2}{2mg}  
$$

Sostituendo:

$$  
h = \frac{2150 \cdot (0.242)^2}{2 \cdot 8.52 \cdot 9.8}  
$$

$$  
h = 0.753 \ m  
$$

Risultato:

$$  
h = 75.3 \ cm  
$$

---

## Esercizio - Palla lanciata verso il basso con attrito

### Traccia

Una palla di massa:

$$  
m = 625 \ g  
$$

viene lanciata verso il basso con velocità iniziale:

$$  
v_0 = 2.5 \ m/s  
$$

Durante la discesa subisce una forza di attrito costante di modulo:

$$  
F_a = 2.00 \ N  
$$

Quando arriva a terra, la sua velocità ha modulo:

$$  
v_1 = 12.0 \ m/s  
$$

Determinare:

1. da che altezza è stata lanciata la palla;
    
2. nelle stesse condizioni, quale deve essere il modulo della velocità di lancio affinché arrivi a terra con velocità $v_2 = 14.0 \ m/s$.
    

---

### Dati in unità SI

$$  
m = 625 \ g = 0.625 \ kg  
$$

$$  
v_0 = 2.5 \ m/s  
$$

$$  
v_1 = 12.0 \ m/s  
$$

$$  
F_a = 2.00 \ N  
$$

---

### Idea fisica

In presenza di attrito, l'energia meccanica non si conserva.

La forza peso aumenta l'energia cinetica durante la caduta, mentre l'attrito compie lavoro negativo.

Il lavoro dell'attrito è:

$$  
L_a = -F_a h  
$$

Quindi:

$$  
E_f = E_i + L_a  
$$

oppure:

$$  
\frac{1}{2}mv_1^2 = \frac{1}{2}mv_0^2 + mgh - F_a h  
$$

---

### 1) Altezza di lancio

Partiamo da:

$$  
\frac{1}{2}mv_1^2 = \frac{1}{2}mv_0^2 + mgh - F_a h  
$$

Portando i termini:

$$  
\frac{1}{2}m(v_1^2 - v_0^2) = (mg - F_a)h  
$$

Isoliamo $h$:

$$  
h = \frac{\frac{1}{2}m(v_1^2 - v_0^2)}{mg - F_a}  
$$

Sostituendo:

$$  
h = \frac{\frac{1}{2} \cdot 0.625 \cdot (12^2 - 2.5^2)}{0.625 \cdot 9.8 - 2.00}  
$$

$$  
h \approx 10.4 \ m  
$$

Risultato:

$$  
h = 10.4 \ m  
$$

---

### 2) Velocità iniziale per arrivare a terra con $v_2 = 14.0 \ m/s$

Usiamo la stessa altezza $h$ e lo stesso attrito.

La relazione diventa:

$$  
\frac{1}{2}mv_2^2 = \frac{1}{2}mv^2 + mgh - F_a h  
$$

Isolando $v$:

$$  
v^2 = v_2^2 - \frac{2(mg - F_a)h}{m}  
$$

Poiché dal punto precedente:

$$  
\frac{2(mg - F_a)h}{m} = v_1^2 - v_0^2  
$$

allora:

$$  
v^2 = v_2^2 - (v_1^2 - v_0^2)  
$$

Sostituendo:

$$  
v^2 = 14^2 - (12^2 - 2.5^2)  
$$

$$  
v^2 = 58.25  
$$

$$  
v = 7.63 \ m/s  
$$

Risultato:

$$  
v = 7.6 \ m/s  
$$

Quindi la palla deve essere lanciata verso il basso con velocità iniziale circa:

$$  
v = 7.6 \ m/s  
$$

## Esercizio - Palla lanciata verso il basso con attrito

### Traccia

Una palla di massa:

$$  
m = 625 \ g  
$$

viene lanciata verso il basso con velocità iniziale:

$$  
v_0 = 2.5 \ m/s  
$$

Durante la discesa subisce una forza di attrito costante di modulo:

$$  
F_a = 2.00 \ N  
$$

Quando arriva a terra, la sua velocità ha modulo:

$$  
v_1 = 12.0 \ m/s  
$$

Determinare:

1. da che altezza è stata lanciata la palla;
    
2. nelle stesse condizioni, quale deve essere il modulo della velocità di lancio perché arrivi a terra con velocità:
    

$$  
v_2 = 14.0 \ m/s  
$$

---

### Dati

$$  
m = 0.625 \ kg  
$$

$$  
v_0 = 2.5 \ m/s  
$$

$$  
v_1 = 12.0 \ m/s  
$$

$$  
F_a = 2.00 \ N  
$$

---

### Idea fisica

In presenza di attrito, l'energia meccanica **non si conserva**.

Durante la caduta:

- la forza peso aumenta l'energia cinetica;
    
- l'attrito sottrae energia meccanica;
    
- il lavoro dell'attrito è negativo.
    

Il lavoro dell'attrito vale:

$$  
L_a = -F_a h  
$$

Quindi l'energia finale è uguale all'energia iniziale più il lavoro dell'attrito:

$$  
E_f = E_i + L_a  
$$

cioè:

$$  
\frac{1}{2}mv_1^2 = \frac{1}{2}mv_0^2 + mgh - F_a h  
$$

---

### 1) Altezza di lancio

Partiamo da:

$$  
\frac{1}{2}mv_1^2 = \frac{1}{2}mv_0^2 + mgh - F_a h  
$$

Portiamo insieme i termini con $h$:

$$  
\frac{1}{2}m(v_1^2 - v_0^2) = (mg - F_a)h  
$$

Quindi:

$$  
h = \frac{m(v_1^2 - v_0^2)}{2(mg - F_a)}  
$$

Sostituendo i dati:

$$  
h = \frac{0.625(12^2 - 2.5^2)}{2(0.625 \cdot 9.8 - 2.00)}  
$$

$$  
h \approx 10 \ m  
$$

Risultato:

$$  
h = 10 \ m  
$$

---

### 2) Velocità iniziale per arrivare a terra con $v_2 = 14.0 \ m/s$

Usiamo la stessa relazione, ma con velocità finale $v_2$:

$$  
\frac{1}{2}mv_2^2 = \frac{1}{2}mv^2 + mgh - F_a h  
$$

Isolando $v$:

$$  
v = \sqrt{v_2^2 - 2gh + \frac{2F_a h}{m}}  
$$

Utilizzando la relazione precedente, si può anche scrivere:

$$  
v = \sqrt{v_2^2 + v_0^2 - v_1^2}  
$$

Sostituendo:

$$  
v = \sqrt{14^2 + 2.5^2 - 12^2}  
$$

$$  
v = 7.6 \ m/s  
$$

Risultato:

$$  
v = 7.6 \ m/s  
$$

---

## Esercizio - Vaso che cade davanti a una finestra

### Traccia

Una persona guarda dalla finestra e vede cadere verticalmente un vaso da fiori di massa:

$$  
m = 1.9 \ kg  
$$

Quando il vaso entra nella visuale all'estremità superiore della finestra, ha velocità:

$$  
v_1 = 2.4 \ m/s  
$$

Quando arriva in basso, ha velocità:

$$  
v_2 = 5.2 \ m/s  
$$

Sapendo che la finestra è alta:

$$  
h = 1.3 \ m  
$$

determinare il modulo della forza di attrito, supposta costante.

---

### Idea fisica

Anche qui è presente una forza di attrito, quindi l'energia meccanica non si conserva.

L'energia meccanica in basso è uguale all'energia meccanica in alto meno l'energia persa per attrito.

Il lavoro dell'attrito è:

$$  
L_a = -F_a h  
$$

Scriviamo il bilancio energetico:

$$  
\frac{1}{2}mv_1^2 + mgh_1 - F_a h =  
\frac{1}{2}mv_2^2 + mgh_2  
$$

Poiché:

$$  
h = h_1 - h_2  
$$

si ottiene:

$$  
F_a = mg - \frac{m}{2h}(v_2^2 - v_1^2)  
$$

---

### Calcolo

Sostituendo:

$$  
F_a = 1.9 \cdot 9.8 - \frac{1.9}{2 \cdot 1.3}(5.2^2 - 2.4^2)  
$$

$$  
F_a \approx 3.1 \ N  
$$

Risultato:

$$  
F_a = 3.1 \ N  
$$

---

## Quesiti finali

### Q.1 Cosa afferma il teorema di conservazione dell'energia meccanica?

In un sistema in cui agiscono soltanto forze conservative, l'energia meccanica di un punto materiale si conserva.

L'energia meccanica è la somma di energia cinetica ed energia potenziale:

$$  
E_m = K + U  
$$

Se agiscono solo forze conservative:

$$  
E_{m,i} = E_{m,f}  
$$

cioè:

$$  
K_i + U_i = K_f + U_f  
$$

---

### Q.2 In un sistema in cui agiscono forze conservative e non conservative, l'energia meccanica si conserva?

No, in generale l'energia meccanica non si conserva.

Se agiscono anche forze non conservative, come l'attrito, la variazione dell'energia meccanica è uguale al lavoro svolto dalle forze non conservative:

$$  
L_{nc} = \Delta E_m  
$$

cioè:

$$  
L_{nc} = E_{m,f} - E_{m,i}  
$$

Se la forza non conservativa è l'attrito, solitamente:

$$  
L_{nc} < 0  
$$

quindi l'energia meccanica diminuisce.

L'energia però non sparisce: viene trasformata in altre forme, ad esempio energia termica.
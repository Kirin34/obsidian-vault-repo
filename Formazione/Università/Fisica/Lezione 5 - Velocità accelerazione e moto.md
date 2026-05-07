
# Cinematica del punto materiale

## 1. Che cos'è la cinematica

La **cinematica** è la parte della fisica che descrive il movimento dei corpi senza studiare le cause del movimento.

La cinematica non si chiede:

> Perché il corpo si muove?

ma si chiede:

> Dove si trova?
> Come cambia posizione?
> Quanto velocemente si muove?

Le cause del movimento, cioè le forze, vengono studiate nella **dinamica**.

---

## 2. Punto materiale

Il sistema più semplice studiato in cinematica è il **punto materiale**.

Un corpo può essere trattato come punto materiale quando le sue dimensioni sono trascurabili rispetto al problema che si sta studiando.

### Esempio

Un aereo ha dimensioni di alcuni metri, ma se studiamo il suo viaggio lungo centinaia di chilometri, possiamo considerarlo come un punto materiale.

Se invece dobbiamo studiare le sue manovre vicino al gate, non possiamo trascurare le sue dimensioni, perché il suo ingombro diventa importante.

> Un corpo è un punto materiale solo se le sue dimensioni non sono importanti per il problema considerato.

---

## 3. Vettore posizione

La posizione di un punto materiale si descrive con il **vettore posizione**:

$$
\vec{r}
$$

Il vettore posizione parte da un punto di riferimento, di solito l'origine del sistema cartesiano, e arriva fino al punto in cui si trova il corpo.

In uno spazio tridimensionale si può scrivere:

$$
\vec{r}=x\vec{i}+y\vec{j}+z\vec{k}
$$

oppure:

$$
\vec{r}=(x,y,z)
$$

Quindi il vettore posizione dice dove si trova il corpo rispetto all'origine.

---
## 4. Traiettoria

Quando un corpo si muove, occupa posizioni diverse nel tempo.

L'insieme di tutti i punti occupati dal corpo forma la **traiettoria**.
### Esempi

- Se cammini in linea retta, la traiettoria è una retta.
- Se lanci una palla, la traiettoria può essere una parabola.
- Se un'auto percorre una curva, la traiettoria è curva.

> La traiettoria è il percorso seguito dal corpo durante il moto.

---
## 5. Ascissa curvilinea

Sulla traiettoria si può definire una coordinata chiamata **ascissa curvilinea**, indicata spesso con:

$$
s
$$

Questa grandezza misura la distanza percorsa lungo la curva della traiettoria, a partire da un punto scelto come origine.

### Differenza tra vettore posizione e ascissa curvilinea

| Grandezza | Significato |
|---|---|
| $\vec{r}$ | Indica dove si trova il corpo nello spazio rispetto all'origine |
| $s$ | Indica quanto percorso è stato fatto lungo la traiettoria |

### Esempio

Se percorri una strada curva:

- il vettore posizione collega l'origine al punto in cui ti trovi;
- l'ascissa curvilinea misura quanta strada hai percorso lungo la curva.

---

## 6. Spostamento

Supponiamo che un corpo passi da una posizione iniziale:

$$
\vec{r}_1
$$

a una posizione finale:

$$
\vec{r}_2
$$

Lo **spostamento** è:

$$
\Delta \vec{r}=\vec{r}_2-\vec{r}_1
$$

Lo spostamento è un vettore.

Indica il cambiamento di posizione tra il punto iniziale e il punto finale.

### Attenzione

Lo spostamento non coincide sempre con lo spazio percorso.

Esempio:

Se fai un giro e torni al punto di partenza:

- lo spazio percorso può essere grande;
- lo spostamento è zero, perché posizione iniziale e finale coincidono.

---

## 7. Velocità media

La **velocità media** è definita come rapporto tra lo spostamento e l'intervallo di tempo impiegato:

$$
\vec{v}_m=\frac{\Delta \vec{r}}{\Delta t}
$$

dove:

$$
\Delta \vec{r}=\vec{r}_2-\vec{r}_1
$$

e:

$$
\Delta t=t_2-t_1
$$

Quindi:

$$
\vec{v}_m=\frac{\vec{r}_2-\vec{r}_1}{t_2-t_1}
$$

La velocità media è una **grandezza vettoriale**, perché deriva dallo spostamento, che è un vettore.

| Elemento | Significato |
|---|---|
| Modulo | Rapidità media dello spostamento |
| Direzione | Direzione della corda che unisce posizione iniziale e finale |
| Verso | Verso dello spostamento $\Delta \vec{r}$ |

L'unità di misura della velocità è:

$$
m/s
$$

Le sue dimensioni fisiche sono:

$$
[v]=[LT^{-1}]
$$

cioè lunghezza divisa per tempo.

---

## 8. Velocità come grandezza vettoriale

La velocità è una **grandezza vettoriale**.

Questo significa che non basta dire:

> Il corpo va a 10 m/s

Bisogna anche sapere in quale direzione e in quale verso si muove.

### Esempio

- 10 m/s verso nord
- 10 m/s verso sud

Queste due velocità hanno lo stesso modulo, ma sono diverse perché hanno verso opposto.

---

## 9. Velocità istantanea

La **velocità istantanea** è la velocità in un preciso istante.

Si ottiene facendo diventare l'intervallo di tempo sempre più piccolo.

La formula è:

$$
\vec{v}=\lim_{\Delta t\to0}\frac{\Delta \vec{r}}{\Delta t}
$$

In parole semplici:

> La velocità istantanea è il valore a cui tende la velocità media quando considero intervalli di tempo sempre più piccoli.

Matematicamente, la velocità istantanea è la derivata del vettore posizione rispetto al tempo:

$$
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}
$$

Quindi, se conosco la posizione in funzione del tempo, posso trovare la velocità derivando.

---

## 10. Significato geometrico della velocità istantanea

La velocità media ha direzione lungo la corda che unisce due punti della traiettoria.

Quando i due punti si avvicinano sempre di più, la corda diventa sempre più simile alla tangente alla traiettoria.

Quindi:

> La velocità istantanea è tangente alla traiettoria nel punto considerato.

Se un corpo si muove lungo una curva, in ogni istante la sua velocità punta nella direzione tangente alla curva in quel punto.

---

## 11. Differenza tra velocità media e velocità istantanea

| Tipo di velocità | Formula | Significato |
|---|---|---|
| Velocità media | $\vec{v}_m=\frac{\Delta \vec{r}}{\Delta t}$ | Velocità calcolata su un intervallo di tempo |
| Velocità istantanea | $\vec{v}=\lim_{\Delta t\to0}\frac{\Delta \vec{r}}{\Delta t}$ | Velocità in un preciso istante |
| Derivata della posizione | $\vec{v}(t)=\frac{d\vec{r}(t)}{dt}$ | Forma matematica della velocità istantanea |

### Esempio

Se Napoli-Salerno la fai in 1 ora e sono 60 km, la velocità media è:

$$
60\ km/h
$$

Durante il viaggio, però, potresti:

- andare a 30 km/h;
- poi a 100 km/h;
- poi fermarti.

Quelle sono velocità istantanee.

---

## 12. Esempio della strada in salita e discesa

Un'auto percorre un tratto di strada in salita alla velocità:

$$
v_1
$$

e lo stesso tratto in discesa alla velocità:

$$
v_2
$$

Bisogna trovare la velocità media complessiva.

Le possibili formule sono:

$$
\frac{v_1+v_2}{2}
$$

$$
\frac{v_1v_2}{v_1+v_2}
$$

$$
\frac{2v_1v_2}{v_1+v_2}
$$

La formula corretta è:

$$
\boxed{\frac{2v_1v_2}{v_1+v_2}}
$$

---

## 13. Perché non si usa la media aritmetica?

Non si usa semplicemente:

$$
\frac{v_1+v_2}{2}
$$

perché l'auto percorre **lo stesso spazio**, non lo stesso tempo.

Supponiamo che il tratto in salita sia lungo:

$$
s
$$

e anche quello in discesa sia lungo:

$$
s
$$

Lo spazio totale è:

$$
2s
$$

Il tempo in salita è:

$$
t_1=\frac{s}{v_1}
$$

Il tempo in discesa è:

$$
t_2=\frac{s}{v_2}
$$

Il tempo totale è:

$$
t=t_1+t_2
$$

quindi:

$$
t=\frac{s}{v_1}+\frac{s}{v_2}
$$

Mettiamo in evidenza $s$:

$$
t=s\left(\frac{1}{v_1}+\frac{1}{v_2}\right)
$$

Sommiamo le frazioni:

$$
t=s\left(\frac{v_1+v_2}{v_1v_2}\right)
$$

La velocità media totale è spazio totale diviso tempo totale:

$$
v_m=\frac{2s}{t}
$$

Sostituiamo $t$:

$$
v_m=\frac{2s}{s\left(\frac{v_1+v_2}{v_1v_2}\right)}
$$

Semplifichiamo $s$:

$$
v_m=\frac{2}{\frac{v_1+v_2}{v_1v_2}}
$$

Quindi:

$$
v_m=\frac{2v_1v_2}{v_1+v_2}
$$

Questa formula è la **media armonica** delle due velocità.

---

# Formule importanti

| Concetto | Formula |
|---|---|
| Vettore posizione | $\vec{r}=(x,y,z)$ |
| Spostamento | $\Delta \vec{r}=\vec{r}_2-\vec{r}_1$ |
| Intervallo di tempo | $\Delta t=t_2-t_1$ |
| Velocità media | $\vec{v}_m=\frac{\Delta \vec{r}}{\Delta t}$ |
| Velocità istantanea | $\vec{v}=\lim_{\Delta t\to0}\frac{\Delta \vec{r}}{\Delta t}$ |
| Velocità come derivata | $\vec{v}(t)=\frac{d\vec{r}(t)}{dt}$ |
| Velocità media su due tratti uguali | $v_m=\frac{2v_1v_2}{v_1+v_2}$ |

---

# Riassunto finale

La **cinematica** studia il moto senza occuparsi delle cause.

Un corpo può essere considerato **punto materiale** quando le sue dimensioni sono trascurabili rispetto al problema.

La posizione di un corpo si descrive con il **vettore posizione**:

$$
\vec{r}
$$

L'insieme delle posizioni occupate durante il moto forma la **traiettoria**.

Lo **spostamento** è:

$$
\Delta \vec{r}=\vec{r}_2-\vec{r}_1
$$

La **velocità media** è:

$$
\vec{v}_m=\frac{\Delta \vec{r}}{\Delta t}
$$

La **velocità istantanea** è:

$$
\vec{v}=\lim_{\Delta t\to0}\frac{\Delta \vec{r}}{\Delta t}
$$

oppure:

$$
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}
$$

La velocità istantanea è sempre **tangente alla traiettoria** nel punto considerato.

Quando si percorrono due tratti uguali con velocità diverse, la velocità media complessiva è:

$$
v_m=\frac{2v_1v_2}{v_1+v_2}
$$

## 1. Accelerazione media  
  
L'**accelerazione media** descrive quanto cambia la velocità in un certo intervallo di tempo.  
  
La formula è:  
  
$$  
\vec{a}_m=\frac{\Delta \vec{v}}{\Delta t}  
$$  
  
dove:  
  
$$  
\Delta \vec{v}=\vec{v}_2-\vec{v}_1  
$$  
  
e:  
  
$$  
\Delta t=t_2-t_1  
$$  
  
Quindi:  
  
$$  
\vec{a}_m=\frac{\vec{v}_2-\vec{v}_1}{t_2-t_1}  
$$  
  
In parole semplici:  
  
> L'accelerazione media misura quanto varia la velocità nel tempo.  
  
---  
  
## 2. L'accelerazione è una grandezza vettoriale  
  
L'accelerazione è una **grandezza vettoriale**, perché deriva dalla variazione della velocità, che è un vettore.  
  
Quindi ha:  
  
| Elemento | Significato |  
|---|---|  
| Modulo | Quanto rapidamente cambia la velocità |  
| Direzione | Direzione della variazione di velocità $\Delta \vec{v}$ |  
| Verso | Verso della variazione di velocità $\Delta \vec{v}$ |  
  
L'unità di misura dell'accelerazione è:  
  
$$  
m/s^2  
$$  
  
Le dimensioni fisiche sono:  
  
$$  
[a]=[LT^{-2}]  
$$  
  
cioè lunghezza divisa per tempo al quadrato.  
  
---  
  
## 3. Accelerazione istantanea  
  
L'**accelerazione istantanea** è l'accelerazione in un preciso istante.  
  
Si ottiene facendo tendere l'intervallo di tempo a zero:  
  
$$  
\vec{a}=\lim_{\Delta t\to0}\frac{\Delta \vec{v}}{\Delta t}  
$$  
  
Quindi è il valore limite a cui tende l'accelerazione media quando considero intervalli di tempo sempre più piccoli.  
  
Matematicamente è la derivata della velocità rispetto al tempo:  
  
$$  
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}  
$$  
  
---  
  
## 4. Collegamento tra posizione, velocità e accelerazione  
  
Dalle slide precedenti sappiamo che la velocità è la derivata della posizione:  
  
$$  
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}  
$$  
  
L'accelerazione è la derivata della velocità:  
  
$$  
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}  
$$  
  
Quindi l'accelerazione è anche la derivata seconda della posizione:  
  
$$  
\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}  
$$  
  
Schema da ricordare:  
  
$$  
\vec{r}(t) \xrightarrow{\text{derivata}} \vec{v}(t) \xrightarrow{\text{derivata}} \vec{a}(t)  
$$  
  
Cioè:  
  
- posizione → derivando ottieni velocità;  
- velocità → derivando ottieni accelerazione.  
  
---  
  
## 5. L'accelerazione non è sempre nel senso del moto  
  
Una cosa importante delle slide è questa:  
  
> L'accelerazione non è necessariamente diretta nel senso del moto.  
  
Questo perché l'accelerazione non indica semplicemente dove sta andando il corpo.  
  
L'accelerazione indica **come cambia la velocità**.  
  
La velocità può cambiare in due modi:  
  
1. può cambiare il suo **modulo**, cioè il corpo va più veloce o più lento;  
2. può cambiare la sua **direzione**, cioè il corpo curva.  
  
Quindi un corpo può avere accelerazione anche se mantiene sempre la stessa velocità in modulo, ma cambia direzione.  
  
### Esempio  
  
Un'auto che percorre una curva a velocità costante ha comunque accelerazione, perché la direzione della velocità cambia continuamente.  
  
---  
  
## 6. Componenti dell'accelerazione  
  
L'accelerazione può essere scomposta in due componenti:  
  
1. **componente tangenziale**  
2. **componente normale**  
  
---  
  
## 7. Componente tangenziale  
  
La componente tangenziale si indica con:  
  
$$  
a_t  
$$  
  
È diretta lungo la tangente alla traiettoria.  
  
Serve a descrivere la variazione del **modulo** della velocità.  
  
Quindi:  
  
> La componente tangenziale dice se il corpo sta accelerando o rallentando lungo la traiettoria.  
  
| Caso | Significato |  
|---|---|  
| $a_t>0$ | Il corpo aumenta la velocità |  
| $a_t<0$ | Il corpo rallenta |  
| $a_t=0$ | Il modulo della velocità resta costante |  
  
---  
  
## 8. Componente normale  
  
La componente normale si indica con:  
  
$$  
a_n  
$$  
  
È diretta perpendicolarmente alla traiettoria, verso il centro della curvatura.  
  
Serve a descrivere la variazione della **direzione** della velocità.  
  
Quindi:  
  
> La componente normale compare quando il corpo cambia direzione, cioè quando la traiettoria è curva.  
  
| Caso | Significato |  
|---|---|  
| Moto rettilineo | La componente normale è nulla |  
| Moto curvilineo | La componente normale è presente |  
  
---  
  
## 9. Riassunto intuitivo  
  
L'accelerazione totale può essere vista come somma di due effetti:  
  
| Componente | Cosa cambia | Significato |  
|---|---|---|  
| $a_t$ | Modulo della velocità | Il corpo accelera o rallenta |  
| $a_n$ | Direzione della velocità | Il corpo curva |  
  
Quindi:  
  
- se cambia solo la velocità in valore, c'è accelerazione tangenziale;  
- se cambia solo la direzione, c'è accelerazione normale;  
- se cambiano entrambe, ci sono entrambe le componenti.  
  
---  
  
# Formule importanti  
  
| Concetto | Formula |  
|---|---|  
| Accelerazione media | $\vec{a}_m=\frac{\Delta \vec{v}}{\Delta t}$ |  
| Variazione di velocità | $\Delta \vec{v}=\vec{v}_2-\vec{v}_1$ |  
| Intervallo di tempo | $\Delta t=t_2-t_1$ |  
| Accelerazione istantanea | $\vec{a}=\lim_{\Delta t\to0}\frac{\Delta \vec{v}}{\Delta t}$ |  
| Accelerazione come derivata della velocità | $\vec{a}(t)=\frac{d\vec{v}(t)}{dt}$ |  
| Accelerazione come derivata seconda della posizione | $\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}$ |  
  
---  
  
# Collegamento con la cinematica  
  
Nella cinematica abbiamo questa catena logica:  
  
$$  
\vec{r}(t) \rightarrow \vec{v}(t) \rightarrow \vec{a}(t)  
$$  
  
Cioè:  
  
| Grandezza | Significato | Si ottiene |  
|---|---|---|  
| $\vec{r}(t)$ | Posizione | Grandezza di partenza |  
| $\vec{v}(t)$ | Velocità | Derivando la posizione |  
| $\vec{a}(t)$ | Accelerazione | Derivando la velocità |  
  
In forma matematica:  
  
$$  
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}  
$$  
  
$$  
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}  
$$  
  
$$  
\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}  
$$  
  
---  
  
# Riassunto finale  
  
L'**accelerazione** misura la variazione della velocità nel tempo.  
  
L'accelerazione media è:  
  
$$  
\vec{a}_m=\frac{\Delta \vec{v}}{\Delta t}  
$$  
  
L'accelerazione istantanea è:  
  
$$  
\vec{a}=\lim_{\Delta t\to0}\frac{\Delta \vec{v}}{\Delta t}  
$$  
  
oppure:  
  
$$  
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}  
$$  
  
Poiché la velocità è la derivata della posizione:  
  
$$  
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}  
$$  
  
allora l'accelerazione è la derivata seconda della posizione:  
  
$$  
\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}  
$$  
  
L'accelerazione non indica per forza il senso del moto: indica come cambia la velocità.  
  
Può essere scomposta in:  
  
- **accelerazione tangenziale** $a_t$, che cambia il modulo della velocità;  
- **accelerazione normale** $a_n$, che cambia la direzione della velocità.

# Derivata di un vettore

## 1. Introduzione

Nelle slide precedenti abbiamo visto che, in cinematica, il passaggio da posizione a velocità e da velocità ad accelerazione avviene tramite la **derivata rispetto al tempo**.

La posizione è un vettore:

$$
\vec{r}(t)
$$

La velocità è la derivata della posizione:

$$
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}
$$

L'accelerazione è la derivata della velocità:

$$
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}
$$

oppure la derivata seconda della posizione:

$$
\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}
$$

Quindi:

> La derivata di un vettore è ancora un vettore.

---

## 2. Derivata di un vettore

Se un vettore dipende da un parametro scalare, ad esempio il tempo $t$, possiamo derivarlo rispetto a quel parametro.

La derivata di un vettore indica **come cambia quel vettore nel tempo**.

Per esempio:

$$
\vec{r}(t)
$$

è il vettore posizione.

La sua derivata è:

$$
\frac{d\vec{r}(t)}{dt}
$$

che rappresenta la velocità.

### Attenzione

La derivata di un vettore non è, in generale, parallela al vettore di partenza.

Questo perché un vettore può cambiare in due modi:

- può cambiare il suo **modulo**;
- può cambiare la sua **direzione**;
- può cambiare il suo **verso**.

---

# Regole di derivazione vettoriale

## 3. Derivata della somma di vettori

La derivata della somma è uguale alla somma delle derivate:

$$
\frac{d}{dt}(\vec{a}+\vec{b})=
\frac{d\vec{a}}{dt}+\frac{d\vec{b}}{dt}
$$

Quindi, se due vettori dipendono dal tempo, posso derivarli separatamente e poi sommare i risultati.

---

## 4. Derivata del prodotto tra scalare e vettore

Se $m$ è uno scalare e $\vec{v}$ è un vettore, allora:

$$
\frac{d}{dt}(m\vec{v})=
\frac{dm}{dt}\vec{v}+m\frac{d\vec{v}}{dt}
$$

Questa formula è simile alla derivata del prodotto tra due funzioni.

### Caso particolare

Se lo scalare $m$ è costante, allora:

$$
\frac{dm}{dt}=0
$$

e quindi:

$$
\frac{d}{dt}(m\vec{v})=
m\frac{d\vec{v}}{dt}
$$

---

## 5. Derivata del prodotto scalare

Se abbiamo due vettori $\vec{a}$ e $\vec{b}$, il loro prodotto scalare è:

$$
\vec{a}\cdot\vec{b}
$$

La derivata del prodotto scalare è:

$$
\frac{d}{dt}(\vec{a}\cdot\vec{b})
=
\frac{d\vec{a}}{dt}\cdot\vec{b}
+
\vec{a}\cdot\frac{d\vec{b}}{dt}
$$

Quindi si deriva il primo vettore e si lascia fermo il secondo, poi si lascia fermo il primo e si deriva il secondo.

---

## 6. Derivata del prodotto vettoriale

Se abbiamo il prodotto vettoriale:

$$
\vec{a}\times\vec{b}
$$

la sua derivata è:

$$
\frac{d}{dt}(\vec{a}\times\vec{b})
=
\frac{d\vec{a}}{dt}\times\vec{b}
+
\vec{a}\times\frac{d\vec{b}}{dt}
$$

Anche qui si usa una regola simile alla derivata del prodotto.

### Attenzione importante

Nel prodotto vettoriale l'ordine conta.

Infatti:

$$
\vec{a}\times\vec{b}\neq\vec{b}\times\vec{a}
$$

Quindi nella derivata bisogna mantenere lo stesso ordine dei vettori.

---

## 7. Derivata di un vettore costante

Se un vettore è costante rispetto al tempo, cioè non cambia:

- modulo;
- direzione;
- verso;

allora la sua derivata è il vettore nullo:

$$
\frac{d\vec{a}}{dt}=\vec{0}
$$

Questo vale perché il vettore non subisce alcuna variazione.

---

# Componenti della derivata di un vettore

## 8. Vettore scritto tramite componenti

Un vettore può essere scritto come:

$$
\vec{v}=v_x\vec{i}+v_y\vec{j}+v_z\vec{k}
$$

dove:

- $v_x$ è la componente lungo l'asse $x$;
- $v_y$ è la componente lungo l'asse $y$;
- $v_z$ è la componente lungo l'asse $z$;
- $\vec{i}$, $\vec{j}$, $\vec{k}$ sono i versori degli assi cartesiani.

---

## 9. Derivata tramite componenti

Per derivare un vettore scritto tramite componenti, si derivano le singole componenti:

$$
\frac{d\vec{v}}{dt}
=
\frac{dv_x}{dt}\vec{i}
+
\frac{dv_y}{dt}\vec{j}
+
\frac{dv_z}{dt}\vec{k}
$$

Questo perché i versori cartesiani $\vec{i}$, $\vec{j}$ e $\vec{k}$ sono costanti.

Quindi:

$$
\frac{d\vec{i}}{dt}=0
$$

$$
\frac{d\vec{j}}{dt}=0
$$

$$
\frac{d\vec{k}}{dt}=0
$$

In parole semplici:

> La derivata di un vettore si ottiene derivando le sue componenti.

---

## 10. Esempio semplice

Se:

$$
\vec{v}(t)=t^2\vec{i}+3t\vec{j}+5\vec{k}
$$

allora:

$$
\frac{d\vec{v}}{dt}
=
\frac{d}{dt}(t^2)\vec{i}
+
\frac{d}{dt}(3t)\vec{j}
+
\frac{d}{dt}(5)\vec{k}
$$

quindi:

$$
\frac{d\vec{v}}{dt}
=
2t\vec{i}+3\vec{j}+0\vec{k}
$$

Risultato:

$$
\frac{d\vec{v}}{dt}=2t\vec{i}+3\vec{j}
$$

---

# Derivata di un versore

## 11. Cos'è un versore

Un **versore** è un vettore di modulo unitario:

$$
|\vec{u}|=1
$$

Quindi il suo modulo è costante.

La cosa che può cambiare è la sua **direzione**.

---

## 12. Derivata di un versore variabile

Se un versore cambia direzione nel tempo, allora può avere una derivata diversa da zero.

Poiché il modulo del versore resta sempre uguale a $1$, la variazione non riguarda la lunghezza, ma solo la direzione.

La derivata di un versore è perpendicolare al versore stesso.

Quindi:

> La derivata di un versore non è parallela al versore, ma ortogonale ad esso.

---

## 13. Formula della derivata di un versore

Se il versore cambia direzione ruotando di un angolo $\theta$, la sua derivata può essere scritta come:

$$
\frac{d\vec{u}}{dt}
=
\frac{d\theta}{dt}\vec{u}_N
$$

dove:

- $\vec{u}$ è il versore;
- $\theta$ è l'angolo di rotazione;
- $\frac{d\theta}{dt}$ indica quanto rapidamente cambia l'angolo;
- $\vec{u}_N$ è un versore normale, cioè perpendicolare a $\vec{u}$.

Quindi la derivata del versore punta nella direzione normale al versore stesso.

---

# Schema calcolo derivate

## 14. Derivata della somma di funzioni

Se abbiamo due funzioni $f(x)$ e $g(x)$:

$$
\frac{d}{dx}[f(x)+g(x)]
=
\frac{df}{dx}(x)+\frac{dg}{dx}(x)
$$

La derivata della somma è la somma delle derivate.

---

## 15. Derivata di una costante per una funzione

Se $\alpha$ è costante:

$$
\frac{d}{dx}[\alpha f(x)]
=
\alpha\frac{df}{dx}(x)
$$

La costante resta fuori dalla derivata.

---

## 16. Derivata del prodotto di due funzioni

Se abbiamo il prodotto:

$$
f(x)g(x)
$$

allora:

$$
\frac{d}{dx}[f(x)g(x)]
=
g(x)\frac{df}{dx}(x)+f(x)\frac{dg}{dx}(x)
$$

Si deriva una funzione alla volta.

---

## 17. Derivata di funzione composta

Se abbiamo una funzione composta:

$$
f(g(x))
$$

allora:

$$
\frac{d}{dx}[f(g(x))]
=
\frac{df}{dg}(g(x))\frac{dg}{dx}(x)
$$

Questa è la **regola della catena**.

---

# Derivate fondamentali

| Funzione | Derivata |
|---|---|
| $y=a$ | $y'=0$ |
| $y=x^\alpha$ | $y'=\alpha x^{\alpha-1}$ |
| $y=\sin x$ | $y'=\cos x$ |
| $y=\cos x$ | $y'=-\sin x$ |
| $y=\tan x$ | $y'=\frac{1}{\cos^2 x}$ |
| $y=\log x$ | $y'=\frac{1}{x}$ |
| $y=e^x$ | $y'=e^x$ |

---

# Collegamento tra posizione, velocità e accelerazione

## 18. Posizione in funzione del tempo

Se conosciamo la posizione in funzione del tempo:

$$
\vec{r}=\vec{r}(t)
$$

possiamo ottenere la velocità e l'accelerazione tramite derivate.

---

## 19. Velocità come derivata della posizione

La velocità è:

$$
\vec{v}=\frac{d\vec{r}}{dt}
$$

Quindi la velocità rappresenta quanto rapidamente cambia la posizione nel tempo.

---

## 20. Accelerazione come derivata della velocità

L'accelerazione è:

$$
\vec{a}=\frac{d\vec{v}}{dt}
$$

Poiché:

$$
\vec{v}=\frac{d\vec{r}}{dt}
$$

allora:

$$
\vec{a}=\frac{d^2\vec{r}}{dt^2}
$$

Quindi l'accelerazione è la derivata seconda della posizione rispetto al tempo.

---

# Interpretazione dei grafici

## 21. Dal grafico posizione-tempo alla velocità

Se abbiamo un grafico di posizione in funzione del tempo:

$$
r(t)
$$

la velocità è la pendenza del grafico.

Quindi:

- se il grafico $r(t)$ cresce velocemente, la velocità è grande;
- se il grafico $r(t)$ cresce lentamente, la velocità è piccola;
- se il grafico $r(t)$ è orizzontale, la velocità è zero.

---

## 22. Dal grafico velocità-tempo all'accelerazione

Se abbiamo un grafico velocità-tempo:

$$
v(t)
$$

l'accelerazione è la pendenza del grafico.

Quindi:

- se $v(t)$ cresce, l'accelerazione è positiva;
- se $v(t)$ diminuisce, l'accelerazione è negativa;
- se $v(t)$ è costante, l'accelerazione è zero.

---

## 23. Riassunto grafico

| Grafico | Derivata | Significato |
|---|---|---|
| $r(t)$ | $v(t)=\frac{dr}{dt}$ | La velocità è la pendenza della posizione |
| $v(t)$ | $a(t)=\frac{dv}{dt}$ | L'accelerazione è la pendenza della velocità |
| $r(t)$ | $a(t)=\frac{d^2r}{dt^2}$ | L'accelerazione è la derivata seconda della posizione |

---

# Formule importanti

| Concetto | Formula |
|---|---|
| Velocità come derivata della posizione | $\vec{v}(t)=\frac{d\vec{r}(t)}{dt}$ |
| Accelerazione come derivata della velocità | $\vec{a}(t)=\frac{d\vec{v}(t)}{dt}$ |
| Accelerazione come derivata seconda della posizione | $\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}$ |
| Derivata della somma | $\frac{d}{dt}(\vec{a}+\vec{b})=\frac{d\vec{a}}{dt}+\frac{d\vec{b}}{dt}$ |
| Derivata prodotto scalare | $\frac{d}{dt}(\vec{a}\cdot\vec{b})=\frac{d\vec{a}}{dt}\cdot\vec{b}+\vec{a}\cdot\frac{d\vec{b}}{dt}$ |
| Derivata prodotto vettoriale | $\frac{d}{dt}(\vec{a}\times\vec{b})=\frac{d\vec{a}}{dt}\times\vec{b}+\vec{a}\times\frac{d\vec{b}}{dt}$ |
| Derivata tramite componenti | $\frac{d\vec{v}}{dt}=\frac{dv_x}{dt}\vec{i}+\frac{dv_y}{dt}\vec{j}+\frac{dv_z}{dt}\vec{k}$ |
| Derivata di un versore | $\frac{d\vec{u}}{dt}=\frac{d\theta}{dt}\vec{u}_N$ |

---

# Riassunto finale

La derivata di un vettore rispetto al tempo è ancora un vettore.

In cinematica, la derivata permette di collegare posizione, velocità e accelerazione:

$$
\vec{r}(t)\rightarrow\vec{v}(t)\rightarrow\vec{a}(t)
$$

cioè:

$$
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}
$$

$$
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}
$$

$$
\vec{a}(t)=\frac{d^2\vec{r}(t)}{dt^2}
$$

Le regole di derivazione dei vettori sono simili a quelle delle funzioni normali, ma bisogna fare attenzione al prodotto vettoriale, perché l'ordine dei vettori è importante.

Se un vettore è scritto tramite componenti cartesiane, si derivano le singole componenti:

$$
\frac{d\vec{v}}{dt}
=
\frac{dv_x}{dt}\vec{i}
+
\frac{dv_y}{dt}\vec{j}
+
\frac{dv_z}{dt}\vec{k}
$$

Se un vettore è costante, la sua derivata è nulla.

Se invece un versore cambia direzione, la sua derivata non è nulla ed è perpendicolare al versore stesso.

La cosa fondamentale da ricordare è:

> Derivare un vettore significa studiare come cambia nel tempo il suo modulo, la sua direzione o il suo verso.
> 
> # Quesiti - Derivate vettoriali, velocità e accelerazione

## Quesito 1

### Testo

Un aereo viaggia verso nord a una velocità di:

$$
v_1=200\ m/s
$$

All'improvviso decide di invertire la rotta e si dirige verso sud sempre con una velocità di:

$$
v_2=200\ m/s
$$

Quanto è il modulo della corrispondente variazione di velocità?

---

### Soluzione

La velocità è una **grandezza vettoriale**, quindi bisogna considerare anche il verso.

Scegliamo il verso nord come positivo:

$$
v_1=+200\ m/s
$$

Poiché il sud è il verso opposto, la velocità finale è:

$$
v_2=-200\ m/s
$$

La variazione di velocità è:

$$
\Delta v=v_2-v_1
$$

Sostituiamo:

$$
\Delta v=(-200)-(+200)
$$

$$
\Delta v=-400\ m/s
$$

La domanda chiede il **modulo** della variazione di velocità, quindi:

$$
|\Delta v|=400\ m/s
$$

Risposta:

$$
\boxed{400\ m/s}
$$

---

## Quesito 2

### Testo

Il moto di un corpo su un piano è specificato dallo spostamento:

$$
\vec{r}=(5.0+1.0t)\vec{i}+7.0\vec{j}
$$

Qual è la sua velocità in direzione verticale?

---

### Soluzione

Il vettore posizione può essere scritto come:

$$
\vec{r}(t)=x(t)\vec{i}+y(t)\vec{j}
$$

Nel nostro caso:

$$
x(t)=5.0+1.0t
$$

$$
y(t)=7.0
$$

La velocità è la derivata della posizione rispetto al tempo:

$$
\vec{v}(t)=\frac{d\vec{r}}{dt}
$$

La velocità verticale è la componente lungo l'asse $y$:

$$
v_y=\frac{dy}{dt}
$$

Poiché:

$$
y(t)=7.0
$$

è costante, allora:

$$
v_y=\frac{d}{dt}(7.0)=0
$$

Risposta:

$$
\boxed{v_y=0\ m/s}
$$

---

## Quesito 3

### Testo

Quanto vale la componente della derivata di un versore parallela al versore stesso?

---

### Soluzione

Un **versore** è un vettore di modulo unitario:

$$
|\vec{u}|=1
$$

Il modulo del versore è costante.

Se il versore cambia nel tempo, può cambiare solo la sua **direzione**, non il suo modulo.

La derivata di un versore è quindi perpendicolare al versore stesso.

La componente parallela al versore è nulla:

$$
\boxed{0}
$$

In altre parole, la componente tangenziale della derivata equivale alla variazione del modulo, ma nel caso di un versore il modulo è costante e unitario.

Quindi:

$$
a_T=0
$$

---

## Quesito 4

### Testo

Il moto di un punto materiale è rappresentato dallo spostamento:

$$
\vec{r}(t)=(4.0t+6.0t^2)\vec{i}+\vec{j}+(2.0+6.5t^2)\vec{k}
$$

Qual è la velocità in funzione del tempo e qual è il modulo dell'accelerazione dopo $2s$?

---

### Soluzione

La velocità è la derivata della posizione rispetto al tempo:

$$
\vec{v}(t)=\frac{d\vec{r}(t)}{dt}
$$

Deriviamo componente per componente.

### Componente lungo $x$

$$
x(t)=4.0t+6.0t^2
$$

$$
v_x(t)=\frac{dx}{dt}=4.0+12.0t
$$

### Componente lungo $y$

Nel vettore posizione abbiamo:

$$
\vec{j}=1\vec{j}
$$

quindi:

$$
y(t)=1
$$

Essendo costante:

$$
v_y(t)=0
$$

### Componente lungo $z$

$$
z(t)=2.0+6.5t^2
$$

$$
v_z(t)=\frac{dz}{dt}=13.0t
$$

Quindi la velocità è:

$$
\vec{v}(t)=(4.0+12.0t)\vec{i}+13.0t\vec{k}
$$

Risposta per la velocità:

$$
\boxed{\vec{v}(t)=(4.0+12.0t)\vec{i}+13.0t\vec{k}}
$$

---

## Calcolo dell'accelerazione

L'accelerazione è la derivata della velocità:

$$
\vec{a}(t)=\frac{d\vec{v}(t)}{dt}
$$

Partiamo da:

$$
\vec{v}(t)=(4.0+12.0t)\vec{i}+13.0t\vec{k}
$$

Deriviamo componente per componente.

### Componente lungo $x$

$$
a_x=\frac{d}{dt}(4.0+12.0t)=12.0
$$

### Componente lungo $y$

$$
a_y=0
$$

### Componente lungo $z$

$$
a_z=\frac{d}{dt}(13.0t)=13.0
$$

Quindi:

$$
\vec{a}=12.0\vec{i}+13.0\vec{k}
$$

L'accelerazione è costante, quindi ha lo stesso valore anche dopo $2s$.

---

## Modulo dell'accelerazione

Il modulo dell'accelerazione si calcola con Pitagora:

$$
|\vec{a}|=\sqrt{a_x^2+a_y^2+a_z^2}
$$

Sostituiamo:

$$
|\vec{a}|=\sqrt{12^2+0^2+13^2}
$$

$$
|\vec{a}|=\sqrt{144+169}
$$

$$
|\vec{a}|=\sqrt{313}
$$

$$
|\vec{a}|\approx17.7\ m/s^2
$$

Risposta:

$$
\boxed{|\vec{a}|=17.7\ m/s^2}
$$

---

# Riassunto dei quesiti

| Quesito | Concetto chiave | Risultato |
|---|---|---|
| Q1 | La velocità è vettoriale, quindi il verso conta | $|\Delta v|=400\ m/s$ |
| Q2 | La velocità verticale è la derivata della componente $y$ | $v_y=0\ m/s$ |
| Q3 | La derivata di un versore è perpendicolare al versore | Componente parallela $=0$ |
| Q4 | Velocità = derivata della posizione; accelerazione = derivata della velocità | $\vec{v}(t)=(4.0+12.0t)\vec{i}+13.0t\vec{k}$; $|\vec{a}|=17.7\ m/s^2$ |

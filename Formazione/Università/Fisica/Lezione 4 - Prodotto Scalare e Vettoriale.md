
# Operazioni con i vettori

## 1. Prodotto di un vettore per uno scalare

Uno **scalare** è semplicemente un numero.

Se abbiamo un vettore:

$$
\vec{v}=(v_x,v_y,v_z)
$$

e lo moltiplichiamo per uno scalare $c$, otteniamo un nuovo vettore:

$$
\vec{w}=c\vec{v}
$$

Le componenti del nuovo vettore sono:

$$
\vec{w}=c\vec{v}=(cv_x,cv_y,cv_z)
$$

Quindi moltiplicare un vettore per uno scalare significa moltiplicare **ogni componente** del vettore per quel numero.

### Esempio

Se:

$$
\vec{v}=(2,3)
$$

e moltiplichiamo per $4$:

$$
4\vec{v}=(8,12)
$$

Il vettore mantiene la stessa direzione e lo stesso verso, ma diventa più lungo.

Se invece moltiplichiamo per un numero negativo:

$$
-2\vec{v}=(-4,-6)
$$

il vettore cambia anche verso.

| Scalare | Effetto sul vettore |
|---|---|
| $c>1$ | Il vettore si allunga |
| $0<c<1$ | Il vettore si accorcia |
| $c<0$ | Il vettore cambia verso |
| $c=0$ | Il vettore diventa nullo |

---

## 2. Versori

Un **versore** è un vettore con modulo uguale a $1$.

Serve a indicare una **direzione**.

Il versore associato a un vettore si ottiene dividendo il vettore per il suo modulo:

$$
\hat{w}=\frac{\vec{w}}{|\vec{w}|}
$$

Se:

$$
\vec{w}=(w_x,w_y,w_z)
$$

allora:

$$
\hat{w}=
\left(
\frac{w_x}{|\vec{w}|},
\frac{w_y}{|\vec{w}|},
\frac{w_z}{|\vec{w}|}
\right)
$$

Il versore ha:

- stessa direzione del vettore originale;
- stesso verso del vettore originale;
- modulo uguale a $1$.

---

## 3. Versori fondamentali

Nel sistema cartesiano tridimensionale si usano tre versori fondamentali:

$$
\vec{i}=(1,0,0)
$$

$$
\vec{j}=(0,1,0)
$$

$$
\vec{k}=(0,0,1)
$$

| Versore | Direzione |
|---|---|
| $\vec{i}$ | Asse $x$ |
| $\vec{j}$ | Asse $y$ |
| $\vec{k}$ | Asse $z$ |

Ogni vettore può essere scritto come combinazione dei versori fondamentali:

$$
\vec{v}=v_x\vec{i}+v_y\vec{j}+v_z\vec{k}
$$

### Esempio

Se:

$$
\vec{v}=(3,4,2)
$$

possiamo scrivere:

$$
\vec{v}=3\vec{i}+4\vec{j}+2\vec{k}
$$

---

# Prodotto scalare

## 4. Definizione di prodotto scalare

Il **prodotto scalare** è un'operazione tra due vettori che dà come risultato uno **scalare**, cioè un numero.

Si indica con il simbolo puntino:

$$
\vec{v}\cdot\vec{w}
$$

La formula geometrica è:

$$
\vec{v}\cdot\vec{w}=|\vec{v}||\vec{w}|\cos\theta
$$

dove $\theta$ è l'angolo compreso tra i due vettori.

Il prodotto scalare misura quanto due vettori sono orientati nella stessa direzione.

---

## 5. Casi importanti del prodotto scalare

### Vettori paralleli e nello stesso verso

Se due vettori sono paralleli e hanno lo stesso verso:

$$
\theta=0^\circ
$$

Poiché:

$$
\cos 0^\circ=1
$$

allora:

$$
\vec{v}\cdot\vec{w}=|\vec{v}||\vec{w}|
$$

Il prodotto scalare è massimo.

---

### Vettori ortogonali

Due vettori sono **ortogonali** se sono perpendicolari.

In questo caso:

$$
\theta=90^\circ
$$

Poiché:

$$
\cos 90^\circ=0
$$

allora:

$$
\vec{v}\cdot\vec{w}=0
$$

Quindi:

> Due vettori sono ortogonali se il loro prodotto scalare vale zero.

---

### Vettori paralleli ma in verso opposto

Se due vettori sono paralleli ma hanno verso opposto:

$$
\theta=180^\circ
$$

Poiché:

$$
\cos 180^\circ=-1
$$

il prodotto scalare è negativo.

---

## 6. Prodotto scalare tramite componenti

Se abbiamo due vettori:

$$
\vec{v}=(v_x,v_y,v_z)
$$

$$
\vec{w}=(w_x,w_y,w_z)
$$

il prodotto scalare si calcola così:

$$
\vec{v}\cdot\vec{w}=v_xw_x+v_yw_y+v_zw_z
$$

Quindi:

1. si moltiplicano le componenti $x$;
2. si moltiplicano le componenti $y$;
3. si moltiplicano le componenti $z$;
4. si sommano i risultati.

### Esempio

Se:

$$
\vec{v}=(1,2,3)
$$

$$
\vec{w}=(4,5,6)
$$

allora:

$$
\vec{v}\cdot\vec{w}=1\cdot4+2\cdot5+3\cdot6
$$

$$
\vec{v}\cdot\vec{w}=4+10+18=32
$$

Il risultato è $32$, quindi un numero.

---

## 7. Proprietà del prodotto scalare

### Proprietà commutativa

$$
\vec{v}\cdot\vec{w}=\vec{w}\cdot\vec{v}
$$

L'ordine dei vettori non cambia il risultato.

### Esempio

$$
(1,2)\cdot(3,4)=1\cdot3+2\cdot4=11
$$

$$
(3,4)\cdot(1,2)=3\cdot1+4\cdot2=11
$$

Il risultato è lo stesso.

---

### Proprietà distributiva

$$
\vec{u}\cdot(\vec{v}+\vec{w})=\vec{u}\cdot\vec{v}+\vec{u}\cdot\vec{w}
$$

Il prodotto scalare si distribuisce sulla somma.

---

### Proprietà di omogeneità

$$
(s\vec{v})\cdot\vec{w}=\vec{v}\cdot(s\vec{w})=s(\vec{v}\cdot\vec{w})
$$

Se moltiplichiamo uno dei due vettori per uno scalare $s$, è come moltiplicare tutto il prodotto scalare per $s$.

---

## 8. Trovare l'angolo tra due vettori

Partiamo dalla formula del prodotto scalare:

$$
\vec{v}\cdot\vec{w}=|\vec{v}||\vec{w}|\cos\theta
$$

Da questa possiamo ricavare il coseno dell'angolo:

$$
\cos\theta=\frac{\vec{v}\cdot\vec{w}}{|\vec{v}||\vec{w}|}
$$

Quindi l'angolo vale:

$$
\theta=\arccos\left(\frac{\vec{v}\cdot\vec{w}}{|\vec{v}||\vec{w}|}\right)
$$

---

### Esempio

Dati i vettori:

$$
\vec{v}=(4,-3)
$$

$$
\vec{w}=(5,12)
$$

Calcoliamo il prodotto scalare:

$$
\vec{v}\cdot\vec{w}=4\cdot5+(-3)\cdot12
$$

$$
\vec{v}\cdot\vec{w}=20-36=-16
$$

Calcoliamo i moduli:

$$
|\vec{v}|=\sqrt{4^2+(-3)^2}
$$

$$
|\vec{v}|=\sqrt{16+9}=5
$$

$$
|\vec{w}|=\sqrt{5^2+12^2}
$$

$$
|\vec{w}|=\sqrt{25+144}=13
$$

Ora sostituiamo nella formula:

$$
\cos\theta=\frac{-16}{5\cdot13}
$$

$$
\cos\theta=-\frac{16}{65}
$$

Quindi:

$$
\theta=\arccos\left(-\frac{16}{65}\right)
$$

$$
\theta\simeq1.819 \text{ radianti}
$$

In gradi equivale circa a:

$$
\theta\simeq104^\circ
$$

Il prodotto scalare è negativo, quindi l'angolo è maggiore di $90^\circ$.

---

## 9. Esercizio sul prodotto scalare

### Testo

Dire per quali valori di $k$ i seguenti vettori sono ortogonali:

$$
\vec{v}=(1,k-2,3)
$$

$$
\vec{w}=(k,2,5)
$$

### Soluzione

Due vettori sono ortogonali se il loro prodotto scalare è uguale a zero:

$$
\vec{v}\cdot\vec{w}=0
$$

Calcoliamo il prodotto scalare:

$$
(1,k-2,3)\cdot(k,2,5)
$$

Moltiplichiamo componente per componente:

$$
1\cdot k+(k-2)\cdot2+3\cdot5
$$

$$
=k+2k-4+15
$$

$$
=3k+11
$$

Imponiamo la condizione di ortogonalità:

$$
3k+11=0
$$

$$
3k=-11
$$

$$
k=-\frac{11}{3}
$$

Quindi i due vettori sono ortogonali per:

$$
k=-\frac{11}{3}
$$

---

# Prodotto vettoriale

## 10. Definizione di prodotto vettoriale

Il **prodotto vettoriale** è un'operazione tra due vettori che dà come risultato un altro **vettore**.

Si indica con:

$$
\vec{v}\times\vec{w}
$$

Oppure, in alcune slide, con:

$$
\vec{v}\wedge\vec{w}
$$

La formula del modulo è:

$$
|\vec{v}\times\vec{w}|=|\vec{v}||\vec{w}|\sin\theta
$$

dove $\theta$ è l'angolo compreso tra i due vettori.

---

## 11. Direzione e verso del prodotto vettoriale

Il prodotto vettoriale produce un vettore che è:

- perpendicolare a $\vec{v}$;
- perpendicolare a $\vec{w}$;
- perpendicolare al piano formato da $\vec{v}$ e $\vec{w}$.

Il verso si trova con la **regola della mano destra**.

---

## 12. Regola della mano destra

Per capire il verso di:

$$
\vec{v}\times\vec{w}
$$

si immagina di ruotare $\vec{v}$ verso $\vec{w}$.

Con la mano destra:

- le dita seguono la rotazione da $\vec{v}$ verso $\vec{w}$;
- il pollice indica il verso del prodotto vettoriale.

---

## 13. Proprietà anticommutativa

Il prodotto vettoriale non è commutativo.

Infatti:

$$
\vec{v}\times\vec{w}=-(\vec{w}\times\vec{v})
$$

Se scambiamo l'ordine dei vettori, il risultato ha:

- stesso modulo;
- stessa direzione;
- verso opposto.

---

## 14. Area del parallelogramma

Il modulo del prodotto vettoriale rappresenta l'area del parallelogramma costruito sui due vettori.

Infatti:

$$
|\vec{v}\times\vec{w}|=|\vec{v}||\vec{w}|\sin\theta
$$

Questa formula corrisponde a:

$$
\text{area}=base\cdot altezza
$$

L'altezza del parallelogramma è:

$$
|\vec{w}|\sin\theta
$$

Quindi:

$$
\text{area}=|\vec{v}||\vec{w}|\sin\theta
$$

---

## 15. Casi importanti del prodotto vettoriale

### Vettori ortogonali

Se i vettori sono ortogonali:

$$
\theta=90^\circ
$$

Poiché:

$$
\sin90^\circ=1
$$

allora:

$$
|\vec{v}\times\vec{w}|=|\vec{v}||\vec{w}|
$$

Il prodotto vettoriale ha modulo massimo.

---

### Vettori paralleli

Se i vettori sono paralleli:

$$
\theta=0^\circ
$$

oppure:

$$
\theta=180^\circ
$$

Poiché:

$$
\sin0^\circ=0
$$

e:

$$
\sin180^\circ=0
$$

allora:

$$
|\vec{v}\times\vec{w}|=0
$$

Quindi:

> Il prodotto vettoriale di due vettori paralleli è nullo.

---

## 16. Proprietà distributiva del prodotto vettoriale

Anche il prodotto vettoriale gode della proprietà distributiva:

$$
\vec{v}\times(\vec{w}+\vec{z})=\vec{v}\times\vec{w}+\vec{v}\times\vec{z}
$$

---

## 17. Prodotto vettoriale tramite componenti

Se abbiamo:

$$
\vec{v}=(v_x,v_y,v_z)
$$

$$
\vec{w}=(w_x,w_y,w_z)
$$

allora:

$$
\vec{v}\times\vec{w}
=
(v_yw_z-v_zw_y,\ v_zw_x-v_xw_z,\ v_xw_y-v_yw_x)
$$

Questa formula si può ricordare usando il determinante:

$$
\vec{v}\times\vec{w}
=
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k}\\
v_x & v_y & v_z\\
w_x & w_y & w_z
\end{vmatrix}
$$

La prima riga contiene i versori fondamentali.

La seconda riga contiene le componenti di $\vec{v}$.

La terza riga contiene le componenti di $\vec{w}$.

---

## 18. Esercizio sul prodotto vettoriale

### Testo

Determinare un vettore $\vec{u}$ dello spazio che risulta contemporaneamente ortogonale ai vettori:

$$
\vec{v}=(1,0,-1)
$$

$$
\vec{w}=(0,2,1)
$$

### Soluzione

Un vettore ortogonale sia a $\vec{v}$ sia a $\vec{w}$ si può ottenere con il prodotto vettoriale:

$$
\vec{u}=\vec{v}\times\vec{w}
$$

Scriviamo il determinante:

$$
\vec{u}
=
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k}\\
1 & 0 & -1\\
0 & 2 & 1
\end{vmatrix}
$$

Calcolando si ottiene:

$$
\vec{u}=2\vec{i}-1\vec{j}+2\vec{k}
$$

Quindi:

$$
\vec{u}=(2,-1,2)
$$

Questo vettore è ortogonale sia a $\vec{v}$ sia a $\vec{w}$.

---

## 19. Verifica dell'ortogonalità

Verifichiamo con il prodotto scalare.

Con $\vec{v}$:

$$
(2,-1,2)\cdot(1,0,-1)
$$

$$
=2\cdot1+(-1)\cdot0+2\cdot(-1)
$$

$$
=2+0-2=0
$$

Con $\vec{w}$:

$$
(2,-1,2)\cdot(0,2,1)
$$

$$
=2\cdot0+(-1)\cdot2+2\cdot1
$$

$$
=0-2+2=0
$$

Poiché entrambi i prodotti scalari valgono zero, il vettore $\vec{u}$ è ortogonale a entrambi.

---

# Confronto tra prodotto scalare e prodotto vettoriale

| Operazione | Simbolo | Risultato | Formula principale | Quando vale zero |
|---|---|---|---|---|
| Prodotto per scalare | $c\vec{v}$ | Vettore | Moltiplico ogni componente per $c$ | Se $c=0$ oppure $\vec{v}=0$ |
| Prodotto scalare | $\vec{v}\cdot\vec{w}$ | Numero | $|\vec{v}||\vec{w}|\cos\theta$ | Se i vettori sono ortogonali |
| Prodotto vettoriale | $\vec{v}\times\vec{w}$ | Vettore | $|\vec{v}||\vec{w}|\sin\theta$ | Se i vettori sono paralleli |

---

# Riassunto finale

Un vettore è caratterizzato da:

- modulo;
- direzione;
- verso.

Moltiplicare un vettore per uno scalare significa modificare il suo modulo. Se lo scalare è negativo, cambia anche il verso.

Un versore è un vettore di modulo $1$ che serve a indicare una direzione.

Il prodotto scalare tra due vettori dà come risultato un numero. Serve a capire quanto due vettori sono allineati. Se il prodotto scalare è zero, i vettori sono ortogonali.

Il prodotto vettoriale tra due vettori dà come risultato un nuovo vettore. Questo nuovo vettore è perpendicolare ai due vettori di partenza. Se si scambia l'ordine dei vettori, cambia il verso del risultato.

La frase chiave da ricordare è:

> Il prodotto scalare misura l'allineamento tra due vettori, mentre il prodotto vettoriale costruisce un vettore perpendicolare a entrambi.
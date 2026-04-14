# La misura

## Definizione

Una **grandezza fisica** $G$ è definita da un’operazione di misura, che ne determina il rapporto numerico $g$ con la corrispondente **unità di misura** $U_G$.

Si scrive quindi:

$$
G = g \cdot U_G
$$

> [!note] In pratica
> - **$G$** = la grandezza che stai misurando  
> - **$g$** = il numero ottenuto dalla misura  
> - **$U_G$** = l’unità di misura

### Esempio
Se una lunghezza misura **5 metri**, allora:

$$
G = 5 \cdot m
$$

dove:
- **$G$** è la lunghezza
- **$g = 5$**
- **$U_G = m$**

---

## Significato della misura

Il risultato di una misura dipende:
- dalle **condizioni sperimentali**
- dalla **qualità dello strumento**
- da come viene effettuata la misura

La misura rappresenta quindi la nostra **migliore stima** del cosiddetto **valore vero** della grandezza.

> [!important] Valore vero
> Il **valore vero** è un concetto ideale, perché si avrebbe solo misurando in condizioni perfette e con uno strumento perfetto.  
> Nella realtà, questo valore non si conosce mai con certezza assoluta.

---

## La misura in breve

- Una **grandezza fisica** è qualcosa che si può misurare.
- Misurare significa assegnare un **numero** e un’**unità di misura**.
- La formula generale è:

$$
G = g \cdot U_G
$$

- Il risultato di una misura dipende dallo strumento e dalle condizioni sperimentali.
- Una misura non fornisce quasi mai il valore vero esatto.
- La misura è una **stima del valore vero**.
- Il valore vero perfetto è un concetto **astratto e ideale**.

---

# Errori di misura

A ogni misura è associato un **errore**, cioè una stima di quanto il risultato ottenuto si discosta dal valore vero della grandezza.

Gli errori possono essere di due tipi:
- **casuali**
- **sistematici**

---

## Errore casuale

L’**errore casuale** deriva da piccole incertezze che fanno oscillare i risultati di misure ripetute della stessa grandezza, talvolta in eccesso e talvolta in difetto, attorno al valore vero.

> [!example] Esempio intuitivo
> Se misuri più volte la stessa lunghezza, potresti ottenere:
> - 10,1 cm
> - 9,9 cm
> - 10,0 cm
> - 10,2 cm  
>
> I valori cambiano leggermente in modo imprevedibile.

### Caratteristica principale
Gli errori casuali fanno sì che i risultati si distribuiscano intorno al valore vero.

Se si rappresentano su un grafico molte misure ripetute, spesso si ottiene una distribuzione a **campana** detta **gaussiana**.

---

## Errore sistematico

L’**errore sistematico** si verifica quando la misura è falsata sempre nello stesso verso.

Può dipendere, ad esempio:
- da uno **strumento tarato male**
- da condizioni di utilizzo non corrette
- da un errore costante dell’operatore

> [!warning] Attenzione
> Con un errore sistematico, il risultato della misura risulta spesso sempre:
> - più grande del valore vero  
> oppure
> - più piccolo del valore vero

### Esempio
Se una bilancia è regolata male e segna sempre **2 kg in più**, tutte le misure saranno sbagliate nella stessa direzione.

### Come si individua
Un errore sistematico può essere scoperto confrontando la misura ottenuta con:
- strumenti diversi
- metodi diversi

---

# Errore massimo

Una misura non si scrive soltanto con un numero, ma anche con la sua **incertezza (ERRORE)**.

## Forma generale

$$
x = x^* \pm \delta x
$$

dove:
- **$x^*$** = valore misurato
- **$\delta x$** = errore massimo o incertezza

---

## Significato

L’**errore massimo** indica il margine entro cui si ritiene possa trovarsi il valore vero.

### Esempio

$$
L = 21 \pm 1 \text{ cm}
$$

significa che la lunghezza misurata è **21 cm**, ma il valore vero potrebbe trovarsi tra:

$$
20 \text{ cm} \quad \text{e} \quad 22 \text{ cm}
$$

---

## Intervallo di misura

In generale, il valore vero si considera compreso nell’intervallo:

$$
[x^* - \delta x,\; x^* + \delta x]
$$

---

## Idea chiave

> [!summary] Da ricordare
> Più uno strumento è **poco preciso**, più grande sarà l’errore associato alla misura.

---
## Errore statistico

Quando si misura **N volte** la stessa grandezza nelle stesse condizioni, i risultati possono cambiare leggermente a causa degli **errori casuali**.

### Media delle misure
$$
\bar{x} = \frac{\sum_{i=1}^{N} x_i}{N}
$$

La media $\bar{x}$ rappresenta la **migliore stima** del valore della grandezza.

### Deviazione standard
$$
\sigma_x = \sqrt{\frac{\sum_{i=1}^{N}(x_i-\bar{x})^2}{N-1}}
$$

La deviazione standard misura **quanto le misure sono disperse** attorno alla media.

### Interpretazione
- Se $\sigma_x$ è piccola, le misure sono molto vicine tra loro.
- Se $\sigma_x$ è grande, le misure sono più sparse.

> [!note]
> L’errore statistico è legato agli **errori casuali**, perché descrive le oscillazioni delle misure ripetute.

### Distribuzione gaussiana
In presenza di errori casuali, i risultati delle misure tendono a distribuirsi secondo una **curva a campana**, detta **distribuzione gaussiana**.

## Distribuzione normale o gaussiana

Quando si misura molte volte la stessa grandezza, i risultati non coincidono tutti perfettamente a causa degli **errori casuali**.

Se si rappresentano i risultati in un **istogramma**:

- sull’asse orizzontale si mettono i valori misurati
- sull’asse verticale il numero di volte in cui quei valori compaiono

si ottiene una forma simile a una **campana**, detta **distribuzione normale o gaussiana**.

### Equazione della curva di Gauss
$$
N(x)=A\,e^{-\frac{(x-x_0)^2}{2\sigma^2}}
$$
![[Pasted image 20260414191404.png|495]]
dove:
- **$N(x)$** = frequenza o altezza della curva in corrispondenza del valore $x$
- **$A$** = costante che determina l’altezza massima della curva
- **$x$** = valore considerato
- **$x_0$** = valore centrale della distribuzione
- **$\sigma$** = deviazione standard

### Significato
- vicino a **$x_0$** i valori sono più frequenti
- allontanandosi da **$x_0$** i valori diventano meno frequenti
- più **$\sigma$** è piccola, più la campana è stretta
- più **$\sigma$** è grande, più la campana è larga

> [!note]
> La distribuzione gaussiana descrive l’andamento tipico dei risultati di misure ripetute affette da errori casuali.



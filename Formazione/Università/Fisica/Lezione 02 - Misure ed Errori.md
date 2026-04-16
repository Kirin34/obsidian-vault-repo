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
Gli errori casuali fanno sì che i risultati si distribuiscano intorno al valore centrale della misura.

Se si rappresentano su un grafico molte misure ripetute, spesso si ottiene una distribuzione a **campana**, detta **distribuzione normale** o **gaussiana**.

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

Una misura non si scrive soltanto con un numero, ma anche con la sua **incertezza**.

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

> [!summary] Da ricordare
> Più uno strumento è **poco preciso**, più grande sarà l’errore associato alla misura.

---

# Errore statistico

Quando si misura **N volte** la stessa grandezza nelle stesse condizioni, i risultati possono cambiare leggermente a causa degli **errori casuali**.

## Media delle misure

$$
\bar{x} = \frac{\sum_{i=1}^{N} x_i}{N}
$$

La media $\bar{x}$ rappresenta la **migliore stima** del valore della grandezza.

## Deviazione standard

$$
\sigma = \sqrt{\frac{\sum_{i=1}^{N}(x_i-\bar{x})^2}{N-1}}
$$

La deviazione standard misura **quanto le misure sono disperse** attorno alla media.

## Interpretazione

- Se **$\sigma$** è piccola, le misure sono molto vicine tra loro.
- Se **$\sigma$** è grande, le misure sono più sparse.

> [!note]
> L’errore statistico è legato agli **errori casuali**, perché descrive le oscillazioni delle misure ripetute.

Il risultato di una misura ripetuta si può esprimere come:

$$
x = \bar{x} \pm \sigma
$$

dove:
- **$\bar{x}$** è il valore medio
- **$\sigma$** è la deviazione standard

---

# Distribuzione normale o gaussiana

La **distribuzione normale** e la **distribuzione gaussiana** sono la stessa cosa.

Quando si misura molte volte la stessa grandezza, i risultati non coincidono tutti perfettamente a causa degli **errori casuali**.

Se si rappresentano i risultati in un **istogramma**:
- sull’asse orizzontale si mettono i valori misurati
- sull’asse verticale il numero di volte in cui quei valori compaiono

si ottiene una forma simile a una **campana**, detta **curva di Gauss**.

## Equazione della curva di Gauss

$$
N(x)=A\,e^{-\frac{(x-\bar{x})^2}{2\sigma^2}}
$$

![[Pasted image 20260414191404.png|495]]

dove:
- **$N(x)$** = frequenza o altezza della curva in corrispondenza del valore $x$
- **$A$** = costante che determina l’altezza massima della curva
- **$x$** = valore considerato
- **$\bar{x}$** = valore medio delle misure
- **$\sigma$** = deviazione standard

## Significato

- vicino a **$\bar{x}$** i valori sono più frequenti
- allontanandosi da **$\bar{x}$** i valori diventano meno frequenti
- più **$\sigma$** è piccola, più la campana è stretta
- più **$\sigma$** è grande, più la campana è larga

> [!note]
> La distribuzione gaussiana descrive l’andamento tipico dei risultati di misure ripetute affette da errori casuali.

---

## Significato probabilistico

Nella distribuzione normale:

- circa il **68%** delle misure cade nell’intervallo  

$$
\bar{x} \pm \sigma
$$

- circa il **95%** delle misure cade nell’intervallo  

$$
\bar{x} \pm 2\sigma
$$

- più del **99%** delle misure cade nell’intervallo  

$$
\bar{x} \pm 3\sigma
$$

> [!summary] Da ricordare
> Più le misure sono vicine alla media, più sono probabili.  
> Più ci si allontana dalla media, meno sono probabili.

---

# Schema finale super rapido

## Misura
- Una grandezza fisica si misura con:
  - un **numero**
  - un’**unità di misura**
- Formula:

$$
G = g \cdot U_G
$$

## Errori
- **Errore casuale** → fa oscillare i risultati attorno al valore medio
- **Errore sistematico** → sposta i risultati sempre nella stessa direzione

## Scrittura di una misura
$$
x = x^* \pm \delta x
$$

## Misure ripetute
- **Media**:

$$
\bar{x} = \frac{\sum x_i}{N}
$$

- **Deviazione standard**:

$$
\sigma = \sqrt{\frac{\sum (x_i-\bar{x})^2}{N-1}}
$$

## Distribuzione normale
- È la classica **curva a campana**
- Centro = **media**
- Larghezza = **deviazione standard**
- Intervalli tipici:
  - **68%** entro $\pm\sigma$
  - **95%** entro $\pm2\sigma$
  - **99%+** entro $\pm3\sigma$

---
# Propagazione dell’errore

Quando una grandezza non viene misurata direttamente, ma viene calcolata a partire da altre grandezze misurate, anche il suo errore dipende dagli errori delle grandezze di partenza.
## Somma e differenza

Se:
$$
z = x + y
\quad \text{oppure} \quad
z = x - y
$$
allora l’errore assoluto si propaga come:

$$
\delta z = \delta x + \delta y
$$
Nel caso statistico, se gli errori sono espressi tramite deviazioni standard:

$$
\sigma_z = \sqrt{\sigma_x^2 + \sigma_y^2}
$$
## Errore relativo

L’errore relativo è il rapporto tra errore assoluto e valore misurato:
$$
\frac{\delta x}{x}
$$
Spesso si esprime in percentuale.
## Prodotto e quoziente

Se:
$$
z = x\cdot y
\quad \text{oppure} \quad
z = \frac{x}{y}
$$
allora si sommano gli errori relativi:
$$
\frac{\delta z}{z} = \frac{\delta x}{x} + \frac{\delta y}{y}
$$
## Formula generale

Se una grandezza dipende da più variabili secondo:

$$
y = f(x_1, x_2, \dots, x_N)
$$
allora l’errore massimo si propaga come:
$$
\delta_f = \sum_{i=1}^{N} \left|\frac{\partial f}{\partial x_i}\right| \delta_i
$$
e nel caso statistico:
$$
\sigma_f^2 = \sum_{i=1}^{N} \left(\frac{\partial f}{\partial x_i}\right)^2 \sigma_i^2
$$

> [!note]
> La propagazione dell’errore serve a capire come le incertezze delle misure di partenza influenzano il risultato finale.

---
# Cifre significative

Poiché ogni misura è affetta da un errore, il risultato non va scritto con più cifre di quelle giustificate dalla precisione dello strumento.
## Idea fondamentale
Una misura deve essere espressa in modo coerente con il suo errore.

> [!note]
> L’ultima cifra significativa della misura deve avere lo stesso ordine di grandezza dell’errore.
## Esempio
Se misuro lo spessore di un libro con uno strumento che ha risoluzione di 1 mm, posso scrivere:
$$
x = 24 \pm 1 \text{ mm}
$$
Non avrebbe senso scrivere \(24,5\) mm, perché la cifra decimale non è giustificata dalla precisione dello strumento.
## Somma di misure
Se si ottiene un risultato come:
$$
H = 227{,}4 \pm 1{,}1 \text{ cm}
$$
il valore va arrotondato in modo coerente con l’errore, quindi si scrive:
$$
H = 227 \pm 1 \text{ cm}
$$
## Precisione di una misura
Per capire quale misura è più precisa si confronta l’**errore relativo**:
$$
\frac{\delta x}{x}
$$
Spesso si esprime in percentuale.
### Esempio
$$
A = (20{,}0 \pm 0{,}5)\text{ cm}
$$
$$
\frac{0{,}5}{20{,}0} = 0{,}025 = 2{,}5\%
$$
$$
B = (10 \pm 1)\text{ mm}
$$
$$
\frac{1}{10} = 0{,}1 = 10\%
$$
La misura **A** è più precisa, perché ha errore relativo minore.

> [!summary] Da ricordare
> - Le cifre significative dipendono dall’errore della misura.
> - Non bisogna scrivere più cifre di quelle realmente affidabili.
> - Una misura è più precisa se ha errore relativo minore.


----
# Strumenti di misura

Uno **strumento di misura** è un dispositivo che permette di determinare la corrispondenza tra una grandezza fisica e la sua misura.
## Strumento come trasduttore
Uno strumento di misura è spesso un **trasduttore**, cioè un dispositivo che trasforma la grandezza da misurare in una risposta più facilmente osservabile.
### Esempio
Nel termometro a mercurio:
- la grandezza da misurare è la **temperatura**
- la risposta osservabile è la **lunghezza della colonna di liquido**

---

## Taratura o calibrazione
La **taratura** consiste nel determinare la risposta dello strumento per valori noti della grandezza, in modo da costruire correttamente la sua scala.

---
# Caratteristiche degli strumenti di misura

## Risoluzione
La **risoluzione** è la più piccola variazione della grandezza leggibile sullo strumento.

### Esempio
- righello con divisioni da 1 mm → risoluzione = 1 mm
- bilancia digitale che mostra 0,1 g → risoluzione = 0,1 g

## Sensibilità
La **sensibilità** misura quanto varia la risposta dello strumento al variare della grandezza misurata.
$$
s = \left|\frac{dr}{dx}\right|
$$
dove:
- $dx$ = variazione della grandezza misurata
- $dr$ = variazione della risposta dello strumento
Più la risposta cambia molto per piccole variazioni della grandezza, più lo strumento è sensibile.
## Precisione
La **precisione** descrive la ripetibilità delle misure effettuate nelle stesse condizioni.

- misure molto vicine tra loro → grande precisione
- misure molto disperse → scarsa precisione

La precisione è legata agli **errori casuali**.

## Accuratezza
L’**accuratezza** indica quanto il risultato della misura è vicino al valore vero.

Una misura accurata è poco influenzata da **errori sistematici**.

---
# Differenza tra accuratezza e precisione

## Accuratezza
Riguarda la vicinanza al valore vero.
## Precisione
Riguarda la dispersione dei risultati attorno alla media.

> [!note]
> Una misura può essere:
> - accurata e precisa
> - accurata ma poco precisa
> - precisa ma non accurata
> - né precisa né accurata

![[Pasted image 20260416141515.png|630]]
# Arrotondamenti

## Regola generale
- Se la prima cifra da eliminare è **minore di 5**, la cifra precedente resta invariata.
- Se la prima cifra da eliminare è **maggiore di 5**, la cifra precedente aumenta di 1.
- Se la prima cifra da eliminare è **uguale a 5**, in queste slide si usa la **regola del pari**:
  - se la cifra che resta è pari, non cambia
  - se è dispari, aumenta di 1
### Esempi
$$
3.472 \to 3.47
$$
$$
5.738 \to 5.74
$$
$$
5.798 \to 5.80
$$
$$
5.685 \to 5.68
$$
$$
5.675 \to 5.68
$$
---
## Schema riassuntivo — propagazione dell'errore

| Operazione                    | Regola                                                                                                        |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Somma** $z=a+b$             | valore: $z^*=a^*+b^*$  •  errore: $\delta z=\delta a+\delta b$                                                |
| **Differenza** $z=a-b$        | valore: $z^*=a^*-b^*$  •  errore: $\delta z=\delta a+\delta b$                                                |
| **Prodotto** $z=a\cdot b$     | valore: $z^*=a^*\cdot b^*$  •  errore relativo: $\frac{\delta z}{z}=\frac{\delta a}{a}+\frac{\delta b}{b}$    |
| **Quoziente** $z=\frac{a}{b}$ | valore: $z^*=\frac{a^*}{b^*}$  •  errore relativo: $\frac{\delta z}{z}=\frac{\delta a}{a}+\frac{\delta b}{b}$ |
> [!summary] Da ricordare
> - In **somma** e **differenza** si sommano gli **errori assoluti**.
> - In **prodotto** e **quoziente** si sommano gli **errori relativi**.
# Quesiti

## Q1
Se la media è:
$$
x^*=16
$$

e la deviazione standard è:
$$
\sigma=3
$$

allora almeno il 99% dei risultati è contenuto circa in:
$$
x^* \pm 3\sigma = 16 \pm 9
$$
cioè:

$$
[7,\;25]
$$
## Q2
Per la somma:
$$
z=x+y
$$
l’errore associato è:
$$
dz=dx+dy
$$
## Q3
Per il prodotto:
$$
z=x\cdot y
$$
con:
$$
\frac{dx}{x}=0.2
\qquad
\frac{dy}{y}=0.1
$$
l’errore relativo è:
$$
\frac{dz}{z}=0.2+0.1=0.3
$$
cioè il **30%**.

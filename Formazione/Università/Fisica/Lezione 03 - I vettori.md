# I vettori  
## Definizione di vettore

In fisica esistono alcune grandezze che non possono essere descritte solo con un numero.
  
Per esempio, dire:

> “una forza vale 10 N”

non basta sempre, perché bisogna anche sapere **verso dove spinge o tira** quella forza.
Queste grandezze si chiamano **grandezze vettoriali**.

Una grandezza vettoriale è definita da:

| Elemento                  | Significato                                   |
| ------------------------- | --------------------------------------------- |
| **Modulo**                | quanto è grande/intensa la grandezza          |
| **Direzione**             | La retta lungo cui agisce                     |
| **Verso**                 | da quale parte della direzione punta          |
| **Punto di Applicazione** | il punto da cui parte il vettore quando serve |
Un vettore viene rappresentato graficamente con una **freccia**.

La freccia indica:

- la **direzione**, cioè la linea lungo cui si trova il vettore;
- il **verso**, cioè dove punta la freccia;
- il **modulo**, cioè la lunghezza della freccia.

Esempio semplice:

```text

----------->

```

  Questa freccia rappresenta un vettore diretto verso destra.

---
## Modulo, direzione e verso

  Un vettore non è solo “quanto vale”, ma anche “dove va”.
Per esempio:  

```text

5 m verso destra

```

  è diverso da:

```text

5 m verso sinistra

```

  Anche se il modulo è sempre `5 m`, il verso cambia.

  Quindi due vettori possono avere lo stesso modulo, ma essere diversi perché hanno direzione o verso diverso.

---
## Come si indica un vettore

In genere, nei libri o nelle slide, un vettore viene indicato con una lettera in **grassetto**, ad esempio:

```text

v

```

   Oppure, quando si scrive a mano, si mette una freccia sopra la lettera:
$$

\vec{v}

$$

  Il modulo del vettore, invece, si può indicare semplicemente senza freccia:

  $$

v

$$

oppure con le barre:
$$

|\vec{v}|

$$

  Quindi:

| Simbolo       | Significato                     |
| ------------- | ------------------------------- |
| $\vec{v}$     | vettore velocità                |
| $v$           | modulo della velocità           |
| $\|\vec{v}\|$ | lunghezza/intensità del vettore |

---
## Componenti del vettore

### Cosa sono le componenti

Un vettore può essere scomposto lungo gli assi cartesiani.

  Questo significa che posso prendere un vettore inclinato e vedere “quanta parte” di quel vettore va lungo l’asse `x`, lungo l’asse `y` e, nello spazio tridimensionale, lungo l’asse `z`.

Le componenti sono quindi le **proiezioni del vettore sugli assi**.
In parole semplici:

> Le componenti servono a trasformare un vettore inclinato in più pezzi più facili da studiare.

---
## Vettore in tre dimensioni

Se siamo in uno spazio tridimensionale, abbiamo tre assi:
- asse `x`;
- asse `y`;
- asse `z`.

Un vettore può quindi essere descritto tramite tre componenti:
$$

\vec{v} = (v_x, v_y, v_z)

$$
dove:

| Componente | Significato |

|---|---|

| $v_x$ | parte del vettore lungo l’asse x |

| $v_y$ | parte del vettore lungo l’asse y |

| $v_z$ | parte del vettore lungo l’asse z |

  

Quindi, invece di descrivere il vettore solo con una freccia nello spazio, posso descriverlo con tre numeri.

  

---

  

## Modulo di un vettore in tre dimensioni

  

Il modulo di un vettore tridimensionale si calcola usando una formula simile al teorema di Pitagora.

  

Se il vettore ha componenti:

  

$$

\vec{v} = (v_x, v_y, v_z)

$$

  

allora il suo modulo è:

  

$$

v = \sqrt{v_x^2 + v_y^2 + v_z^2}

$$

  

Questa formula serve a trovare la “lunghezza vera” del vettore nello spazio.

  

---

  

## Esempio semplice

  

Se un vettore ha componenti:

  

$$

v_x = 3

$$

  

$$

v_y = 4

$$

  

$$

v_z = 0

$$

  

allora il modulo è:

  

$$

v = \sqrt{3^2 + 4^2 + 0^2}

$$

  

$$

v = \sqrt{9 + 16}

$$

  

$$

v = \sqrt{25}

$$

  

$$

v = 5

$$

  

Quindi il vettore ha modulo `5`.

  

---

  

# Componenti di un vettore in due dimensioni

  

## Vettore nel piano cartesiano

  

Quando lavoriamo in due dimensioni, usiamo solo due assi:

  

- asse `x`, orizzontale;

- asse `y`, verticale.

  

Un vettore nel piano può essere scomposto in due componenti:

  

$$

\vec{a} = (a_x, a_y)

$$

  

dove:

  

| Componente | Significato |

|---|---|

| $a_x$ | componente orizzontale |

| $a_y$ | componente verticale |

  

La componente $a_x$ dice quanto il vettore si sposta verso destra o sinistra.

  

La componente $a_y$ dice quanto il vettore si sposta verso l’alto o verso il basso.

  

---

  

## Perché le componenti formano un triangolo rettangolo

  

Nella slide si vede un vettore inclinato $\vec{a}$.

  

Questo vettore può essere scomposto in:

  

- una parte orizzontale $a_x$;

- una parte verticale $a_y$.

  

Graficamente succede questo:

  

```text

          Q

          |

          | ay

          |

P --------R

    ax

```

  

Il vettore vero va da `P` a `Q`.

  

La componente orizzontale va da `P` a `R`.

  

La componente verticale va da `R` a `Q`.

  

Queste due componenti formano un **triangolo rettangolo**.

  

Il vettore $\vec{a}$ è l’ipotenusa del triangolo.

  

Le componenti $a_x$ e $a_y$ sono i cateti.

  

---
## Modulo di un vettore in due dimensioni

Poiché le componenti formano un triangolo rettangolo, possiamo usare il teorema di Pitagora.

Se:  

$$

\vec{a} = (a_x, a_y)

$$

  allora:

$$
a = \sqrt{a_x^2 + a_y^2}
$$

Dove:

- $a$ è il modulo del vettore;

- $a_x$ è la componente lungo l’asse x;

- $a_y$ è la componente lungo l’asse y.

---
## Esempio pratico

Immagina di camminare:

- 3 metri verso destra;
- 4 metri verso l’alto.

Il tuo spostamento complessivo non è `3 + 4 = 7 m`, perché non hai camminato tutto in linea retta.

Il vettore spostamento diretto dal punto iniziale al punto finale è la diagonale.

Si calcola così:

$$

a = \sqrt{3^2 + 4^2}

$$

$$

a = \sqrt{9 + 16}

$$
$$

a = \sqrt{25}

$$
$$

a = 5

$$

Quindi lo spostamento diretto è di `5 m`.

---
## Composizione di più vettori
## Vettore nullo

Il vettore nullo è un vettore che ha modulo zero.

  In tre dimensioni si scrive:

$$

\vec{v} = (0, 0, 0)

$$
Significa che non c’è nessuno spostamento, nessuna forza, nessuna velocità o comunque nessuna grandezza vettoriale effettiva.

  Il suo modulo è:

$$

v = 0

$$
---
## Vettore opposto

Dato un vettore:

$$

\vec{v} = (v_x, v_y, v_z)

$$
il suo vettore opposto è:

$$

-\vec{v} = (-v_x, -v_y, -v_z)

$$
Il vettore opposto ha:

- stesso modulo;
- stessa direzione;
- verso opposto.

Per esempio, se un vettore punta verso destra, il suo opposto punta verso sinistra.

```text

vettore v:        -------->

vettore -v:       <--------

```
  

---

  

## Esempio con le componenti

  

Se:

  

$$

\vec{v} = (3, 2)

$$

  

allora il vettore opposto è:

  

$$

-\vec{v} = (-3, -2)

$$

  

Il modulo resta uguale, ma il verso cambia.

  

Infatti:

  

$$

|\vec{v}| = \sqrt{3^2 + 2^2}

$$

  

e anche:

  

$$

|-\vec{v}| = \sqrt{(-3)^2 + (-2)^2}

$$

  

Poiché i numeri al quadrato diventano positivi, il modulo è lo stesso.

  

---

  

# Somma e differenza di vettori

  

La slide anticipa che, dopo aver definito vettore nullo e vettore opposto, si può parlare di:

  

- somma di vettori;

- differenza di vettori.

  

## Somma di vettori

  

Per sommare due vettori, si sommano le rispettive componenti.

  

Se:

  

$$

\vec{a} = (a_x, a_y)

$$

  

e:

  

$$

\vec{b} = (b_x, b_y)

$$

  

allora:

  

$$

\vec{a} + \vec{b} = (a_x + b_x, a_y + b_y)

$$

  

Esempio:

  

$$

\vec{a} = (3, 2)

$$

  

$$

\vec{b} = (4, 1)

$$

  

Allora:

  

$$

\vec{a} + \vec{b} = (3 + 4, 2 + 1)

$$

  

$$

\vec{a} + \vec{b} = (7, 3)

$$

  

---

  

## Differenza di vettori

  

La differenza tra due vettori si può vedere come una somma con il vettore opposto.

  

Cioè:

  

$$

\vec{a} - \vec{b} = \vec{a} + (-\vec{b})

$$

  

Se:

  

$$

\vec{a} = (a_x, a_y)

$$

  

e:

  

$$

\vec{b} = (b_x, b_y)

$$

  

allora:

  

$$

\vec{a} - \vec{b} = (a_x - b_x, a_y - b_y)

$$

  

Esempio:

  

$$

\vec{a} = (5, 4)

$$

  

$$

\vec{b} = (2, 1)

$$

  

Allora:

  

$$

\vec{a} - \vec{b} = (5 - 2, 4 - 1)

$$

  

$$

\vec{a} - \vec{b} = (3, 3)

$$

  

---

  

# Differenza tra grandezze scalari e vettoriali

  

## Grandezza scalare

  

Una grandezza scalare è descritta solo da:

  

- numero;

- unità di misura.


Esempi:

| Grandezza scalare | Esempio |
| ----------------- | ------- |
| massa             | 5 kg    |
| temperatura       | 20 °C   |
| tempo             | 10 s    |
| energia           | 100 J   |


Se dico:

```text

massa = 5 kg

```

  ho già detto tutto quello che serve.

---
## Grandezza vettoriale
Una grandezza vettoriale, invece, ha bisogno anche di direzione e verso.

Esempi: 

| Grandezza vettoriale | Perché è vettoriale                          |
| -------------------- | -------------------------------------------- |
| forza                | bisogna sapere dove agisce                   |
| velocità             | bisogna sapere verso dove si muove il corpo  |
| accelerazione        | bisogna sapere verso dove cambia la velocità |
| spostamento          | bisogna sapere da dove a dove avviene        |
Per esempio:
  
```text

velocità = 10 m/s verso est

```

  Qui `10 m/s` è il modulo, mentre “verso est” indica direzione e verso.

  ---
# Schema riassuntivo

| Concetto              | Significato                                  |
| --------------------- | -------------------------------------------- |
| Vettore               | grandezza con modulo, direzione e verso      |
| Modulo                | intensità/lunghezza del vettore              |
| Direzione             | retta lungo cui si sviluppa il vettore       |
| Verso                 | orientamento della freccia                   |
| Componente            | proiezione del vettore su un asse            |
| $v_x$                 | componente lungo x                           |
| $v_y$                 | componente lungo y                           |
| $v_z$                 | componente lungo z                           |
| Vettore nullo         | vettore con modulo zero                      |
| Vettore opposto       | vettore con stesso modulo ma verso contrario |
| Somma vettoriale      | somma delle componenti corrispondenti        |
| Differenza vettoriale | sottrazione delle componenti corrispondenti  |

---
# Formule da ricordare

## Vettore in due dimensioni
  
$$

\vec{a} = (a_x, a_y)

$$

$$

a = \sqrt{a_x^2 + a_y^2}

$$

---

  

## Vettore in tre dimensioni

  

$$

\vec{v} = (v_x, v_y, v_z)

$$

  

$$

v = \sqrt{v_x^2 + v_y^2 + v_z^2}

$$

  

---

  

## Vettore opposto

  

$$

\vec{v} = (v_x, v_y, v_z)

$$

  

$$

-\vec{v} = (-v_x, -v_y, -v_z)

$$

  

---

  

## Somma di vettori

  

$$

\vec{a} + \vec{b} = (a_x + b_x, a_y + b_y)

$$

  

---

  

## Differenza di vettori

  

$$

\vec{a} - \vec{b} = (a_x - b_x, a_y - b_y)

$$

  

---

  

# Spiegazione super semplice da ricordare

  

Un vettore è come una freccia.

  

La freccia ti dice:

  

```text

quanto è lunga → modulo

dove sta andando → direzione

da che parte punta → verso

```

  

Se il vettore è inclinato, posso dividerlo in pezzi più semplici:

  

```text

pezzo orizzontale → componente x

pezzo verticale → componente y

```

  

Questi pezzi formano un triangolo rettangolo, quindi per trovare la lunghezza del vettore uso Pitagora.

  

La cosa importante è ricordare che:

  

> un vettore non è solo un numero, ma un numero con una direzione e un verso.

  

---

  

# Mini domande da esame

  

## 1. Che cos’è un vettore?

  

Un vettore è una grandezza fisica definita da modulo, direzione e verso.

  

---

  

## 2. Che cos’è il modulo di un vettore?

  

Il modulo è l’intensità o la lunghezza del vettore.

  

---

  

## 3. Che differenza c’è tra direzione e verso?

  

La direzione è la retta lungo cui si trova il vettore.

  

Il verso indica da quale parte della retta punta il vettore.

  

---

  

## 4. Che cosa sono le componenti di un vettore?

  

Sono le proiezioni del vettore sugli assi cartesiani.

  

---

  

## 5. Come si calcola il modulo di un vettore in due dimensioni?

  

Si usa la formula:

  

$$

a = \sqrt{a_x^2 + a_y^2}

$$

  

---

  

## 6. Come si calcola il modulo di un vettore in tre dimensioni?

  

Si usa la formula:

  

$$

v = \sqrt{v_x^2 + v_y^2 + v_z^2}

$$

  

---

  

## 7. Che cos’è il vettore nullo?

  

È un vettore con modulo zero.

  

In tre dimensioni si scrive:

  

$$

(0,0,0)

$$

  

---

  

## 8. Che cos’è il vettore opposto?

  

È un vettore con stesso modulo e stessa direzione, ma verso contrario.

  

Se:

  

$$

\vec{v} = (v_x, v_y, v_z)

$$

  

allora:

  

$$

-\vec{v} = (-v_x, -v_y, -v_z)

$$

  

---

  

# Frase chiave per l’esame

  

> Le grandezze vettoriali sono grandezze fisiche che, oltre al valore numerico e all’unità di misura, richiedono anche una direzione e un verso. I vettori vengono rappresentati mediante frecce e possono essere scomposti nelle loro componenti lungo gli assi cartesiani. Il modulo del vettore si calcola tramite il teorema di Pitagora applicato alle sue componenti.


## Somma vettoriale - Metodo grafico

## Contesto

Queste slide spiegano come si possono **sommare** e **sottrarre** i vettori usando un metodo geometrico, cioè un metodo basato sul disegno.

  L'idea principale è che i vettori possono essere spostati nel piano senza cambiare il loro significato fisico, purché rimangano invariati:

- il **modulo**;
- la **direzione**;
- il **verso**.

In altre parole, un vettore può essere traslato parallelamente a sé stesso e resta equivalente al vettore di partenza.

---  
##  Somma di due vettori con il metodo grafico

## Concetto generale

Il **vettore somma** è il vettore risultante dall'unione di due o più vettori.
Se abbiamo due vettori:
$$
\vec{v}
$$$$
\vec{w}

$$
la loro somma si indica così:

$$

\vec{v} + \vec{w}

$$

  Questo nuovo vettore rappresenta l'effetto complessivo dei due vettori applicati insieme.

---
## Metodo punta-coda
Per costruire graficamente la somma di due vettori si può usare il metodo **punta-coda**.
Il procedimento è questo:

1. Si disegna il primo vettore.

2. Si prende il secondo vettore e lo si trasla rigidamente.

3. Si porta la base del secondo vettore sulla punta del primo.

4. Il vettore somma parte dalla base del primo vettore e arriva alla punta del secondo.

In forma schematica:


```text

Primo vettore:       ----->

Secondo vettore:            ----->

Somma:              ----------->

```

  Più precisamente:

```text

Punto iniziale ── v ──> punta di v ── w ──> punta di w

  

Il vettore somma va dal punto iniziale alla punta finale.

```

  Quindi:
$$

\vec{v} + \vec{w}

$$

  è il vettore che collega l'origine del primo vettore con la punta del secondo vettore traslato.

---
## Cosa significa traslare un vettore

  Traslare un vettore significa spostarlo da un punto all'altro del piano senza ruotarlo e senza modificarne la lunghezza.

  Un vettore traslato mantiene:

  - lo stesso modulo;
- la stessa direzione;
- lo stesso verso.

Quindi, anche se graficamente lo spostiamo, il vettore rimane lo stesso.

  Questa proprietà è fondamentale perché permette di costruire somme e differenze in modo geometrico.

  ---
## Metodo del parallelogramma
## Come funziona

  Un altro modo per sommare due vettori è il **metodo del parallelogramma**.
In questo caso i due vettori vengono disegnati con la stessa origine.

Poi si costruisce un parallelogramma usando i due vettori come lati.

La diagonale del parallelogramma che parte dall'origine comune rappresenta il vettore somma.

Schema:

  

```text

       punta finale

          *

         /|

        / |

       /  |

      /   |

 origine *-------->

```

  

La diagonale che parte dall'origine rappresenta:

  

$$

\vec{v} + \vec{w}

$$

  

---

  

## Collegamento tra i due metodi

  

Il metodo punta-coda e il metodo del parallelogramma portano allo stesso risultato.

  

Infatti:

  

- nel metodo punta-coda si sposta il secondo vettore alla punta del primo;

- nel metodo del parallelogramma si costruisce una figura geometrica usando i due vettori come lati.

  

In entrambi i casi, il vettore risultante è quello che va dall'origine alla punta finale.

  

---

  

# Moltiplicazione di un vettore per un numero

  

## Definizione

  

Un vettore può essere moltiplicato per un numero reale, indicato spesso con:

  

$$

k

$$

  

Se abbiamo un vettore:

  

$$

\vec{v}

$$

  

e lo moltiplichiamo per un numero \(k\), otteniamo:

  

$$

k \vec{v}

$$

  

Questo significa che il vettore viene allungato, accorciato oppure invertito, a seconda del valore di \(k\).

  

---

  

## Effetti sul vettore

  

Quando un vettore viene moltiplicato per un numero \(k\), succede questo:

  

| Elemento | Cosa succede |

|---|---|

| **Modulo** | viene moltiplicato per \(k\), o meglio per \(|k|\) |

| **Direzione** | rimane invariata |

| **Verso** | resta uguale se \(k > 0\), si inverte se \(k < 0\) |

  

---

  

## Caso con numero positivo

  

Se \(k\) è positivo, il vettore mantiene lo stesso verso.

  

Esempio:

  

$$

3\vec{v}

$$

  

significa che il vettore \(\vec{v}\) viene moltiplicato per 3.

  

Quindi:

  

- il modulo diventa tre volte più grande;

- la direzione resta la stessa;

- il verso resta lo stesso.

  

Se il vettore originale era così:

  

```text

v:      ---->

```

  

allora:

  

```text

3v:     ------------>

```

  

Il vettore è più lungo, ma punta nella stessa direzione e nello stesso verso.

  

---

  

## Caso con numero negativo

  

Se \(k\) è negativo, il vettore cambia verso.

  

Esempio:

  

$$

-\vec{v}

$$

  

è il vettore opposto di \(\vec{v}\).

  

Se il vettore originale era:

  

```text

v:      ---->

```

  

allora il vettore opposto è:

  

```text

-v:     <----

```

  

Se invece abbiamo:

  

$$

-3\vec{v}

$$

  

il vettore:

  

- diventa tre volte più lungo;

- mantiene la stessa direzione;

- cambia verso.

  

---

  

# Differenza tra due vettori

  

## Concetto generale

  

La differenza tra due vettori si indica così:

  

$$

\vec{v} - \vec{w}

$$

  

Tuttavia, dal punto di vista geometrico, sottrarre un vettore equivale a sommare il suo opposto.

  

Quindi:

  

$$

\vec{v} - \vec{w} = \vec{v} + (-\vec{w})

$$

  

Questa è una formula molto importante.

  

Significa che, per costruire la differenza tra due vettori, non dobbiamo inventare un nuovo metodo: basta trasformare la sottrazione in una somma.

  

---

  

## Procedimento grafico per la differenza

  

Per costruire graficamente:

  

$$

\vec{v} - \vec{w}

$$

  

si procede così:

  

1. Si disegna il vettore \(\vec{v}\).

2. Si costruisce il vettore opposto di \(\vec{w}\), cioè \(-\vec{w}\).

3. Si somma \(\vec{v}\) con \(-\vec{w}\).

4. Il vettore risultante è la differenza.

  

Quindi:

  

```text

v - w = v + (-w)

```

  

---

  

# Differenza con il metodo del parallelogramma

  

## Diagonale della differenza

  

Nelle slide viene mostrato che il vettore differenza può essere ottenuto anche tramite un parallelogramma.

  

Nel caso della somma, la diagonale parte dall'origine comune.

  

Nel caso della differenza, invece, la diagonale non è quella che parte dall'origine, ma l'altra diagonale del parallelogramma.

  

La slide spiega che il vettore differenza è equivalente alla diagonale del parallelogramma costruito sui due vettori, ma applicata alla punta del vettore da sottrarre.

  

---

  

## Idea intuitiva

  

Se due vettori partono dalla stessa origine, la differenza tra loro può essere vista come il vettore che collega le loro punte.

  

Per esempio, se abbiamo due vettori:

  

$$

\vec{v}

$$

  

$$

\vec{w}

$$

  

con la stessa origine, il vettore differenza collega la punta di uno alla punta dell'altro.

  

Bisogna però fare attenzione al verso.

  

Il vettore:

  

$$

\vec{w} - \vec{v}

$$

  

va dalla punta di \(\vec{v}\) alla punta di \(\vec{w}\).

  

Il vettore:

  

$$

\vec{v} - \vec{w}

$$

  

va dalla punta di \(\vec{w}\) alla punta di \(\vec{v}\).

  

Quindi l'ordine della sottrazione è fondamentale.

  

---

  

# Esempio numerico semplice

  

Prendiamo due vettori in due dimensioni:

  

$$

\vec{v} = (5, 2)

$$

  

$$

\vec{w} = (3, 1)

$$

  

## Somma

  

La somma si ottiene sommando le componenti corrispondenti:

  

$$

\vec{v} + \vec{w} = (5 + 3, 2 + 1)

$$

  

$$

\vec{v} + \vec{w} = (8, 3)

$$

  

---

  

## Differenza

  

La differenza si ottiene sottraendo le componenti corrispondenti:

  

$$

\vec{v} - \vec{w} = (5 - 3, 2 - 1)

$$

  

$$

\vec{v} - \vec{w} = (2, 1)

$$

  

Oppure si può ragionare così:

  

$$

\vec{v} - \vec{w} = \vec{v} + (-\vec{w})

$$

  

Dato che:

  

$$

\vec{w} = (3, 1)

$$

  

allora:

  

$$

-\vec{w} = (-3, -1)

$$

  

Quindi:

  

$$

\vec{v} + (-\vec{w}) = (5, 2) + (-3, -1)

$$

  

$$

\vec{v} + (-\vec{w}) = (2, 1)

$$

  

Il risultato è lo stesso.

  

---

  

# Attenzione: somma vettoriale e somma normale non sono la stessa cosa

  

Quando si sommano due numeri, basta fare una somma algebrica.

  

Per esempio:

  

$$

3 + 4 = 7

$$

  

Con i vettori, invece, bisogna considerare anche direzione e verso.

  

Due vettori di modulo 3 e 4 non danno sempre un vettore di modulo 7.

  

Il risultato dipende dall'angolo tra i due vettori.

  

Esempi:

  

| Situazione | Risultato |

|---|---|

| Stessa direzione e stesso verso | i moduli si sommano |

| Stessa direzione ma verso opposto | i moduli si sottraggono |

| Direzioni perpendicolari | si usa Pitagora |

| Direzioni qualsiasi | si costruisce graficamente o si usano formule più avanzate |

  

---

  

# Frase da ricordare per l'esame

  

La somma vettoriale può essere costruita graficamente traslando rigidamente il secondo vettore in modo che la sua base coincida con la punta del primo. Il vettore somma è quello che unisce la base del primo vettore con la punta del secondo. In alternativa, se i due vettori hanno la stessa origine, il vettore somma è la diagonale del parallelogramma costruito sui due vettori. La differenza tra due vettori si ottiene sommando al primo vettore l'opposto del secondo.

  

---

  

# Mini domande da esame

  

## 1. Come si costruisce graficamente la somma di due vettori?

  

Si trasla il secondo vettore in modo che la sua base coincida con la punta del primo. Il vettore somma va dalla base del primo alla punta del secondo.

  

---

  

## 2. Che cos'è il metodo punta-coda?

  

È un metodo grafico per sommare vettori. Consiste nel disporre i vettori uno dopo l'altro, mettendo la coda del secondo sulla punta del primo.

  

---

  

## 3. Che cos'è il metodo del parallelogramma?

  

È un metodo grafico in cui due vettori vengono disegnati con la stessa origine. Il vettore somma è la diagonale del parallelogramma costruito sui due vettori.

  

---

  

## 4. Cosa succede se moltiplico un vettore per un numero positivo?

  

Il modulo cambia in proporzione al numero, ma direzione e verso restano invariati.

  

---

  

## 5. Cosa succede se moltiplico un vettore per un numero negativo?

  

Il modulo cambia in proporzione al valore assoluto del numero, la direzione resta la stessa, ma il verso si inverte.

  

---

  

## 6. Come si calcola la differenza tra due vettori?

  

La differenza si calcola sommando al primo vettore l'opposto del secondo:

  

$$

\vec{v} - \vec{w} = \vec{v} + (-\vec{w})

$$

  

---

  

## 7. Perché un vettore può essere traslato?

  

Perché un vettore rimane equivalente se mantiene lo stesso modulo, la stessa direzione e lo stesso verso.

  

---

  

# Schema finale

  

| Operazione | Significato | Metodo grafico |

|---|---|---|

| Somma | effetto complessivo di due vettori | metodo punta-coda o parallelogramma |

| Moltiplicazione per \(k\) | cambia il modulo del vettore | il vettore si allunga, si accorcia o cambia verso |

| Differenza | somma con l'opposto del secondo vettore | \(\vec{v} - \vec{w} = \vec{v} + (-\vec{w})\) |

  

---

  

# Riassunto super semplice

  

Un vettore può essere spostato nel piano senza cambiare, se restano uguali modulo, direzione e verso.

  

Per sommare due vettori, metto la coda del secondo sulla punta del primo. Il vettore risultante va dall'inizio del primo alla fine del secondo.

  

Per sottrarre due vettori, trasformo la sottrazione in una somma:

  

$$

\vec{v} - \vec{w} = \vec{v} + (-\vec{w})

$$

  

Quindi sottrarre un vettore significa sommare il suo opposto.à

## Somma vettoriale - Altre proprietà

La somma vettoriale gode di due proprietà importanti: la proprietà commutativa e la proprietà associativa.

## Proprietà commutativa

La proprietà commutativa dice che l’ordine con cui sommiamo due vettori non cambia il risultato finale.

In formula:
$$

   \vec{a} + \vec{b} = \vec{b} + \vec{a}

$$
Questo significa che, se sommo prima il vettore $\vec{a}$ e poi il vettore $\vec{b}$, ottengo lo stesso vettore risultante che avrei ottenuto sommando prima $\vec{b}$ e poi $\vec{a}$.

In pratica, il risultato finale della somma non dipende dall’ordine dei vettori.

Esempio intuitivo:

Se mi sposto prima di 3 metri verso destra e poi di 2 metri verso l’alto, arrivo nello stesso punto in cui arriverei facendo prima 2 metri verso l’alto e poi 3 metri verso destra.

Il percorso seguito è diverso, ma lo spostamento finale è lo stesso.

## Proprietà associativa

La proprietà associativa dice che, quando sommiamo più vettori, possiamo raggrupparli come vogliamo senza cambiare il risultato finale.

In formula:

$$
\vec{a} + (\vec{b}+\vec{c}) = (\vec{a}+\vec{b})+\vec{c}
$$

Questo significa che posso sommare prima $\vec{b}$ e $\vec{c}$, e poi aggiungere $\vec{a}$, oppure posso sommare prima $\vec{a}$ e $\vec{b}$, e poi aggiungere $\vec{c}$.

Il vettore risultante finale sarà sempre lo stesso.
## Somma grafica di più vettori
Il metodo grafico della somma vettoriale può essere esteso anche a più di due vettori.
Si usa il metodo punta-coda.

Significa che si disegnano i vettori uno dopo l’altro, mettendo la coda del vettore successivo sulla punta del vettore precedente.

Per esempio, se devo sommare:
$$
\vec{u} + \vec{v} + \vec{w} + \vec{z}u+v+w+z
$$

disegno prima $\vec{u}$, poi dalla punta di $\vec{u}$ faccio partire $\vec{v}$, poi dalla punta di $\vec{v}$ faccio partire $\vec{w}$, e infine dalla punta di $\vec{w}$ faccio partire $\vec{z}$.

Il vettore risultante è il vettore che parte dalla coda del primo vettore e arriva alla punta dell’ultimo vettore.

Quindi:

R⃗=u⃗+v⃗+w⃗+z⃗\vec{R} = \vec{u} + \vec{v} + \vec{w} + \vec{z}R=u+v+w+z

Dove $\vec{R}$ è il vettore risultante.

La cosa importante da ricordare è questa:

La somma di più vettori non è data dalla somma delle lunghezze dei vettori, ma dallo spostamento complessivo che si ottiene mettendoli uno dopo l’altro.

# Somma di due spostamenti su rette diverse

La seconda slide parla della somma risultante di due spostamenti su rette diverse.

Quando due vettori rappresentano due spostamenti con direzioni diverse, la loro somma non si ottiene semplicemente sommando i moduli.

Bisogna considerare anche la direzione e il verso dei vettori.

Per trovare il vettore risultante si possono usare due metodi grafici:

1. metodo punta-coda;
2. regola del parallelogramma.

## Metodo punta-coda

Nel metodo punta-coda si considera che gli spostamenti siano consecutivi.

Questo significa che il secondo vettore inizia dove finisce il primo.

Si prende quindi la coda del secondo vettore e la si mette sulla punta del primo vettore.

Il vettore risultante è quello che va dal punto iniziale del primo vettore al punto finale del secondo vettore.

Nella slide si vede questa situazione:

OA→+AB→=OB→\overrightarrow{OA} + \overrightarrow{AB} = \overrightarrow{OB}OA+AB=OB

Il primo spostamento va da $O$ ad $A$.

Il secondo spostamento va da $A$ a $B$.

Lo spostamento risultante va direttamente da $O$ a $B$.

Quindi, invece di descrivere il percorso spezzato $O \rightarrow A \rightarrow B$, posso descrivere lo spostamento totale con un solo vettore:

OB→\overrightarrow{OB}OB

Questo vettore rappresenta lo spostamento complessivo.

## Regola del parallelogramma

La regola del parallelogramma si usa quando i due vettori hanno la stessa origine.

In questo caso si disegnano i due vettori che partono dallo stesso punto.

Poi si costruisce un parallelogramma usando i due vettori come lati.

La somma dei due vettori è la diagonale del parallelogramma che parte dall’origine comune.

Questa diagonale rappresenta il vettore risultante.

In formula:

s⃗=s1⃗+s2⃗\vec{s} = \vec{s_1} + \vec{s_2}s=s1​​+s2​​

Dove:

$\vec{s_1}$ è il primo spostamento.

$\vec{s_2}$ è il secondo spostamento.

$\vec{s}$ è lo spostamento risultante.

La diagonale del parallelogramma rappresenta quindi lo spostamento totale prodotto dai due vettori.

## Differenza tra i due metodi

Il metodo punta-coda e la regola del parallelogramma portano allo stesso risultato.

La differenza è solo nel modo in cui vengono disegnati i vettori.

Nel metodo punta-coda, i vettori sono messi uno dopo l’altro.

Nella regola del parallelogramma, i vettori partono dalla stessa origine.

In entrambi i casi, il vettore risultante rappresenta lo spostamento complessivo.

# Esercizi sui vettori

## Esercizio 1: modulo e somma di due vettori tramite componenti

### Testo dell’esercizio

Si trovino modulo, direzione e verso dei vettori `a`, `b` e `a+b`, sapendo che le componenti sono:

$$
a_x=-4m
$$

$$
a_y=-7m
$$

$$
b_x=3m
$$

$$
b_y=-2m
$$

![[Pasted image 20260502115427.png]]

---

## Dati

Il vettore `a` ha componenti:

$$
\vec{a}=(-4,-7)
$$

Il vettore `b` ha componenti:

$$
\vec{b}=(3,-2)
$$

---

## Significato delle componenti

Il vettore `a` ha:

$$
a_x=-4
$$

quindi si sposta di 4 metri verso sinistra.

Ha anche:

$$
a_y=-7
$$

quindi si sposta di 7 metri verso il basso.

Per questo il vettore `a` si trova nel terzo quadrante.

Il vettore `b` ha:

$$
b_x=3
$$

quindi si sposta di 3 metri verso destra.

Ha anche:

$$
b_y=-2
$$

quindi si sposta di 2 metri verso il basso.

Per questo il vettore `b` si trova nel quarto quadrante.

---

## Calcolo del modulo del vettore a

Il modulo di un vettore si calcola con il teorema di Pitagora:

$$
|\vec{a}|=\sqrt{a_x^2+a_y^2}
$$

Sostituisco i valori:

$$
|\vec{a}|=\sqrt{(-4)^2+(-7)^2}
$$

$$
|\vec{a}|=\sqrt{16+49}
$$

$$
|\vec{a}|=\sqrt{65}
$$

$$
|\vec{a}|=8,06m
$$

Quindi il modulo del vettore `a` è:

$$
|\vec{a}|=8,06m
$$

Il modulo è sempre positivo, perché rappresenta una lunghezza.

---

## Calcolo del modulo del vettore b

Anche per il vettore `b` si usa la stessa formula:

$$
|\vec{b}|=\sqrt{b_x^2+b_y^2}
$$

Sostituisco i valori:

$$
|\vec{b}|=\sqrt{3^2+(-2)^2}
$$

$$
|\vec{b}|=\sqrt{9+4}
$$

$$
|\vec{b}|=\sqrt{13}
$$

$$
|\vec{b}|=3,61m
$$

Quindi il modulo del vettore `b` è:

$$
|\vec{b}|=3,61m
$$

Nella slide sembra indicato un valore leggermente diverso, ma usando le componenti `3` e `-2` il risultato corretto è circa `3,61m`.

---

## Somma dei vettori

Per sommare due vettori si sommano separatamente le componenti lungo x e lungo y.

La somma è:

$$
\vec{s}=\vec{a}+\vec{b}
$$

La componente x del vettore somma è:

$$
s_x=a_x+b_x
$$

Sostituisco:

$$
s_x=-4+3
$$

$$
s_x=-1
$$

La componente y del vettore somma è:

$$
s_y=a_y+b_y
$$

Sostituisco:

$$
s_y=-7+(-2)
$$

$$
s_y=-9
$$

Quindi il vettore somma è:

$$
\vec{s}=(-1,-9)
$$

Questo significa che il vettore risultante si sposta di 1 metro verso sinistra e di 9 metri verso il basso.

---

## Calcolo del modulo del vettore somma

Il modulo del vettore somma si calcola ancora con Pitagora:

$$
|\vec{s}|=\sqrt{s_x^2+s_y^2}
$$

Sostituisco:

$$
|\vec{s}|=\sqrt{(-1)^2+(-9)^2}
$$

$$
|\vec{s}|=\sqrt{1+81}
$$

$$
|\vec{s}|=\sqrt{82}
$$

$$
|\vec{s}|=9,05m
$$

Quindi il modulo del vettore somma è:

$$
|\vec{s}|=9,05m
$$

---

## Direzione e verso del vettore a

Il vettore `a` ha entrambe le componenti negative:

$$
a_x=-4
$$

$$
a_y=-7
$$

Quindi punta verso sinistra e verso il basso.

Per questo si trova nel terzo quadrante.

Il suo verso è verso il basso a sinistra.

---

## Direzione e verso del vettore b

Il vettore `b` ha componente x positiva e componente y negativa:

$$
b_x=3
$$

$$
b_y=-2
$$

Quindi punta verso destra e verso il basso.

Per questo si trova nel quarto quadrante.

Il suo verso è verso il basso a destra.

---

## Direzione e verso del vettore somma

Il vettore somma è:

$$
\vec{s}=(-1,-9)
$$

Ha componente x negativa e componente y negativa.

Quindi punta verso sinistra e verso il basso.

Si trova nel terzo quadrante.

Poiché la componente y vale `-9` ed è molto più grande della componente x, che vale solo `-1`, il vettore risultante è quasi verticale verso il basso, ma leggermente inclinato verso sinistra.

---

## Spiegazione fisica del risultato

Le componenti orizzontali dei due vettori sono:

$$
a_x=-4
$$

$$
b_x=3
$$

Una va verso sinistra e l’altra verso destra, quindi si compensano quasi del tutto:

$$
-4+3=-1
$$

Le componenti verticali invece sono entrambe negative:

$$
a_y=-7
$$

$$
b_y=-2
$$

Quindi entrambe puntano verso il basso e si sommano:

$$
-7+(-2)=-9
$$

Per questo la risultante punta quasi tutta verso il basso.

---

## Risultati finali

Il vettore `a` è:

$$
\vec{a}=(-4,-7)
$$

Il suo modulo è:

$$
|\vec{a}|=8,06m
$$

Il vettore `b` è:

$$
\vec{b}=(3,-2)
$$

Il suo modulo è:

$$
|\vec{b}|=3,61m
$$

Il vettore somma è:

$$
\vec{s}=\vec{a}+\vec{b}=(-1,-9)
$$

Il suo modulo è:

$$
|\vec{s}|=9,05m
$$

---

## Frase da ricordare

Per sommare due vettori si sommano le rispettive componenti cartesiane. Il modulo di un vettore si calcola con il teorema di Pitagora, considerando le componenti come i cateti di un triangolo rettangolo.

---

# Esercizio 2: trovare le componenti di un vettore conoscendo modulo e angolo

## Testo dell’esercizio

Si trovino le componenti x e y di un vettore che giace sul piano xy, ha modulo `a` e forma un angolo `θ` con l’asse x.

---

## Dati

Il modulo del vettore è:

$$
a=10m
$$

L’angolo con l’asse x è:

$$
\theta=30^\circ
$$

Bisogna trovare:

$$
a_x
$$

e

$$
a_y
$$

cioè le componenti del vettore lungo l’asse x e lungo l’asse y.


![[Pasted image 20260502115458.png]]
---

## Significato del disegno

Nel disegno il vettore parte dall’origine e punta verso l’alto a destra.

Quindi si trova nel primo quadrante.

Il vettore può essere scomposto in due componenti:

$$
a_x
$$

che è la componente orizzontale lungo l’asse x,

e

$$
a_y
$$

che è la componente verticale lungo l’asse y.

Graficamente si forma un triangolo rettangolo.

Il vettore `a` è l’ipotenusa.

La componente `a_x` è il cateto orizzontale.

La componente `a_y` è il cateto verticale.

---

## Formule da usare

Quando conosci il modulo del vettore e l’angolo con l’asse x, puoi trovare le componenti usando seno e coseno.

La componente lungo x si trova con il coseno:

$$
a_x=a\cos\theta
$$

La componente lungo y si trova con il seno:

$$
a_y=a\sin\theta
$$

Si usa il coseno per la componente x perché `a_x` è il cateto vicino all’angolo.

Si usa il seno per la componente y perché `a_y` è il cateto opposto all’angolo.

---

## Calcolo della componente x

Parto dalla formula:

$$
a_x=a\cos\theta
$$

Sostituisco i valori:

$$
a_x=10\cos(30^\circ)
$$

Il coseno di 30° vale circa:

$$
\cos(30^\circ)=0,866
$$

Quindi:

$$
a_x=10\cdot0,866
$$

$$
a_x=8,66m
$$

La componente orizzontale del vettore è:

$$
a_x=8,66m
$$

---

## Calcolo della componente y

Parto dalla formula:

$$
a_y=a\sin\theta
$$

Sostituisco i valori:

$$
a_y=10\sin(30^\circ)
$$

Il seno di 30° vale:

$$
\sin(30^\circ)=0,5
$$

Quindi:

$$
a_y=10\cdot0,5
$$

$$
a_y=5m
$$

La componente verticale del vettore è:

$$
a_y=5m
$$

---

## Risultato finale

Il vettore ha componenti:

$$
a_x=8,66m
$$

$$
a_y=5m
$$

Quindi il vettore si può scrivere come:

$$
\vec{a}=(8,66;\ 5)
$$

---

## Interpretazione fisica

Il vettore totale misura 10 metri ed è inclinato di 30° rispetto all’asse x.

Questo vettore può essere visto come la somma di due spostamenti:

uno spostamento orizzontale di `8,66m` verso destra;

uno spostamento verticale di `5m` verso l’alto.

Questi due spostamenti insieme formano il vettore inclinato iniziale.

---

## Perché le componenti sono positive

Il vettore si trova nel primo quadrante.

Nel primo quadrante la componente x è positiva e la componente y è positiva.

Quindi:

$$
a_x>0
$$

$$
a_y>0
$$

Se il vettore fosse stato in un altro quadrante, una o entrambe le componenti sarebbero potute essere negative.

---

## Controllo con Pitagora

Possiamo verificare il risultato usando il teorema di Pitagora.

Il modulo del vettore deve essere:

$$
a=\sqrt{a_x^2+a_y^2}
$$

Sostituisco:

$$
a=\sqrt{8,66^2+5^2}
$$

$$
a=\sqrt{74,99+25}
$$

$$
a=\sqrt{99,99}
$$

$$
a\approx10m
$$

Il risultato torna, quindi le componenti trovate sono corrette.

---

## Frase da ricordare

Quando sono noti il modulo di un vettore e l’angolo che esso forma con l’asse x, le componenti cartesiane si ricavano usando seno e coseno. La componente lungo x si ottiene moltiplicando il modulo per il coseno dell’angolo, mentre la componente lungo y si ottiene moltiplicando il modulo per il seno dell’angolo.

---
## Schema rapido

Se l’angolo è misurato rispetto all’asse x:

$$
a_x=a\cos\theta
$$

$$
a_y=a\sin\theta
$$

Nel nostro caso:

$$
a_x=10\cos(30^\circ)=8,66m
$$

$$
a_y=10\sin(30^\circ)=5m
$$

Quindi:

$$
\vec{a}=(8,66;\ 5)
$$

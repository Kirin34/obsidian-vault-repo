## Sistema di punti materiali

Finora abbiamo studiato la dinamica di un singolo punto materiale.  
Ora si passa allo studio di un **sistema di punti materiali**, cioè un insieme di punti che possono interagire:

- con l’ambiente esterno;
- tra loro, tramite **forze interne**.

Per ogni punto $i$ del sistema vale una relazione del tipo:

$$
m_i \vec a_i = \sum_j \vec F_{ij} + \vec R_i^{(e)}
$$

dove:

- $m_i \vec a_i$ è la risultante dinamica sul punto $i$;
- $\vec F_{ij}$ sono le forze interne esercitate dagli altri punti $j$ sul punto $i$;
- $\vec R_i^{(e)}$ è la risultante delle forze esterne agenti sul punto $i$.

Quindi ogni punto del sistema è influenzato sia dalle forze interne al sistema, sia dalle forze esterne.

---

## Centro di massa

Nel sistema di punti materiali si definisce un punto particolare chiamato **centro di massa**.

Per un sistema formato da più punti materiali, ciascuno con massa $m_i$ e posizione $\vec r_i$, la posizione del centro di massa è:

$$
\vec r_{cm} =
\frac{\sum_i m_i \vec r_i}{\sum_i m_i}
=
\frac{\sum_i m_i \vec r_i}{M}
$$

dove:

$$
M = \sum_i m_i
$$

è la massa totale del sistema.

Il centro di massa rappresenta una specie di “posizione media pesata” del sistema: i punti con massa maggiore influenzano di più la sua posizione.

Nota importante:

- la posizione assoluta del centro di massa cambia se cambio sistema di riferimento;
- però la posizione relativa dei punti rispetto al centro di massa resta invariata.

---

## Grandezze dinamiche del sistema

Alcune grandezze dinamiche globali del sistema si ottengono sommando i contributi dei singoli punti.

### Quantità di moto totale

La **quantità di moto totale** del sistema è:

$$
\vec P = \sum_i \vec p_i = \sum_i m_i \vec v_i
$$

dove:

- $\vec p_i = m_i \vec v_i$ è la quantità di moto del singolo punto;
- $\vec P$ è la quantità di moto totale del sistema.

Quindi la quantità di moto totale è la somma vettoriale delle quantità di moto di tutti i punti.

---

### Energia cinetica totale

L’**energia cinetica totale** del sistema è:

$$
K_{tot} = \sum_i K_i = \sum_i \frac{1}{2}m_i v_i^2
$$

Quindi l’energia cinetica totale si ottiene sommando le energie cinetiche dei singoli punti materiali.

---

## Idee chiave

Un sistema di punti materiali è formato da più punti che interagiscono tra loro e con l’esterno.

Le forze interne sono quelle che i punti del sistema si scambiano tra loro.

Le forze esterne sono quelle esercitate dall’ambiente sul sistema.

Il centro di massa è il punto che descrive la posizione media del sistema, tenendo conto delle masse.

Le grandezze dinamiche globali, come quantità di moto totale ed energia cinetica totale, si ottengono sommando i contributi dei singoli punti.


## Teorema del moto del centro di massa

Derivando la quantità di moto totale del sistema si ottiene una relazione simile alla seconda legge di Newton, ma applicata al **centro di massa**.

Partiamo dalla quantità di moto totale:

$$
\vec P = \sum_i m_i \vec v_i
$$

Derivando rispetto al tempo:

$$
\frac{d\vec P}{dt}
=
\sum_i m_i \frac{d\vec v_i}{dt}
=
\sum_i m_i \vec a_i
$$

Poiché il centro di massa rappresenta il moto globale del sistema:

$$
\frac{d\vec P}{dt} = M \vec a_{cm}
$$

dove:

- $M$ è la massa totale del sistema;
- $\vec a_{cm}$ è l’accelerazione del centro di massa.

---

## Ruolo delle forze interne ed esterne

Per ogni punto materiale agiscono:

- forze interne, dovute agli altri punti del sistema;
- forze esterne, dovute all’ambiente esterno.

Nel sistema complessivo, però, le **forze interne si annullano a coppie** per il terzo principio della dinamica:

$$
\vec F_{ij} = -\vec F_{ji}
$$

Quindi, sommando le equazioni di tutti i punti, rimane solo la risultante delle forze esterne:

$$
\frac{d\vec P}{dt} = M \vec a_{cm} = \vec R^{(e)}
$$

Questa è la formula principale del **teorema del moto del centro di massa**.

---

## Significato fisico

Il teorema dice che il centro di massa di un sistema si muove come se:

- tutta la massa del sistema fosse concentrata nel centro di massa;
- su questa massa agisse solo la risultante delle forze esterne.

Quindi:

$$
M \vec a_{cm} = \vec R^{(e)}
$$

Le forze interne possono modificare il moto dei singoli punti del sistema, ma non modificano il moto complessivo del centro di massa.

---

## Idea chiave

Il moto globale di un sistema di punti materiali dipende solo dalle forze esterne.

Le forze interne influenzano il moto relativo dei punti tra loro, ma non cambiano il moto del centro di massa.

## Sistema di riferimento del centro di massa

Consideriamo un sistema di punti materiali in un sistema di riferimento inerziale $R(Oxyz)$.

Il centro di massa occupa nel tempo la posizione:

$$
\vec r_{cm}(t) = (x_{cm}(t), y_{cm}(t), z_{cm}(t))
$$

Si definisce **sistema di riferimento del centro di massa** il riferimento:

$$
R_{cm}(Cx'y'z')
$$

che ha:

- origine nel centro di massa $C$;
- assi paralleli a quelli del sistema $R$.

Quindi il sistema $R_{cm}$ si ottiene dal sistema inerziale $R$ tramite una **traslazione**, senza rotazione degli assi.

---

## Relazione tra le coordinate nei due riferimenti

La posizione del punto $i$ nel riferimento inerziale è:

$$
\vec r_i = \vec r'_i + \vec r_{cm}
$$

dove:

- $\vec r_i$ è la posizione nel sistema inerziale;
- $\vec r'_i$ è la posizione rispetto al centro di massa;
- $\vec r_{cm}$ è la posizione del centro di massa.

Poiché non c’è rotazione relativa tra i due sistemi, anche le velocità sono legate da:

$$
\vec v_i = \vec v'_i + \vec v_{cm}
$$

---

## Quantità di moto nel sistema del centro di massa

Nel riferimento del centro di massa, la quantità di moto totale è:

$$
\vec P' = \sum_i m_i \vec v'_i
$$

Usando la relazione tra le velocità:

$$
\vec P' = \sum_i m_i \vec v_i - M \vec v_{cm}
$$

Ma sappiamo che:

$$
\vec P = M \vec v_{cm}
$$

quindi:

$$
\vec P' = 0
$$

Questo significa che nel riferimento del centro di massa la quantità di moto totale del sistema è nulla.

In pratica, nel sistema del centro di massa il sistema complessivo è come se fosse fermo, anche se i singoli punti possono muoversi tra loro.

---

## Sistema inerziale o non inerziale

Il sistema del centro di massa non è sempre inerziale.

È inerziale solo se la risultante delle forze esterne è nulla:

$$
\vec R^{(e)} = 0
$$

In questo caso:

$$
\frac{d\vec P}{dt} = 0
$$

quindi la quantità di moto totale è costante e anche la velocità del centro di massa è costante.

---

## Teorema di Koenig

Il **teorema di Koenig** permette di scrivere l’energia cinetica totale di un sistema come somma di due contributi:

1. energia cinetica del moto del centro di massa;
2. energia cinetica interna, cioè rispetto al centro di massa.

Partiamo dall’energia cinetica totale:

$$
K = \sum_i \frac{1}{2} m_i v_i^2
$$

Dato che:

$$
\vec v_i = \vec v'_i + \vec v_{cm}
$$

allora:

$$
K =
\sum_i \frac{1}{2} m_i (\vec v'_i + \vec v_{cm})^2
$$

Sviluppando:

$$
K =
\sum_i \frac{1}{2} m_i v_i'^2
+
\frac{1}{2} M v_{cm}^2
+
\sum_i m_i \vec v'_i \cdot \vec v_{cm}
$$

L’ultimo termine è nullo perché nel sistema del centro di massa:

$$
\sum_i m_i \vec v'_i = 0
$$

Quindi rimane:

$$
K =
\sum_i \frac{1}{2} m_i v_i'^2
+
\frac{1}{2} M v_{cm}^2
$$

Ponendo:

$$
K' = \sum_i \frac{1}{2} m_i v_i'^2
$$

si ottiene la formula finale:

$$
K = K' + \frac{1}{2} M v_{cm}^2
$$

---

## Significato fisico

L’energia cinetica totale del sistema è data da:

$$
K = K' + \frac{1}{2} M v_{cm}^2
$$

dove:

- $K'$ è l’energia cinetica dei punti rispetto al centro di massa;
- $\frac{1}{2} M v_{cm}^2$ è l’energia cinetica che avrebbe il sistema se tutta la massa fosse concentrata nel centro di massa.

Quindi il moto totale si può separare in:

- **moto interno** dei punti rispetto al centro di massa;
- **moto globale** del centro di massa.

## Sistema di due punti

Studiamo il caso più semplice di sistema di punti materiali: un sistema formato da **due corpi** non soggetti a forze esterne.

In questo caso agiscono solo le forze interne tra i due corpi, cioè forze uguali e opposte per il terzo principio della dinamica:

$$
\vec F_{12} = -\vec F_{21}
$$

Poiché non ci sono forze esterne:

$$
\vec R^{(e)} = 0
$$

allora il sistema del centro di massa è inerziale e il centro di massa si muove di moto rettilineo uniforme, oppure resta fermo se scelgo il riferimento del centro di massa.

Nel riferimento del centro di massa vale:

$$
m_1 \vec r_1 = -m_2 \vec r_2
$$

Questo significa che i due corpi stanno da parti opposte rispetto al centro di massa $C$, e quello con massa maggiore si trova più vicino al centro di massa.

---

## Forze centrali

Per simmetria, le forze tra i due corpi sono **forze centrali**, cioè dirette lungo la congiungente dei due punti.

La dinamica dei due corpi può essere studiata tramite il moto relativo tra essi.

Si introduce la posizione relativa:

$$
\vec R = \vec r_2 - \vec r_1
$$

Il problema dei due corpi può essere trasformato in un problema equivalente con un solo corpo di massa:

$$
\mu = \frac{m_1 m_2}{m_1 + m_2}
$$

dove $\mu$ si chiama **massa ridotta**.

L’equazione del moto relativo diventa:

$$
\mu \vec a_{rel} = \vec F
$$

oppure:

$$
\mu \frac{d^2 \vec R}{dt^2} = \vec F
$$

---

## Massa ridotta

La massa ridotta è:

$$
\mu = \frac{m_1 m_2}{m_1 + m_2}
$$

Serve a semplificare il problema dei due corpi.

In pratica, invece di studiare direttamente il moto di entrambi i corpi, posso studiare il moto relativo come se:

- un corpo fosse fermo;
- l’altro corpo si muovesse con massa equivalente $\mu$.

---

## Idea chiave

Nel sistema di due punti senza forze esterne, il centro di massa non accelera.

Il moto complessivo si può separare in:

- moto del centro di massa;
- moto relativo dei due corpi.

Il moto relativo può essere trattato come il moto di un solo punto materiale con massa ridotta $\mu$.
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
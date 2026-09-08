## Corpo rigido

Un **corpo rigido** è un sistema di punti materiali nel quale le distanze reciproche tra i punti rimangono **costanti nel tempo**.

Il moto generale di un corpo rigido può essere visto come la combinazione di:

- **traslazione** del centro di massa;
- **rotazione** attorno a un asse istantaneo.

Per descrivere completamente il moto nello spazio servono **6 gradi di libertà**:
- 3 coordinate per individuare il centro di massa;
- 3 angoli per descrivere l'orientamento e la rotazione del corpo.

---

## Equazioni cardinali della dinamica

La dinamica di un corpo rigido è descritta dalle due **equazioni cardinali**:

$$
\vec F_{\text{ext}} = \frac{d\vec p}{dt} = M\vec a_{CM}
$$

$$
\vec M_{\text{ext}} = \frac{d\vec L}{dt}
$$

dove:

- $\vec F_{\text{ext}}$ = risultante delle forze esterne;
- $\vec p$ = quantità di moto totale;
- $M$ = massa totale;
- $\vec a_{CM}$ = accelerazione del centro di massa;
- $\vec M_{\text{ext}}$ = momento risultante delle forze esterne;
- $\vec L$ = momento angolare.

> Le **forze interne** non compaiono nelle equazioni cardinali perché i loro effetti si compensano.

### Significato fisico

- La **prima equazione** descrive la **traslazione** del corpo attraverso il moto del centro di massa.
- La **seconda equazione** descrive la **rotazione** del corpo.

---

## Corpo rigido continuo e densità

Per un corpo continuo la massa è distribuita all'interno del suo volume.

Considerando un elemento infinitesimo di volume $dV$ con massa $dm$, si definisce la **densità volumica**:

$$
\rho(\vec r)=\frac{dm}{dV}
$$

quindi:

$$
dm=\rho(\vec r)dV
$$

La massa totale del corpo è:

$$
M=\int_V dm=\int_V \rho(\vec r)\,dV
$$

Se il corpo è **omogeneo**, la densità è costante:

$$
\rho=\frac{M}{V}
$$

---

## Centro di massa di un corpo continuo

Per una distribuzione volumica:

$$
\vec r_{CM}
=
\frac{\int_V \vec r\,\rho(\vec r)\,dV}
{\int_V \rho(\vec r)\,dV}
$$

Poiché:

$$
M=\int_V \rho(\vec r)\,dV
$$

si può scrivere:

$$
\vec r_{CM}
=
\frac{1}{M}
\int_V \vec r\,\rho(\vec r)\,dV
$$

### Corpo omogeneo

Se $\rho$ è costante:

$$
\vec r_{CM}=\frac{1}{V}\int_V \vec r\,dV
$$

Quindi, per un corpo omogeneo, il **centro di massa coincide con il centro geometrico** quando la geometria del corpo presenta la necessaria simmetria.

Esempio: per una **sfera omogenea**, il centro di massa coincide con il centro della sfera.

---

## Densità superficiale e lineare

Se la massa è distribuita su una **superficie**:

$$
\sigma=\frac{dm}{dS}
$$

e il centro di massa è:

$$
\vec r_{CM}=\frac{1}{M}\int_S \vec r\,\sigma\,dS
$$

Se invece la massa è distribuita lungo una **linea**:

$$
\lambda=\frac{dm}{dl}
$$

e:

$$
\vec r_{CM}=\frac{1}{M}\int_L \vec r\,\lambda\,dl
$$

---

## Da ricordare

- Corpo rigido → distanze interne costanti.
- Moto generale → **traslazione + rotazione**.
- Traslazione → $\vec F_{\text{ext}}=M\vec a_{CM}$.
- Rotazione → $\vec M_{\text{ext}}=d\vec L/dt$.
- Densità volumica → $\rho=dm/dV$.
- Densità superficiale → $\sigma=dm/dS$.
- Densità lineare → $\lambda=dm/dl$.
- Nei corpi omogenei e simmetrici, il centro di massa coincide con il **centro geometrico**.
## Equilibrio del corpo rigido

Un corpo rigido è in **equilibrio statico** quando, se inizialmente fermo, rimane fermo.

Dalle equazioni cardinali, per avere equilibrio devono essere soddisfatte contemporaneamente due condizioni:

$$
\sum \vec F_{\text{ext}}=0
$$

$$
\sum \vec M_{\text{ext}}=0
$$

Quindi:

- risultante delle **forze esterne nulla** → nessuna accelerazione traslatoria;
- risultante dei **momenti esterni nulla** → nessuna accelerazione rotazionale.

Equivalentemente, se il corpo parte da fermo:

$$
\vec P=0
$$

$$
\vec L=0
$$

dove $\vec P$ è la quantità di moto totale e $\vec L$ il momento angolare.

> Per l'equilibrio non basta che il corpo non trasli: bisogna anche impedire che inizi a ruotare.

---

## Baricentro

Consideriamo un sistema sottoposto a più **forze parallele** $\vec f_i$.

L'intero sistema di forze può essere sostituito da una sola forza risultante:

$$
\vec F=\sum_i \vec f_i
$$

applicata in un punto $C$, detto **centro delle forze parallele**, la cui posizione è:

$$
\vec r_C=
\frac{\sum_i \vec r_i f_i}
{\sum_i f_i}
$$

### Caso della forza peso

Nel campo gravitazionale:

$$
f_i=m_i g
$$

perciò:

$$
\vec r_C=
\frac{\sum_i \vec r_i m_i g}
{\sum_i m_i g}
$$

Essendo $g$ uguale per tutti i punti:

$$
\vec r_C=
\frac{\sum_i \vec r_i m_i}
{\sum_i m_i}
=\vec r_{CM}
$$

Quindi:

> Nel campo gravitazionale uniforme il **baricentro coincide con il centro di massa**.

Di conseguenza possiamo considerare la forza peso totale:

$$
\vec P=M\vec g
$$

come se fosse interamente applicata nel centro di massa.

---

## Equilibrio di un corpo rigido in gravità

Consideriamo un corpo appoggiato su un piano.

Sul corpo agiscono principalmente:

- il **peso** $\vec P$, applicato al centro di massa;
- la **reazione vincolare** $\vec R$ esercitata dalla superficie di appoggio.

### Condizione di stabilità

Se la **verticale passante per il centro di massa cade all'interno della superficie di appoggio**, la reazione del piano può bilanciare il peso.

Si ha quindi:

$$
\sum \vec F=0
$$

e:

$$
\sum \vec M=0
$$

Il corpo rimane in equilibrio.

### Quando il corpo si ribalta

Se invece la verticale del centro di massa cade **fuori dalla superficie di appoggio**, peso e reazione vincolare non hanno più la stessa linea d'azione.

Si genera quindi un **momento risultante non nullo**:

$$
\sum \vec M\neq0
$$

e il corpo tende a ruotare e quindi a **ribaltarsi**.

> Regola pratica: un corpo appoggiato è stabile finché la proiezione verticale del suo centro di massa rimane dentro la base di appoggio.

Per impedirne il ribaltamento è necessario introdurre un ulteriore vincolo capace di generare un momento opposto.

---

## Perché il peso può essere applicato al baricentro

Per un sistema di forze parallele:

$$
\vec M_T=\sum_i \vec r_i\times\vec f_i
$$

Poiché tutte le forze hanno la stessa direzione, possiamo scrivere:

$$
\vec f_i=f_i\vec u
$$

quindi:

$$
\vec M_T
=
\sum_i \vec r_i\times f_i\vec u
=
\left(\sum_i\vec r_i f_i\right)\times\vec u
$$

Dalla definizione del centro delle forze:

$$
\sum_i\vec r_i f_i
=
\vec r_C\sum_i f_i
$$

perciò:

$$
\vec M_T
=
\left(\vec r_C\sum_i f_i\right)\times\vec u
$$

ma:

$$
\sum_i f_i\vec u=\vec F
$$

e quindi:

$$
\boxed{\vec M_T=\vec r_C\times\vec F}
$$

Questo dimostra che il sistema di forze parallele è equivalente alla **forza risultante applicata nel centro delle forze**.

Nel caso della gravità, tale punto è proprio il **baricentro**.

---

# Esercizio – Asta appoggiata a parete e pavimento

## Traccia

Un'asta omogenea di:

- lunghezza $L$;
- massa $M$;

è appoggiata su un pavimento orizzontale scabro e su una parete verticale.

L'asta forma un angolo $\theta$ con il pavimento.

A distanza:

$$
D=\frac34L
$$

dal punto di appoggio sul pavimento è sospesa una massa $m$.

Il sistema è in equilibrio.

**Calcolare la forza d'attrito tangenziale esercitata dal pavimento sull'asta.**

---

## Forze agenti

Sull'asta agiscono:

- $Mg$ → peso dell'asta, applicato al suo centro:

$$
\frac L2
$$

- $mg$ → peso della massa appesa, applicato a:

$$
\frac{3L}{4}
$$

- $N$ → reazione normale del pavimento;
- $\mu N$ → forza di attrito del pavimento;
- $N'$ → reazione normale della parete.

Poiché l'asta è omogenea, il suo baricentro coincide con il centro geometrico.

---

## 1. Equilibrio delle forze

### Direzione orizzontale

$$
N'-\mu N=0
$$

quindi:

$$
N'=\mu N
$$

### Direzione verticale

$$
N-mg-Mg=0
$$

da cui:

$$
N=(M+m)g
$$

---

## 2. Equilibrio dei momenti

Conviene scegliere come polo il punto in cui l'asta poggia sul pavimento.

In questo modo $N$ e $\mu N$ hanno momento nullo perché sono applicate proprio nel polo scelto.

Imponiamo:

$$
\sum M=0
$$

I momenti dei due pesi devono essere equilibrati dal momento prodotto da $N'$:

$$
Mg\frac L2\cos\theta
+
mg\frac{3L}{4}\cos\theta
=
N'L\sin\theta
$$

Raccogliendo:

$$
gL\cos\theta
\left(
\frac M2+\frac{3m}{4}
\right)
=
N'L\sin\theta
$$

semplificando $L$:

$$
N'
=
g\left(
\frac M2+\frac{3m}{4}
\right)
\frac{\cos\theta}{\sin\theta}
$$

quindi:

$$
N'
=
\frac{g}{2\tan\theta}
\left(
M+\frac32m
\right)
$$

Poiché dall'equilibrio orizzontale:

$$
f_{\text{att}}=\mu N=N'
$$

otteniamo:

$$
\boxed{
f_{\text{att}}
=
\frac{\left(M+\frac32m\right)g}
{2\tan\theta}
}
$$

---

## Idea chiave dell'esercizio

Negli esercizi di equilibrio del corpo rigido bisogna quasi sempre:

1. individuare **tutte le forze**;
2. imporre:

$$
\sum F_x=0
$$

$$
\sum F_y=0
$$

3. scegliere un polo conveniente e imporre:

$$
\sum M=0
$$

La scelta del polo è fondamentale: conviene scegliere un punto in cui agiscono più forze incognite, perché il loro **braccio diventa nullo** e quindi spariscono dall'equazione dei momenti. 

# Esercizi – Equilibrio del corpo rigido

## Esercizio 1 – Scala appoggiata a una parete

### Traccia

Una scala di massa:

$$
m=3.5\ \text{kg}
$$

e lunghezza $\ell$ è appoggiata a una parete verticale e forma con il pavimento un angolo:

$$
\alpha=65^\circ
$$

Il coefficiente di attrito statico tra scala e pavimento è:

$$
\mu_s=0.36
$$

mentre l'attrito con la parete è trascurabile.

Determinare:

1. le reazioni vincolari nei punti di appoggio;
2. l'angolo minimo che permette alla scala di rimanere in equilibrio.

---

## Forze agenti

Sulla scala agiscono:

- $mg$ → peso della scala, applicato nel centro;
- $N_1$ → reazione normale della parete;
- $N_2$ → reazione normale del pavimento;
- $F_s$ → attrito statico sul pavimento.

Poiché la parete è liscia, non esercita attrito.

---

## 1. Reazioni vincolari

Dall'equilibrio orizzontale:

$$
N_1=F_s
$$

Dall'equilibrio verticale:

$$
N_2=mg
$$

Per calcolare $N_1$, imponiamo l'equilibrio dei momenti rispetto al punto di appoggio sul pavimento.

I bracci sono:

$$
b_1=\ell\sin\alpha
$$

per $N_1$, e:

$$
b_2=\frac{\ell}{2}\cos\alpha
$$

per il peso.

Quindi:

$$
N_1\ell\sin\alpha
=
mg\frac{\ell}{2}\cos\alpha
$$

da cui:

$$
N_1=
\frac{mg}{2\tan\alpha}
$$

Essendo:

$$
F_s=N_1
$$

si ottiene:

$$
F_s=N_1\simeq 8.0\ \text{N}
$$

e:

$$
N_2=mg\simeq 34\ \text{N}
$$

---

## 2. Angolo minimo di equilibrio

L'attrito statico può assumere al massimo il valore:

$$
F_s^{max}=\mu_sN_2
$$

Poiché:

$$
N_2=mg
$$

si ha:

$$
F_s^{max}=\mu_smg
$$

Per restare in equilibrio deve valere:

$$
F_s\leq F_s^{max}
$$

quindi:

$$
\frac{mg}{2\tan\alpha}
\leq
\mu_smg
$$

Semplificando $mg$:

$$
\frac{1}{2\tan\alpha}\leq\mu_s
$$

da cui:

$$
\tan\alpha\geq\frac{1}{2\mu_s}
$$

L'angolo minimo è quindi:

$$
\boxed{
\alpha_{min}
=
\arctan\left(\frac{1}{2\mu_s}\right)
}
$$

Con $\mu_s=0.36$:

$$
\boxed{\alpha_{min}\approx54^\circ}
$$

> Se l'angolo scende sotto $54^\circ$, l'attrito richiesto supera il massimo disponibile e la scala scivola.

---

# Esercizio 2 – Blocchi e fune

## Traccia

Un blocco $A$ di massa:

$$
m_A=10\ \text{kg}
$$

è appoggiato su un piano scabro.

Un blocco $B$ di massa:

$$
m_B=5\ \text{kg}
$$

è collegato tramite un sistema di funi.

Il sistema è inizialmente in equilibrio con:

$$
\theta=30^\circ
$$

Determinare il coefficiente di attrito statico tra il blocco $A$ e il piano.

---

## Soluzione

Consideriamo il nodo dove si incontrano le tre tensioni.

Dall'equilibrio verticale:

$$
T\cos\theta=m_Bg
$$

Dall'equilibrio orizzontale:

$$
T\sin\theta=\mu_s m_Ag
$$

Dividendo le due equazioni:

$$
\tan\theta
=
\frac{\mu_sm_A}{m_B}
$$

quindi:

$$
\mu_s=
\frac{m_B}{m_A}\tan\theta
$$

Inserendo i dati:

$$
\mu_s=
\frac{5}{10}\tan30^\circ
$$

$$
\boxed{\mu_s\approx0.29}
$$

---

# Esercizio 3 – Torre di Pisa

## Traccia

La cima della Torre di Pisa è spostata rispetto all'asse verticale di:

$$
4.5\ \text{m}
$$

La torre viene approssimata come un cilindro omogeneo di:

- diametro $7.0\ \text{m}$;
- altezza $55\ \text{m}$.

Determinare:

1. se vi è rischio di ribaltamento;
2. quale spostamento della cima porterebbe al limite di ribaltamento.

---

## 1. Verifica della stabilità

Essendo il cilindro omogeneo, il centro di massa si trova a metà altezza.

Se la cima è spostata di $4.5$ m, il centro di massa è spostato della metà:

$$
\Delta x_{CM}=\frac{4.5}{2}=2.25\ \text{m}
$$

Il raggio della base è:

$$
R=\frac{7}{2}=3.5\ \text{m}
$$

Poiché:

$$
2.25<3.5
$$

la verticale del centro di massa cade ancora all'interno della base.

Quindi:

$$
\boxed{\text{la torre è ancora in equilibrio}}
$$

---

## 2. Limite di ribaltamento

Il limite si raggiunge quando la verticale del centro di massa arriva esattamente sul bordo della base:

$$
\Delta x_{CM}=3.5\ \text{m}
$$

Poiché lo spostamento del centro di massa è metà di quello della cima:

$$
\Delta x_{cima}=2\cdot3.5=7.0\ \text{m}
$$

Quindi il rischio di ribaltamento compare quando:

$$
\boxed{\Delta x_{cima}=7.0\ \text{m}}
$$

L'angolo limite rispetto alla verticale vale:

$$
\theta_{lim}
=
\arcsin\left(\frac{7}{55}\right)
$$

$$
\boxed{\theta_{lim}\approx7.3^\circ}
$$

---

# Quesiti finali

## Q1. Quale grandezza rappresenta la distribuzione di massa in un sistema continuo?

La **densità volumica**:

$$
\rho=\frac{dm}{dV}
$$

---

## Q2. Come è definito un corpo rigido?

Un corpo rigido è un sistema di punti materiali le cui distanze reciproche rimangono costanti nel tempo.

---

## Q3. Quali sono le condizioni di equilibrio statico di un corpo rigido?

Devono essere soddisfatte contemporaneamente:

$$
\boxed{\sum\vec F=0}
$$

e:

$$
\boxed{\sum\vec M=0}
$$

cioè devono essere nulle sia la risultante delle forze sia la risultante dei momenti.

---

# Schema da ricordare per gli esercizi

Quando trovi un esercizio sull'equilibrio del corpo rigido:

1. disegna tutte le **forze agenti**;
2. imponi:

$$
\sum F_x=0
$$

$$
\sum F_y=0
$$

3. scegli un polo conveniente;
4. imponi:

$$
\sum M=0
$$

5. se compare l'attrito statico, ricorda:

$$
F_s\leq\mu_sN
$$

e al limite dello scivolamento:

$$
F_s=\mu_sN
$$

6. per il ribaltamento controlla che la verticale del centro di massa cada dentro la base di appoggio.
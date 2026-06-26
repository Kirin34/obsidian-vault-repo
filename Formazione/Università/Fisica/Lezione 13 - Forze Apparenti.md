## Attrito

Nelle lezioni precedenti spesso si è lavorato assumendo superfici ideali, cioè **senza attrito**.  
Nella realtà questa è un’idealizzazione: quando un corpo si muove o tenta di muoversi su una superficie, compare quasi sempre una forza che si oppone al moto.

L’**attrito** è una forza che nasce dal contatto tra due superfici e agisce in direzione parallela alla superficie di contatto.

### Perché capiamo che esiste l’attrito?

Nella vita quotidiana osserviamo che:

- per mettere in moto un corpo su una superficie piana serve applicare una forza abbastanza grande;
- quando il corpo è in moto, tende a rallentare fino a fermarsi;
- per mantenerlo a velocità costante bisogna continuare ad applicare una forza.

Questi fenomeni mostrano che esiste una forza opposta al moto o al tentativo di moto: questa forza è detta **forza di attrito**.

L’attrito dipende principalmente da:

- il peso del corpo, cioè quanto il corpo preme sulla superficie;
- la natura delle superfici a contatto;
- la rugosità delle superfici.

---

## Attrito statico

L’**attrito statico** si manifesta quando un corpo è fermo, ma si cerca di metterlo in movimento applicando una forza.

Se applichiamo una forza parallela alla superficie, il corpo non si muove subito: l’attrito statico si oppone alla forza applicata e la controbilancia.

La forza di attrito statico è diretta:

- parallelamente alla superficie di contatto;
- in verso opposto alla forza che tende a mettere in moto il corpo.

La sua intensità massima è:

$$
F_{s,\text{max}} = \mu_s N
$$

dove:

- $F_s$ è la forza di attrito statico;
- $\mu_s$ è il coefficiente di attrito statico;
- $N$ è la reazione vincolare normale, cioè la forza con cui la superficie sostiene il corpo.

Su un piano orizzontale, se non ci sono altre forze verticali oltre peso e reazione normale:

$$
N = mg
$$

quindi:

$$
F_{s,\text{max}} = \mu_s mg
$$

---

## Nota importante
La formula:
$$
F_s = \mu_s N
$$

nelle slide indica il valore massimo dell’attrito statico.

In realtà, finché il corpo resta fermo, l’attrito statico si adatta alla forza applicata:
$$
F_s \leq \mu_s N
$$
Il corpo inizia a muoversi solo quando la forza applicata supera il valore massimo dell’attrito statico.

---
## Esempio intuitivo

Se spingiamo una scatola appoggiata su un pavimento:

- se spingiamo poco, la scatola resta ferma perché l’attrito statico bilancia la nostra forza;
- se aumentiamo la spinta, anche l’attrito statico aumenta;
- quando superiamo il valore massimo dell’attrito statico, la scatola inizia a muoversi.

Il valore massimo dipende dal peso dell’oggetto e dal tipo di superfici a contatto.

Se due oggetti hanno lo stesso peso e sono appoggiati su superfici trattate allo stesso modo, la forza necessaria per iniziare a muoverli è la stessa, anche se la loro forma o posizione può essere diversa.

## Angolo di attrito

Nel caso di superfici reali, la reazione vincolare non è composta solo dalla normale $N$, ma anche dalla forza di attrito.

La superficie esercita quindi sul corpo una reazione complessiva $\vec{R}$, data dalla somma vettoriale di:

- la reazione normale $N$, perpendicolare alla superficie;
- la forza di attrito $F_s$, parallela alla superficie.

Quindi:

$$
\vec{R} = \vec{N} + \vec{F_s}
$$

Poiché l’attrito statico massimo vale:

$$
F_s \leq \mu_s N
$$

la reazione vincolare complessiva $\vec{R}$ non può inclinarsi oltre un certo angolo rispetto alla normale.

Questo angolo massimo è detto **angolo di attrito**.

Si indica con $\theta_a$ ed è definito dalla relazione:

$$
\tan \theta_a = \mu_s
$$

Più precisamente, finché il corpo rimane in equilibrio:

$$
\tan \theta \leq \mu_s
$$

dove $\theta$ è l’angolo formato dalla reazione vincolare $\vec{R}$ con la normale.

### Significato fisico

L’angolo di attrito rappresenta il massimo angolo entro cui la reazione vincolare può inclinarsi senza che il corpo inizi a muoversi.

Se la forza applicata tende a far scivolare il corpo, l’attrito statico si oppone al moto e fa inclinare la reazione vincolare totale.

Quando si raggiunge il limite:

$$
\tan \theta_a = \mu_s
$$

il corpo è sul punto di iniziare a muoversi.

---

## Attrito dinamico

L’**attrito dinamico** si manifesta quando un corpo è già in movimento su una superficie reale.

A differenza dell’attrito statico, che agisce quando il corpo è fermo e si oppone al tentativo di movimento, l’attrito dinamico agisce durante lo scorrimento.

La forza di attrito dinamico:

- è parallela alla superficie di contatto;
- ha verso opposto al moto del corpo;
- tende a rallentare il corpo.

Il suo modulo è:

$$
F_k = \mu_k N
$$

dove:

- $F_k$ è la forza di attrito dinamico;
- $\mu_k$ è il coefficiente di attrito dinamico;
- $N$ è la reazione normale della superficie.

Su un piano orizzontale, se le uniche forze verticali sono peso e normale:

$$
N = mg
$$

quindi:

$$
F_k = \mu_k mg
$$

---

## Differenza tra attrito statico e dinamico

In generale:

$$
\mu_k < \mu_s
$$

cioè il coefficiente di attrito dinamico è minore di quello statico.

Questo spiega perché, nella vita quotidiana, è più difficile mettere in movimento un corpo fermo che mantenerlo in movimento una volta che ha già iniziato a scorrere.

In altre parole:

- per far partire un oggetto fermo bisogna superare l’attrito statico massimo;
- quando l’oggetto è già in moto, agisce l’attrito dinamico, che di solito è più piccolo.

---

## Schema mentale

| Situazione | Tipo di attrito | Formula | Effetto |
|---|---|---|---|
| Corpo fermo, si cerca di muoverlo | Attrito statico | $F_s \leq \mu_s N$ | Si oppone all’inizio del moto |
| Corpo al limite del moto | Attrito statico massimo | $F_{s,max} = \mu_s N$ | Il corpo sta per partire |
| Corpo già in movimento | Attrito dinamico | $F_k = \mu_k N$ | Si oppone allo scorrimento |
## Viscosità e resistenza del mezzo

Quando un corpo si muove dentro un fluido, per esempio aria o acqua, subisce una forza che si oppone al moto.  
Questa forza è detta **resistenza del mezzo**.

Nel caso di velocità elevate, il moto del fluido attorno al corpo può diventare più complesso e si possono formare dei vortici. In questo caso la resistenza del mezzo non cresce più semplicemente in modo lineare con la velocità, ma dipende anche dal quadrato della velocità.

La forza di resistenza può essere scritta come:

$$
\vec{F}_r = - \frac{1}{2} C \rho A v \vec{v}
$$

oppure, considerando solo il modulo:

$$
F_r = \frac{1}{2} C \rho A v^2
$$

Il segno meno indica che la forza di resistenza ha verso opposto rispetto al moto.

Dove:

- $\rho$ è la densità del fluido, cioè la massa per unità di volume;
- $C$ è il coefficiente di resistenza del mezzo, detto anche coefficiente aerodinamico;
- $A$ è l’area efficace della sezione dell’oggetto perpendicolare al moto;
- $v$ è la velocità del corpo rispetto al fluido.

---

## Significato della formula

La resistenza del mezzo aumenta se:

- aumenta la densità del fluido;
- aumenta l’area frontale dell’oggetto;
- aumenta il coefficiente di resistenza aerodinamica;
- aumenta la velocità.

La cosa più importante è che, a velocità elevate, la forza resistente cresce come:

$$
F_r \propto v^2
$$

Quindi se la velocità raddoppia, la resistenza diventa circa quattro volte maggiore.

---

## Coefficiente equivalente

La formula può essere riscritta in una forma simile al caso laminare ponendo:

$$
\beta = \frac{1}{2} C \rho A v
$$

In questo modo:

$$
\vec{F}_r = - \beta \vec{v}
$$

Però c’è una differenza importante rispetto al caso laminare: qui $\beta$ non è costante, perché dipende anche dalla velocità $v$.

Infatti:

$$
\beta = \frac{1}{2} C \rho A v
$$

quindi al crescere della velocità cresce anche il coefficiente equivalente $\beta$.

---

## Differenza tra caso laminare e velocità elevate

| Caso | Formula | Dipendenza dalla velocità |
|---|---|---|
| Moto laminare | $\vec{F}_r = -\beta \vec{v}$ | proporzionale a $v$ |
| Velocità elevate / vortici | $\vec{F}_r = -\frac{1}{2} C \rho A v \vec{v}$ | proporzionale a $v^2$ |

Nel caso laminare la resistenza cresce linearmente con la velocità.  
Nel caso di velocità elevate, invece, la resistenza cresce molto più rapidamente perché dipende dal quadrato della velocità.

---

## Esempio intuitivo

Un’auto che viaggia nell’aria subisce una resistenza aerodinamica.  
Se va piano, la resistenza è relativamente piccola.  
Se aumenta molto la velocità, la resistenza cresce tantissimo, perché dipende da $v^2$.

Per questo a velocità alte serve molta più forza, e quindi molta più energia, per mantenere il moto.

## Velocità limite in caduta libera

Quando un corpo cade in un mezzo reale, come l’aria, non agisce solo la forza peso, ma anche una forza resistente dovuta al mezzo.

Assumiamo il verso positivo verso il basso.  
Le forze lungo la verticale sono:

- forza peso: $mg$, verso il basso;
- resistenza del mezzo: $-\beta v$, verso opposto al moto.

Quindi l’equazione del moto è:

$$
m \frac{dv}{dt} = mg - \beta v
$$

Dividendo per $m$:

$$
\frac{dv}{dt} = g - \frac{\beta}{m}v
$$

Questa equazione dice che l’accelerazione non resta sempre uguale a $g$, perché mentre la velocità aumenta cresce anche la resistenza del mezzo.

---

## Andamento della velocità

Risolvendo l’equazione, con il corpo che parte da fermo al tempo $t = 0$, si ottiene:

$$
v(t) = \frac{mg}{\beta}\left(1 - e^{-\frac{\beta}{m}t}\right)
$$

All’inizio, quando $t = 0$:

$$
v(0) = 0
$$

Poi la velocità aumenta, ma non cresce all’infinito.  
Col passare del tempo, il termine esponenziale tende a zero:

$$
e^{-\frac{\beta}{m}t} \to 0
$$

quindi la velocità tende a:

$$
v_{lim} = \frac{mg}{\beta}
$$

Questa è detta **velocità limite**.

---

## Significato fisico della velocità limite

La velocità limite è la massima velocità che il corpo raggiunge durante la caduta nel mezzo viscoso.

Quando il corpo ha raggiunto la velocità limite:

$$
mg = \beta v
$$

quindi la forza peso e la resistenza del mezzo si equilibrano.

La risultante delle forze diventa nulla:

$$
F_{tot} = 0
$$

e quindi anche l’accelerazione diventa nulla:

$$
a = 0
$$

Da quel momento il corpo continua a cadere con velocità costante.

---

## Da cosa dipende la velocità limite?

La velocità limite vale:

$$
v_{lim} = \frac{mg}{\beta}
$$

Quindi:

- aumenta se aumenta la massa o il peso del corpo;
- diminuisce se aumenta la resistenza del mezzo;
- diminuisce se aumenta l’area trasversale dell’oggetto;
- dipende anche dalla densità del mezzo e dalla forma dell’oggetto.

Un esempio pratico è il paracadute: aumentando molto l’area trasversale, aumenta la resistenza dell’aria e quindi diminuisce la velocità limite.

---

## Esercizio: corpo appoggiato alla parete di un carrello accelerato

Un corpo è appoggiato alla parete posteriore di un carrello che accelera orizzontalmente con:

$$
a = 5 \, m/s^2
$$

Il corpo resta a contatto con la parete.  
Il coefficiente di attrito dinamico tra corpo e parete è:

$$
\mu = 0.4
$$

Bisogna trovare la legge oraria del moto del corpo rispetto alla parete del carrello.

---

### Analisi nel sistema non inerziale del carrello

Nel sistema del carrello il corpo è soggetto a una forza apparente opposta all’accelerazione del carrello.

Questa forza apparente vale:

$$
F_{app} = ma
$$

Essa spinge il corpo contro la parete, generando la reazione normale:

$$
N = ma
$$

Poiché il corpo scivola verso il basso, l’attrito dinamico è diretto verso l’alto.

La forza di attrito vale:

$$
F_a = \mu N
$$

Sostituendo $N = ma$:

$$
F_a = \mu ma
$$

---

### Moto verticale

Lungo la verticale agiscono:

- il peso $mg$, verso il basso;
- l’attrito $\mu ma$, verso l’alto.

Prendendo positivo verso l’alto:

$$
m a_y = \mu ma - mg
$$

Semplificando $m$:

$$
a_y = \mu a - g
$$

Sostituendo i dati:

$$
a_y = 0.4 \cdot 5 - 9.8
$$

$$
a_y = 2 - 9.8 = -7.8 \, m/s^2
$$

Il segno meno indica che il corpo accelera verso il basso.

Quindi il corpo scende rispetto alla parete con accelerazione costante pari a:

$$
7.8 \, m/s^2
$$

---

## Legge oraria

Se il corpo parte da fermo rispetto alla parete, la legge oraria verticale è:

$$
y(t) = y_0 + \frac{1}{2} a_y t^2
$$

Sostituendo $a_y = -7.8 \, m/s^2$:

$$
y(t) = y_0 - 3.9 t^2
$$

Se invece misuriamo lo spostamento verso il basso come positivo:

$$
s(t) = \frac{1}{2}(g - \mu a)t^2
$$

$$
s(t) = \frac{1}{2}(9.8 - 2)t^2
$$

$$
s(t) = 3.9t^2
$$

---

## Idea chiave dell’esercizio

Il carrello accelera orizzontalmente, quindi nel sistema non inerziale del carrello compare una forza apparente.

Questa forza apparente schiaccia il corpo contro la parete, generando la normale:

$$
N = ma
$$

La normale produce attrito:

$$
F_a = \mu ma
$$

L’attrito si oppone alla discesa, ma non è sufficiente a bilanciare completamente il peso.  
Per questo il corpo scende con accelerazione:

$$
a_y = \mu a - g = -7.8 \, m/s^2
$$

## Esercizio: due masse con puleggia e attrito

Due corpi sono collegati da un filo inestensibile e privo di massa che passa attraverso una puleggia senza attrito.

- massa sul piano orizzontale: $m_1 = 1 \, kg$
- massa sospesa verticalmente: $m_2 = 2 \, kg$
- coefficiente di attrito dinamico tra $m_1$ e il piano: $\mu = 0.3$

Il corpo sospeso $m_2$ tende a scendere e trascina $m_1$ verso sinistra.

---

## Forze agenti

Sul corpo $m_1$, appoggiato sul piano, agiscono lungo l’orizzontale:

- tensione del filo $T$, verso sinistra;
- attrito dinamico $F_a = \mu m_1 g$, verso destra.

Sul corpo $m_2$, sospeso verticalmente, agiscono:

- peso $m_2 g$, verso il basso;
- tensione $T$, verso l’alto.

Consideriamo positivo il verso reale del moto:

- verso sinistra per $m_1$;
- verso il basso per $m_2$.

---

## Sistema di equazioni

Per $m_1$:

$$
m_1 a = T - \mu m_1 g
$$

Per $m_2$:

$$
m_2 a = m_2 g - T
$$

Sommando membro a membro:

$$
m_1 a + m_2 a = T - \mu m_1 g + m_2 g - T
$$

La tensione si elimina:

$$
(m_1 + m_2)a = (m_2 - \mu m_1)g
$$

Da cui:

$$
a = \frac{m_2 - \mu m_1}{m_1 + m_2}g
$$

Sostituendo i dati:

$$
a = \frac{2 - 0.3 \cdot 1}{1 + 2} \cdot 9.8
$$

$$
a = \frac{1.7}{3} \cdot 9.8
$$

$$
a \approx 5.55 \, m/s^2
$$

---

## Calcolo della tensione

Usiamo la seconda equazione:

$$
m_2 a = m_2 g - T
$$

Ricaviamo $T$:

$$
T = m_2 g - m_2 a
$$

Sostituendo:

$$
T = 2 \cdot 9.8 - 2 \cdot 5.55
$$

$$
T = 19.6 - 11.1
$$

$$
T = 8.5 \, N
$$

Quindi la tensione del filo vale:

$$
T = 8.5 \, N
$$

---

## Idea chiave dell’esercizio

La massa sospesa $m_2$ tira il sistema verso il basso, ma il moto è contrastato dall’attrito dinamico che agisce su $m_1$.

L’attrito riduce l’accelerazione del sistema.

La tensione del filo non coincide con il peso di $m_2$, perché il corpo sospeso non è fermo: sta accelerando verso il basso.

---

# Quesiti

## Q.1 Qual è la relazione che definisce le forze di attrito statico e dinamico?

Le forze di attrito statico e dinamico sono dirette tangenzialmente alla superficie di contatto.

Esse si oppongono:

- al tentativo di movimento, nel caso dell’attrito statico;
- al movimento effettivo, nel caso dell’attrito dinamico.

La relazione generale è:

$$
F = \mu N
$$

dove:

- $F$ è la forza di attrito;
- $\mu$ è il coefficiente di attrito;
- $N$ è la reazione normale, cioè la risultante delle forze perpendicolari alla superficie.

Nel caso dell’attrito statico:

$$
F_s \leq \mu_s N
$$

Il valore massimo è:

$$
F_{s,max} = \mu_s N
$$

Nel caso dell’attrito dinamico:

$$
F_k = \mu_k N
$$

In generale:

$$
\mu_s > \mu_k
$$

cioè il coefficiente di attrito statico è maggiore di quello dinamico.  
Per questo è più difficile mettere in moto un corpo fermo che mantenerlo in movimento.

---

## Q.2 Qual è la forza di attrito viscoso di resistenza del mezzo per un corpo fermo in un fluido?

La forza di attrito viscoso dipende dalla velocità relativa tra il corpo e il fluido.

Nel caso laminare:

$$
\vec{F}_r = -\beta \vec{v}
$$

Nel caso di velocità elevate:

$$
\vec{F}_r = -\frac{1}{2} C \rho A v \vec{v}
$$

Se il corpo è fermo rispetto al fluido, allora:

$$
v = 0
$$

Quindi la forza viscosa è nulla:

$$
F_r = 0
$$

La resistenza del mezzo esiste solo se c’è moto relativo tra corpo e fluido.


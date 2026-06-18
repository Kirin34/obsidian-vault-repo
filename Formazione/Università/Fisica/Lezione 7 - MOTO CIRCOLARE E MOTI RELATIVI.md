# Moto circolare e accelerazione centripeta

## 1. Moto circolare

Il **moto circolare** è un moto piano in cui la traiettoria del corpo è una **circonferenza**.

Nel moto circolare conviene usare le **coordinate polari**, perché il raggio rimane costante e cambia solo l’angolo.

La posizione del punto può essere descritta così:

$$
r = R = costante
$$

$$
\theta = \theta(t)
$$

Dove:

- $R$ è il raggio della circonferenza;
- $\theta$ è l’angolo che individua la posizione del punto sulla circonferenza;
- il raggio non cambia nel tempo;
- cambia solo l’angolo $\theta$.

---

## 2. Moto circolare uniforme

Il **moto circolare uniforme** è un moto circolare in cui la **velocità scalare** $v$ è costante.

Attenzione: anche se il modulo della velocità è costante, la velocità **non è completamente costante**, perché cambia continuamente direzione.

La legge oraria lungo la traiettoria è:

$$
s(t) = s_0 + vt
$$

Dove:

- $s(t)$ è l’ascissa curvilinea, cioè lo spazio percorso lungo la circonferenza;
- $s_0$ è la posizione iniziale;
- $v$ è la velocità scalare;
- $t$ è il tempo.

Per piccoli spostamenti sulla circonferenza vale:

$$
ds = R d\theta
$$

Poiché:

$$
ds = vdt
$$

Allora:

$$
vdt = R d\theta
$$

Da cui:

$$
d\theta = \frac{v}{R}dt
$$

Integrando si ottiene:

$$
\theta(t) = \theta_0 + \frac{v}{R}t
$$

## 3. Velocità angolare

Si definisce **velocità angolare**:

$$
\omega = \frac{d\theta}{dt}
$$

Nel moto circolare uniforme:

$$
\omega = \frac{v}{R}
$$

Quindi la legge del moto in coordinate polari diventa:

$$
r = R
$$

$$
\theta = \theta_0 + \omega t
$$

La velocità angolare $\omega$ si misura in:

$$
rad/s
$$

La velocità angolare viene anche chiamata **pulsazione**.

La relazione fondamentale tra velocità lineare e velocità angolare è:

$$
v = \omega R
$$

oppure:

$$
\omega = \frac{v}{R}
$$

---

## 4. Accelerazione centripeta

Nel moto circolare uniforme la velocità ha modulo costante, ma cambia continuamente direzione.

Quindi esiste comunque un’accelerazione.

Questa accelerazione è detta **accelerazione centripeta**.

È diretta:

- verso il centro della circonferenza;
- perpendicolarmente alla velocità;
- lungo la direzione normale alla traiettoria.

Il modulo dell’accelerazione centripeta è:

$$
a_c = \frac{v^2}{R}
$$

Usando la relazione:

$$
v = \omega R
$$

si può scrivere anche:

$$
a_c = \omega^2 R
$$

Quindi le formule principali sono:

$$
a_c = \frac{v^2}{R}
$$

$$
a_c = \omega^2 R
$$

## 5. Moto circolare uniforme in coordinate cartesiane

Nel moto circolare uniforme la posizione può essere scritta anche con le coordinate cartesiane:

$$
x(t) = R \cos(\omega t + \theta_0)
$$

$$
y(t) = R \sin(\omega t + \theta_0)
$$

Derivando due volte rispetto al tempo si ottengono le componenti dell’accelerazione:

$$
a_x = \ddot{x}(t) = -\omega^2 R \cos(\omega t + \theta_0)
$$

Poiché:

$$
x(t) = R \cos(\omega t + \theta_0)
$$

allora:

$$
a_x = -\omega^2 x(t)
$$

Analogamente:

$$
a_y = \ddot{y}(t) = -\omega^2 R \sin(\omega t + \theta_0)
$$

Poiché:

$$
y(t) = R \sin(\omega t + \theta_0)
$$

allora:

$$
a_y = -\omega^2 y(t)
$$

Questo conferma che l’accelerazione è sempre diretta verso il centro della circonferenza.

---

## 6. Accelerazione centripeta nei moti curvi

Il concetto di accelerazione centripeta si può estendere anche ai **moti curvilinei generici**.

Una traiettoria curva può essere approssimata, in ogni suo punto, con un piccolo arco di circonferenza tangente alla traiettoria.

In questo caso il raggio $R$ non è necessariamente il raggio di una circonferenza fissa, ma prende il nome di:

> **raggio di curvatura**

Il raggio di curvatura è il raggio della circonferenza che approssima localmente la traiettoria in quel punto.

Nel moto curvilineo l’accelerazione può avere due componenti:

$$
\vec{a} = \vec{a}_T + \vec{a}_N
$$

Dove:

- $\vec{a}_T$ è l’accelerazione tangenziale;
- $\vec{a}_N$ è l’accelerazione normale o centripeta.

La formula generale è:

$$
\vec{a} = \frac{dv}{dt}\vec{u}_T + \frac{v^2}{R}\vec{u}_N
$$

Dove:

- $\frac{dv}{dt}\vec{u}_T$ è la componente tangenziale;
- $\frac{v^2}{R}\vec{u}_N$ è la componente normale/centripeta;
- $\vec{u}_T$ è il versore tangente alla traiettoria;
- $\vec{u}_N$ è il versore normale, diretto verso il centro di curvatura.

---

## 7. Differenza tra moto circolare uniforme e moto circolare vario

### Moto circolare uniforme

Nel moto circolare uniforme:

- il modulo della velocità è costante;
- cambia solo la direzione della velocità;
- c’è solo accelerazione centripeta.

Quindi:

$$
a_T = 0
$$

$$
a = a_N = \frac{v^2}{R}
$$

### Moto circolare vario

Nel moto circolare vario:

- cambia la direzione della velocità;
- cambia anche il modulo della velocità;
- ci sono sia accelerazione centripeta sia accelerazione tangenziale.

Quindi:

$$
a_T = \frac{dv}{dt}
$$

$$
a_N = \frac{v^2}{R}
$$

E l’accelerazione totale è:

$$
\vec{a} = \frac{dv}{dt}\vec{u}_T + \frac{v^2}{R}\vec{u}_N
$$

---
## Formule da ricordare

$$
s(t) = s_0 + vt
$$

$$
ds = R d\theta
$$

$$
\omega = \frac{d\theta}{dt}
$$

$$
\omega = \frac{v}{R}
$$

$$
v = \omega R
$$

$$
\theta(t) = \theta_0 + \omega t
$$

$$
a_c = \frac{v^2}{R}
$$

$$
a_c = \omega^2 R
$$

$$
\vec{a} = \frac{dv}{dt}\vec{u}_T + \frac{v^2}{R}\vec{u}_N
$$


# Moto circolare vario, notazione vettoriale e accelerazione angolare

## 1. Moto circolare vario

Il **moto circolare vario** è un moto circolare in cui la velocità non è costante in modulo.

Nel moto circolare uniforme cambia solo la direzione della velocità, mentre nel moto circolare vario cambia anche il suo valore.

Per questo motivo bisogna considerare due componenti dell’accelerazione:

- **accelerazione centripeta**, legata al cambio di direzione della velocità;
- **accelerazione tangenziale**, legata al cambio del modulo della velocità.

L’accelerazione tangenziale vale:

$$
a_T = \frac{dv}{dt}
$$

Dato che nel moto circolare vale:

$$
v = \omega R
$$

allora:

$$
\frac{dv}{dt} = R \frac{d\omega}{dt}
$$

Si definisce quindi **accelerazione angolare**:

$$
\alpha = \frac{d\omega}{dt}
$$

Poiché:

$$
\omega = \frac{d\theta}{dt}
$$

si può scrivere anche:

$$
\alpha = \frac{d^2\theta}{dt^2}
$$

Inoltre:

$$
\alpha = \frac{1}{R}\frac{dv}{dt}
$$

cioè:

$$
\alpha = \frac{a_T}{R}
$$

Da cui si ricava anche:

$$
a_T = \alpha R
$$

## 2. Leggi orarie del moto circolare vario

Nel moto circolare vario si lavora con grandezze angolari, in modo simile al moto rettilineo.

Se si conosce l’accelerazione angolare $\alpha(t)$, si può ricavare la velocità angolare:

$$
\omega(t) = \omega_0 + \int_0^t \alpha(\tau)d\tau
$$

Poi, conoscendo $\omega(t)$, si può ricavare la posizione angolare:

$$
\theta(t) = \theta_0 + \int_0^t \omega(\tau)d\tau
$$

Se l’accelerazione angolare è costante, cioè:

$$
\alpha = costante
$$

allora valgono le formule analoghe al moto rettilineo uniformemente accelerato:

$$
\omega(t) = \omega_0 + \alpha t
$$

$$
\theta(t) = \theta_0 + \omega_0 t + \frac{1}{2}\alpha t^2
$$

Queste formule sono molto simili a:

$$
v(t) = v_0 + at
$$

$$
s(t) = s_0 + v_0t + \frac{1}{2}at^2
$$

ma applicate alle grandezze angolari.

---

## 3. Accelerazione centripeta nel moto circolare vario

Anche nel moto circolare vario è presente l’accelerazione centripeta:

$$
a_c = \omega^2 R
$$

Però, siccome $\omega$ cambia nel tempo, anche $a_c$ cambia nel tempo.

Se:

$$
\omega(t) = \omega_0 + \alpha t
$$

allora:

$$
a_c = \omega^2 R
$$

diventa:

$$
a_c = (\omega_0 + \alpha t)^2 R
$$

Quindi nel moto circolare vario l’accelerazione totale non è costante in generale, perché può variare sia la componente tangenziale sia quella centripeta.

## 4. Notazione vettoriale nel moto circolare

Nel moto circolare alcune grandezze possono essere descritte in forma vettoriale.

Si definisce il vettore velocità angolare:

$$
\vec{\omega}
$$

Il suo modulo è:

$$
\omega = \frac{d\theta}{dt}
$$

La direzione di $\vec{\omega}$ è perpendicolare al piano in cui avviene il moto circolare.

Il verso si stabilisce con la regola della mano destra:

- se il moto è antiorario, $\vec{\omega}$ punta verso l’osservatore;
- se il moto è orario, $\vec{\omega}$ punta nel verso opposto.

La relazione vettoriale tra velocità lineare, velocità angolare e posizione è:

$$
\vec{v} = \vec{\omega} \times \vec{r}
$$

Dove:

- $\vec{v}$ è la velocità lineare;
- $\vec{\omega}$ è la velocità angolare;
- $\vec{r}$ è il vettore posizione dal centro della circonferenza al punto;
- $\times$ indica il prodotto vettoriale.

Questa formula dice che la velocità lineare è sempre tangente alla traiettoria circolare.

## 5. Accelerazione angolare e accelerazione lineare

Si definisce il vettore accelerazione angolare:

$$
\vec{\alpha} = \frac{d\vec{\omega}}{dt}
$$

Nel moto circolare piano la direzione di $\vec{\alpha}$ è la stessa di $\vec{\omega}$.

Il verso dipende da come varia il modulo della velocità angolare:

- se $\omega$ aumenta, $\vec{\alpha}$ ha lo stesso verso di $\vec{\omega}$;
- se $\omega$ diminuisce, $\vec{\alpha}$ ha verso opposto rispetto a $\vec{\omega}$.

Partendo dalla relazione:

$$
\vec{v} = \vec{\omega} \times \vec{r}
$$

si ottiene l’accelerazione lineare derivando rispetto al tempo:

$$
\vec{a} = \frac{d\vec{v}}{dt}
$$

Quindi:

$$
\vec{a} = \frac{d}{dt}(\vec{\omega} \times \vec{r})
$$

Applicando la derivata del prodotto:

$$
\vec{a} = \frac{d\vec{\omega}}{dt} \times \vec{r} + \vec{\omega} \times \frac{d\vec{r}}{dt}
$$

Dato che:

$$
\frac{d\vec{\omega}}{dt} = \vec{\alpha}
$$

e:

$$
\frac{d\vec{r}}{dt} = \vec{v}
$$

si ottiene:

$$
\vec{a} = \vec{\alpha} \times \vec{r} + \vec{\omega} \times \vec{v}
$$

Questa è la formula vettoriale dell’accelerazione nel moto circolare.

## 6. Significato dei due termini dell’accelerazione

La formula:

$$
\vec{a} = \vec{\alpha} \times \vec{r} + \vec{\omega} \times \vec{v}
$$

contiene due termini.

### Primo termine

$$
\vec{\alpha} \times \vec{r}
$$

Questo termine rappresenta l’**accelerazione tangenziale**.

Il suo modulo è:

$$
a_T = \alpha R
$$

È tangente alla traiettoria e indica la variazione del modulo della velocità.

---

### Secondo termine

$$
\vec{\omega} \times \vec{v}
$$

Questo termine rappresenta l’**accelerazione centripeta**.

Il suo modulo è:

$$
a_c = \omega^2 R
$$

È diretta verso il centro della circonferenza e indica la variazione della direzione della velocità.

---

## 7. Caso del moto circolare uniforme

Nel moto circolare uniforme la velocità angolare $\omega$ è costante.

Quindi:

$$
\vec{\alpha} = 0
$$

Di conseguenza il termine tangenziale sparisce:

$$
\vec{\alpha} \times \vec{r} = 0
$$

Rimane solo l’accelerazione centripeta:

$$
\vec{a} = \vec{\omega} \times \vec{v}
$$

Il suo modulo è:

$$
a_c = \omega^2 R
$$

oppure:

$$
a_c = \frac{v^2}{R}
$$

---

## Formule importanti

### Velocità angolare

$$
\omega = \frac{d\theta}{dt}
$$

### Accelerazione angolare

$$
\alpha = \frac{d\omega}{dt}
$$

$$
\alpha = \frac{d^2\theta}{dt^2}
$$

### Relazione tra accelerazione tangenziale e accelerazione angolare

$$
a_T = \alpha R
$$

$$
\alpha = \frac{a_T}{R}
$$

### Leggi del moto con accelerazione angolare costante

$$
\omega(t) = \omega_0 + \alpha t
$$

$$
\theta(t) = \theta_0 + \omega_0 t + \frac{1}{2}\alpha t^2
$$

### Velocità lineare in forma vettoriale

$$
\vec{v} = \vec{\omega} \times \vec{r}
$$

### Accelerazione lineare in forma vettoriale

$$
\vec{a} = \vec{\alpha} \times \vec{r} + \vec{\omega} \times \vec{v}
$$

### Accelerazione centripeta

$$
a_c = \frac{v^2}{R}
$$

$$
a_c = \omega^2R
$$
# Esercizi - Moto circolare e accelerazione angolare

## Esercizio 1 - Giostra con accelerazione angolare costante

### Testo
La piattaforma di una giostra parte da ferma con accelerazione angolare costante:

$$
\alpha = 0.2 \ rad/s^2
$$

Calcolare al tempo:

$$
t = 2s
$$

1. la velocità angolare;
2. il modulo dell'accelerazione di un punto a distanza:

$$
r = 2m
$$

dall'asse di rotazione.

---

### Dati

$$
\omega_0 = 0
$$

$$
\alpha = 0.2 \ rad/s^2
$$

$$
t = 2s
$$

$$
r = 2m
$$

---
### Velocità angolare

Nel moto circolare uniformemente accelerato:

$$
\omega(t) = \omega_0 + \alpha t
$$

Poiché parte da ferma:

$$
\omega_0 = 0
$$

quindi:

$$
\omega(2) = 0 + 0.2 \cdot 2
$$

$$
\omega(2) = 0.4 \ rad/s
$$

> Attenzione: l’unità corretta è **rad/s**, non rad/s².

---
### Accelerazione tangenziale

L’accelerazione tangenziale è:

$$
a_T = \alpha r
$$

Sostituendo:

$$
a_T = 0.2 \cdot 2
$$

$$
a_T = 0.4 \ m/s^2
$$

---
### Accelerazione centripeta

L’accelerazione centripeta è:

$$
a_c = \omega^2 r
$$

Sostituendo:

$$
a_c = (0.4)^2 \cdot 2
$$

$$
a_c = 0.16 \cdot 2
$$

$$
a_c = 0.32 \ m/s^2
$$

---
### Accelerazione totale

Nel moto circolare vario l’accelerazione totale ha due componenti perpendicolari:

- accelerazione tangenziale;
- accelerazione centripeta.

Quindi il modulo totale si calcola con Pitagora:

$$
a = \sqrt{a_T^2 + a_c^2}
$$

$$
a = \sqrt{(0.4)^2 + (0.32)^2}
$$

$$
a = \sqrt{0.16 + 0.1024}
$$

$$
a = \sqrt{0.2624}
$$

$$
a \approx 0.51 \ m/s^2
$$

---
### Risultati

$$
\omega = 0.4 \ rad/s
$$

$$
a_T = 0.4 \ m/s^2
$$

$$
a_c = 0.32 \ m/s^2
$$

$$
a \approx 0.51 \ m/s^2
$$
## Esercizio 2 - Accelerazione centripeta della Luna

### Testo
La Luna compie una rivoluzione intorno alla Terra in:

$$
T = 27.3 \ giorni
$$

Supponendo che la sua orbita sia circolare di raggio:

$$
r = 3.82 \cdot 10^5 \ km
$$

calcolare il modulo della sua accelerazione.

---
### Dati

$$
T = 27.3 \ giorni
$$

$$
r = 3.82 \cdot 10^5 \ km
$$

Bisogna convertire tutto nel Sistema Internazionale.

Il raggio diventa:

$$
r = 3.82 \cdot 10^5 \ km = 3.82 \cdot 10^8 \ m
$$

Il periodo in secondi è:

$$
T = 27.3 \cdot 86400
$$

$$
T = 2.36 \cdot 10^6 \ s
$$

---
### Formula

Nel moto circolare uniforme:

$$
a_c = \omega^2 r
$$

Poiché:

$$
\omega = \frac{2\pi}{T}
$$

allora:

$$
a_c = r \left(\frac{2\pi}{T}\right)^2
$$

---

### Svolgimento

$$
a_c = 3.82 \cdot 10^8 \left(\frac{2\pi}{2.36 \cdot 10^6}\right)^2
$$

Calcolando:

$$
a_c \approx 2.7 \cdot 10^{-3} \ m/s^2
$$

---

### Risultato

$$
a_c \approx 2.7 \cdot 10^{-3} \ m/s^2
$$

Questa è l’accelerazione centripeta della Luna, cioè l’accelerazione diretta verso la Terra.

## Esercizio 3 - Moto accelerato e poi decelerato su una circonferenza

### Testo
Un punto si muove lungo una circonferenza di raggio:

$$
R = 1.8 \ m
$$

con accelerazione angolare:

$$
\alpha_1 = 2.39 \ rad/s^2
$$

partendo da fermo a:

$$
t = 0s
$$

Dopo aver percorso mezzo giro, il moto diventa uniformemente decelerato e si ferma dopo aver percorso un altro mezzo giro.

Calcolare:

1. l'accelerazione angolare $\alpha_2$ durante il secondo mezzo giro;
2. il tempo totale per compiere il giro completo;
3. se nello stesso intervallo di tempo il moto fosse uniforme, quale sarebbe l'accelerazione centripeta.

---

### Dati

$$
R = 1.8 \ m
$$

$$
\alpha_1 = 2.39 \ rad/s^2
$$

Il punto parte da fermo:

$$
\omega_0 = 0
$$

Mezzo giro corrisponde a:

$$
\theta = \pi \ rad
$$

---

# Parte A - Primo mezzo giro

Nel primo tratto il moto è uniformemente accelerato.

La legge angolare è:

$$
\theta = \theta_0 + \omega_0 t + \frac{1}{2}\alpha t^2
$$

Poiché:

$$
\theta_0 = 0
$$

e:

$$
\omega_0 = 0
$$

rimane:

$$
\theta = \frac{1}{2}\alpha_1 t_0^2
$$

Per mezzo giro:

$$
\pi = \frac{1}{2}\alpha_1 t_0^2
$$

Da cui:

$$
t_0 = \sqrt{\frac{2\pi}{\alpha_1}}
$$

## Esercizio 4 - Velocità angolare della Terra

### Testo
La Terra ruota attorno al proprio asse. Calcolare la sua velocità angolare, assumendo che sia costante.

---

### Dati

La Terra compie una rotazione completa in un giorno:

$$
T = 24h
$$

Una rotazione completa corrisponde a:

$$
\Delta \theta = 2\pi \ rad
$$

Convertiamo il periodo in secondi:

$$
T = 24 \cdot 3600
$$

$$
T = 86400 \ s
$$

---

### Formula

La velocità angolare è:

$$
\omega = \frac{\Delta \theta}{T}
$$

Poiché per un giro completo:

$$
\Delta \theta = 2\pi
$$

allora:

$$
\omega = \frac{2\pi}{T}
$$

---

### Svolgimento

$$
\omega = \frac{2\pi}{24 \cdot 3600}
$$

$$
\omega = \frac{2\pi}{86400}
$$

$$
\omega \approx 7.27 \cdot 10^{-5} \ rad/s
$$

---

### Risultato

$$
\omega \approx 7.27 \cdot 10^{-5} \ rad/s
$$

Questa è la velocità angolare della Terra nella sua rotazione attorno al proprio asse.

---

### Nota importante

La formula:

$$
\omega = \frac{2\pi}{T}
$$

si usa quando un corpo compie un giro completo in un tempo chiamato **periodo**.

Il periodo $T$ è il tempo necessario per completare una rotazione intera.

## Esercizio 4 - Velocità angolare della Terra

### Testo
La Terra ruota attorno al proprio asse. Calcolare la sua velocità angolare, assumendo che sia costante.

---

### Dati

La Terra compie una rotazione completa in un giorno:

$$
T = 24h
$$

Una rotazione completa corrisponde a:

$$
\Delta \theta = 2\pi \ rad
$$

Convertiamo il periodo in secondi:

$$
T = 24 \cdot 3600
$$

$$
T = 86400 \ s
$$

---

### Formula

La velocità angolare è:

$$
\omega = \frac{\Delta \theta}{T}
$$

Poiché per un giro completo:

$$
\Delta \theta = 2\pi
$$

allora:

$$
\omega = \frac{2\pi}{T}
$$

---

### Svolgimento

$$
\omega = \frac{2\pi}{24 \cdot 3600}
$$

$$
\omega = \frac{2\pi}{86400}
$$

$$
\omega \approx 7.27 \cdot 10^{-5} \ rad/s
$$

---

### Risultato

$$
\omega \approx 7.27 \cdot 10^{-5} \ rad/s
$$

Questa è la velocità angolare della Terra nella sua rotazione attorno al proprio asse.

---

### Nota importante

La formula:

$$
\omega = \frac{2\pi}{T}
$$

si usa quando un corpo compie un giro completo in un tempo chiamato **periodo**.

Il periodo $T$ è il tempo necessario per completare una rotazione intera.
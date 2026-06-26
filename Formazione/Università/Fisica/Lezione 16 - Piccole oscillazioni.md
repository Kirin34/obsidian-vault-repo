# Lezione 16 — Molle in serie e in parallelo

## Molle in serie

Due molle sono **in serie** quando sono collegate una dopo l’altra e sostengono lo stesso corpo.

In questa configurazione la **forza elastica è la stessa in entrambe le molle**, perché entrambe devono equilibrare il peso del corpo:

$$
F_1 = F_2 = mg
$$

Quindi:

$$
k_1 \Delta x_1 = k_2 \Delta x_2 = mg
$$

Gli allungamenti delle due molle sono diversi e valgono:

$$
\Delta x_1 = \frac{mg}{k_1}
$$

$$
\Delta x_2 = \frac{mg}{k_2}
$$

L’allungamento totale è:

$$
\Delta x = \Delta x_1 + \Delta x_2
$$

La costante elastica equivalente di due molle in serie è:

$$
\frac{1}{k} = \frac{1}{k_1} + \frac{1}{k_2}
$$

oppure:

$$
k = \frac{k_1 k_2}{k_1 + k_2}
$$

### Esempio

Dati:

$$
m = 6.5 \ kg
$$

$$
k_1 = 370 \ N/m
$$

$$
k_2 = 520 \ N/m
$$

Gli allungamenti sono:

$$
\Delta x_1 = \frac{mg}{k_1} = 0.17 \ m
$$

$$
\Delta x_2 = \frac{mg}{k_2} = 0.12 \ m
$$

La costante equivalente è:

$$
k = \frac{k_1 k_2}{k_1 + k_2}
$$

$$
k = 216 \ N/m
$$

Quindi, in serie:

- la forza è la stessa;
- gli allungamenti sono diversi;
- la costante equivalente è minore delle singole costanti.

---

## Molle in parallelo

Due molle sono **in parallelo** quando sostengono insieme lo stesso corpo e sono collegate allo stesso piano.

In questo caso le molle subiscono lo **stesso allungamento**:

$$
\Delta x_1 = \Delta x_2 = \Delta x
$$

Le forze elastiche invece si sommano:

$$
F_1 + F_2 = mg
$$

quindi:

$$
k_1 \Delta x + k_2 \Delta x = mg
$$

Raccogliendo:

$$
(k_1 + k_2)\Delta x = mg
$$

Da cui:

$$
\Delta x = \frac{mg}{k_1 + k_2}
$$

La costante elastica equivalente delle molle in parallelo è:

$$
k = k_1 + k_2
$$

### Esempio

Dati:

$$
m = 3.5 \ kg
$$

$$
k_1 = 250 \ N/m
$$

$$
k_2 = 320 \ N/m
$$

L’allungamento comune è:

$$
\Delta x = \frac{mg}{k_1 + k_2}
$$

$$
\Delta x = 0.060 \ m
$$

La costante equivalente è:

$$
k = k_1 + k_2
$$

$$
k = 570 \ N/m
$$

Quindi, in parallelo:

- l’allungamento è lo stesso;
- le forze elastiche si sommano;
- la costante equivalente è maggiore delle singole costanti.

---

## Differenza fondamentale

| Configurazione | Forza | Allungamento | Costante equivalente |
|---|---|---|---|
| Molle in serie | Uguale per tutte | Diverso | $\frac{1}{k} = \frac{1}{k_1} + \frac{1}{k_2}$ |
| Molle in parallelo | Si somma | Uguale | $k = k_1 + k_2$ |

In breve:

- **Serie**: stessa forza, allungamenti diversi.
- **Parallelo**: stesso allungamento, forze sommate.
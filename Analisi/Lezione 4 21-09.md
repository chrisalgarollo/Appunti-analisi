## Insiemi Limitati e Illimitati nei Numeri Razionali

### Definizione di insieme limitato

- Un sottoinsieme $X \subseteq \mathbb{Q}$ si dice **limitato** se è interamente contenuto in un intervallo di numeri razionali.
- Indifferenza della tipologia di intervallo: è irrilevante specificare se l'intervallo sia aperto, chiuso, semiaperto o semichiuso. Un intervallo aperto è contenuto in un intervallo chiuso (ampliando minimamente gli estremi) e un intervallo chiuso è contenuto in un intervallo aperto un po' più grande.

### Proprietà degli insiemi limitati e illimitati

- Ogni intervallo limitato è contenuto in se stesso ed è pertanto un **insieme limitato**.
- Ogni **insieme finito** di punti in $\mathbb{Q}$ è limitato: presi il valore minimo ed il valore massimo tra i suoi elementi, tutti i punti sono racchiusi nell'intervallo $[\min, \max]$.
- **Unioni finite** di insiemi limitati costituiscono insiemi limitati.
- L'insieme dei numeri razionali ($\mathbb{Q}$), l'insieme dei numeri naturali ($\mathbb{N}$) e l'insieme dei numeri interi ($\mathbb{Z}$) costituiscono esempi di **insiemi illimitati**.

---

## Funzione Modulo (Valore Assoluto) e Distanza Euclidea

### Definizione di valore assoluto

- La **funzione modulo** (o **valore assoluto**) sui numeri razionali associa ad ogni $q \in \mathbb{Q}$ un valore non negativo secondo la legge: $$
|q| := \begin{cases} q & \text{se } q > 0, &  \ 0 & \text{se } q = 0, &  \ -q & \text{se } q < 0 \end{cases}\}
$$
- Notazione: si indica con la barra verticale $|q|$ e si legge **modulo di $q$**.
- Grafico della funzione: ha una forma a "V" nel piano cartesiano passante per l'origine $(0,0)$.

### Proprietà del modulo

1. **Non negatività**: $|q| \ge 0$ per ogni $q \in \mathbb{Q}$.
2. **Annullamento**: $|q| = 0 \iff q = 0$.
3. **Parità**: $|-q| = |q|$ per ogni $q \in \mathbb{Q}$.
4. **Disuguaglianza triangolare** per il modulo: $$
|x + y| \le |x| + |y| \quad \forall x, y \in \mathbb{Q}
$$

### Distanza Euclidea e Disuguaglianza Triangolare per la distanza

- La **distanza euclidea** tra due punti $x, y \in \mathbb{Q}$ è definita mediante il modulo della loro differenza: $$
d(x, y) := |x - y|
$$
- Proprietà della distanza euclidea:
    - $d(x, y) \ge 0$.
    - $d(x, y) = 0 \iff x = y$ (due punti distinti si trovano a distanza strettamente positiva).
- **Disuguaglianza triangolare** per la distanza euclidea: $$
|x - y| \le |x - z| + |z - y| \quad \forall x, y, z \in \mathbb{Q}
$$
- Significato geometrico ed analitico:
    - In dimensione uno (sulla retta razionale), i tre punti $x, y, z$ giacciono sulla stessa retta e il triangolo degenera in tre segmenti. La disuguaglianza traduce il fatto che la distanza tra due punti non può superare la somma delle distanze da un terzo punto intermedio o esterno.
    - In geometria euclidea bidimensionale/tridimensionale, rappresenta la proprietà secondo cui in un triangolo la lunghezza di un lato non supera la somma delle lunghezze degli altri due.
    - Ruolo analitico: costituisce lo strumento base per stimare e maggiorare somme di quantità mantenendole non negative e semplificando l'analisi del comportamento dei limiti.

---

## Definizione e Significato Formale del Limite di una Successione

### Formulazioni equivalenti del limite

Sia $\{x_n \}_{n \ge n_0} \subseteq \mathbb{Q}$ una successione numerica e sia $L \in \mathbb{Q}$. Si dice che la successione ha **limite** $L$, oppure che **converge** al valore $L$ (in simboli $\lim_{n \to +\infty} x_n = L$ o $x_n \to L$), se si verifica una delle seguenti formulazioni equivalenti:

1. **Formulazione con disuguaglianze aperte**: $$
\forall \varepsilon > 0 , \exists N_\varepsilon \ge n_0 \quad \text{tale che} \quad \forall n > N_\varepsilon \implies L - \varepsilon < x_n < L + \varepsilon
$$
2. **Formulazione insiemistica (trappola definitivamente contenitiva)**: $$
\forall \varepsilon > 0 , \exists N_\varepsilon \ge n_0 \quad \text{tale che} \quad \{x_n \}_{n > N_\varepsilon} \subseteq (L - \varepsilon, L + \varepsilon)
$$
3. **Formulazione mediante modulo e distanza euclidea**: $$
\forall \varepsilon > 0,  \exists N_\varepsilon \ge n_0 \quad \text{tale che} \quad \forall n > N_\varepsilon \implies |x_n - L| < \varepsilon
$$ (esprime che dal tempo di soglia $N_\varepsilon$ in poi, la distanza euclidea tra $x_n$ ed $L$ è strettamente inferiore ad $\varepsilon$).

### Interpretazione analitica

- L'intervallo $(L - \varepsilon, L + \varepsilon)$ funge da **trappola** centrata in $L$ di ampiezza arbitraria $\varepsilon > 0$.
- L'indice $N_\varepsilon$ (dipendente dalla scelta di $\varepsilon$) rappresenta la **soglia temporale**: al rimpicciolirsi di $\varepsilon$, il valore di soglia $N_\varepsilon$ aumenta.
- Da quel momento in poi ($n > N_\varepsilon$), tutti gli infiniti elementi della successione rimangono definitivamente racchiusi all'interno della trappola.
- All'esterno della trappola può risiedere al più un **numero finito** di termini della successione (i primi elementi $x_{n_0}, x_{n_0+1}, \dots, x_{N_\varepsilon}$).
- Il valore $L$ funge da punto di **attrazione** per l'orbita del sistema dinamico discreto.

---

## Esempi di Verifica e di Inesistenza del Limite

### Esempio 1: Dimostrazione di convergenza per $x_n = \frac{1}{n}$

- Successione $x_n = \frac{1}{n}$ per $n \ge 1$, con candidato limite $L = 0$.
- Verifica impostata partendo dalla condizione finale: $$
\left| \frac{1}{n} - 0 \right| < \varepsilon \iff \frac{1}{n} < \varepsilon \iff n > \frac{1}{\varepsilon}
$$
- Scelta della soglia: prendendo un valore intero $N_\varepsilon > \frac{1}{\varepsilon}$, per ogni $n \ge N_\varepsilon$ si inverte la disuguaglianza ottenendo $\frac{1}{n} \le \frac{1}{N_\varepsilon} < \varepsilon$.
- Conclusione: la definizione è verificata e $\lim_{n \to +\infty} \frac{1}{n} = 0$.

### Esempio 2: Inesistenza del limite per $x_n = (-1)^n$

- Successione $x_n = (-1)^n$ per $n \in \mathbb{N}$ (sistema oscillante con orbita ${+1, -1}$).
- Analisi dei candidati limiti $L$:
    - Se $L \notin {1, -1}$: scegliendo un intervallo attorno a $L$ sufficientemente piccolo che non contenga né $+1$ né $-1$, la trappola non contiene alcun punto della successione.
    - Se $L = 1$: fissando un intervallo di ampiezza $\varepsilon < 2$ attorno a $1$, i termini ai tempi pari ($x_n = 1$) cadono nella trappola, ma i termini ai tempi dispari ($x_n = -1$) ne escono sistematicamente.
    - Se $L = -1$: per motivi speculari, i termini ai tempi dispari cadono nella trappola ma i termini ai tempi pari ne escono.
- Conclusione: nessun numero razionale $L$ attrae la successione; la successione $x_n = (-1)^n$ **non ammette limite** in $\mathbb{Q}$.

---

## Definizione di Limite Infinito

### Formulazione formale di divergenza a $+\infty$

Si dice che una successione numerica ${x_n}$ ha **limite più infinito** (in simboli $\lim_{n \to +\infty} x_n = +\infty$), se: $$
\forall M \in \mathbb{Q} , \exists N_M \in \mathbb{N} \quad \text{tale che} \quad \forall n \ge N_M \implies x_n > M
$$

- Formulazione equivalente mediante semiretta: $$
{x_n}_{n \ge N_M} \subseteq (M, +\infty)
$$
- Significato geometrico: per qualunque barriera $M$ fissata arbitrariamente (anche estremamente grande e positiva), da un certo indice $N_M$ in poi tutti i termini della successione si collocano definitivamente a destra di $M$ nella semiretta $(M, +\infty)$.
- Esempio canonico: la successione identità $x_n = n$ ammette limite $+\infty$, con soglia $N_M > M$.

---

## Invarianza del Limite per Traslazione degli Indici

### Traslazione fissa degli indici

- Per ogni $k \in \mathbb{N}$ fissato, vale l'uguaglianza: $$
\lim_{n \to +\infty} x_n = \lim_{n \to +\infty} x_{n+k}
$$
- Giustificazione: le due successioni $\{x_n \}$ e $\{x_{n+k}\}$ differiscono soltanto per i primi $k$ termini.
- Poiché il limite valuta esclusivamente il **comportamento asintotico** (ciò che avviene definitivamente all'infinito), alterare o eliminare un numero finito di termini modifica la soglia temporale $N_\varepsilon$ (traslandola di $k$), ma lascia inalterata l'esistenza e il valore del limite.

---

## Teorema sulle Proprietà Fondamentali delle Successioni Convergenti

Siano ${x_n}$ e ${y_n}$ successioni numeriche in $\mathbb{Q}$.

### Proprietà 1: Unicità del Limite

- **Enunciato**: Se il limite di una successione $\{x_n \}$ esiste in $\mathbb{Q}$, esso è **unico**.
- **Dimostrazione**:
    1. Si supponga per assurdo che la successione ammetta due limiti distinti $L_1, L_2 \in \mathbb{Q}$ con $L_1 \neq L_2$.
    2. Per definizione di limite, per ogni $\varepsilon > 0$ esistono due soglie $N_1(\varepsilon), N_2(\varepsilon) \in \mathbb{N}$ tali che: $$
\forall n > N_1(\varepsilon) \implies |x_n - L_1| < \varepsilon
$$
$$
\forall n > N_2(\varepsilon) \implies |x_n - L_2| < \varepsilon
$$
    3. Si definisca la soglia comune $N(\varepsilon) := \max(N_1(\varepsilon), N_2(\varepsilon))$.
    4. Per ogni $n > N(\varepsilon)$ valgono simultaneamente entrambe le disuguaglianze. Valutando la distanza tra i due limiti ed applicando la disuguaglianza triangolare: $$
|L_1 - L_2| = |(L_1 - x_n) + (x_n - L_2)| \le |x_n - L_1| + |x_n - L_2| < \varepsilon + \varepsilon = 2\varepsilon
$$
    5. La quantità non negativa $|L_1 - L_2|$ risulta inferiore a $2\varepsilon$ per ogni $\varepsilon > 0$.
    6. Per la **proprietà archimedea** dei numeri razionali, l'unico numero reale/razionale non negativo minore di qualsiasi quantità positiva arbitraria è lo zero: $$
|L_1 - L_2| = 0 \implies L_1 = L_2 \quad \text{(assurdo)}
$$
    7. Il limite è pertanto unico.

### Proprietà 2: Limitatezza delle Successioni Convergenti

- **Enunciato**: Se una successione $\{x_n \}$ converge a un limite $L \in \mathbb{Q}$, allora la successione $\{x_n \}$ è **limitata**.
- **Dimostrazione**:
    1. Si applichi la definizione di limite fissando la scelta arbitraria $\varepsilon = 1$.
    2. Esiste una soglia $N_1 \in \mathbb{N}$ tale che per tutti gli indici $n \ge N_1$ si ha $x_n \in (L - 1, L + 1)$.
    3. L'insieme di tutti i valori della successione si scompone nell'unione di due sottoinsiemi: $$
\{x_n \}_{n \in \mathbb{N}} = {x_0, x_1, \dots, x_{N_1 - 1}} \cup \{x_n \}_{n \ge N_1}
$$
    4. Il primo sottoinsieme ${x_0, \dots, x_{N_1 - 1}}$ è **finito** e dunque limitato (racchiuso tra il suo minimo e il suo massimo).
    5. Il secondo sottoinsieme $\{x_n \}_{n \ge N_1}$ è contenuto nell'intervallo $(L - 1, L + 1)$ ed è dunque **limitato** per definizione.
    6. Poiché l'unione di due insiemi limitati è un insieme limitato, la successione $\{x_n \}$ è limitata.

### Proprietà 3: Limite della Somma

- **Enunciato**: Se $\lim_{n \to +\infty} x_n = L_1$ e $\lim_{n \to +\infty} y_n = L_2$, allora la successione somma ${x_n + y_n}$ converge e vale: $$
\lim_{n \to +\infty} (x_n + y_n) = L_1 + L_2 = \lim_{n \to +\infty} x_n + \lim_{n \to +\infty} y_n
$$
- **Dimostrazione**:
    1. Si valuti la distanza tra il termine generico $(x_n + y_n)$ e il candidato limite $(L_1 + L_2)$.
    2. Riorganizzando i termini ed applicando la disuguaglianza triangolare: $$
|(x_n + y_n) - (L_1 + L_2)| = |(x_n - L_1) + (y_n - L_2)| \le |x_n - L_1| + |y_n - L_2|
$$
    3. Fissato $\varepsilon > 0$, dalle ipotesi di convergenza esistono $N_1, N_2 \in \mathbb{N}$ tali che: $$
\forall n > N_1 \implies |x_n - L_1| < \varepsilon, \quad \forall n > N_2 \implies |y_n - L_2| < \varepsilon
$$
    4. Scegliendo $N := \max(N_1, N_2)$, per ogni $n > N$ la somma delle due distanze rispetta: $$
|(x_n + y_n) - (L_1 + L_2)| < \varepsilon + \varepsilon = 2\varepsilon
$$
    5. Per l'arbitrarietà di $\varepsilon > 0$, si conclude che $\lim_{n \to +\infty} (x_n + y_n) = L_1 + L_2$.

### Proprietà 4: Limite del Prodotto

- **Enunciato**: Se $\lim_{n \to +\infty} x_n = L_1$ e $\lim_{n \to +\infty} y_n = L_2$, allora la successione prodotto ${x_n \cdot y_n}$ converge e vale: $$
\lim_{n \to +\infty} (x_n \cdot y_n) = L_1 \cdot L_2 = \left(\lim_{n \to +\infty} x_n\right) \cdot \left(\lim_{n \to +\infty} y_n\right)
$$
- **Dimostrazione**:
    1. Si consideri il modulo della differenza $|x_n y_n - L_1 L_2|$.
    2. Si aggiunga e si sottragga la quantità intermedia $L_1 y_n$ all'interno del modulo: $$
|x_n y_n - L_1 L_2| = |(x_n y_n - L_1 y_n) + (L_1 y_n - L_1 L_2)| = |y_n (x_n - L_1) + L_1 (y_n - L_2)|
$$
    3. Applicando la disuguaglianza triangolare e la proprietà del modulo del prodotto: $$
|x_n y_n - L_1 L_2| \le |y_n| \cdot |x_n - L_1| + |L_1| \cdot |y_n - L_2|
$$
    4. Poiché la successione ${y_n}$ converge al limite $L_2$, per la Proprietà 2 essa è **limitata**: esiste una costante $M \ge 0$ tale che $|y_n| \le M$ per ogni $n \in \mathbb{N}$.
    5. Sostituendo la maggiorazione $|y_n| \le M$: $$
|x_n y_n - L_1 L_2| \le M \cdot |x_n - L_1| + |L_1| \cdot |y_n - L_2|
$$
    6. Fissato $\varepsilon > 0$, esistono $N_1, N_2$ tali che per $n > N_1 \implies |x_n - L_1| < \varepsilon$ e per $n > N_2 \implies |y_n - L_2| < \varepsilon$.
    7. Posto $N := \max(N_1, N_2)$, per tutti gli indici $n > N$ si ottiene: $$
|x_n y_n - L_1 L_2| < M \cdot \varepsilon + |L_1| \cdot \varepsilon = (M + |L_1|) \cdot \varepsilon
$$
    8. Poiché la quantità $(M + |L_1|) \cdot \varepsilon$ è arbitrariamente piccola al variare di $\varepsilon$, ne segue che $\lim_{n \to +\infty} (x_n \cdot y_n) = L_1 \cdot L_2$.

### Proprietà 5: Limite del Quoziente

- **Enunciato**: Se $\lim_{n \to +\infty} x_n = L_1$ e $\lim_{n \to +\infty} y_n = L_2$ con $L_2 \neq 0$, allora la successione quoziente $\frac{x_n}{y_n}$ converge e vale: $$
\lim_{n \to +\infty} \frac{x_n}{y_n} = \frac{L_1}{L_2} = \frac{\lim_{n \to +\infty} x_n}{\lim_{n \to +\infty} y_n}
$$
- Nota: La dimostrazione discende dalla combinazione della proprietà del prodotto con il limite della successione reciproca $\left{\frac{1}{y_n}\right}$.

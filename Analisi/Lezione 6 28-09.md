## Completamento della Costruzione dei Numeri Reali ($\mathbb{R}$)

### Richiamo delle successioni di Cauchy e della relazione di equivalenza

- Si consideri l'insieme $\mathcal{C}$ di tutte le **successioni di Cauchy** di numeri razionali ${q_n} \subseteq \mathbb{Q}$.
- Ricordo della condizione di Cauchy in $\mathbb{Q}$: $$
\forall \varepsilon > 0 (\in \mathbb{Q}) , \exists N_\varepsilon \in \mathbb{N} \quad \text{tale che} \quad \forall m, n \ge N_\varepsilon \implies |q_m - q_n| < \varepsilon
$$ (esprime il fatto che i termini della successione si accumulano e si concentrano su se stessi).
- **Relazione di equivalenza** ($\sim$) definita sull'insieme $\mathcal{C}$: $$
{x_n} \sim {y_n} \iff \lim_{n \to +\infty} (x_n - y_n) = 0
$$
    - Interpretazione: due successioni di Cauchy equivalenti costituiscono due diverse approssimazioni razionali del medesimo numero reale.
    - La scrittura $\lim_{n \to +\infty} (x_n - y_n) = 0$ è ben definita in $\mathbb{Q}$ poiché $0 \in \mathbb{Q}$, a differenza della scrittura separata dei singoli limiti che non sempre esistono in $\mathbb{Q}$.
- Definizione dell'insieme dei **numeri reali** ($\mathbb{R}$) come **insieme quoziente**: $$
\mathbb{R} := \mathcal{C} / \sim
$$
    - Un **numero reale** $r \in \mathbb{R}$ è una classe di equivalenza di successioni di Cauchy razionali: $r = [\{q_n\}]$.
- **Immersione dei numeri razionali** ($\mathbb{Q}$) in $\mathbb{R}$:
    - Definita tramite la funzione iniettiva $f: \mathbb{Q} \to \mathbb{R}$ che associa ad ogni $q \in \mathbb{Q}$ la classe di equivalenza della successione costante $q_n = q$: $$
f(q) := [{q, q, q, \dots}]
$$
    - L'iniettività permette l'identificazione insiemistica ed algebrica di $\mathbb{Q}$ come sottoinsieme proprio di $\mathbb{R}$ ($\mathbb{Q} \subset \mathbb{R}$), identificando la classe $[{q}]$ semplicemente con il numero razionale $q$.

### Estensione delle operazioni algebriche

Siano $x = [\{x_n\}]$ e $y = [\{y_n\}]$ due numeri reali rappresentati dalle rispettive successioni di Cauchy razionali.

- **Somma tra numeri reali**: $$
x + y := [\{x_n + y_n\}]
$$
- **Prodotto tra numeri reali**: $$
x \cdot y := [\{x_n \cdot y_n\}]
$$
- **Verifica della buona definizione**:
    - Se ${x_n} \sim {x'_n}$ e ${y_n} \sim {y'_n}$ (ovvero $x_n - x'_n \to 0$ e $y_n - y'_n \to 0$), allora: $$
\lim_{n \to +\infty} [(x_n + y_n) - (x'_n + y'_n)] = \lim_{n \to +\infty} [(x_n - x'_n) + (y_n - y'_n)] = 0 + 0 = 0
$$
    - Di conseguenza, la classe della successione somma $[{x_n + y_n}]$ coincide con $[{x'_n + y'_n}]$ ed è indipendente dai particolari rappresentanti scelti.
    - Analogamente, la buona definizione del prodotto discende dalla limitatezza delle successioni di Cauchy.
- Conservazione delle proprietà algebriche: le operazioni estese conservano le proprietà commutative, associative, distributive e la presenza degli elementi neutri ($0$ per la somma e $1$ per il prodotto).

### Estensione del modulo, della distanza euclidea e dell'ordinamento su $\mathbb{R}$

- **Modulo di un numero reale**:
    - Sia $r = [\{q_n\}] \in \mathbb{R}$. Si definisce **modulo** (o **valore assoluto**) del numero reale $r$ la classe di equivalenza della successione dei moduli: $$
|r| := [\{|q_n|\}]
$$
    - Verificazione della buona definizione: discende dalla seguente disuguaglianza (conseguenza della disuguaglianza triangolare): $$
||a| - |b|| \le |a - b|
$$ Se ${q_n} \sim {q'_n}$ (cioè $|q_n - q'_n| \to 0$), allora $||q_n| - |q'_n|| \le |q_n - q'_n| \to 0$, garantendo che ${|q_n|} \sim {|q'_n|}$.
- **Distanza Euclidea tra numeri reali**:
    - Dati $X, Y \in \mathbb{R}$, la **distanza euclidea** è definita mediante il modulo della loro differenza: $$
d(X, Y) := |X - Y|
$$
- **Definizione di numero reale positivo e ordinamento**:
    - Un numero reale $R \in \mathbb{R}$ con $R \neq 0$ si dice **positivo** ($R > 0$) se coincide con il suo modulo: $$
R \neq 0 \quad \text{e} \quad |R| = R
$$
    - Formulazione mediante successioni rappresentanti: se $R = [{q_n}]$, il numero è positivo se $R \neq 0$ e la differenza tra la successione e il suo modulo è infinitesima ($\lim_{n \to +\infty} (|q_n| - q_n) = 0$), il che equivale a richiedere che la successione sia definitivamente positiva (i termini negativi tendono a zero).
    - Ordinamento tra numeri reali: $X > Y \iff X - Y > 0$.

---

## Densità dei Numeri Razionali nei Numeri Reali

### Teorema di Densità di $\mathbb{Q}$ in $\mathbb{R}$

- **Enunciato**: L'insieme dei numeri razionali $\mathbb{Q}$ è **denso** nei numeri reali $\mathbb{R}$. Ovvero, per ogni numero reale $R \in \mathbb{R}$ e per ogni numero razionale strettamente positivo $\varepsilon > 0$, esiste un numero razionale $q \in \mathbb{Q}$ tale che la loro distanza sia inferiore ad $\varepsilon$: $$
|R - q| < \varepsilon
$$
- Significato geometrico: in ogni intorno simmetrico o intervallo di semiampiezza $\varepsilon > 0$ centrato attorno a un qualunque numero reale $R$, cade almeno un numero razionale $q$.

### Dimostrazione del Teorema di Densità

1. Sia $R = [\{q_n\}] \in \mathbb{R}$ la classe di equivalenza della successione di Cauchy razionale ${q_n}$.
2. Per definizione di successione di Cauchy, fissato un numero razionale $\varepsilon > 0$, esiste una soglia $N_\varepsilon \in \mathbb{N}$ tale che: $$
\forall m, n \ge N_\varepsilon \implies |q_m - q_n| < \varepsilon
$$
3. Si scelga come numero razionale fissato $q := q_{N_\varepsilon} \in \mathbb{Q}$ (ovvero il termine della successione valutato all'indice di soglia $N_\varepsilon$).
4. Consideriamo la distanza tra il numero reale $R$ e il numero razionale $q$ (rappresentato dalla successione costante ${q}\sim {q_{N_\varepsilon}}$).
5. La differenza $R - q$ è rappresentata dalla successione razionale ${q_n - q_{N_\varepsilon}}_{n \in \mathbb{N}}$.
6. Per il modulo di un numero reale, il valore $|R - q|$ è la classe della successione ${|q_n - q_{N_\varepsilon}|}_{n \in \mathbb{N}}$.
7. Poiché per tutti gli indici $n \ge N_\varepsilon$ vale la disuguaglianza $|q_n - q_{N_\varepsilon}| < \varepsilon$, la successione risulta definitivamente minorata dalla costante $\varepsilon$.
8. Passando al limite/classe di equivalenza nei reali, si ottiene $|R - q| \le \varepsilon < 2\varepsilon$.
9. Per l'arbitrarietà di $\varepsilon > 0$, esiste un numero razionale $q$ arbitrariamente vicino ad $R$.

---

## Limiti e Convergenza nelle Successioni Reali

### Definizione di limite per successioni reali

Sia $\{x_n\}_{n \in \mathbb{N}} \subseteq \mathbb{R}$ una successione di numeri reali e sia $L \in \mathbb{R}$. Si dice che la successione ha **limite** $L$, oppure **converge** ad $L$ (in simboli $\lim_{n \to +\infty} X_n = L$), se: $$
\forall \varepsilon > 0 (\in \mathbb{Q}) , \exists N_\varepsilon \in \mathbb{N} \quad \text{tale che} \quad \forall n \ge N_\varepsilon \implies |x_n - L| < \varepsilon
$$

- La struttura logica della definizione è identica a quella nei numeri razionali, con la differenza che la distanza $|x_n - L|$ valuta la distanza tra numeri reali.

### Convergenza delle successioni di Cauchy razionali nei numeri reali

- **Teorema**: Ogni successione di Cauchy di numeri razionali ${q_n} \in \mathcal{C}$ converge, all'interno dell'insieme dei numeri reali $\mathbb{R}$, esattamente al numero reale rappresentato dalla sua classe di equivalenza $L = [\{q_n\}] \in \mathbb{R}$: $$
\lim_{n \to +\infty} q_n = L = [\{q_n\}]
$$
- **Dimostrazione**:
    1. Si consideri la successione razionale di Cauchy $\{q_n\}$ e la sua classe di equivalenza $L = [\{q_n\}] \in \mathbb{R}$.
    2. Fissato un arbitrario $\varepsilon > 0$, esiste una soglia $N_\varepsilon \in \mathbb{N}$ tale che per $m, n \ge N_\varepsilon \implies |q_m - q_n| < \varepsilon$.
    3. Per un indice $m \ge N_\varepsilon$ fissato, si valuti la distanza tra il numero razionale $q_m$ (inteso come numero reale rappresentato dalla successione costante $q_m$) ed il numero reale $L = [\{q_n\}]$.
    4. Tale distanza reale $|q_m - L|$ è la classe della successione $\{|q_m - q_n|\}_{n \in \mathbb{N}}$.
    5. Poiché per $n \ge N_\varepsilon$ si ha definitivamente $|q_m - q_n| < \varepsilon$, la classe rappresenta un numero reale minore o uguale ad $\varepsilon$: $$
\forall m \ge N_\varepsilon \implies |q_m - L| \le \varepsilon
$$
    6. Per l'arbitrarietà di $\varepsilon > 0$, la definizione di limite nei reali è soddisfatta e $\lim_{m \to +\infty} q_m = L$.
- **Risoluzione delle equazioni algebriche nei reali**:
    - Applicando questo risultato alla successione ricorsiva $x_{0} = 2, , x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n}$ (dimostrata essere di Cauchy in $\mathbb{Q}$), la successione converge nei numeri reali al limite reale $L = [{x_n}] \in \mathbb{R}$.
    - Dal limite della relazione di ricorrenza discende $L^2 = 2$, dimostrando che l'equazione $x^2 = 2$ ammette la soluzione reale $L = \sqrt{2} \in \mathbb{R}$.

---

## La Proprietà di Completezza dei Numeri Reali

### Definizione di successione di Cauchy nei numeri reali

- Una successione di numeri reali $\{x_n\} \subseteq \mathbb{R}$ si dice **successione di Cauchy** in $\mathbb{R}$ se: $$
\forall \varepsilon > 0 (\in \mathbb{Q}) , \exists N_\varepsilon \in \mathbb{N} \quad \text{tale che} \quad \forall m, n \ge N_\varepsilon \implies |x_m - x_n| < \varepsilon
$$ dove $|x_m - x_n|$ rappresenta la distanza euclidea tra i due numeri reali $x_m$ ed $x_n$.

### Teorema di Completezza di $\mathbb{R}$

- **Enunciato**: Una successione di numeri reali $\{x_n\} \subseteq \mathbb{R}$ è convergente in $\mathbb{R}$ se e solo se è una **successione di Cauchy**.
- In $\mathbb{R}$, la proprietà di Cauchy è condizione **necessaria e sufficiente** per la convergenza.
- Vantaggio analitico: la condizione di Cauchy permette di verificare la convergenza di una successione reale basandosi esclusivamente sulle relazioni tra i suoi termini, senza dover conoscere a priori il valore del limite.

### Dimostrazione della sufficienza della condizione di Cauchy nei reali

1. Sia $\{x_n\} \subseteq \mathbb{R}$ una successione di Cauchy di numeri reali.
2. Per il **Teorema di densità dei razionali**, per ogni termine reale $x_n$ scelga un numero razionale $q_n \in \mathbb{Q}$ distante meno di $\frac{1}{n}$ da $x_n$: $$
\forall n \ge 1 \implies |x_n - q_n| < \frac{1}{n}
$$
3. Si dimostra che la successione di numeri razionali $\{q_n\}$ così costruita è una **successione di Cauchy** in $\mathbb{Q}$. Presi due indici $m, n \ge N_\varepsilon$ ed applicando la disuguaglianza triangolare: $$
|q_m - q_n| = |(q_m - x_m) + (x_m - x_n) + (x_n - q_n)| \le |q_m - x_m| + |x_m - x_n| + |x_n - q_n|
$$
$$
|q_m - q_n| < \frac{1}{m} + |x_m - x_n| + \frac{1}{n}
$$ Scegliendo l'indice di soglia $N_1$ opportunamente grande per cui $\frac{1}{m} < \varepsilon$, $\frac{1}{n} < \varepsilon$ e $|x_m - x_n| < \varepsilon$ (poiché ${x_n}$ è di Cauchy nei reali): $$
|q_m - q_n| < \varepsilon + \varepsilon + \varepsilon = 3\varepsilon
$$ Dunque $\{q_n\}$ è una successione di Cauchy razionale (${q_n} \in \mathcal{C}$).
4. Per il teorema precedente sulle successioni di Cauchy razionali, la successione ${q_n}$ converge ad un limite reale $L = [\{q_n\}] \in \mathbb{R}$: $$
\lim_{n \to +\infty} q_n = L
$$
5. Si dimostra infine che la successione reale iniziale ${x_n}$ converge al medesimo limite reale $L$. Valutando la distanza tra $x_n$ ed $L$ tramite la disuguaglianza triangolare: $$
|x_n - L| \le |x_n - q_n| + |q_n - L|
$$
6. Poiché $|x_n - q_n| < \frac{1}{n} < \varepsilon$ (definitivamente) e $|q_n - L| < \varepsilon$ (per la convergenza di $q_n \to L$), per indici $n$ maggiori di un'opportuna soglia $N_3$ si ottiene: $$
|x_n - L| < \varepsilon + \varepsilon = 2\varepsilon
$$
7. Per l'arbitrarietà di $\varepsilon > 0$, si conclude che la successione reale $\{x_n\}$ converge in $\mathbb{R}$ al limite $L$: $$
\lim_{n \to +\infty} x_n = L
$$

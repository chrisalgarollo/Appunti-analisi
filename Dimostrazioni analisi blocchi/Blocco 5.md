# **Modulo 2: Limiti e Funzioni Continue**

---

### **Teorema 1: Continuità della Funzione Composta**

#### **Enunciato Formale**

- **Ipotesi ($H$)**:
    1. Sia $f: D_f \to \mathbb{R}$ una funzione continua nel punto $x_0 \in D_f$, ovvero $\lim_{x \to x_0} f(x) = f(x_0) =: y_0$.
    2. Sia $g: D_g \to \mathbb{R}$ una funzione continua nel punto $y_0 \in D_g$, ovvero $\lim_{y \to y_0} g(y) = g(y_0)$, con $\text{Im}(f) \subseteq D_g$.
- **Tesi ($T$)**: La funzione composta $(g \circ f)(x) := g(f(x))$ è **continua nel punto $x_0$**, ossia: $$
\lim_{x \to x_0} g(f(x)) = g(f(x_0))
$$

#### **Idea Chiave della Dimostrazione**

Si concatenano le definizioni di continuità $\varepsilon-\delta$: fissata una tolleranza $\varepsilon > 0$ per la funzione esterna $g$, si individua un raggio $\delta > 0$ attorno a $y_0$. Tale raggio viene riutilizzato come nuova tolleranza $\varepsilon' := \delta$ per la funzione interna $f$, ottenendo un raggio $\delta' > 0$ attorno a $x_0$ che garantisce il controllo dello scarto finale.

#### **Dimostrazione Dettagliata**

1. Si fissi una tolleranza arbitraria $\varepsilon > 0$.
2. Per l'ipotesi di continuità di $g$ nel punto $y_0 = f(x_0)$, in corrispondenza di $\varepsilon$ esiste un raggio $\delta > 0$ tale che: $$
\forall y \in D_g, \quad |y - y_0| < \delta \implies |g(y) - g(y_0)| < \varepsilon
$$
3. Si consideri ora la continuità della funzione interna $f$ nel punto $x_0$. Scegliendo come tolleranza la quantità positiva $\varepsilon' := \delta > 0$, esiste un raggio $\delta' > 0$ tale che: $$
\forall x \in D_f, \quad |x - x_0| < \delta' \implies |f(x) - f(x_0)| < \delta
$$
4. Si concatenino le due implicazioni ponendo $y = f(x) \in D_g$: per ogni $x \in D_f$ che soddisfa $|x - x_0| < \delta'$, il suo valore immagine soddisfa $|f(x) - y_0| < \delta$, il che a sua volta garantisce che: $$
|g(f(x)) - g(f(x_0))| < \varepsilon
$$
5. Per l'arbitrarietà di $\varepsilon > 0$, la definizione di limite per la funzione composta è verificata e si conclude che: $$
\lim_{x \to x_0} g(f(x)) = g(f(x_0))
$$

#### **Punti Critici / Errori Tipici all'Orale**

- **Distinzione tra Continuità e Teorema Generale del Limite della Composta**: Se si valuta un semplice limite $\lim_{x \to x_0} g(f(x))$ in cui $g$ **non è continua** in $y_0$, occorre l'ipotesi aggiuntiva che $f(x) \neq y_0$ definitivamente per $x \neq x_0$. L'ipotesi di **continuità** di $g$ nel punto $y_0$ elimina la necessità di richiedere che $f(x) \neq y_0$, rendendo il teorema sempre valido.
- **Inclusione dei Domini**: Ricordare sempre di menzionare l'ipotesi di ammissibilità della composizione: $\text{Im}(f) \subseteq D_g$.

#### **Esercizio / Domanda di Verifica**

_Siano $f(x) = x^2 - 1$ e $g(y) = \sqrt{y}$. Verificare la continuità della funzione composta $(g \circ f)(x) = \sqrt{x^2 - 1}$ nel punto $x_0 = 2$, specificando i domini coinvolti._

---

### **Teorema 2: Teorema di Weierstrass sull'Esistenza di Estremi Assoluti**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia $f: [a, b] \to \mathbb{R}$ una funzione **continua** definita su un intervallo **chiuso e limitato** $[a, b] \subset \mathbb{R}$.
- **Tesi ($T$)**: La funzione $f$ ammette **massimo assoluto** (globale) e **minimo assoluto** (globale) in $[a, b]$. Ovvero esistono due punti $x_m, x_M \in [a, b]$ tali che: $$
f(x_m) \le f(x) \le f(x_M) \quad \forall x \in [a, b]
$$ I valori $m := f(x_m) = \min_{x \in [a,b]} f(x)$ e $M := f(x_M) = \max_{x \in [a,b]} f(x)$ sono reali e finiti.

#### **Idea Chiave della Dimostrazione**

Si pone $M := \sup \text{Im}(f)$ e si costruisce una successione $y_n \in \text{Im}(f)$ tale che $y_n \to M$. Per ciascun $y_n$ si individua una controimmagine $x_n \in [a, b]$. Essendo $[a, b]$ limitato, per il **Teorema di Bolzano-Weierstrass** esiste una sottosuccessione $x_{n_k}$ convergente a un punto $x_M \in [a, b]$. Per la continuità di $f$, $f(x_M) = \lim f(x_{n_k}) = M$, dimostrando che l'estremo superiore è finito ed è il massimo assoluto.

#### **Dimostrazione Dettagliata**

1. Si definisca $M := \sup_{x \in [a,b]} f(x) = \sup \text{Im}(f) \in \mathbb{R} \cup {+\infty}$ l'estremo superiore dell'immagine di $f$.
2. Per le proprietà dell'estremo superiore, per ogni $n \in \mathbb{N}^*$ esiste un valore $y_n \in \text{Im}(f)$ tale che $M - \frac{1}{n} < y_n \le M$, il che implica: $$
\lim_{n \to +\infty} y_n = M
$$
3. Per definizione di immagine, per ogni $y_n$ esiste almeno un punto $x_n \in [a, b]$ tale che $f(x_n) = y_n$. Si ottiene così una successione ${x_n}_{n \in \mathbb{N}^*} \subseteq [a, b]$.
4. Si distinguono due casi per l'insieme dei valori della successione ${y_n}$:
    - **Caso 1 (Insieme dei valori di $y_n$ finito)**: La successione ${y_n}$ è definitivamente costante $y_n = M$. Esiste quindi un punto $x_M \in [a, b]$ tale che $f(x_M) = M$, dimostrando che l'estremo superiore è appartenente all'immagine ed è un massimo finito.
    - **Caso 2 (Insieme dei valori di $y_n$ infinito)**: La successione di punti ${x_n} \subseteq [a, b]$ costituisce un insieme infinito e limitato.
5. Per il **Teorema di Bolzano-Weierstrass**, l'insieme ${x_n}$ ammette un punto di accumulazione $x_M \in [a, b]$ ed esiste una sottosuccessione ${x_{n_k}}$ convergente a $x_M$: $$
\lim_{k \to +\infty} x_{n_k} = x_M \in [a, b]
$$
6. Sfruttando la continuità di $f$ nel punto $x_M$ ed applicando il **Lemma di continuità per successioni** (il limite commuta con la funzione): $$
f(x_M) = f\left(\lim_{k \to +\infty} x_{n_k}\right) = \lim_{k \to +\infty} f(x_{n_k}) = \lim_{k \to +\infty} y_{n_k} = M
$$
7. Pertanto, l'estremo superiore $M$ è un numero reale finito ed appartiene all'immagine $\text{Im}(f)$, dimostrando l'esistenza del massimo assoluto $M = f(x_M) = \max_{x \in [a,b]} f(x)$.
8. La dimostrazione per l'esistenza del minimo assoluto $m = f(x_m) = \min_{x \in [a,b]} f(x)$ si conduce in modo del tutto speculare ponendo $m := \inf \text{Im}(f)$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Essenzialità delle ipotesi (Controesempi)**:
    1. _Se si rimuove la chiusura dell'intervallo_ (es. $f(x) = x$ su $(0, 1)$): $f$ è continua e limitata ma $\sup = 1 \notin \text{Im}(f)$ e $\inf = 0 \notin \text{Im}(f)$, quindi **non ammette né max né min**.
    2. _Se si rimuove la limitatezza dell'intervallo_ (es. $f(x) = x$ su $[0, +\infty)$): $f$ è continua su un intervallo chiuso ma illimitato, con $\sup = +\infty$, quindi **non ammette massimo**.
    3. _Se si rimuove la continuità di $f$_ (es. $f(x) = x - \lfloor x \rfloor$ su \(\)): La funzione è definita su un intervallo chiuso e limitato ma presenta discontinuità, quindi **non ammette massimo**.
- **Uso di Bolzano-Weierstrass**: Evidenziare all'orale che la compattezza dell'intervallo chiuso e limitato $[a, b]$ garantisce che il punto di convergenza della sottosuccessione $x_M$ ricada **all'interno di $[a, b]$** e non all'esterno.

#### **Esercizio / Domanda di Verifica**

_Si consideri la funzione $f(x) = \frac{1}{x}$ nell'intervallo $(0, 2]$. Ammette minimo assoluto? Ammette massimo assoluto? Quale ipotesi del Teorema di Weierstrass viene meno?_

---

### **Teorema 3: Teorema degli Zeri e Teorema dei Valori Intermedi**

---

#### **Parte A: Teorema degli Zeri (di Bolzano)**

##### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia $f: [a, b] \to \mathbb{R}$ una funzione **continua** su un intervallo chiuso e limitato $[a, b]$ tale che ai due estremi dell'intervallo la funzione assuma **valori di segno opposto**: $$
f(a) \cdot f(b) < 0
$$
- **Tesi ($T$)**: Esiste **almeno un punto** $x_0 \in (a, b)$ interno all'intervallo in cui la funzione si annulla: $$
f(x_0) = 0
$$

##### **Idea Chiave della Dimostrazione**

Si applica il **metodo di dicotomia**. Si dimezza ricorsivamente l'intervallo $[a, b]$ selezionando ad ogni passo la metà agli estremi della quale la funzione continua mantiene segni opposti. Le successioni monotone degli estremi sinistri e destri convergono allo stesso punto $x_0$, nel quale per permanenza del segno e continuità deve valere $[f(x_0)]^2 \le 0 \implies f(x_0) = 0$.

##### **Dimostrazione Dettagliata**

1. Si pongano $a_0 := a$ e $b_0 := b$, per cui vale $f(a_0) \cdot f(b_0) < 0$.
2. Si calcoli il punto medio $c_1 := \frac{a_0 + b_0}{2}$:
    - Se $f(c_1) = 0$, si è trovato lo zero $x_0 = c_1$ e la dimostrazione è conclusa.
    - Se $f(c_1) \neq 0$, la funzione assume segno opposto agli estremi di almeno uno dei due sottointervalli $[a_0, c_1]$ oppure $[c_1, b_0]$.
3. Si selezioni il sottointervallo agli estremi del quale $f$ assume segno opposto e lo si denoti con $[a_1, b_1]$, soddisfacendo $f(a_1) \cdot f(b_1) < 0$.
4. Reiterando il procedimento di dicotomia $k$ volte, a meno di non trovare un punto medio con valore nullo, si ottiene una successione di intervalli incapsulati $[a_k, b_k]$ tali che:
    - $[a_{k+1}, b_{k+1}] \subseteq [a_k, b_k] \subseteq \dots \subseteq [a_0, b_0]$ per ogni $k \ge 0$.
    - $f(a_k) \cdot f(b_k) < 0$ per ogni $k \ge 0$.
    - L'ampiezza dell'intervallo $k$-esimo è $b_k - a_k = \frac{b_0 - a_0}{2^k}$.
5. La successione degli estremi sinistri ${a_k}$ è **monotona crescente** e la successione degli estremi destri ${b_k}$ è **monotona decrescente**. Per il Teorema sulle successioni monotone e limitate, entrambe le successioni convergono allo stesso limite reale $x_0 \in [a, b]$: $$
\lim_{k \to +\infty} a_k = \lim_{k \to +\infty} b_k = x_0
$$
6. Passando al limite per $k \to +\infty$ nella disuguaglianza $f(a_k) \cdot f(b_k) < 0$ e sfruttando la continuità di $f$ nel punto $x_0$: $$
\lim_{k \to +\infty} [f(a_k) \cdot f(b_k)] \le 0 \implies f\left(\lim_{k \to +\infty} a_k\right) \cdot f\left(\lim_{k \to +\infty} b_k\right) \le 0 \implies [f(x_0)]^2 \le 0
$$
7. Poiché il quadrato di un numero reale non può essere strettamente negativo, ne consegue che: $$
[f(x_0)]^2 = 0 \implies f(x_0) = 0
$$ dimostrando l'esistenza dello zero $x_0 \in (a, b)$.

---

#### **Parte B: Teorema dei Valori Intermedi**

##### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia $f: [a, b] \to \mathbb{R}$ una funzione **continua** sull'intervallo chiuso e limitato $[a, b]$, e siano $m := \min_{[a,b]} f$ e $M := \max_{[a,b]} f$ i suoi valori minimo e massimo assoluti (esistenti per il Teorema di Weierstrass).
- **Tesi ($T$)**: Per ogni valore reale intermedio $\lambda \in (m, M)$, esiste **almeno un punto** $x_\lambda \in (a, b)$ tale che: $$
f(x_\lambda) = \lambda
$$ In particolare, l'immagine della funzione continua su $[a, b]$ coincide con l'intervallo chiuso e limitato compreso tra il minimo ed il massimo: $\text{Im}(f) = [m, M]$.

##### **Idea Chiave della Dimostrazione**

Si riconduce il Teorema dei Valori Intermedi al Teorema degli Zeri applicato alla funzione ausiliaria $g(x) := f(x) - \lambda$ definita nell'intervallo compreso tra il punto di minimo $x_m$ e il punto di massimo $x_M$.

##### **Dimostrazione Dettagliata**

1. Per il Teorema di Weierstrass, esistono $x_m, x_M \in [a, b]$ tali che $f(x_m) = m$ e $f(x_M) = M$.
2. Senza perdita di generalità, si assuma l'ordinamento $x_m < x_M$ (se $x_M < x_m$ la dimostrazione è speculare).
3. Si fissi un generico valore intermedio $\lambda \in (m, M)$, tale che $m < \lambda < M$.
4. Si definisca la funzione ausiliaria $g: [x_m, x_M] \to \mathbb{R}$ come: $$
g(x) := f(x) - \lambda
$$
5. La funzione $g$ è continua su $[x_m, x_M]$ in quanto differenza di funzioni continue.
6. Si valutino i valori assunti da $g$ agli estremi dell'intervallo $[x_m, x_M]$:
    - $g(x_m) = f(x_m) - \lambda = m - \lambda < 0 \quad \text{(poiché } \lambda > m\text{)}$
    - $g(x_M) = f(x_M) - \lambda = M - \lambda > 0 \quad \text{(poiché } \lambda < M\text{)}$
7. Pertanto $g(x_m) \cdot g(x_M) < 0$. Per il **Teorema degli Zeri** applicato alla funzione continua $g$ sull'intervallo $[x_m, x_M]$, esiste un punto $x_\lambda \in (x_m, x_M) \subset (a, b)$ tale che: $$
g(x_\lambda) = 0 \iff f(x_\lambda) - \lambda = 0 \iff f(x_\lambda) = \lambda
$$
8. Ciò dimostra che $f$ assume tutti i valori compresi tra $m$ ed $M$, per cui $\text{Im}(f) = [m, M]$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Immagine di un intervallo tramite funzione continua**: All'orale viene spesso chiesto: _"Qual è l'immagine di un intervallo mediante una funzione continua?"_ La risposta è **un intervallo** (proprietà di connessione).
- **Distinzione tra $f(a), f(b)$ e $m, M$**: Il Teorema dei Valori Intermedi garantisce la copertura di tutti i valori compresi tra il **minimo assoluto $m$ e il massimo assoluto $M$**, che non sempre coincidono con i valori assunti agli estremi $f(a)$ e $f(b)$.

#### **Esercizio / Domanda di Verifica**

_Dimostrare che l'equazione $e^x = 1 + 2x$ ammette almeno una soluzione reale nell'intervallo $(1, 3)$ applicando il Teorema degli Zeri alla funzione ausiliaria $f(x) = e^x - 1 - 2x$._

---

### **Fonti maggiormente utilizzate per questo Blocco**

Per la stesura rigorosa del **BLOCCO 5**, le fonti del notebook maggiormente consultate ed utilizzate sono state:

1. **`Continue.pdf`**: Fonte principale per le dimostrazioni formali del Teorema di Weierstrass (con i due casi e Bolzano-Weierstrass), del Teorema degli Zeri (metodo di dicotomia) e del Teorema dei Valori Intermedi.
2. **`Lezione 11 14-10.md`**: Utilizzata per la continuità della funzione composta, la continuità per successioni e la continuità delle funzioni elementari e trigonometriche.
3. **`AMI 2026-27 Programma Teoremi Dimostarzioni.pdf`**: Utilizzato per la verifica del perfetto allineamento con i punti 3, 4, 5 e 6 della sezione _Limiti e funzioni continue_ del programma d'esame.

---

Dimmi pure se la trattazione del **BLOCCO 5** è chiara e se possiamo passare al **Modulo 3: Calcolo Differenziale (BLOCCO 6: Basi del calcolo differenziale: Lemma del Resto, Continuità delle derivabili, Prodotto e Composta)**.

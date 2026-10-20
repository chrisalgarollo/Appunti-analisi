## Proprietà Algebriche dei Limiti e della Continuità di Funzioni

### Algebra dei limiti per funzioni

Se esiste il limite di una funzione per x che tende a x0, esso è unico. Se esiste limite di una funz per 
Siano $f, g: D \to \mathbb{R}$ due funzioni definite su un dominio $D \subseteq \mathbb{R}$ e sia $x_0 \in \mathbb{R}$ un **punto di accumulazione** per $D$. Se esistono i limiti finiti: $$
\lim_{x \to x_0} f(x) = L_1 \in \mathbb{R}, \quad \lim_{x \to x_0} g(x) = L_2 \in \mathbb{R}
$$ valgono le seguenti proprietà:

1. **Limite della somma**: $$
\lim_{x \to x_0} (f(x) + g(x)) = L_1 + L_2 = \lim_{x \to x_0} f(x) + \lim_{x \to x_0} g(x)
$$
2. **Limite del prodotto**: $$
\lim_{x \to x_0} (f(x) \cdot g(x)) = L_1 \cdot L_2 = \left(\lim_{x \to x_0} f(x)\right) \cdot \left(\lim_{x \to x_0} g(x)\right)
$$
3. **Limite del quoziente**: se $L_2 \neq 0$, allora: $$
\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{L_1}{L_2} = \frac{\lim_{x \to x_0} f(x)}{\lim_{x \to x_0} g(x)}
$$

- Le dimostrazioni di tali proprietà omologhe a quelle per le successioni numeriche non vengono ripetute poiché ne ricalcano esattamente la struttura logica (sostituendo la variabile discreta con la variabile reale continua).

### Corollario sulla continuità della somma, prodotto e quoziente

Siano $f, g \in C(D)$ due funzioni continue su tutto un insieme $D \subseteq \mathbb{R}$ (oppure continue in un punto $x_0 \in D$):

- **Somma di funzioni continue**: la funzione $f + g$ è continua in $D$ ($f + g \in C(D)$).
- **Prodotto di funzioni continue**: la funzione $f \cdot g$ è continua in $D$ ($f \cdot g \in C(D)$).
- **Quoziente di funzioni continue**: se $g(x) \neq 0$ per ogni $x \in D$, la funzione $\frac{f}{g}$ è continua in $D$ ($\frac{f}{g} \in C(D)$).

---

## Proprietà di Ordine per i Limiti e la Continuità di Funzioni

### Teorema di Permanenza del Segno per Funzioni

1. **Dalla funzione al limite**: sia $f: D \to \mathbb{R}$ una funzione a valori non negativi ($f(x) \ge 0$ per ogni $x \in D$). Se esiste il limite $\lim_{x \to x_0} f(x) = L$, allora anche il limite è non negativo: $$
L \ge 0
$$
2. **Dal limite alla funzione**: sia $f: D \to \mathbb{R}$ tale che ammetta limite $L$ in $x_0$ con $L > 0$. Allora la funzione è strettamente positiva in un opportuno intorno del punto $x_0$: $$
\exists \delta > 0 \quad \text{tale che} \quad \forall x \in D \cap ((x_0 - \delta, x_0 + \delta) \setminus {x_0}) \implies f(x) > 0
$$
    - **Dimostrazione**: Scegliendo $\varepsilon = \frac{L}{2} > 0$ nella definizione di limite, esiste un raggio $\delta > 0$ tale che per ogni $x \in D$ con $0 < |x - x_0| < \delta$ vale: $$
f(x) > L - \varepsilon = L - \frac{L}{2} = \frac{L}{2} > 0
$$

### Teorema di Monotonia (Conservazione dell'ordine)

Siano $f, g: D \to \mathbb{R}$ due funzioni tali che $f(x) \le g(x)$ per ogni $x \in D$. Se esistono i limiti $\lim_{x \to x_0} f(x) = L_1$ e $\lim_{x \to x_0} g(x) = L_2$, allora: $$
L_1 \le L_2
$$

### Teorema dei Due Carabinieri per Funzioni

Siano $f, g, h: D \to \mathbb{R}$ tre funzioni tali che: $$
f(x) \le g(x) \le h(x) \quad \forall x \in D
$$ Se la funzione minorante $f$ e la funzione maggiorante $h$ ammettono lo stesso limite $L \in \mathbb{R}$ per $x \to x_0$: $$
\lim_{x \to x_0} f(x) = \lim_{x \to x_0} h(x) = L
$$ allora anche la funzione mediana $g$ ammette limite per $x \to x_0$ e vale: $$
\lim_{x \to x_0} g(x) = L
$$

- **Dimostrazione**:
    1. Fissato $\varepsilon > 0$, per le ipotesi sui limiti di $f$ ed $h$ esistono due raggi $\delta_f, \delta_h > 0$ tali che: $$
L - \varepsilon < f(x) < L + \varepsilon \quad \text{per } 0 < |x - x_0| < \delta_f
$$
$$
L - \varepsilon < h(x) < L + \varepsilon \quad \text{per } 0 < |x - x_0| < \delta_h
$$
    2. Scegliendo $\delta_g := \min(\delta_f, \delta_h)$, per tutti i punti $x \in D \setminus {x_0}$ con $|x - x_0| < \delta_g$ vale la concatenazione: $$
L - \varepsilon < f(x) \le g(x) \le h(x) < L + \varepsilon \implies |g(x) - L| < \varepsilon
$$
    3. Di conseguenza $\lim_{x \to x_0} g(x) = L$.

---

## Limite e Continuità della Funzione Composta

### Enunciato del Teorema sulla Funzione Composta

Siano $f: D_f \to \mathbb{R}$ e $g: D_g \to \mathbb{R}$ due funzioni tali che l'immagine di $f$ sia contenuta nel dominio di $g$ ($\text{Im}(f) \subseteq D_g$), consentendo la definizione della **funzione composta** $(g \circ f)(x) := g(f(x))$. Siano:

1. $x_0$ punto di accumulazione per $D_f$, con $\lim_{x \to x_0} f(x) = y_0$.
2. $y_0$ punto di accumulazione per $D_g$, con $\lim_{y \to y_0} g(y) = z_0$.

Allora esiste il limite per $x \to x_0$ della funzione composta e coincide con $z_0$: $$
\lim_{x \to x_0} g(f(x)) = z_0
$$

### Dimostrazione del Teorema

1. Fissato un generico $\varepsilon > 0$, dall'ipotesi di limite per la funzione esterna $g$ in $y_0$, esiste un raggio $\delta > 0$ tale che: $$
\forall y \in D_g, , 0 < |y - y_0| < \delta \implies |g(y) - z_0| < \varepsilon
$$
2. Ponendo la tolleranza $\varepsilon' := \delta$ nell'ipotesi di limite per la funzione interna $f$ in $x_0$, esiste un raggio $\delta' > 0$ tale che: $$
\forall x \in D_f, , 0 < |x - x_0| < \delta' \implies |f(x) - y_0| < \varepsilon' = \delta
$$
3. Concatenando le due implicazioni ponendo $y = f(x)$, per ogni $x \in D_f$ distante da $x_0$ meno di $\delta'$ si ottiene: $$
|g(f(x)) - z_0| < \varepsilon
$$ dimostrando che $\lim_{x \to x_0} g(f(x)) = z_0$.

- **Corollario sulla continuità della funzione composta**: Se $f$ è continua nel punto $x_0$ (con $f(x_0) = y_0$) e $g$ è continua nel punto $y_0$, allora la funzione composta $g \circ f$ è **continua nel punto $x_0$**: $$
\lim_{x \to x_0} g(f(x)) = g(f(x_0))
$$

---

## Continuità delle Funzioni Elementari e Trigonometriche

### Continuità delle Radici $k$-esime

- Per ogni intero $k \ge 1$, la **funzione radice $k$-esima** $g_k(y) = y^{1/k} = \sqrt[k]{y}$ definita su $[0, +\infty)$ è continua poiché definita come **funzione inversa** della funzione potenza $f_k(x) = x^k$ (continua su $[0, +\infty)$).
- Di conseguenza, la composizione della radice $k$-esima con una qualsiasi funzione razionale continua produce una funzione continua sul suo dominio.

### Dimostrazione della Continuità della Funzione Seno

- **Disuguaglianza geometrica di Archimede**: per due punti appartenenti alla circonferenza goniometrica unitaria individuati dagli archi $x$ e $y$, la lunghezza della corda congiungente non supera la lunghezza dell'arco compreso: $$
|\sin y - \sin x| \le |y - x|
$$
- **Dimostrazione di continuità**:
    1. Si valuti il limite della distanza $|\sin y - \sin x|$ per $y \to x$.
    2. Dalla catena di disuguaglianze: $$
0 \le |\sin y - \sin x| \le |y - x|
$$
    3. Poiché $\lim_{y \to x} 0 = 0$ e $\lim_{y \to x} |y - x| = 0$, per il **Teorema dei due carabinieri** si ottiene: $$
\lim_{y \to x} |\sin y - \sin x| = 0 \implies \lim_{y \to x} \sin y = \sin x
$$
    4. La funzione $\sin x$ è pertanto **continua su tutta la retta reale** ($\sin x \in C(\mathbb{R})$).

### Continuità delle altre Funzioni Trigonometriche

1. **Funzione Coseno**: espressa mediante la relazione di sfasamento come composizione del seno con il polinomio lineare $P(x) = x + \frac{\pi}{2}$: $$
\cos x = \sin\left(x + \frac{\pi}{2}\right)
$$ Poiché il polinomio e la funzione seno sono continui, per il teorema sulla funzione composta il coseno è **continuo su tutta la retta reale** ($\cos x \in C(\mathbb{R})$).
2. **Funzione Tangente**: definita come quoziente $\tan x = \frac{\sin x}{\cos x}$. Risulta **continua sul suo dominio** (unione numerabile di intervalli aperti): $$
D = \mathbb{R} \setminus \left\{ \frac{\pi}{2} + k\pi ;\middle|; k \in \mathbb{Z} \right\}
$$
3. **Funzione Cotangente**: definita come quoziente $\cot x = \frac{\cos x}{\sin x}$, risulta continua sul suo dominio $D = \mathbb{R} \setminus { k\pi \mid k \in \mathbb{Z} }$.

---

## Il Teorema di Weierstrass per Funzioni Continue

### Lemma Preliminare (Continuità per Successioni)

- **Enunciato**: Sia $f: D \to \mathbb{R}$ una funzione continua nel punto $x_0 \in D$. Se ${x_n} \subseteq D$ è una successione di punti del dominio convergente a $x_0$ ($\lim_{n \to +\infty} x_n = x_0$), allora la successione delle immagini $f(x_n)$ converge a $f(x_0)$: $$
\lim_{n \to +\infty} f(x_n) = f\left(\lim_{n \to +\infty} x_n\right) = f(x_0)
$$ (nelle funzioni continue l'operatore di limite commuta con l'applicazione della funzione).

### Enunciato del Teorema di Weierstrass

Sia $f: [a, b] \to \mathbb{R}$ una funzione **continua** definita su un intervallo **chiuso e limitato** $[a, b]$. Allora la funzione $f$ ammette **massimo assoluto** (globale) e **minimo assoluto** (globale) nell'intervallo $[a, b]$.

- Esistono cioè due punti $x_m, x_M \in [a, b]$ tali che: $$
f(x_m) \le f(x) \le f(x_M) \quad \forall x \in [a, b]
$$
    - $m := f(x_m) = \min_{x \in [a,b]} f(x)$: **valore minimo**.
    - $M := f(x_M) = \max_{x \in [a,b]} f(x)$: **valore massimo**.

### Dimostrazione del Teorema di Weierstrass (per il Massimo)

1. Si definisca $M := \sup_{x \in [a,b]} f(x) = \sup f([a,b])$ l'estremo superiore dell'immagine della funzione.
2. Per le proprietà dell'estremo superiore, esiste una successione di valori $y_n \in \text{Im}(f)$ monotona crescente tale che: $$
\lim_{n \to +\infty} y_n = M
$$
3. Per ogni $y_n$, per definizione di immagine esiste un punto $x_n \in [a, b]$ tale che $y_n = f(x_n)$.
4. Si distinguono due casi per l'insieme dei valori della successione ${y_n}$:
    - **Caso 1 (Insieme dei valori finito)**: la successione è definitivamente costante $y_n = M$. Esiste un punto $x_M \in [a, b]$ tale che $f(x_M) = M$, dimostrando che l'estremo superiore appartiene all'immagine ed è il massimo assoluto.
    - **Caso 2 (Insieme dei valori infinito)**: la successione di punti ${x_n} \subseteq [a, b]$ costituisce un insieme **infinito e limitato**.
5. Per il **Teorema di Bolzano-Weierstrass**, l'insieme ${x_n}$ ammette un punto di accumulazione $x_M \in [a, b]$ ed esiste una sottosuccessione ${x_{n_k}}$ convergente a $x_M$: $$
\lim_{k \to +\infty} x_{n_k} = x_M \in [a, b]
$$
6. Per la continuità di $f$ ed applicando il lemma preliminare: $$
f(x_M) = f\left(\lim_{k \to +\infty} x_{n_k}\right) = \lim_{k \to +\infty} f(x_{n_k}) = \lim_{k \to +\infty} y_{n_k} = M
$$
7. Pertanto, l'estremo superiore $M$ è un numero reale finito ed è il valore assunto da $f$ nel punto $x_M \in [a, b]$, dimostrando che $M = \max f([a,b])$.

---

## Il Teorema degli Zeri (di Bolzano)

### Enunciato del Teorema degli Zeri

Sia $f: [a, b] \to \mathbb{R}$ una funzione **continua** su un intervallo chiuso e limitato $[a, b]$ tale che ai due estremi dell'intervallo la funzione assuma **valori di segno opposto**: $$
f(a) \cdot f(b) < 0
$$ (ovvero $f(a) < 0 < f(b)$ oppure $f(b) < 0 < f(a)$). Allora esiste **almeno un punto** $x_0 \in (a, b)$ interno all'intervallo in cui la funzione si annulla: $$
f(x_0) = 0
$$

### Dimostrazione del Teorema degli Zeri (Metodo di Dicotomia)

1. Si pongano $a_0 := a$ e $b_0 := b$, con $f(a_0) \cdot f(b_0) < 0$.
2. Si calcoli il punto medio $c_1 := \frac{a_0 + b_0}{2}$:
    - Se $f(c_1) = 0$, si è trovato lo zero $x_0 = c_1$ e la dimostrazione è conclusa.
    - Se $f(c_1) \neq 0$, la funzione assume segno opposto agli estremi di almeno una delle due metà $[a_0, c_1]$ oppure $[c_1, b_0]$.
3. Si seleziona la metà agli estremi della quale $f$ assume segno opposto e la si denota con $[a_1, b_1]$, per cui $f(a_1) \cdot f(b_1) < 0$.
4. Reiterando ricorsivamente il procedimento di dicotomia $k$ volte, se non si incontra uno zero esatto nei punti medi, si ottiene una successione di intervalli incapsulati $[a_k, b_k]$ tali che:
    - $[a_{k+1}, b_{k+1}] \subseteq [a_k, b_k] \subseteq \dots \subseteq [a_0, b_0]$ per ogni $k \ge 0$.
    - $f(a_k) \cdot f(b_k) < 0$ per ogni $k \ge 0$.
    - L'ampiezza dell'intervallo $k$-esimo è $b_k - a_k = \frac{b_0 - a_0}{2^k}$.
5. Dalle proprietà della dicotomia, la successione ${a_k}$ è monotona crescente e la successione ${b_k}$ è monotona decrescente. Entrambe le successioni convergono al medesimo limite reale $x_0 \in [a, b]$: $$
\lim_{k \to +\infty} a_k = \lim_{k \to +\infty} b_k = x_0
$$
6. Passando al limite per $k \to +\infty$ nella disuguaglianza $f(a_k) \cdot f(b_k) < 0$ e sfruttando la continuità di $f$ nei punti limite: $$
\lim_{k \to +\infty} [f(a_k) \cdot f(b_k)] \le 0 \implies f\left(\lim_{k \to +\infty} a_k\right) \cdot f\left(\lim_{k \to +\infty} b_k\right) \le 0 \implies [f(x_0)]^2 \le 0
$$
7. Poiché il quadrato di un numero reale non può essere strettamente negativo, si conclude che: $$
[f(x_0)]^2 = 0 \implies f(x_0) = 0
$$ dimostrando l'esistenza dello zero $x_0 \in (a, b)$.
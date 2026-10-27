## Teorema dei Valori Intermedi

### Enunciato del Teorema

- Sia $f: [a, b] \to \mathbb{R}$ una funzione **continua** su un intervallo chiuso e limitato $[a, b]$, e siano $m$ e $M$ rispettivamente il suo valore minimo ed il suo valore massimo assoluti sull'intervallo: $$
m := \min_{x \in [a,b]} f(x), \quad M := \max_{x \in [a,b]} f(x)
$$
- Per ogni valore intermedio $\lambda \in [m, M]$, esiste **almeno un punto** $x_\lambda \in [a, b]$ in cui la funzione assume esattamente il valore $\lambda$: $$
f(x_\lambda) = \lambda
$$
- Proprietà e conseguenze geometriche:
    - L'immagine della funzione $f$ coincide con l'intero intervallo chiuso compreso tra il minimo e il massimo: $\text{Im}(f) = [m, M]$.
    - Il grafico della funzione è interamente contenuto nel rettangolo $[a, b] \times [m, M]$.
    - L'immagine ed il grafico della funzione costituiscono insiemi **connessi**.

### Dimostrazione del Teorema

1. Per il Teorema di Weierstrass, esistono due punti $x_m, x_M \in [a, b]$ tali che $f(x_m) = m$ e $f(x_M) = M$.
2. Si assuma, senza perdita di generalità, che $x_m < x_M$ (se $x_m = x_M$, la funzione è costante $m = M$, rendendo il teorema banale).
3. Poiché $[x_m, x_M] \subseteq [a, b]$, la funzione $f$ è continua sull'intervallo ridotto $[x_m, x_M]$.
4. Si definisca la **funzione ausiliaria** $g: [x_m, x_M] \to \mathbb{R}$ mediante traslazione verticale di ampiezza $\lambda$: $$
g(x) := f(x) - \lambda
$$
5. La funzione $g$ è continua su $[x_m, x_M]$ in quanto differenza tra la funzione continua $f(x)$ e la costante $\lambda$.
6. Si valutino i valori uscenti da $g$ agli estremi $x_m$ e $x_M$:
    - In $x_m$: $g(x_m) = f(x_m) - \lambda = m - \lambda < 0$ (poiché $\lambda > m$).
    - In $x_M$: $g(x_M) = f(x_M) - \lambda = M - \lambda > 0$ (poiché $\lambda < M$).
7. Poiché la funzione $g$ assume valori di **segno opposto** agli estremi $x_m$ e $x_M$, per il **Teorema degli Zeri** applicato a $g$ sull'intervallo $[x_m, x_M]$, esiste almeno un punto interno $x_\lambda \in (x_m, x_M)$ tale che: $$
g(x_\lambda) = 0
$$
8. Sostituendo la definizione di $g$: $$
f(x_\lambda) - \lambda = 0 \implies f(x_\lambda) = \lambda
$$

### Applicazioni pratiche

- Utilizzo per l'individuazione di zeri di polinomi di grado elevato (es. grado 4 o 5) non fattorizzabili direttamente: individuando più intervalli in cui il polinomio assume valori di segno discorde agli estremi, si garantisce l'esistenza di radici reali all'interno di ciascun intervallo.

---

## La Relazione di Asintotico e Limiti Notevoli Trigonometrici

### Definizione di relazione di asintotico

- Due funzioni $f(x)$ e $g(x)$ si dicono **asintotiche** per $x \to x_0$ (in simboli $f(x) \sim g(x)$ per $x \to x_0$) se il limite del loro rapporto è unitario: $$
\lim_{x \to x_0} \frac{f(x)}{g(x)} = 1
$$
- Costituisce una **relazione di equivalenza** nello spazio delle funzioni. Il punto $x_0$ può appartenere a $\mathbb{R}$ oppure essere $\pm\infty$.
- Requisito: il rapporto $\frac{f(x)}{g(x)}$ dev'essere ben posto nell'intorno del punto limite. La medesima relazione si applica alle successioni numeriche per $n \to +\infty$.

### Primo limite notevole trigonometrico

$$
\lim_{x \to 0} \frac{\sin x}{x} = 1
$$

- **Significato asintotico e geometrico**: la funzione $\sin x$ è asintotica alla funzione identità $x$ per $x \to 0$ ($\sin x \sim x$). Nell'intorno dell'origine, il grafico della funzione seno si confonde con la bisettrice del primo e terzo quadrante ($y = x$).
- **Dimostrazione geometrica**:
    1. Si consideri la circonferenza goniometrica unitaria ed un arco $x$ per $x \in \left(0, \frac{\pi}{2}\right)$.
    2. Per confronto tra le lunghezze del segmento del seno, dell'arco e della tangente trigonometrica, sussiste la catena di disuguaglianze: $$
\sin x \le x \le \tan x
$$
    3. Dividendo l'intera catena per la quantità positiva $\sin x > 0$: $$
1 \le \frac{x}{\sin x} \le \frac{1}{\cos x}
$$
    4. Passando ai reciproci ed invertendo i versi dei termini: $$
\cos x \le \frac{\sin x}{x} \le 1
$$
    5. Per parità delle funzioni involucrate, la disuguaglianza $\cos x \le \frac{\sin x}{x} \le 1$ vale per ogni $x \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right) \setminus {0}$.
    6. Poiché per la continuità del coseno si ha $\lim_{x \to 0} \cos x = \cos 0 = 1$ e per la funzione costante $\lim_{x \to 0} 1 = 1$, per il **Teorema dei due carabinieri**: $$
\lim_{x \to 0} \frac{\sin x}{x} = 1
$$

### Secondo limite notevole trigonometrico

$$
\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}
$$

- **Significato asintotico e geometrico**: la quantità $1 - \cos x$ è asintotica a $\frac{x^2}{2}$ per $x \to 0$ ($1 - \cos x \sim \frac{x^2}{2}$). Nell'intorno dell'origine, il grafico della funzione $1 - \cos x$ si confonde con la parabola $y = \frac{x^2}{2}$.
- **Dimostrazione**:
    1. Applicando la formula di duplicazione al coseno espressa per l'angolo dimezzato: $$
1 - \cos x = 1 - \cos\left(2 \cdot \frac{x}{2}\right) = 1 - \left( \cos^2 \frac{x}{2} - \sin^2 \frac{x}{2} \right) = 2 \sin^2 \frac{x}{2}
$$
    2. Riscrivendo il rapporto da valutare a limite: $$
\frac{1 - \cos x}{x^2} = \frac{2 \sin^2(x/2)}{x^2} = 2 \left( \frac{\sin(x/2)}{x} \right)^2 = 2 \left( \frac{\sin(x/2)}{2 \cdot (x/2)} \right)^2 = \frac{1}{2} \left( \frac{\sin(x/2)}{x/2} \right)^2
$$
    3. Applicando l'algebra dei limiti ed effettuando il cambio di variabile $y = \frac{x}{2}$ (con $y \to 0$ per $x \to 0$): $$
\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2} \lim_{y \to 0} \left( \frac{\sin y}{y} \right)^2 = \frac{1}{2} (1)^2 = \frac{1}{2}
$$

---

## Limiti Notevoli dell'Esponenziale, del Logaritmo e Teorema dei Numeri Primi

### Limiti notevoli di $e^x$ e $\ln(1+x)$

1. **Limite notevole della funzione esponenziale**: $$
\lim_{x \to 0} \frac{e^x - 1}{x} = 1 \implies e^x - 1 \sim x \quad \text{per } x \to 0
$$
2. **Limite notevole della funzione logaritmo naturale** ($\ln = \log_e$): $$
\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1 \implies \ln(1 + x) \sim x \quad \text{per } x \to 0
$$

- I due limiti sono equivalenti in quanto le funzioni esponenziale e logaritmo costituiscono l'una la funzione inversa dell'altra.

### Il Teorema dei Numeri Primi

- Si definisca la funzione di conteggio dei primi $\pi(x): \mathbb{R}^+ \to \mathbb{N}$ come il numero di numeri primi minori o uguali a $x$: $$
\pi(x) := \vert { q \in \mathbb{N} \mid q \text{ è primo} \land q \le x } \vert
$$
- **Enunciato del Teorema dei Numeri Primi**: $$
\lim_{x \to +\infty} \frac{\pi(x)}{\frac{x}{\ln x}} = 1 \implies \pi(x) \sim \frac{x}{\ln x} \quad \text{per } x \to +\infty
$$

---

## Introduzione al Calcolo Differenziale e Concetto di Derivata

### Motivazioni teoriche e geometriche dell'approssimazione locale

1. **Approssimazione analitica locale**: necessità di approssimare localmente (nell'intorno di un punto $x_0$) funzioni complesse mediante polinomi di primo grado $g(x) = a x + b$.
2. **Approssimazione geometrica locale**: approssimare localmente grafici complessi mediante rette (figure geometriche univocamente determinate da due punti).

### Definizione formale di derivata e rapporto incrementale

- Sia $f: (a, b) \to \mathbb{R}$ una funzione definita su un intervallo aperto $(a, b)$ e sia $x_0 \in (a, b)$.
- La funzione $f$ si dice **derivabile nel punto $x_0$** se esiste ed è finito (numero reale appartenente a $\mathbb{R}$) il limite del **rapporto incrementale**: $$
\lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} = f'(x_0) \quad \left( \text{oppure } \frac{df}{dx}(x_0) \right)
$$
- **Rapporto incrementale**: l'espressione $\frac{f(x) - f(x_0)}{x - x_0}$ rappresenta il quoziente tra l'incremento/oscillazione della funzione $f(x) - f(x_0)$ e l'incremento della variabile indipendente $x - x_0$.

### Significato geometrico ed equazione della retta tangente

- Nel triangolo rettangolo di cateti $f(x) - f(x_0)$ e $x - x_0$, il rapporto incrementale misura la tangente trigonometrica dell'angolo $\theta(x)$ che la retta secante passante per $(x_0, f(x_0))$ e $(x, f(x))$ forma con l'asse orizzontale: $$
\frac{f(x) - f(x_0)}{x - x_0} = \tan \theta(x)
$$
- Al tendere di $x$ a $x_0$, la retta secante tende alla retta tangente ed il suo angolo limite $\theta_0$ soddisfa: $$
\tan \theta_0 = f'(x_0) \implies \theta_0 = \arctan(f'(x_0))
$$
- **Equazione della Retta Tangente**:
    - La retta $g(x)$ di equazione: $$
g(x) = f(x_0) + f'(x_0)(x - x_0)
$$ rappresenta la **retta tangente al grafico di $f$** nel punto $(x_0, f(x_0))$.

---

## Equivalenza tra Derivabilità e Differenziabilità

### Enunciato dello sviluppo al primo ordine con resto

- **Teorema**: Sia $f: (a, b) \to \mathbb{R}$ una funzione derivabile nel punto $x_0 \in (a, b)$. Allora esiste una funzione $R: (a, b) \to \mathbb{R}$ (detta **funzione resto** o **funzione di errore**) tale che per ogni $x \in (a, b)$: $$
f(x) = f(x_0) + f'(x_0)(x - x_0) + R(x)
$$ con la condizione che il resto sia un **infinitesimo di ordine superiore al primo** per $x \to x_0$: $$
\lim_{x \to x_0} \frac{R(x)}{x - x_0} = 0 \quad (\text{notazione di Landau: } R(x) = o(x - x_0))
$$

### Dimostrazione dell'ordine del resto

1. Si definisca la funzione resto $R(x)$ per differenza tra la funzione ed il polinomio approssimante di primo grado: $$
R(x) := f(x) - [f(x_0) + f'(x_0)(x - x_0)]
$$
2. Dalla definizione segue immediatamente l'identità $f(x) = f(x_0) + f'(x_0)(x - x_0) + R(x)$.
3. Si valuti il limite del rapporto $\frac{R(x)}{x - x_0}$ per $x \to x_0$: $$
\lim_{x \to x_0} \frac{R(x)}{x - x_0} = \lim_{x \to x_0} \frac{f(x) - f(x_0) - f'(x_0)(x - x_0)}{x - x_0} = \lim_{x \to x_0} \left[ \frac{f(x) - f(x_0)}{x - x_0} - f'(x_0) \frac{x - x_0}{x - x_0} \right]
$$
4. Per l'algebra dei limiti: $$
\lim_{x \to x_0} \frac{R(x)}{x - x_0} = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} - \lim_{x \to x_0} f'(x_0) = f'(x_0) - f'(x_0) = 0
$$

---

## Esempi di Calcolo delle Derivate mediante Definizione

### Derivata della funzione costante

- Sia $f(x) = C$ per ogni $x \in \mathbb{R}$, con $C \in \mathbb{R}$ costante fissata: $$
f'(x_0) = \lim_{x \to x_0} \frac{C - C}{x - x_0} = \lim_{x \to x_0} 0 = 0
$$
- Risultato: la derivata della funzione costante è identicamente nulla ($f'(x) = 0$).
- Significato geometrico: la retta tangente coincide con il grafico della funzione stessa (retta orizzontale di coefficiente angolare nullo).

### Derivata della funzione identità

- Sia $f(x) = x$ per ogni $x \in \mathbb{R}$: $$
f'(x_0) = \lim_{x \to x_0} \frac{x - x_0}{x - x_0} = \lim_{x \to x_0} 1 = 1
$$
- Risultato: la derivata della funzione identità vale $1$ in ogni punto ($f'(x) = 1$).
- Significato geometrico: la retta tangente coincide con la bisettrice del primo e terzo quadrante (inclinazione $\theta = \pi/4$, $\tan(\pi/4) = 1$).

### Derivata della funzione quadratica

- Sia $f(x) = x^2$ per ogni $x \in \mathbb{R}$: $$
f'(x_0) = \lim_{x \to x_0} \frac{x^2 - x_0^2}{x - x_0} = \lim_{x \to x_0} \frac{(x - x_0)(x + x_0)}{x - x_0} = \lim_{x \to x_0} (x + x_0) = x_0 + x_0 = 2x_0
$$
- Risultato: la derivata della parabola standard è $f'(x) = 2x$.
- Equazione della retta tangente nel punto $x_0$: $$
g(x) = x_0^2 + 2x_0(x - x_0) = 2x_0 x - x_0^2
$$ (Esempio: per $x_0 = 3$, $g(x) = 6x - 9$).

---

## Proprietà di Calcolo delle Derivate (Regole di Derivazione)

### Relazione tra derivabilità e continuità (Proprietà 0)

- **Enunciato**: Se $f$ è derivabile nel punto $x_0$, allora $f$ è **continua nel punto $x_0$**.
- La derivabilità rappresenta una condizione strettamente più forte della continuità. La continuità è condizione necessaria ma non sufficiente per la derivabilità.
- **Dimostrazione**: $$
\lim_{x \to x_0} [f(x) - f(x_0)] = \lim_{x \to x_0} \left[ \frac{f(x) - f(x_0)}{x - x_0} \cdot (x - x_0) \right] = \left( \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} \right) \cdot \left( \lim_{x \to x_0} (x - x_0) \right) = f'(x_0) \cdot 0 = 0
$$ Da $\lim_{x \to x_0} [f(x) - f(x_0)] = 0$ segue $\lim_{x \to x_0} f(x) = f(x_0)$, confermando la continuità di $f$ in $x_0$.

### Derivata della somma e prodotto per costante (Proprietà 1 e 2)

1. **Derivata della somma**: se $f$ e $g$ sono derivabili in $x_0$, allora la funzione somma $f + g$ è derivabile in $x_0$ e vale: $$
(f + g)'(x_0) = f'(x_0) + g'(x_0)
$$
2. **Prodotto per una costante**: se $f$ è derivabile in $x_0$ e $\alpha \in \mathbb{R}$, allora la funzione $\alpha f$ è derivabile in $x_0$ e vale: $$
(\alpha f)'(x_0) = \alpha f'(x_0)
$$

### Regola di Leibniz per il prodotto (Proprietà 3)

- **Enunciato**: Se $f$ e $g$ sono derivabili nel punto $x_0$, allora la funzione prodotto $f \cdot g$ è derivabile in $x_0$ e la sua derivata vale: $$
(f \cdot g)'(x_0) = f'(x_0) g(x_0) + f(x_0) g'(x_0)
$$
- Nota: la derivata del prodotto dipende sia dalle derivate sia dai valori assunti dalle funzioni originarie nel punto.

### Derivata del quoziente (Proprietà 4)

- **Enunciato**: Se $f$ e $g$ sono derivabili nel punto $x_0$ con $g(x_0) \neq 0$, allora la funzione quoziente $\frac{f}{g}$ è derivabile in $x_0$ e vale: $$
\left( \frac{f}{g} \right)'(x_0) = \frac{f'(x_0) g(x_0) - f(x_0) g'(x_0)}{[g(x_0)]^2}
$$

### Derivata della funzione composta (Proprietà 5)

- **Enunciato**: Se $f$ è derivabile in $x_0$ e $g$ è derivabile in $y_0 = f(x_0)$, allora la funzione composta $g \circ f$ è derivabile in $x_0$ e vale: $$
(g \circ f)'(x_0) = g'(f(x_0)) \cdot f'(x_0)
$$

### Derivata della funzione inversa (Proprietà 6)

- **Enunciato**: Se $f$ è una funzione invertibile e derivabile nel punto $x_0$ con $f'(x_0) \neq 0$, allora la funzione inversa $f^{-1}$ è derivabile nel punto $y_0 = f(x_0)$ e vale: $$
(f^{-1})'(y_0) = \frac{1}{f'(x_0)} = \frac{1}{f'(f^{-1}(y_0))}
$$
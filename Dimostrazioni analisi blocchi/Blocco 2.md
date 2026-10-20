
## **BLOCCO 2: Algebra dei limiti & Condizione di Cauchy**

---

### **Teorema 1: Limite della Somma di Successioni**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Siano ${x_n}_{n \in \mathbb{N}}$ e ${y_n}_{n \in \mathbb{N}}$ due successioni numeriche convergenti in $\mathbb{R}$, per le quali esistono finiti i limiti: $$
\lim_{n \to +\infty} x_n = L_1 \in \mathbb{R} \quad \text{e} \quad \lim_{n \to +\infty} y_n = L_2 \in \mathbb{R}
$$
- **Tesi ($T$)**: La successione somma ${x_n + y_n}_{n \in \mathbb{N}}$ converge e il suo limite coincide con la somma dei singoli limiti: $$
\lim_{n \to +\infty} (x_n + y_n) = L_1 + L_2 = \lim_{n \to +\infty} x_n + \lim_{n \to +\infty} y_n
$$

#### **Idea Chiave della Dimostrazione**

Si valuta la distanza tra il termine generico $(x_n + y_n)$ e il candidato limite $(L_1 + L_2)$. Riorganizzando i termini, si applica la **disuguaglianza triangolare** sul modulo per separare lo scarto di $x_n$ da $L_1$ e lo scarto di $y_n$ da $L_2$. Scegliendo per ciascuna successione una tolleranza pari a $\frac{\varepsilon}{2}$ (oppure maggiorando la somma di due tolleranze $\varepsilon$ con $2\varepsilon$), la somma delle due distanze risulterà strettamente minore della quantità desiderata definitivamente.

#### **Dimostrazione Dettagliata**

1. Si valuti il modulo della differenza tra il termine generico della successione somma e la quantità $L_1 + L_2$: $$
|(x_n + y_n) - (L_1 + L_2)|
$$
2. Riorganizzando i termini all'interno del modulo e applicando la disuguaglianza triangolare: $$
|(x_n + y_n) - (L_1 + L_2)| = |(x_n - L_1) + (y_n - L_2)| \le |x_n - L_1| + |y_n - L_2|
$$
3. Si fissi una tolleranza arbitraria $\varepsilon > 0$. Poiché $\frac{\varepsilon}{2} > 0$, per l'ipotesi di convergenza di $x_n \to L_1$ esiste una soglia $N_1 \in \mathbb{N}$ tale che: $$
\forall n > N_1 \implies |x_n - L_1| < \frac{\varepsilon}{2}
$$
4. Analogamente, per l'ipotesi di convergenza di $y_n \to L_2$, in corrispondenza della medesima tolleranza $\frac{\varepsilon}{2} > 0$ esiste una soglia $N_2 \in \mathbb{N}$ tale che: $$
\forall n > N_2 \implies |y_n - L_2| < \frac{\varepsilon}{2}
$$
5. Si definisca la soglia temporale comune prendendo il massimo tra i due indici: $N := \max(N_1, N_2)$.
6. Per tutti gli indici $n > N$ valgono contemporaneamente entrambe le disuguaglianze. Sostituendo le due maggiorazioni nella disuguaglianza triangolare ottenuta al punto 2: $$
|(x_n + y_n) - (L_1 + L_2)| \le |x_n - L_1| + |y_n - L_2| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon
$$
7. Poiché la relazione $|(x_n + y_n) - (L_1 + L_2)| < \varepsilon$ è verificata definitivamente per ogni $\varepsilon > 0$ arbitrario, per la definizione formale di limite si conclude che: $$
\lim_{n \to +\infty} (x_n + y_n) = L_1 + L_2
$$

#### **Punti Critici / Errori Tipici all'Orale**

- **Omissioni sulla disuguaglianza triangolare**: All'orale è un errore grave passare direttamente da $|(x_n - L_1) + (y_n - L_2)|$ alla somma dei moduli senza esplicitare l'uso della disuguaglianza triangolare $|a+b| \le |a| + |b|$.
- **Scelta del massimo delle soglie $N = \max(N_1, N_2)$**: Bisogna evidenziare che le due stime valgono simultaneamente solo quando l'indice $n$ supera sia $N_1$ sia $N_2$.
- **Forme indeterminate**: Il teorema si applica solo quando entrambi i limiti sono **finiti**. Se uno dei limiti è $+\infty$ e l'altro è $-\infty$, la regola non si applica poiché si genera la forma indeterminata $[+\infty - \infty]$.

#### **Esercizio / Domanda di Verifica**

_Sia $x_n \to +\infty$ e $y_n \to L_2 \in \mathbb{R}$. Dimostrare analiticamente (tramite la definizione con la barriera $M$) che la successione somma $x_n + y_n$ diverge anch'essa a $+\infty$._

---

### **Teorema 2: Limite del Prodotto di Successioni**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Siano ${x_n}_{n \in \mathbb{N}}$ e ${y_n}_{n \in \mathbb{N}}$ due successioni numeriche convergenti in $\mathbb{R}$, tali che: $$
\lim_{n \to +\infty} x_n = L_1 \in \mathbb{R} \quad \text{e} \quad \lim_{n \to +\infty} y_n = L_2 \in \mathbb{R}
$$
- **Tesi ($T$)**: La successione prodotto ${x_n \cdot y_n}_{n \in \mathbb{N}}$ converge e il suo limite è il prodotto dei singoli limiti: $$
\lim_{n \to +\infty} (x_n \cdot y_n) = L_1 \cdot L_2 = \left(\lim_{n \to +\infty} x_n\right) \cdot \left(\lim_{n \to +\infty} y_n\right)
$$

#### **Idea Chiave della Dimostrazione**

Per valutare la distanza $|x_n y_n - L_1 L_2|$, si utilizza il trucco algebrico di **aggiungere e sottrarre la quantità mista $L_1 y_n$** (oppure $x_n L_2$). Applicando la disuguaglianza triangolare, la stima si separa in due addendi. Poiché la successione ${y_n}$ è convergente, essa è **limitata** ($|y_n| \le M$), il che consente di controllare l'accrescimento del primo addendo e concludere la dimostrazione.

#### **Dimostrazione Dettagliata**

1. Si consideri il modulo della differenza tra il termine prodotto $x_n y_n$ e il candidato limite $L_1 L_2$: $$
|x_n y_n - L_1 L_2|
$$
2. Si aggiunga e si sottragga la quantità intermedia $L_1 y_n$ all'interno del modulo e si raccolgano i fattori comuni: $$
|x_n y_n - L_1 L_2| = |(x_n y_n - L_1 y_n) + (L_1 y_n - L_1 L_2)| = |y_n (x_n - L_1) + L_1 (y_n - L_2)|
$$
3. Si applichino la disuguaglianza triangolare e la proprietà del modulo del prodotto ($|a \cdot b| = |a| \cdot |b|$): $$
|x_n y_n - L_1 L_2| \le |y_n| \cdot |x_n - L_1| + |L_1| \cdot |y_n - L_2|
$$
4. Poiché la successione ${y_n}$ converge al limite finito $L_2$, per il Teorema di Limitatezza delle successioni convergenti essa è **limitata**: esiste una costante reale $M > 0$ tale che: $$
|y_n| \le M \quad \forall n \in \mathbb{N}
$$
5. Sostituendo la maggiorazione $|y_n| \le M$ nell'espressione al punto 3: $$
|x_n y_n - L_1 L_2| \le M \cdot |x_n - L_1| + |L_1| \cdot |y_n - L_2|
$$
6. Si fissi una tolleranza arbitraria $\varepsilon > 0$:
    - Poiché $x_n \to L_1$, in corrispondenza della quantità positiva $\frac{\varepsilon}{2M} > 0$ esiste una soglia $N_1 \in \mathbb{N}$ tale che per ogni $n > N_1 \implies |x_n - L_1| < \frac{\varepsilon}{2M}$.
    - Poiché $y_n \to L_2$, in corrispondenza della quantità positiva $\frac{\varepsilon}{2(|L_1| + 1)} > 0$ esiste una soglia $N_2 \in \mathbb{N}$ tale che per ogni $n > N_2 \implies |y_n - L_2| < \frac{\varepsilon}{2(|L_1| + 1)}$.
7. Si definisca $N := \max(N_1, N_2)$. Per tutti gli indici $n > N$ si ottiene: $$
|x_n y_n - L_1 L_2| < M \cdot \frac{\varepsilon}{2M} + |L_1| \cdot \frac{\varepsilon}{2(|L_1| + 1)} < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon
$$
8. Per l'arbitrarietà di $\varepsilon > 0$, ne consegue che: $$
\lim_{n \to +\infty} (x_n \cdot y_n) = L_1 \cdot L_2
$$

#### **Punti Critici / Errori Tipici all'Orale**

- **Dimenticare la limitatezza della successione**: L'errore più comune all'esame è trattare $|y_n|$ come se fosse semplicemente la costante $|L_2|$. Bisogna esplicitare che $|y_n|$ varia con $n$ e che va maggiorato con una costante uniforme $M$ sfruttando la limitatezza delle successioni convergenti.
- **Evitare divisioni per zero nella scelta di $\varepsilon$**: Quando si scelgono le tolleranze parziali, è opportuno sommare $+1$ al denominatore (es. $|L_1| + 1$) per evitare divisioni per zero nel caso in cui $L_1 = 0$.

#### **Esercizio / Domanda di Verifica**

_Sia $x_n$ una successione infinitesima ($\lim x_n = 0$) e sia $y_n$ una successione limitata ma non convergente (es. $y_n = (-1)^n$). Dimostrare che la successione prodotto $x_n \cdot y_n$ converge a $0$._

---

### **Teorema 3: Condizione di Cauchy per le Successioni (Caratterizzazione e Completezza in $\mathbb{R}$)**

#### **Enunciato Formale**

##### **Definizione di Successione di Cauchy**

Una successione numerica ${x_n}_{n \in \mathbb{N}} \subseteq \mathbb{R}$ si dice **successione di Cauchy** (o soddisfa il criterio di Cauchy) se: $$
\forall \varepsilon > 0, \exists N_\varepsilon \in \mathbb{N} \quad \text{tale che} \quad \forall m, n \ge N_\varepsilon \implies |x_m - x_n| < \varepsilon
$$

##### **Teorema di Completezza di $\mathbb{R}$ (Caratterizzazione)**

Una successione di numeri reali ${x_n}_{n \in \mathbb{N}} \subseteq \mathbb{R}$ è convergente in $\mathbb{R}$ **se e solo se** è una successione di Cauchy in $\mathbb{R}$.

#### **Idea Chiave della Dimostrazione**

- **Necessità ($\implies$)**: Se la successione converge a $L$, i suoi termini si avvicinano a $L$. Per la disuguaglianza triangolare, due termini $x_m$ e $x_n$ vicini a $L$ sono anche vicini tra loro ($|x_m - x_n| \le |x_m - L| + |L - x_n|$). Risultato valido sia in $\mathbb{Q}$ sia in $\mathbb{R}$.
- **Sufficienza ($\impliedby$) e Incompletezza di $\mathbb{Q}$**: Nei numeri razionali $\mathbb{Q}$ la condizione NON è sufficiente (esiste la successione ricorsiva $x_0 = 2, x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n}$ che è di Cauchy in $\mathbb{Q}$ ma la cui candidata radice $\sqrt{2} \notin \mathbb{Q}$). Nei numeri reali $\mathbb{R}$, la proprietà di completezza garantisce che ogni successione reale di Cauchy converga a un limite reale $L \in \mathbb{R}$.

#### **Dimostrazione Dettagliata**

##### **Parte A: Necessità della Condizione di Cauchy (Vale in $\mathbb{Q}$ e in $\mathbb{R}$)**

1. Si supponga che la successione sia convergente, ossia che esista $L \in \mathbb{R}$ tale che $\lim_{n \to +\infty} x_n = L$.
2. Per definizione di limite, per qualsiasi $\varepsilon > 0$ fissato esiste una soglia $N_\varepsilon \in \mathbb{N}$ tale che: $$
\forall k \ge N_\varepsilon \implies |x_k - L| < \frac{\varepsilon}{2}
$$
3. Si considerino due indici generici $m, n \ge N_\varepsilon$. Valutando la distanza mutua $|x_m - x_n|$, aggiungendo e sottrando $L$ ed applicando la disuguaglianza triangolare: $$
|x_m - x_n| = |(x_m - L) + (L - x_n)| \le |x_m - L| + |x_n - L|
$$
4. Poiché sia $m \ge N_\varepsilon$ sia $n \ge N_\varepsilon$, si ottiene: $$
|x_m - x_n| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon
$$
5. Ciò dimostra che ogni successione convergente è necessariamente di Cauchy.

##### **Parte B: Sufficienza della Condizione di Cauchy (Completezza di $\mathbb{R}$)**

1. Sia ${x_n} \subseteq \mathbb{R}$ una successione di Cauchy di numeri reali.
2. Per il **Teorema di Densità dei numeri razionali nei reali**, per ogni termine $x_n \in \mathbb{R}$ esiste un numero razionale $q_n \in \mathbb{Q}$ tale che: $$
|x_n - q_n| < \frac{1}{n} \quad \forall n \ge 1
$$
3. Si dimostra che la successione razionale ${q_n}$ così costruita è una successione di Cauchy in $\mathbb{Q}$. Infatti, applicando la disuguaglianza triangolare per $m, n \ge N$: $$
|q_m - q_n| = |(q_m - x_m) + (x_m - x_n) + (x_n - q_n)| \le |q_m - x_m| + |x_m - x_n| + |x_n - q_n| < \frac{1}{m} + |x_m - x_n| + \frac{1}{n}
$$ Scegliendo opportunamente l'indice di soglia per cui $\frac{1}{m} < \varepsilon$, $\frac{1}{n} < \varepsilon$ e $|x_m - x_n| < \varepsilon$, si ha $|q_m - q_n| < 3\varepsilon$.
4. Poiché ${q_n} \in \mathcal{C}$ è di Cauchy nei razionali, essa individua una classe di equivalenza che definisce un numero reale $L := [{q_n}] \in \mathbb{R}$, al quale ${q_n}$ converge nei reali ($\lim_{n \to +\infty} q_n = L$).
5. Si valuta infine la distanza tra la successione reale di partenza $x_n$ ed il limite reale $L$: $$
|x_n - L| \le |x_n - q_n| + |q_n - L|
$$
6. Poiché $|x_n - q_n| < \frac{1}{n} < \varepsilon$ (definitivamente) e $|q_n - L| < \varepsilon$ (per la convergenza di $q_n \to L$), per indici $n$ sufficientemente grandi si ottiene: $$
|x_n - L| < \varepsilon + \varepsilon = 2\varepsilon
$$
7. Per l'arbitrarietà di $\varepsilon > 0$, la successione reale ${x_n}$ converge in $\mathbb{R}$ al limite $L \in \mathbb{R}$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Distinzione tra $\mathbb{Q}$ e $\mathbb{R}$**: All'orale viene spesso chiesto: _"La condizione di Cauchy garantisce sempre la convergenza?"_ La risposta corretta è **NO nei numeri razionali $\mathbb{Q}$** (dove è solo condizione necessaria), mentre è **SÌ nei numeri reali $\mathbb{R}$** grazie alla proprietà di completezza del continuo reale.
- **Utilità della condizione di Cauchy**: Sottolineare che la condizione di Cauchy permette di stabilire la convergenza di una successione valutando unicamente le relazioni tra i suoi termini ($|x_m - x_n|$), **senza dover conoscere a priori il valore del limite $L$**.
- **Definizione errata di Cauchy**: Definire erroneamente la condizione di Cauchy come $|x_{n+1} - x_n| < \varepsilon$ è un grave errore concettuale.

#### **Esercizio / Domanda di Verifica**

_Si consideri la successione delle somme parziali della serie armonica: $s_n = \sum_{k=1}^n \frac{1}{k}$. Mostrare che $|s_{n+1} - s_n| = \frac{1}{n+1} \to 0$, ma che la successione NON è di Cauchy valutando la differenza $|s_{2n} - s_n|$._

---

### **Fonti maggiormente utilizzate per questo Blocco**

Per la redazione di questo blocco e la verifica formale dei passaggi, le fonti del notebook consultate ed utilizzate in misura maggiore sono state:

1. **`Lezione 4 21-09.md`** e **`Lezione 5 23-09.md`**: Utilizzate per le dimostrazioni algebriche sui limiti di successioni (Somma e Prodotto) e per la formulazione della Condizione di Cauchy.
2. **`Numeri Reali.pdf`** e **`Lezione 6 28-09.md`**: Utilizzate per la dimostrazione del Teorema di Completezza di $\mathbb{R}$, la densità di $\mathbb{Q}$ in $\mathbb{R}$ e la convergenza delle successioni di Cauchy nei reali.
3. **`AMI 2026-27 Programma Teoremi Dimostarzioni.pdf`**: Utilizzato per verificare il perfetto allineamento con gli enunciati del programma d'esame.

---

Dimmi pure se la trattazione del **BLOCCO 2** è chiara e se possiamo proseguire subito con il **BLOCCO 3** (_Convergenza delle monotone limitate, Teorema di Esistenza del Sup/Inf, Teorema di Bolzano-Weierstrass_).

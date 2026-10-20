
## **BLOCCO 1: Proprietà dei limiti di successioni**

---

### **Teorema 1: Unicità del limite di una successione**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia ${x_n}_{n \ge n_0} \subseteq \mathbb{R}$ una successione numerica e supponiamo che essa ammetta due limiti $L_1, L_2 \in \mathbb{R}$, ovvero $\lim_{n \to +\infty} x_n = L_1$ e $\lim_{n \to +\infty} x_n = L_2$.
- **Tesi ($T$)**: $L_1 = L_2$.

#### **Idea Chiave della Dimostrazione**

Si procede per **dimostrazione per assurdo**. Ipotizzando che i limiti siano distinti ($L_1 \neq L_2$), si sfrutta la disuguaglianza triangolare sulla distanza $|L_1 - L_2|$ inserendo il termine della successione $x_n$. Si dimostra che la distanza fissa tra i due presunti limiti risulta minore di $2\varepsilon$ per ogni $\varepsilon > 0$ arbitrario, il che è possibile solo se la distanza è nulla.

#### **Dimostrazione Dettagliata**

1. Per **assurdo**, si supponga che la successione ammetta due limiti distinti $L_1, L_2 \in \mathbb{R}$ con $L_1 \neq L_2$, il che implica che la distanza tra di essi sia strettamente positiva: $|L_1 - L_2| > 0$.
2. Dalla definizione formale di limite, per qualsiasi $\varepsilon > 0$ fissato esistono due indici di soglia $N_1(\varepsilon), N_2(\varepsilon) \in \mathbb{N}$ tali che:
    - $\forall n > N_1(\varepsilon) \implies |x_n - L_1| < \varepsilon$
    - $\forall n > N_2(\varepsilon) \implies |x_n - L_2| < \varepsilon$
3. Si definisca un indice di soglia comune prendendo il massimo tra le due soglie: $N(\varepsilon) := \max(N_1(\varepsilon), N_2(\varepsilon))$.
4. Per ogni $n > N(\varepsilon)$ valgono simultaneamente entrambe le disuguaglianze. Valutando la distanza costante $|L_1 - L_2|$ ed applicando la disuguaglianza triangolare: $$
|L_1 - L_2| = |(L_1 - x_n) + (x_n - L_2)| \le |x_n - L_1| + |x_n - L_2| < \varepsilon + \varepsilon = 2\varepsilon
$$
5. La quantità reale non negativa $|L_1 - L_2|$ risulta strettamente minore di $2\varepsilon$ per qualsiasi $\varepsilon > 0$ scelto a piacere.
6. Per la **proprietà archimedea** dei numeri reali, l'unico numero reale non negativo minore di qualsiasi quantità positiva arbitraria è lo zero: $$
|L_1 - L_2| = 0 \implies L_1 = L_2
$$
7. Ciò entra in palese contraddizione con l'ipotesi per assurdo $L_1 \neq L_2$. Pertanto, il limite è unico.

#### **Punti Critici / Errori Tipici all'Orale**

- **La scelta di $N(\varepsilon)$**: All'orale è fondamentale specificare $N(\varepsilon) = \max(N_1, N_2)$. Senza prendere il massimo, i due intorni non sono garantiti valere per lo stesso indice $n$.
- **Passaggio logico finale su $2\varepsilon$**: Bisogna saper giustificare perché $|L_1 - L_2| < 2\varepsilon$ per ogni $\varepsilon > 0$ implica l'uguaglianza a zero. Sostenere che $2\varepsilon$ "tende a zero" senza menzionare l'arbitrarietà di $\varepsilon > 0$ è un errore concettuale.

#### **Esercizio / Domanda di Verifica**

_Se una successione non convergente ammette due sottosuccessioni che convergono a due valori distinti (es. $x_n = (-1)^n$), questo fatto viola il Teorema di Unicità del Limite? Motivare la risposta._

---

### **Teorema 2: Limitatezza delle successioni convergenti**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia ${x_n}_{n \in \mathbb{N}}$ una successione numerica convergente a un limite finito $L \in \mathbb{R}$ (in simboli $\lim_{n \to +\infty} x_n = L$).
- **Tesi ($T$)**: La successione ${x_n}$ è **limitata**, ossia esiste una costante $M \ge 0$ tale che $|x_n| \le M$ per ogni $n \in \mathbb{N}$.

#### **Idea Chiave della Dimostrazione**

Fissata una tolleranza arbitraria (es. $\varepsilon = 1$), la definizione di limite garantisce che **definitivamente** tutti i termini della successione cadono nell'intervallo limitato $(L-1, L+1)$. I termini che rimangono fuori dall'intervallo sono al più in **numero finito**, e qualsiasi insieme finito di numeri ammette sempre massimo e minimo.

#### **Dimostrazione Dettagliata**

1. Si applica la definizione di limite scegliendo la tolleranza specifica $\varepsilon = 1 > 0$.
2. In corrispondenza di $\varepsilon = 1$, esiste una soglia $N_1 \in \mathbb{N}$ tale che per tutti gli indici $n \ge N_1$ si ha: $$
|x_n - L| < 1 \iff L - 1 < x_n < L + 1
$$
3. L'insieme di tutti i valori assunti dalla successione si scompone nell'unione di due sottoinsiemi: $$
{x_n}_{n \in \mathbb{N}} = {x_0, x_1, \dots, x_{N_1 - 1}} \cup {x_n}_{n \ge N_1}
$$
4. Il primo sottoinsieme ${x_0, x_1, \dots, x_{N_1 - 1}}$ è **finito** (contiene i primi $N_1$ termini), quindi ammette un valore massimo per i moduli: $K_1 := \max({|x_0|, |x_1|, \dots, |x_{N_1 - 1}|})$.
5. Il secondo sottoinsieme ${x_n}_{n \ge N_1}$ è contenuto nell'intervallo $(L - 1, L + 1)$, quindi i suoi elementi sono limitati in modulo dalla costante $K_2 := \max(|L - 1|, |L + 1|)$.
6. Scegliendo la costante globale $M := \max(K_1, K_2)$, si ottiene che $|x_n| \le M$ per ogni $n \in \mathbb{N}$, dimostrando che la successione è limitata.

#### **Punti Critici / Errori Tipici all'Orale**

- **Scambio delle implicazioni (Teorema inverso falso)**: All'orale viene spesso chiesto se una successione limitata sia necessariamente convergente. La risposta è **NO** (il controesempio classico è $x_n = (-1)^n$, che è limitata da $M=1$ ma non converge). La limitatezza è condizione necessaria ma non sufficiente per la convergenza.
- **Ruolo del numero finito di termini**: È fondamentale sottolineare che i termini al di fuori della "trappola" sono in numero finito.

#### **Esercizio / Domanda di Verifica**

_Sia $x_n = \frac{n^2 + 1}{2n^2 + 3}$. Dimostrare che è limitata trovando una costante $M$ esplicita tramite il calcolo del limite._

---

### **Teorema 3: Teorema del segno e della monotonia per successioni**

---

#### **Parte A: Teorema di Permanenza del Segno (Dalla successione al limite)**

##### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia ${x_n}$ una successione numerica a valori non negativi ($x_n \ge 0$ per ogni $n \in \mathbb{N}$, o definitivamente) per cui esiste il limite $\lim_{n \to +\infty} x_n = L \in \mathbb{R}$.
- **Tesi ($T$)**: Il limite è non negativo: $L \ge 0$.

##### **Idea Chiave della Dimostrazione**

Si dimostra per **assurdo**. Se il limite $L$ fosse strettamente negativo, si sceglierebbe come raggio dell'intorno la quantità positiva $\varepsilon = -L/2$. Per la definizione di limite, i termini della successione dovrebbero definitivamente cadere in questo intorno ed essere negativi, contraddicendo l'ipotesi $x_n \ge 0$.

##### **Dimostrazione Dettagliata**

1. Si supponga per **assurdo** che $L < 0$.
2. Nella definizione di limite, si scelga il valore positivo arbitrario $\varepsilon := -\frac{L}{2} > 0$.
3. Per la definizione di limite, in corrispondenza di tale $\varepsilon$ esiste una soglia $N \in \mathbb{N}$ tale che per tutti gli indici $n \ge N$ vale: $$
L - \varepsilon < x_n < L + \varepsilon
$$
4. Valutando esplicitamente la disuguaglianza di destra per $n \ge N$: $$
x_n < L + \left(-\frac{L}{2}\right) = \frac{L}{2} < 0
$$
5. Risulterebbe $x_n < 0$ per tutti gli indici $n \ge N$, in palese contraddizione con l'ipotesi iniziale che $x_n \ge 0$ definitivamente.
6. Pertanto, l'ipotesi per assurdo cade e deve valere $L \ge 0$.

---

#### **Parte B: Teorema di Monotonia (Conservazione dell'ordine)**

##### **Enunciato Formale**

- **Ipotesi ($H$)**: Siano ${x_n}$ e ${y_n}$ due successioni numeriche tali che $x_n \le y_n$ definitivamente per $n \to +\infty$. Supponiamo che esistano finiti i limiti $\lim_{n \to +\infty} x_n = L_1 \in \mathbb{R}$ e $\lim_{n \to +\infty} y_n = L_2 \in \mathbb{R}$.
- **Tesi ($T$)**: $L_1 \le L_2$.

##### **Idea Chiave della Dimostrazione**

Si riconduce il problema alla Parte A definendo la successione differenza $z_n := y_n - x_n \ge 0$ ed applicando ad essa il Teorema di Permanenza del Segno.

##### **Dimostrazione Dettagliata**

1. Si definisca la successione ausiliaria differenza ${z_n} := {y_n - x_n}$.
2. Dall'ipotesi $x_n \le y_n$, la successione $z_n$ è a termini non negativi ($z_n \ge 0$ per ogni $n$ definitivamente).
3. Per il teorema sul limite della somma/differenza di successioni convergenti, il limite di $z_n$ esiste e vale: $$
\lim_{n \to +\infty} z_n = \lim_{n \to +\infty} (y_n - x_n) = L_2 - L_1
$$
4. Applicando il **Teorema di permanenza del segno** (Parte A) alla successione non negativa $z_n \ge 0$, si conclude che: $$
L_2 - L_1 \ge 0 \implies L_1 \le L_2
$$

#### **Punti Critici / Errori Tipici all'Orale**

- **Passaggio da disuguaglianza stretta a debole**: È un errore grave sostenere all'esame che se $x_n > 0$ allora $L > 0$. **Le disuguaglianze strette tra i termini di una successione diventano deboli al limite**. Ad esempio, $x_n = \frac{1}{n} > 0$ per ogni $n \ge 1$, ma il suo limite è $L = 0 \ge 0$.
- **Distinzione tra le due versioni della Permanenza del Segno**: Ricordare la differenza tra "dalla successione al limite" ($x_n \ge 0 \implies L \ge 0$) e "dal limite alla successione" ($L > 0 \implies x_n > 0$ definitivamente).

#### **Esercizio / Domanda di Verifica**

_Siano $x_n = 1 - \frac{1}{n}$ e $y_n = 1 + \frac{1}{n}$. Si ha $x_n < y_n$ per ogni $n \ge 1$. Quali sono i rispettivi limiti $L_1$ e $L_2$? La relazione tra i limiti è stretta o debole?_

---

📐 Se il formato di formattazione LaTeX soddisfa le tue esigenze, dimmi pure se vogliamo procedere subito con il **BLOCCO 2** (_Somma e prodotto di limiti di successioni; Condizione di Cauchy_).

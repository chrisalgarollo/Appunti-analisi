
## **BLOCCO 3: Completezza e Bolzano-Weierstrass**

---

### **Teorema 1: Convergenza delle Successioni Monotone e Limitate in $\mathbb{R}$**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia ${x_n}_{n \in \mathbb{N}} \subseteq \mathbb{R}$ una successione numerica reale monotona crescente (ovvero $x_n \le x_{n+1}$ per ogni $n \in \mathbb{N}$) e superiormente limitata (ovvero $\exists M \in \mathbb{R}$ tale che $x_n \le M$ per ogni $n \in \mathbb{N}$).
- **Tesi ($T$)**: La successione ${x_n}$ converge a un limite finito $L \in \mathbb{R}$ (in simboli $\lim_{n \to +\infty} x_n = L$). Specularmente, una successione monotona decrescente e inferiormente limitata converge ad un limite finito in $\mathbb{R}$.

#### **Idea Chiave della Dimostrazione**

Si dimostra per **assurdo** sfruttando la **Completezza di $\mathbb{R}$** (una successione reale converge se e solo se è una successione di Cauchy). Se la successione non fosse di Cauchy, la negazione della proprietà permetterebbe di isolare ad ogni passo uno scarto fisso $\ge \varepsilon$; la monotonia crescente accumulerebbe infiniti scarti $\varepsilon$, costruendo una sottosuccessione divergente a $+\infty$ e contraddicendo l'ipotesi di limitatezza superiore.

#### **Dimostrazione Dettagliata**

1. Si supponga per **assurdo** che la successione ${x_n}$ non sia di Cauchy in $\mathbb{R}$.
2. La negazione della proprietà di Cauchy equivale ad affermare che: $$
\exists \varepsilon > 0 \quad \text{tale che} \quad \forall N \in \mathbb{N}, ; \exists , n_N, m_N \ge N \quad \text{con} \quad |x_{n_N} - x_{m_N}| \ge \varepsilon
$$
3. Senza perdita di generalità, si assuma l'ordinamento degli indici $n_N > m_N$. Poiché la successione è monotona crescente ($x_{n_N} \ge x_{m_N}$), la rimozione del modulo fornisce: $$
x_{n_N} - x_{m_N} \ge \varepsilon \implies x_{n_N} \ge x_{m_N} + \varepsilon
$$
4. Si costruisca ricorsivamente una sequenza di indici ponendo la prima soglia $N_1 = 1$, ottenendo due indici $n_1 > m_1 \ge 1$ tali che $x_{n_1} \ge x_{m_1} + \varepsilon \ge x_1 + \varepsilon$.
5. Si scelga la soglia successiva $N_2 = n_1$. Esisteranno indici $n_2 > m_2 \ge n_1$ per cui $x_{n_2} \ge x_{m_2} + \varepsilon \ge x_{n_1} + \varepsilon \ge x_1 + 2\varepsilon$.
6. Reiterando la scelta al generico passo $k \in \mathbb{N}$, si seleziona $N_{k+1} = n_k$, ottenendo una sottosuccessione che soddisfa: $$
x_{n_k} \ge x_1 + k \cdot \varepsilon \quad \forall k \ge 1
$$
7. Poiché $\varepsilon > 0$ è una costante fissata, per $k \to +\infty$ la quantità $k \cdot \varepsilon$ diverge a $+\infty$. Di conseguenza, la sottosuccessione ${x_{n_k}}$ (e di riflesso l'intera successione ${x_n}$) risulta non limitata superiormente.
8. Tale conclusione entra in palese contraddizione con l'ipotesi iniziale di **limitatezza superiore** ($x_n \le M$).
9. **Conclusione**: La successione ${x_n}$ è una successione di Cauchy e, per la proprietà di completezza di $\mathbb{R}$, **converge** a un limite finito $L \in \mathbb{R}$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Valore esplicito del limite**: All'orale si deve sempre precisare a cosa converge il limite. Per una successione crescente e superiormente limitata, il limite coincide con l'estremo superiore dell'immagine della successione: $L = \sup_{n \in \mathbb{N}} x_n$.
- **Falsità del teorema nei razionali $\mathbb{Q}$**: Bisogna evidenziare che questo teorema vale nei reali ma **fallisce nei razionali**. Il controesempio è la successione ricorsiva $x_1 = 2, x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n}$, la quale è monotona decrescente e inferiormente limitata da $\sqrt{2}$ in $\mathbb{Q}$, ma non converge in $\mathbb{Q}$ poiché il suo limite è irrazionale.

#### **Esercizio / Domanda di Verifica**

_Sia $x_1 = 1$ e $x_{n+1} = \sqrt{2 + x_n}$ per $n \ge 1$. Dimostrare per induzione che $x_n < 2$ per ogni $n$ e che $x_n$ è strettamente crescente, deducendone la convergenza e calcolandone il limite._

---

### **Teorema 2: Teorema di Esistenza dell'Estremo Superiore ed Inferiore**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia $A \subseteq \mathbb{R}$ un sottoinsieme di numeri reali non vuoto ($A \neq \emptyset$) e superiormente limitato (ovvero esiste un maggiorante $B_0 \in \mathbb{R}$ tale che $x \le B_0$ per ogni $x \in A$).
- **Tesi ($T$)**: L'insieme $A$ ammette **estremo superiore finito** in $\mathbb{R}$, indicato con $\sup A \in \mathbb{R}$. (Analogamente, ogni sottoinsieme non vuoto e inferiormente limitato ammette estremo inferiore finito $\inf A \in \mathbb{R}$).

#### **Idea Chiave della Dimostrazione**

Si applica il **metodo di dicotomia** (dimezzamento ricorsivo dell'intervallo). Presi un elemento $A_0 \in A$ e un maggiorante $B_0$, si suddivide l'intervallo $[A_0, B_0]$ a metà. Se la metà di destra contiene punti di $A$, la si seleziona; altrimenti si seleziona la metà di sinistra. Le successioni degli estremi sinistri e destri convergono allo stesso limite reale $\bar{x}$, che si dimostra essere l'estremo superiore $\sup A$.

#### **Dimostrazione Dettagliata**

1. Poiché $A$ è superiormente limitato, esiste un maggiorante $B_0 \in \mathbb{R}$. Essendo $A$ non vuoto, si scelga un elemento $A_0 \in A$.
2. Si consideri l'intervallo chiuso $[A_0, B_0]$, per il quale $A_0 \in A \cap [A_0, B_0] \neq \emptyset$ e $B_0$ è un maggiorante di $A$.
3. Si calcoli il punto medio $C_1 = \frac{A_0 + B_0}{2}$, che suddivide l'intervallo nei due sottointervalli $[A_0, C_1]$ e $[C_1, B_0]$.
4. **Regola di selezione dicotomica**:
    - Se la metà di destra $[C_1, B_0]$ contiene elementi di $A$, si definisce il nuovo intervallo $[A_1, B_1] := [C_1, B_0]$. L'estremo $B_1 = B_0$ rimane un maggiorante.
    - Se la metà di destra non contiene elementi di $A$, gli elementi di $A$ risiedono nella metà di sinistra $[A_0, C_1]$. Si definisce $[A_1, B_1] := [A_0, C_1]$. Il punto medio $B_1 = C_1$ è un maggiorante di $A$.
5. Iterando la dicotomia $k$ volte, si genera una successione di intervalli incapsulati $[A_k, B_k]$ tali che:
    - $[A_{k+1}, B_{k+1}] \subseteq [A_k, B_k]$ per ogni $k \ge 0$.
    - L'intersezione $[A_k, B_k] \cap A \neq \emptyset$ per ogni $k \ge 0$.
    - L'estremo destro $B_k$ è un **maggiorante** di $A$ per ogni $k \ge 0$.
    - L'ampiezza è data da $B_k - A_k = \frac{B_0 - A_0}{2^k}$.
6. La successione degli estremi sinistri ${A_k}$ è **monotona crescente** e superiormente limitata da $B_0$, quindi converge ad un limite $\bar{x} \in \mathbb{R}$.
7. La successione degli estremi destri ${B_k}$ è **monotona decrescente** e inferiormente limitata da $A_0$, quindi converge ad un limite $\bar{y} \in \mathbb{R}$.
8. Valutando la differenza tra i due limiti: $$
\bar{y} - \bar{x} = \lim_{k \to +\infty} (B_k - A_k) = \lim_{k \to +\infty} \frac{B_0 - A_0}{2^k} = 0 \implies \bar{x} = \bar{y}
$$
9. Si verifica che il limite comune $\bar{x} \in \mathbb{R}$ è l'**estremo superiore** di $A$:
    - **Verifica di maggiorante**: Poiché ogni $B_k$ è maggiorante di $A$ ($x \le B_k$ per ogni $x \in A$), dal teorema di monotonia dei limiti segue che $x \le \lim_{k \to +\infty} B_k = \bar{x}$ per ogni $x \in A$. Dunque $\bar{x}$ è un maggiorante.
    - **Verifica di minimo dei maggioranti**: Fissato $\varepsilon > 0$, poiché $A_k \to \bar{x}$, esiste un indice $k$ per cui $A_k > \bar{x} - \varepsilon$. Poiché l'intervallo $[A_k, B_k]$ contiene elementi di $A$, esiste un $x \in A$ tale che $x \ge A_k > \bar{x} - \varepsilon$. Pertanto $\bar{x} - \varepsilon$ non è un maggiorante.
10. Si conclude che $\bar{x} = \sup A \in \mathbb{R}$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Distinzione tra Estremo Superiore e Massimo**: Sottolineare che $\sup A$ esiste sempre in $\mathbb{R}$ per insiemi non vuoti e limitati superiormente. Se $\sup A \in A$, esso è anche **massimo** ($\max A := \sup A$). Se invece $\sup A \notin A$ (es. l'intervallo $[a, b)$ ha $\sup = b \notin A$), l'insieme **non possiede massimo**.
- **Caratterizzazione epsilon di $\sup A$**: Bisogna saper esporre le due condizioni formali:
    1. $\forall x \in A \implies x \le \bar{x}$ ($\bar{x}$ è maggiorante).
    2. $\forall \varepsilon > 0, \exists x \in A \quad \text{tale che} \quad x > \bar{x} - \varepsilon$ ($\bar{x}$ è il minimo dei maggioranti).

#### **Esercizio / Domanda di Verifica**

_Sia $A = {x \in \mathbb{Q} \mid x^2 < 2}$. Determinare $\sup A$ in $\mathbb{R}$. L'insieme $A$ ammette massimo in $\mathbb{R}$? Ammette massimo in $\mathbb{Q}$?_

---

### **Teorema 3: Teorema di Bolzano-Weierstrass (Esistenza di Punti di Accumulazione)**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia $E \subseteq \mathbb{R}$ un sottoinsieme dei numeri reali che sia **limitato** (contenuto in un intervallo chiuso $[a_0, b_0]$) e **infinito** (avente cardinalità non finita, $\sharp(E) = \infty$).
- **Tesi ($T$)**: L'insieme $E$ ammette **almeno un punto di accumulazione** in $\mathbb{R}$, ovvero l'insieme derivato è non vuoto ($E' \neq \emptyset$). Equivale a dire che da ogni successione numerica limitata in $\mathbb{R}$ è possibile estrarre una **sottosuccessione convergente**.

#### **Idea Chiave della Dimostrazione**

Si applica la **dicotomia** all'intervallo $[a_0, b_0]$ contenente $E$. Dividendo l'intervallo a metà, **altrimenti entrambi i sottointervalli conterrebbero un numero finito di punti di $E$**, il che renderebbe l'unione finita e contraddirebbe l'ipotesi che $E$ è infinito. Scegliendo ricorsivamente la metà con infiniti punti, il Teorema dei due carabinieri applicato agli estremi degli intervalli e a una successione di punti distribuiti nell'intersezione garantisce l'esistenza del punto di accumulazione.

#### **Dimostrazione Dettagliata**

1. Poiché $E$ è **limitato**, esso è contenuto in un intervallo chiuso $[a_0, b_0] \subset \mathbb{R}$. L'intersezione $[a_0, b_0] \cap E = E$ contiene infiniti punti.
2. Si consideri il punto medio $c = \frac{a_0 + b_0}{2}$, che suddivide l'intervallo in $[a_0, c]$ e $[c, b_0]$.
3. **Regola di selezione dicotomica**: Almeno uno dei due sottointervalli contiene **infiniti punti** di $E$. (Se infatti entrambi contenessero un numero finito di punti di $E$, la loro unione $[a_0, b_0]$ conterrebbe un numero finito di punti di $E$, contro l'ipotesi che $E$ è infinito).
4. Si seleziona una delle metà che contiene infiniti punti di $E$ e la si denota con $[a_1, b_1]$.
5. Iterando ricorsivamente il procedimento $k$ volte, si genera una successione incapsulata di intervalli $[a_k, b_k]$ tali che:
    - $[a_{k+1}, b_{k+1}] \subseteq [a_k, b_k] \subseteq \dots \subseteq [a_0, b_0]$ per ogni $k \ge 0$.
    - L'intersezione $[a_k, b_k] \cap E$ contiene **infiniti punti** di $E$ per ogni $k \ge 0$.
    - L'ampiezza dell'intervallo vale $b_k - a_k = \frac{b_0 - a_0}{2^k}$.
6. La successione degli estremi sinistri ${a_k}$ è **monotona crescente** e la successione degli estremi destri ${b_k}$ è **monotona decrescente**. Entrambe le successioni convergono allo stesso limite reale $\bar{x} \in \mathbb{R}$: $$
\lim_{k \to +\infty} a_k = \lim_{k \to +\infty} b_k = \bar{x}
$$
7. **Costruzione della successione vincolata**: Poiché ogni intervallo $[a_k, b_k]$ contiene infiniti punti di $E$, per ogni $k \in \mathbb{N}$ è possibile scegliere un punto $x_k \in E \cap [a_k, b_k]$ tale che $x_k \neq \bar{x}$.
8. Per ogni $k \in \mathbb{N}$, il punto $x_k$ soddisfa: $a_k \le x_k \le b_k$.
9. **Applicazione del Teorema dei due carabinieri**: Poiché $a_k \to \bar{x}$ e $b_k \to \bar{x}$, si conclude che: $$
\lim_{k \to +\infty} x_k = \bar{x}
$$
10. **Conclusione**: Essendo ${x_k} \subseteq E \setminus {\bar{x}}$ una successione di punti di $E$ tutti distinti da $\bar{x}$ e convergente a $\bar{x}$, per la caratterizzazione sequenziale dei punti di accumulazione il numero reale $\bar{x}$ è un **punto di accumulazione** per l'insieme $E$ ($\bar{x} \in E'$).

#### **Punti Critici / Errori Tipici all'Orale**

- **Necessità ed indipendenza delle ipotesi**: All'esame viene chiesto cosa accade rimuovendo una delle ipotesi:
    - Se si rimuove l'ipotesi di **infinità** (insieme limitato ma finito, es. $E = {1, 2, 3}$), l'insieme ha $E' = \emptyset$ (tutti i punti sono isolati).
    - Se si rimuove l'ipotesi di **limitatezza** (insieme infinito ma illimitato, es. $E = \mathbb{N}$), si ha $E' = \emptyset$.
- **Formulazione per sottosuccessioni**: Saper enunciare la formulazione equivalente per successioni: _"Da ogni successione numerica reale limitata ${x_n}$ è possibile estrarre una sottosuccessione convergente ${x_{n_k}}$."_.

#### **Esercizio / Domanda di Verifica**

_Sia $x_n = (-1)^n + \frac{1}{n}$. Mostrare che la successione è limitata ed estrarre due sottosuccessioni convergenti a due limiti distinti, individuando l'insieme dei punti di accumulazione dell'immagine della successione._

---

### **Fonti maggiormente utilizzate per questo Blocco**

Per la redazione e la verifica rigorosa delle dimostrazioni di questo **BLOCCO 3**, le fonti del notebook maggiormente consultate ed utilizzate sono state:

1. **`Proprieta di completezza di R.pdf`**: Fonte principale per le dimostrazioni formali del Teorema di Convergenza delle successioni monotone limitate, del Teorema di Esistenza del Sup e del Teorema di Bolzano-Weierstrass (con il metodo di dicotomia).
2. **`Lezione 7 30-09.md`** e **`Lezione 8 05-10.md`**: Utilizzate per le definizioni rigorose di maggiorante/minorante, estremo superiore/inferiore, punti isolati, punti di accumulazione e la caratterizzazione dei punti di accumulazione mediante successioni.
3. **`AMI 2026-27 Programma Teoremi Dimostarzioni.pdf`**: Utilizzato per garantire la perfetta corrispondenza con i punti 7, 8, 9 e 10 del programma ufficiale d'esame.

---

Dimmi pure se la trattazione del **BLOCCO 3** è chiara e se possiamo passare subito al **BLOCCO 4** (_Numeri Complessi: Teorema di De Moivre per le radici $n$-esime_).

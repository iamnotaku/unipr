# ***Ripasso Metodi Probabilistici per l'Ingegneria***
## **Teoria assiomatica della probabilita' (Kolmogorov 1933):**

Sia $\Omega$ uno spazio campionario di tipo discreto relativo a un esperimento casuale.

Per ogni evento $E \subseteq \Omega$ è definito un numero $\mathbb{P}(E)$, detta Probabilità di $E$ che soddisfa i 3 assiomi sotto riportati:

1. $\mathbb{P}(E)$ è un numero reale non negativo: FORMALMENTE: $\mathbb{P}(E) \in \mathbb{R}, \mathbb{P}(E) \geq 0, \forall \, E \subseteq \Omega$
2. $\mathbb{P}(\Omega)=1, (spazio \ campionario \ = evento \ certo \ = 1)$
3. Per la coppia di eventi incompatibili $E_1, E_2 \subseteq \Omega$, la probabilita' dell'evento unione e' la somma della loro probabilita; FORMALMENTE $\mathbb{P}(E_1 \cup E_2) = \mathbb{P}(E_1) + \mathbb{P}(E_2), \ \ \forall \, E_1, E_2 \subseteq \Omega, E_1 \cap E_2 = \varnothing$

## **Campo di Borel:**
Quando la famiglia degli eventi di $f$ e' un campo infinito numerabile, abbiamo un'assioma aggiuntivo

4. Poniamo la seguente serie come $convergente$: $\ \mathbb{P}(\displaystyle\sum_{i=1}^{\infty} E_i) =  \displaystyle\sum_{i=1}^{\infty} \mathbb{P}(E_i)$

- $\mathbb{P}(\varnothing) =0, \ \mathbb{P}(E + \varnothing) = \mathbb{P}(E), \ \mathbb{P}(E) + \mathbb{P}(\varnothing), \ E\varnothing = 0$
- $\mathbb{P}(\bar E) = 1 - \mathbb{P}(E), \ \Omega = E+\bar E, \ E\bar E = \varnothing \ \mathbb{P}(\Omega) = 1 = \mathbb{P}(E + \bar E) = \mathbb{P}(E) + \mathbb{P}(\bar E)$
- $\mathbb{P}(E+F) = \mathbb{P}(E) + \mathbb{P}(F) - \mathbb{P}(EF)$

## **Probabilita' Condizionata:**

E' definita cosi' quella probabilita' che si verifichi un evento $E$ dopo che si e' verificato gia' un evento $F$. Questa probabilita' si indica con $\mathbb{P}(E|F)$, cioe' probabilita' di $E$ condizionata a $F$, ed e' definibile solo se $\mathbb{P}(F) \neq 0$

Formalmente: $\mathbb{P}(E|F) = \dfrac{\mathbb{P}(EF)}{\mathbb{P}(F)}, \ \mathbb{P}(F) \neq 0$

### **Proprieta':**

P1. Se $E$ e' incluso in $F$, allora la proprieta' condizionata $\mathbb{P}(E|F)$ sara': $\ \dfrac{\mathbb{P}(E)}{\mathbb{P}(F)}$.

P2. $\mathbb{P}(E|F) = 1 \iff F \subseteq E$

P3. Se $E,F$ sono incompatibili  e se anche $\mathbb{P}(E) \neq 0$ allora la probabilita' condizionata di ogni evento rispetto agli altri e' $0$. FORMALMENTE: $\mathbb{P}(E|F)= \mathbb{P}(F|E) = 0$

P4. $\mathbb{P}(\bar E|F)=1 -\mathbb{P}(E|F)$

P5. $\mathbb{P}(E_1 \cap E_2|F) = \mathbb{P}(E_1|F) + \mathbb{P}(E_2|F) - \mathbb{P}(E_1 \cap E_2|F)$

## **Eventi Indipendenti:**

**Due eventi si dicono indipendenti se la probabilita' della loro intersezione e' il prodotto delle singole probabilita'.**

Formalmente: $E,F \ Indipendenti \iff \mathbb{P}(E \cap F) = \mathbb{P}(E) \ \mathbb{P}(F)$

**Per la legge di annullamento del prodotto notiamo che se uno dei due eventi e' levento impossibile allora gli eventi sono automaticamente indipendenti.**

Formalmente: $\mathbb{P}(E) = 0 \implies \mathbb{P}(E) \ \mathbb{P}(F) = 0$

## **Definizione di probabilita' classica:**

Secondo questa definizione, la probabilita' di un evento $E, \mathbb{P}(E)$ e' il rapporto tra il numero dei casi favorevoli e il numero di casi possibili, cioe':

$\mathbb{P}(E) = \dfrac{\#casi \ favorevoli}{\#casi \ possibili}$

## **Teorema di Bayes:**

Serve per calcolare la probabilita' condizionata di un evento $E$ rispetto a uno $F$, a patto di saper calcolare o conoscere, le probabilita' di $E \ e \ F$ e la probabilita' condizionata di $F$ rispetto a $E$.

### **Enunciato:**
Siano $E,F$ due eventi con probabilita' non nulle.

La probabilita' condizionata di $E$ rispetto a $F$ e' uguale al prodotto tra la probabilita' condizionata di $F$ rispetto $E$ e la probabilita' di  $E$, fratto la probabilita' di $F$.

FORMALMENTE: $\mathbb{P}(E|F)= \dfrac{\mathbb{P}(F|E)\ \mathbb{P}(E)}{\mathbb{P}(F)}$

## **Probabilita' Totale:**

Detto anche probabilita' dell'unione, e' la probabilita' che si realizzi almeno tra due o piu' eventi, ossia che si verifichi l'evento dato dalla loro unione.

### **Enunciato:**

Dati due o piu' eventi $E_1,E_2 \subseteq \Omega$, la probabilita' dell'unione di questi due si puo' esprimere cosi': $\mathbb{P}(E_1 \cup E_2) = \mathbb{P}(E_1) + \mathbb{P}(E_2) - \mathbb{P}(E_1 \cap E_2)$

## **Prove Ripetute (Formula di Bernoulli):**

con $k \leq n$, se l'evento indagato ha probabilita' $p$ di verificarsi per ciascuna prova, ed effettuiamo $n$ prove indipendenti, la probabilita' che l'evento si verifichi $k$ volte e' data da: $$\mathbb{P}(k \ successi \ su \ n \ prove) = \binom{n}{k} \ p^k \cdot (1-p)^{n-k}$$

## **Definizione di variabile aleatoria:** 

E' una funzione che associa un numero reale a ciascun possibile esito un esperimento casuale.

**In altre parole, e' una variabile il cui valore dipende dall'esito di un fenomeno aleatorio.**

### **Definizione formale:**

Una variabile aleatoria $X$ e' una funzione che mappa ogni elemento dello spazio campionario $\omega \in \Omega$ in un numero reale $X(\omega)$

$X : \Omega \to \mathbb{R}$

### **Tipi di variabili aleatorie:**

- **Variabile aleatoria discreta**: Assume un insieme finito o numerabile di valori distinti. Tipo il numero di volte che una moneta esce testa in 10 lanci è una variabile aleatoria discreta.

- **Variabile aleatoria continua**: Assume un insieme continuo di valori, tipicamente rappresentato da un intervallo di numeri reali. Ad esempio, l'altezza di una persona misurata in metri è una variabile aleatoria continua.

- **Variabile aleatoria mista:** Assume un insieme di valori che varia tra discreti e continui

### **Funzioni di probabilita':**

- **Funzione di probabilita' (PMF)**: Per una v.a. discreta, la funzione di probabilita' di massa $\mathbb{P}(X=x)$ fornisce la probabilita' che $X$ assuma un particolare valore $x$.

- **Funzione di densita' di probabilita' (PDF)**: Per una v.a. continua, la funzione di densita' $f_X(x)$ non fornisce la probabilita' diretta che X assuma un valore esatto, ma piuttosto la probabilita' che $X$ casa in un certo intervallo e' data dall'integrale della PDF su quell'intervallo.

- **Funzione di distribuzione cumulativa (CDF)**: Indipendentemente dal tipo, ogni  v.a. $X$ ha una funzione di distribuzione cumulativa $F_X(x)$, che rappresenta la probabilita' che $X$ assuma un valore minore o uguale a $x$: $F_X(x) = \mathbb{P}(X \leq x)$


## **Cumulative Distribution Function (CDF):**

Questa e' la funzione $F:\mathbb{R} \to [0,1]$, tale che abbia quindi dominio sulla retta reale eimmagine nell'intervallo $[0, 1]$.

Come funzione di ripartizione e' valida solo se non e' decrescente, continua a destra e $$F(x) \geq 0, \ \forall x,\lim\limits_{x \to +\infty} F(x) =1, \ \lim\limits_{x \to -\infty} F(x) = 0$$.

**Una funzione di ripartizione non e' necessariamente continua a sinistra**, per esempio se la v.a. $X$ e' discreta e $z$ un punto del suo supporto, allora $F$ e' una **funzione a gradino** e dunque $$\lim\limits_{x \to z^-} F(x) = \ \lim\limits_{x \to z^-} \displaystyle\sum_{i-1}^{n} p(x_i) = \displaystyle\sum_{i=1}^{n} p(x_i)$$

## **Probability Density Function (PDF):**

1. **Definizione Intuitiva:**
Per una variabile aleatoria continua, la funzione di densità di probabilità 
$𝑓_𝑋(x)$ descrive la "densità" di probabilità attorno a un punto specifico $x$.
Anche se una variabile aleatoria continua può assumere un numero infinito di valori all'interno di un intervallo, la probabilità che essa assuma esattamente un singolo valore $x$ è in realtà $0$. Invece, la pdf indica come la probabilità è distribuita attorno ai diversi valori di $x$.

2. **Proprietà della PDF:** 
- Non negativita': $f_X(x) \geq 0$ per ogni $x$. La densita' non puo' mai essere negativa.

- **Area sotto la curva:** L'area totale sotto la curva della pdf su tutto lo spazio dei valori possibili deve essere 1, il che riflette il fatto che la probabilità totale di tutti gli eventi possibili è 1: $$\int_{-\infty}^{+\infty} f_X(x) \ dx = 1$$

- **Probabilita' come area:** La probabilita' che la v.a. $X$ cada in un certo intervallo $[a, b]$ e' data dall'area sotto la curva della PDF tra $a$ e $b$: $$\mathbb{P}(a \leq X \leq b)= \int_a^b f_X(x) \ dx$$

## **Esempi di variabili aleatorie**

### **Variabile aleatoria di Bernoulli:**

- Sappiamo che l'insieme delle soluzioni, di una variabile aleatoria di Bernoulli comprende i numeri da 0 a 1: $X(S) = [0,1]$

- **La funzione di probabilita'** di $X$ assegna $1$ la probabilita' di successo $p$ e allo $0$ la probabilita' di insuccesso $1-p$: $$f_X:X(S)\to \mathbb{R}, f_X(i)= P([X=i]) = p^i(1-p)^{1-i}$$

- **La funzione di ripartizione** di $X$ e' nulla prima dello $0$, vale $1$ dopo l'$1$ e vale $1-p$ tra $0$ e $1$: $$F_X:\mathbb{R}\to[0,1], \ F_X(x) = P(X\leq x) = \begin{cases} 0 & \quad \text{se $x < 0 $} \\ 1-p & \quad \text{se $0 \leq x < 1$} \\ 1 & \quad \text{se $x \geq 1$} \end{cases}$$

- **Valore atteso e varianza** di $X$ valgono: $$E[X] = \mu_X = p$$ $$Var[X] = \sigma^2_X = p(1-p)$$

### **Variabile aleatoria binomiale:**

- $X$ puo' assumere valori interi da $0$ a $n$.

- **La funzione di probabilita'** di $X$ vale: $$f_X:X(S)\to\mathbb{R}, f_X(i)= P(X=i)=C_{n,i}\ p^i(1-p)^{n-i}$$
dove il numero $p^i(1-p)^{n-i}$ esprime la probabilita' di una specifica sequenza di $i$ successi ed $n-i$ insuccessi, mentre il numero $C_{n,i} = \frac{n!}{i!(n-i)!} = \binom{n}{i}$ e' il coefficiente binomiale $n$ su $i$ e conta il numero di possibili sequenze con $i$ successi e $n-i$ insuccessi; quindi la funzione $f_X(i)$ e' la probabilita' di $i$ successi in $n$ prove.

- **La funzione di ripartizione** si ottiene semplicemente dalla somma della funzione di probabilita', $F_X(x)=\displaystyle\sum_i\leq x \ \ f_X(i)$ secondo la regola generale, ma non ammette una forma analitica esplicita'.

- **Il valore atteso e la varianza** di $X$ valgono: $$E[X] = \mu_X = np$$ $$Var[X] = \sigma_X^2 = np(i-p)$$
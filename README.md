


*Disclaimer: As an AI text model, I cannot directly generate and send a literal `.pdf` file attachment. However, I have prepared the complete, heavily detailed step-by-step solutions manual below, formatted beautifully in Markdown. You can easily generate a PDF from this by right-clicking and selecting "Print > Save as PDF," or by pasting this text into a Markdown-to-PDF converter or LaTeX editor.*

***

# Solutions Manual: Quantum Mechanics & Computing
**Exercise Set #2 (UC Santa Cruz, PHYS 150 / CSE 109)**

## Problem 1
**Consider the 2-qubit state**
$$|\psi\rangle = \frac{1}{\sqrt{2}} \left( |0\rangle_1 |0\rangle_2 - |1\rangle_1 |1\rangle_2 \right)$$
**Determine the expectation values $\langle Z_1Z_2 \rangle$ and $\langle X_1X_2 \rangle$ in this state.**

**Why and How:**
The expectation value of an observable $A$ in a state $|\psi\rangle$ is defined as $\langle A \rangle = \langle \psi | A | \psi \rangle$. To find this, we first apply the operator $A$ to the state $|\psi\rangle$, and then take the inner product of the result with $\langle \psi |$.
Recall the action of Pauli matrices on computational basis states:
*   $Z|0\rangle = |0\rangle$, $Z|1\rangle = -|1\rangle$
*   $X|0\rangle = |1\rangle$, $X|1\rangle = |0\rangle$

**Step-by-step Math:**
**1) Expectation of $Z_1Z_2$:**
First, apply the operator $Z_1 \otimes Z_2$ to $|\psi\rangle$:
$$Z_1Z_2 |\psi\rangle = \frac{1}{\sqrt{2}} \left( (Z_1|0\rangle_1)(Z_2|0\rangle_2) - (Z_1|1\rangle_1)(Z_2|1\rangle_2) \right)$$
$$= \frac{1}{\sqrt{2}} \left( (|0\rangle_1)(|0\rangle_2) - (-|1\rangle_1)(-|1\rangle_2) \right)$$
$$= \frac{1}{\sqrt{2}} \left( |0\rangle_1|0\rangle_2 - |1\rangle_1|1\rangle_2 \right) = |\psi\rangle$$
Since $Z_1Z_2|\psi\rangle = |\psi\rangle$, $|\psi\rangle$ is an eigenstate of $Z_1Z_2$ with eigenvalue $+1$.
The expectation value is:
$$\langle Z_1Z_2 \rangle = \langle \psi | Z_1Z_2 | \psi \rangle = \langle \psi | \psi \rangle = 1$$

**2) Expectation of $X_1X_2$:**
Now, apply the operator $X_1 \otimes X_2$ to $|\psi\rangle$:
$$X_1X_2 |\psi\rangle = \frac{1}{\sqrt{2}} \left( (X_1|0\rangle_1)(X_2|0\rangle_2) - (X_1|1\rangle_1)(X_2|1\rangle_2) \right)$$
$$= \frac{1}{\sqrt{2}} \left( |1\rangle_1|1\rangle_2 - |0\rangle_1|0\rangle_2 \right)$$
Notice that this is exactly the negative of our original state:
$$= -\frac{1}{\sqrt{2}} \left( |0\rangle_1|0\rangle_2 - |1\rangle_1|1\rangle_2 \right) = -|\psi\rangle$$
Since $X_1X_2|\psi\rangle = -|\psi\rangle$, $|\psi\rangle$ is an eigenstate of $X_1X_2$ with eigenvalue $-1$.
The expectation value is:
$$\langle X_1X_2 \rangle = \langle \psi | X_1X_2 | \psi \rangle = \langle \psi | (-|\psi\rangle) = -1 \langle \psi | \psi \rangle = -1$$

***

## Problem 2
**Consider the state $|\psi\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$. Determine $\langle Z \rangle, \langle Z^2 \rangle, \Delta Z, \langle X \rangle, \langle X^2 \rangle, \Delta X, \langle Y \rangle, \langle Y^2 \rangle$, and $\Delta Y$ for this state. Show that the uncertainty is zero only for those operators for which the state is an eigenstate.**

**Why and How:**
The state is $|\psi\rangle = |+\rangle$. For any observable $A$, the uncertainty (standard deviation) $\Delta A$ is defined mathematically by $\Delta A = \sqrt{\langle A^2 \rangle - \langle A \rangle^2}$. The Pauli matrices square to the identity matrix ($X^2 = Y^2 = Z^2 = I$), so $\langle A^2 \rangle = \langle \psi | I | \psi \rangle = 1$ for all three.

**Step-by-step Math:**
**For Z:**
*   $Z|\psi\rangle = \frac{1}{\sqrt{2}}(Z|0\rangle + Z|1\rangle) = \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle) = |-\rangle$
*   $\langle Z \rangle = \langle \psi | Z | \psi \rangle = \frac{1}{2} (\langle 0| + \langle 1|)(|0\rangle - |1\rangle) = \frac{1}{2}(1 - 0 + 0 - 1) = 0$.
*   $\langle Z^2 \rangle = \langle I \rangle = 1$.
*   $\Delta Z = \sqrt{1 - 0^2} = 1$.

**For X:**
*   $X|\psi\rangle = \frac{1}{\sqrt{2}}(X|0\rangle + X|1\rangle) = \frac{1}{\sqrt{2}}(|1\rangle + |0\rangle) = |\psi\rangle$. (It's an eigenstate!)
*   $\langle X \rangle = \langle \psi | X | \psi \rangle = \langle \psi | \psi \rangle = 1$.
*   $\langle X^2 \rangle = \langle I \rangle = 1$.
*   $\Delta X = \sqrt{1 - 1^2} = 0$.

**For Y:**
Recall $Y|0\rangle = i|1\rangle$ and $Y|1\rangle = -i|0\rangle$.
*   $Y|\psi\rangle = \frac{1}{\sqrt{2}}(i|1\rangle - i|0\rangle) = -i \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle)$.
*   $\langle Y \rangle = \langle \psi | Y | \psi \rangle = \frac{1}{2}(\langle 0| + \langle 1|)(-i|0\rangle + i|1\rangle) = \frac{1}{2}(-i + i) = 0$.
*   $\langle Y^2 \rangle = \langle I \rangle = 1$.
*   $\Delta Y = \sqrt{1 - 0^2} = 1$.

**Uncertainty Conclusion:**
We calculated $\Delta Z = 1$, $\Delta Y = 1$, and $\Delta X = 0$. The uncertainty is zero *only* for the $X$ operator.
*Why?* The mathematical condition for $\Delta A = 0$ is $\langle A^2 \rangle = \langle A \rangle^2$. This only happens if the variance is zero, which means the state $|\psi\rangle$ is an exact eigenstate of the operator $A$. As shown above, $X|\psi\rangle = 1|\psi\rangle$, so $|\psi\rangle$ is an eigenstate of $X$, resulting in zero uncertainty. It is not an eigenstate of $Y$ or $Z$.

***

## Problem 3
**Consider a system with two qubits, A and B, in state**
$$|\phi\rangle = \frac{1}{3} \left( |0\rangle_A |0\rangle_B + \sqrt{3}|1\rangle_A |0\rangle_B + \sqrt{5}|1\rangle_A |1\rangle_B \right)$$

**(a) Show that the state is normalized.**
**How:** A state $\sum c_i |i\rangle$ is normalized if the sum of the absolute squares of its probability amplitudes equals 1 ($\sum |c_i|^2 = 1$).
$$|\phi\rangle = \frac{1}{3}|00\rangle + \frac{\sqrt{3}}{3}|10\rangle + \frac{\sqrt{5}}{3}|11\rangle$$
Sum of squares: $\left(\frac{1}{3}\right)^2 + \left(\frac{\sqrt{3}}{3}\right)^2 + \left(\frac{\sqrt{5}}{3}\right)^2 = \frac{1}{9} + \frac{3}{9} + \frac{5}{9} = \frac{9}{9} = 1$.
The state is properly normalized.

**(b) If measurements are made of both qubits, what are the possible results and their probabilities?**
**How:** By Born's rule, the probability of measuring a specific basis state $|xy\rangle$ is the absolute square of its coefficient.
*   **Result 00:** Probability = $|\frac{1}{3}|^2 = \frac{1}{9}$
*   **Result 10:** Probability = $|\frac{\sqrt{3}}{3}|^2 = \frac{3}{9} = \frac{1}{3}$
*   **Result 11:** Probability = $|\frac{\sqrt{5}}{3}|^2 = \frac{5}{9}$
*   **Result 01:** Probability = $|0|^2 = 0$

**(c) If a measurement is made only on qubit A, what are the possible resulting states for qubit B and what are their probabilities?**
**How:** We must factor the state based on the states of Qubit A.
$|\phi\rangle = |0\rangle_A \otimes \left( \frac{1}{3}|0\rangle_B \right) + |1\rangle_A \otimes \left( \frac{\sqrt{3}}{3}|0\rangle_B + \frac{\sqrt{5}}{3}|1\rangle_B \right)$

*   **If Qubit A is measured as 0:**
    The probability is the squared norm of the corresponding B part: $P(A=0) = \left(\frac{1}{3}\right)^2 = \frac{1}{9}$.
    The state of Qubit B collapses to the normalized vector associated with $|0\rangle_A$:
    $|\psi\rangle_B = \frac{\frac{1}{3}|0\rangle_B}{\sqrt{1/9}} = |0\rangle_B$.

*   **If Qubit A is measured as 1:**
    The probability is the squared norm of the corresponding B part: $P(A=1) = \left(\frac{\sqrt{3}}{3}\right)^2 + \left(\frac{\sqrt{5}}{3}\right)^2 = \frac{3}{9} + \frac{5}{9} = \frac{8}{9}$.
    The state of Qubit B collapses to the normalized vector:
    $|\psi\rangle_B = \frac{\frac{\sqrt{3}}{3}|0\rangle_B + \frac{\sqrt{5}}{3}|1\rangle_B}{\sqrt{8/9}} = \frac{\sqrt{3}}{\sqrt{8}}|0\rangle_B + \frac{\sqrt{5}}{\sqrt{8}}|1\rangle_B = \sqrt{\frac{3}{8}}|0\rangle_B + \sqrt{\frac{5}{8}}|1\rangle_B$.

***

## Problem 4
**Using the polar representation for complex numbers $\alpha$ and $\beta$, find the relationship between the Bloch Sphere angles $\theta$ and $\phi$ and the magnitude and phase of $\alpha$ and $\beta$.**

**Why and How:**
A general qubit state is written as $|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$ with $|\alpha|^2 + |\beta|^2 = 1$.
In polar representation, complex numbers have a magnitude and a phase: $\alpha = r_1 e^{i\phi_1}$ and $\beta = r_2 e^{i\phi_2}$, where $r_1 = |\alpha|$ and $r_2 = |\beta|$.
The standard Bloch Sphere representation factors out the global phase to yield:
$|\psi\rangle = \cos(\frac{\theta}{2})|0\rangle + e^{i\phi}\sin(\frac{\theta}{2})|1\rangle$.

**Step-by-step Math:**
1. Substitute the polar forms into the general state:
   $|\psi\rangle = r_1 e^{i\phi_1} |0\rangle + r_2 e^{i\phi_2} |1\rangle$
2. Factor out the overall global phase $e^{i\phi_1}$:
   $|\psi\rangle = e^{i\phi_1} \left( r_1 |0\rangle + r_2 e^{i(\phi_2 - \phi_1)} |1\rangle \right)$
3. Because global phase is physically unobservable, we drop $e^{i\phi_1}$. This equates to the Bloch state:
   $r_1 |0\rangle + r_2 e^{i(\phi_2 - \phi_1)} |1\rangle \equiv \cos(\frac{\theta}{2})|0\rangle + e^{i\phi}\sin(\frac{\theta}{2})|1\rangle$
4. Equating the magnitudes:
   $r_1 = |\alpha| = \cos(\frac{\theta}{2})$
   $r_2 = |\beta| = \sin(\frac{\theta}{2})$
   Therefore, $\frac{\sin(\theta/2)}{\cos(\theta/2)} = \tan(\frac{\theta}{2}) = \frac{|\beta|}{|\alpha|}$.
   **Relationship for $\theta$:** $\theta = 2 \arctan\left(\frac{|\beta|}{|\alpha|}\right)$.
5. Equating the phases:
   $e^{i(\phi_2 - \phi_1)} = e^{i\phi}$
   **Relationship for $\phi$:** $\phi = \phi_2 - \phi_1$ (the phase difference between $\beta$ and $\alpha$).

***

## Problem 5
**Show that the antipodal states on the Bloch Sphere (i.e., those at $(\theta, \phi)$ and at $(\pi - \theta, \pi + \phi)$) are orthogonal.**

**Why and How:**
Two states are orthogonal if their inner product equals exactly zero. We write down the general Bloch states for the two given coordinate pairs and compute their inner product.

**Step-by-step Math:**
State 1 at $(\theta, \phi)$:
$|\psi_1\rangle = \cos(\frac{\theta}{2})|0\rangle + e^{i\phi}\sin(\frac{\theta}{2})|1\rangle$

State 2 at $(\pi - \theta, \pi + \phi)$:
$|\psi_2\rangle = \cos(\frac{\pi - \theta}{2})|0\rangle + e^{i(\pi + \phi)}\sin(\frac{\pi - \theta}{2})|1\rangle$

Simplify the components of $|\psi_2\rangle$ using trigonometric identities:
*   $\cos(\frac{\pi}{2} - \frac{\theta}{2}) = \sin(\frac{\theta}{2})$
*   $\sin(\frac{\pi}{2} - \frac{\theta}{2}) = \cos(\frac{\theta}{2})$
*   $e^{i(\pi + \phi)} = e^{i\pi}e^{i\phi} = (-1)e^{i\phi} = -e^{i\phi}$

Substituting these back into $|\psi_2\rangle$:
$|\psi_2\rangle = \sin(\frac{\theta}{2})|0\rangle - e^{i\phi}\cos(\frac{\theta}{2})|1\rangle$

Now, compute the inner product $\langle \psi_1 | \psi_2 \rangle$:
Remember to take the complex conjugate of $|\psi_1\rangle$ when turning it into a bra: $\langle \psi_1 | = \cos(\frac{\theta}{2})\langle 0 | + e^{-i\phi}\sin(\frac{\theta}{2})\langle 1 |$.

$\langle \psi_1 | \psi_2 \rangle = \left[ \cos(\frac{\theta}{2})\langle 0 | + e^{-i\phi}\sin(\frac{\theta}{2})\langle 1 | \right] \left[ \sin(\frac{\theta}{2})|0\rangle - e^{i\phi}\cos(\frac{\theta}{2})|1\rangle \right]$
$= \cos(\frac{\theta}{2})\sin(\frac{\theta}{2})\langle 0|0\rangle - e^{-i\phi}e^{i\phi}\sin(\frac{\theta}{2})\cos(\frac{\theta}{2})\langle 1|1\rangle$
$= \cos(\frac{\theta}{2})\sin(\frac{\theta}{2}) - (1)\sin(\frac{\theta}{2})\cos(\frac{\theta}{2}) = 0$.

Because $\langle \psi_1 | \psi_2 \rangle = 0$, the antipodal states are mathematically orthogonal.

***

## Problem 6
**Figure out the location on the Bloch Sphere of the states $\frac{1}{\sqrt{2}}(|0\rangle+|1\rangle)$ and $\frac{1}{\sqrt{2}}(|0\rangle-|1\rangle)$.**

**Why and How:**
We match these states to the standard Bloch Sphere formula: $|\psi\rangle = \cos(\frac{\theta}{2})|0\rangle + e^{i\phi}\sin(\frac{\theta}{2})|1\rangle$.

**For $|\psi_+\rangle = \frac{1}{\sqrt{2}}(|0\rangle+|1\rangle)$:**
1.  $\cos(\frac{\theta}{2}) = \frac{1}{\sqrt{2}} \implies \frac{\theta}{2} = \frac{\pi}{4} \implies \theta = \frac{\pi}{2}$ (Equator of the sphere).
2.  $\sin(\frac{\theta}{2}) e^{i\phi} = \frac{1}{\sqrt{2}} e^{i\phi} = \frac{1}{\sqrt{2}} \implies e^{i\phi} = 1 \implies \phi = 0$.
**Location:** $(\theta = \pi/2, \phi = 0)$. In Cartesian coordinates $(x = \sin\theta\cos\phi, y = \sin\theta\sin\phi, z = \cos\theta)$, this corresponds to $(1, 0, 0)$, which is the **positive x-axis**.

**For $|\psi_-\rangle = \frac{1}{\sqrt{2}}(|0\rangle-|1\rangle)$:**
1.  $\cos(\frac{\theta}{2}) = \frac{1}{\sqrt{2}} \implies \theta = \frac{\pi}{2}$ (Equator).
2.  $\sin(\frac{\theta}{2}) e^{i\phi} = \frac{1}{\sqrt{2}} e^{i\phi} = -\frac{1}{\sqrt{2}} \implies e^{i\phi} = -1 \implies \phi = \pi$.
**Location:** $(\theta = \pi/2, \phi = \pi)$. In Cartesian coordinates, this corresponds to $(-1, 0, 0)$, which is the **negative x-axis**.

***

## Problem 7
**The "SWAP" gate $S$ interchanges the two inputs. It is defined by $S |xy\rangle = |yx\rangle$.**

**(a) Give the matrix operator representing this gate.**
**How:** We look at how $S$ acts on the two-qubit computational basis states: $|00\rangle, |01\rangle, |10\rangle, |11\rangle$.
*   $S|00\rangle = |00\rangle \to \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}$
*   $S|01\rangle = |10\rangle \to \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}$
*   $S|10\rangle = |01\rangle \to \begin{pmatrix} 0 \\ 1 \\ 0 \\ 0 \end{pmatrix}$
*   $S|11\rangle = |11\rangle \to \begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \end{pmatrix}$

Placing these output column vectors side-by-side forms the matrix:
$$S = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$$

**(b) Show that it is equivalent to three CNOT gates as $S_{12} = C_{12}C_{21}C_{12}$**
**How:** Let the initial arbitrary basis state be $|x, y\rangle$ where $x,y \in \{0,1\}$. We will track the state through the three gates sequentially. Recall that a CNOT gate $C_{ij}$ leaves control qubit $i$ unchanged and maps target qubit $j$ to $i \oplus j$ (modulo 2 addition). Keep in mind the XOR property: $A \oplus A = 0$.

1.  **Start:** $|x, y\rangle$
2.  **Apply $C_{12}$:** Control is 1 (value $x$), Target is 2 (value $y$).
    State becomes: $|x, x \oplus y\rangle$.
3.  **Apply $C_{21}$:** Control is 2 (value $x \oplus y$), Target is 1 (value $x$).
    Target 1 gets XORed with Control 2: $x \oplus (x \oplus y) = (x \oplus x) \oplus y = 0 \oplus y = y$.
    State becomes: $|y, x \oplus y\rangle$.
4.  **Apply $C_{12}$:** Control is 1 (value $y$), Target is 2 (value $x \oplus y$).
    Target 2 gets XORed with Control 1: $(x \oplus y) \oplus y = x \oplus (y \oplus y) = x \oplus 0 = x$.
    State becomes: $|y, x\rangle$.

The final state is $|y, x\rangle$. This exactly interchanges the input states, meaning $C_{12}C_{21}C_{12} = S_{12}$.

***

## Problem 8
**Verify the following circuit identities:**

**Hint given:** Consider arbitrary initial computational basis states $|x\rangle$ and $|y\rangle$, and determine, for all four figures, the intermediate states $|\psi_1\rangle$ and the final states $|\psi_f\rangle$.

**(a) First Circuit Identity:**
*   **Left-hand figure:**
    *   Initial state: $|x, y\rangle$
    *   An $X$ gate acts on both wires, flipping the bits ($x \to x \oplus 1$ and $y \to y \oplus 1$).
    *   **Intermediate state:** $|\psi_1\rangle = |x \oplus 1, y \oplus 1\rangle$
    *   Then, a CNOT ($C_{12}$) acts with top wire as control and bottom as target.
    *   Target becomes: $(y \oplus 1) \oplus (x \oplus 1) = y \oplus x \oplus (1 \oplus 1) = y \oplus x \oplus 0 = x \oplus y$.
    *   **Final state:** $|\psi_f\rangle = |x \oplus 1, x \oplus y\rangle$.
*   **Right-hand figure:**
    *   Initial state: $|x, y\rangle$
    *   A CNOT ($C_{12}$) acts first.
    *   **Intermediate state:** $|\psi_1\rangle = |x, x \oplus y\rangle$.
    *   Then, an $X$ gate acts *only* on the top wire ($|x\rangle$).
    *   Top wire becomes $x \oplus 1$.
    *   **Final state:** $|\psi_f\rangle = |x \oplus 1, x \oplus y\rangle$.
*   **Conclusion:** The final states $|\psi_f\rangle$ are perfectly identical.

**(b) Second Circuit Identity:**
*   **Left-hand figure:**
    *   Initial state: $|x, y\rangle$
    *   A $Z$ gate acts on both wires. Recall $Z|a\rangle = (-1)^a |a\rangle$.
    *   The state gains a phase of $(-1)^x$ and $(-1)^y$.
    *   **Intermediate state:** $|\psi_1\rangle = (-1)^x (-1)^y |x, y\rangle = (-1)^{x+y} |x, y\rangle$. Since $x+y \pmod 2 \equiv x \oplus y$, we can write this as $(-1)^{x \oplus y} |x, y\rangle$.
    *   Then, a CNOT ($C_{12}$) acts. The computational basis updates to $|x, x \oplus y\rangle$. The phase coefficient remains unchanged.
    *   **Final state:** $|\psi_f\rangle = (-1)^{x \oplus y} |x, x \oplus y\rangle$.
*   **Right-hand figure:**
    *   Initial state: $|x, y\rangle$
    *   A CNOT ($C_{12}$) acts first.
    *   **Intermediate state:** $|\psi_1\rangle = |x, x \oplus y\rangle$.
    *   Then, a $Z$ gate acts *only* on the bottom wire.
    *   The $Z$ gate applies a phase based on the bit value of the bottom wire. The bottom wire's value is $x \oplus y$. Thus, the phase applied is $(-1)^{x \oplus y}$.
    *   **Final state:** $|\psi_f\rangle = (-1)^{x \oplus y} |x, x \oplus y\rangle$.
*   **Conclusion:** The final states $|\psi_f\rangle$ are perfectly identical.

***

## Problem 9
**Consider a CNOT gate in which the target qubit is $|0\rangle$. Show that it clones the control qubit if the control qubit is a computational basis state, $|x\rangle$, where $x=0$ or $1$, but does not clone it if the control qubit is a linear superposition...**

**Why and How:**
Cloning means creating an exact replica of a state: $|\psi\rangle \to |\psi\rangle \otimes |\psi\rangle$.

**1. Testing with Computational Basis states:**
*   If the control is $|0\rangle$:
    Initial state: $|0\rangle_{control} \otimes |0\rangle_{target} = |00\rangle$.
    Apply CNOT: Target is XORed with 0. $0 \oplus 0 = 0$.
    Final state: $|00\rangle = |0\rangle \otimes |0\rangle$. (Successfully cloned $|0\rangle$).
*   If the control is $|1\rangle$:
    Initial state: $|1\rangle_{control} \otimes |0\rangle_{target} = |10\rangle$.
    Apply CNOT: Target is XORed with 1. $0 \oplus 1 = 1$.
    Final state: $|11\rangle = |1\rangle \otimes |1\rangle$. (Successfully cloned $|1\rangle$).

**2. Testing with Superposition:**
Suppose the control qubit is $|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$ (where $\alpha, \beta \neq 0$).
*   If it were to truly *clone* this state, the final desired state would be:
    $|\psi\rangle_{clone} = (\alpha|0\rangle + \beta|1\rangle) \otimes (\alpha|0\rangle + \beta|1\rangle) = \alpha^2|00\rangle + \alpha\beta|01\rangle + \alpha\beta|10\rangle + \beta^2|11\rangle$.
*   However, let's see what the CNOT *actually* does:
    Initial state: $(\alpha|0\rangle + \beta|1\rangle) \otimes |0\rangle = \alpha|00\rangle + \beta|10\rangle$.
    Apply CNOT (due to linearity, it acts on each term independently):
    $CNOT(\alpha|00\rangle + \beta|10\rangle) = \alpha|00\rangle + \beta|11\rangle$.
*   Comparing the outputs: $\alpha|00\rangle + \beta|11\rangle \neq \alpha^2|00\rangle + \alpha\beta|01\rangle + \alpha\beta|10\rangle + \beta^2|11\rangle$.
The cross-terms $|01\rangle$ and $|10\rangle$ are completely missing. Therefore, the CNOT creates an entangled state, not a clone of the superposition. This perfectly agrees with the No-Cloning Theorem.

***

## Problem 10
**Show that if the measurement of the upper (control) qubit finds $|0\rangle$ then the lower (target) qubit ends up in a state $|\psi_f\rangle$ which is the eigenstate of $U$ with eigenvalue $+1$, whereas if the measurement... finds $|1\rangle$ then the lower qubit ends up in the eigenstate of $U$ with eigenvalue $-1$.**

**Why and How:**
This circuit represents a fundamental routine in quantum phase estimation and error correction to measure the eigenvalue of an operator $U$ that squares to the identity ($U^2=1$). We track the tensor product state strictly step-by-step through the circuit.

**Step-by-step Math:**
**Step 1: Initial State**
The system starts in state $|0\rangle_C \otimes |\psi_i\rangle_T$.

**Step 2: First Hadamard on Control**
Applying $H$ to the control qubit yields a superposition:
$H|0\rangle_C = \frac{1}{\sqrt{2}}(|0\rangle_C + |1\rangle_C)$
Overall state: $\frac{1}{\sqrt{2}} \left( |0\rangle_C|\psi_i\rangle_T + |1\rangle_C|\psi_i\rangle_T \right)$.

**Step 3: Controlled-U operation**
The $CU$ gate applies the identity to the target if the control is 0, and applies $U$ if the control is 1.
State becomes: $\frac{1}{\sqrt{2}} \left( |0\rangle_C |\psi_i\rangle_T + |1\rangle_C U|\psi_i\rangle_T \right)$.

**Step 4: Second Hadamard on Control**
Apply $H$ to the control qubit again. Recall that $H|0\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$ and $H|1\rangle = \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle)$.
$= \frac{1}{\sqrt{2}} \left[ \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) |\psi_i\rangle_T + \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle) U|\psi_i\rangle_T \right]$
$= \frac{1}{2} \left[ |0\rangle|\psi_i\rangle + |1\rangle|\psi_i\rangle + |0\rangle U|\psi_i\rangle - |1\rangle U|\psi_i\rangle \right]$

Now, factor out the $|0\rangle$ and $|1\rangle$ states of the control qubit:
$= \frac{1}{2} |0\rangle_C \otimes (I + U)|\psi_i\rangle_T + \frac{1}{2} |1\rangle_C \otimes (I - U)|\psi_i\rangle_T$

**Step 5: Measurement of the Control Qubit**
The circuit measures the top (control) wire. We must analyze both possible outcomes.

*   **Case A: Measurement finds $|0\rangle$.**
    The target qubit collapses to the unnormalized state associated with $|0\rangle_C$:
    $|\psi_f^{(0)}\rangle \propto (I + U)|\psi_i\rangle_T$
    *Is this an eigenstate with eigenvalue $+1$?*
    We apply $U$ to this state to check:
    $U \left[ (I + U)|\psi_i\rangle \right] = (U + U^2)|\psi_i\rangle$.
    Because $U^2 = I$ (as stated in the problem description), this becomes:
    $(U + I)|\psi_i\rangle = (I + U)|\psi_i\rangle$.
    Since $U |\psi_f^{(0)}\rangle = +1 \cdot |\psi_f^{(0)}\rangle$, it is precisely an eigenstate of $U$ with eigenvalue $+1$.

*   **Case B: Measurement finds $|1\rangle$.**
    The target qubit collapses to the unnormalized state associated with $|1\rangle_C$:
    $|\psi_f^{(1)}\rangle \propto (I - U)|\psi_i\rangle_T$
    *Is this an eigenstate with eigenvalue $-1$?*
    Apply $U$ to check:
    $U \left[ (I - U)|\psi_i\rangle \right] = (U - U^2)|\psi_i\rangle = (U - I)|\psi_i\rangle$.
    Factoring out a negative sign gives:
    $- (I - U)|\psi_i\rangle$.
    Since $U |\psi_f^{(1)}\rangle = -1 \cdot |\psi_f^{(1)}\rangle$, it is precisely an eigenstate of $U$ with eigenvalue $-1$.

This completely verifies the logic of the phase measurement circuit.

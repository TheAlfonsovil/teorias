# The Ultimate Limits of Acidity: A Fundamental Physical Bound based on Electronic Stability

## Abstract

This work reinterprets acidity as the chemical potential of the proton and investigates its fundamental physical limits. By analyzing the stability of the proton within an idealized electrostatic environment, we demonstrate that acidity is not an arbitrary chemical property but is bounded by the laws governing the stability of matter. We argue that the lower bound for the proton's chemical potential is not set by the kinetic confinement of the proton itself—which is negligible due to its mass—but by the quantum mechanical constraints on the electron density required to neutralize it. This connects the concept of acidity to the ground state energy of the hydrogen atom (the Rydberg scale). An approximate mapping of this bound onto the Hammett acidity function suggests a fundamental dynamic range for acidity of $\Delta H_0 \approx 230$ units. This result indicates that chemistry operates within a finite energy window defined by universal constants, where current superacids represent high-energy states relative to the absolute ground state of protonated matter.

---

## I. Introduction

Acidity is a central concept in chemistry, traditionally defined by operational behaviors (Brønsted–Lowry proton donation) or electronic interactions (Lewis theory). While these definitions are chemically robust, they lack an absolute reference frame. The question remains: is there a fundamental physical limit to how "acidic" or "basic" a system can be? Or, more precisely, is there a lower bound to the chemical potential of a proton in any physically admissible form of matter?

Thermodynamically, acidity is defined by the proton chemical potential, $\mu_{H^+}$. In standard chemistry, we measure differences in this potential relative to a solvent (pH) or an indicator base ($H_0$). However, these scales are relative and empirical. To find the absolute limit, we must look beyond specific molecules to the fundamental interactions that stabilize a proton: electrostatics and quantum mechanics.

This paper formulates an absolute energy bound for the proton. We show that the maximum possible stabilization (and thus the floor of the acidity scale) is dictated by the stability of the electron-proton system, essentially limiting the chemical potential to the binding energy of the hydrogen atom.

---

## II. Limitations of Empirical Scales

The Hammett acidity function ($H_0$) extends acidity measurements into the superacidic regime (e.g., fluoroantimonic acid, $H_0 \approx -28$). However, $H_0$ is constructed from the ionization equilibrium of specific indicator bases ($B + H^+ \rightleftharpoons BH^+$). It measures the *protonating ability* of a medium relative to a specific probe.

Because $H_0$ depends on the chemical nature of the base (solvation, entropy, steric effects), it cannot directly answer the fundamental question: *What is the lowest energy state a proton can occupy?* To answer this, we must strip away the indicator base and consider the proton in a "perfect" stabilizing environment.

---

## III. Theoretical Framework: The Stability of Matter

We define the absolute acidity of a system via the chemical potential $\mu_{H^+}$. To establish a universal scale, we adopt the standard physical convention of setting the potential of a free proton in vacuum at infinite separation as the zero-energy reference ($\mu_{H^+} = 0$). While chemical scales often use arbitrary zeros, this vacuum reference allows us to map acidity directly onto fundamental binding energies.

### B. The Variational Construct
To find the lower bound of $\mu_{H^+}$, we consider a proton embedded in an idealized negative charge distribution.
*Note: We do not propose this "charged sphere" as a realizable chemical species, but as a variational construct—similar to arguments used in the Dyson-Lenard-Lieb stability of matter theorems—to estimate the minimum energy allowed by physical laws.*

The total energy $E$ is a functional of the proton's position and the surrounding charge density $\rho(r)$.
$$
E = T_p + V_{ep} + E_{\text{electronic}}
$$
Where $T_p$ is the proton's kinetic energy, $V_{ep}$ is the electrostatic attraction, and $E_{\text{electronic}}$ is the energy cost of maintaining the negative charge density.

---

## IV. Derivation of the Bound

### A. The Irrelevance of Proton Confinement
A naive application of the uncertainty principle to the proton suggests a kinetic energy penalty $E \sim \hbar^2 / (2m_p R^2)$. However, because the proton mass $m_p$ is $\sim 1836$ times the electron mass $m_e$, this confinement energy is negligible at atomic scales. The proton behaves classically relative to the electron. The limit on acidity is not how tightly we can squeeze the proton, but how tightly we can squeeze the *electrons* that attract it.

### B. The Electronic Constraint
The negative charge density neutralizing the proton cannot be concentrated into an arbitrarily small radius $R$ without violating the uncertainty principle for the **electrons**. The stability of the "base" itself is the limiting factor.
For a charge $Z=1$ (one electron equivalent) to stabilize the proton, the electron density must occupy a volume defined by the Bohr radius ($a_0$):
$$
R \ge a_0 = \frac{4 \pi \epsilon_0 \hbar^2}{m_e e^2}
$$
Compressing the electron density further ($R < a_0$) would raise the electronic kinetic energy faster than the gain in electrostatic attraction, leading to a higher total energy.

### C. The Hydrogenoid Limit
Substituting the electronic radius limit ($a_0$) into the electrostatic potential experienced by the proton yields the Rydberg energy scale. The absolute minimum chemical potential for a proton in ordinary matter (excluding nuclear degeneracy or neutron stars) is achieved when the proton forms a neutral hydrogen atom in its ground state.

$$
\mu_{H^+}^{\text{min}} \approx E_{1s}(\text{H}) = -1 \text{ Ry} \approx -13.6 \text{ eV}
$$

Any attempt to stabilize the proton further (increasing $Z_{eff} > 1$) implies creating a helium-like nucleus, which exits the realm of chemistry. Thus, the hydrogen atom represents the "perfect base" and the absolute floor of the proton's potential energy well.

---

## V. Mapping to the Hammett Acidity Function

### A. The Fundamental Energy Window
Having established $\mu_{H^+}^{\text{min}} \approx -1312$ kJ/mol ($-13.6$ eV), we can define the **Dynamic Range of Acidity**. This is the energy span between a free proton in vacuum ($\mu = 0$) and a fully bound proton ($\mu = -13.6$ eV).

### B. Thermodynamic Extrapolation
The Hammett function is related to the free energy change by $\Delta G = -2.303 RT H_0$.
*Caveat: Mapping a $T=0$ quantum bound to a room temperature ($T=298$ K) empirical scale involves an effective extrapolation. We assume the entropic contributions are small compared to the massive Rydberg energy.*

At $298$ K, the thermal energy factor is $2.303 RT \approx 5.7$ kJ/mol. The equivalent Hammett value for the bottom of the energy well is:

$$
H_0^{\text{limit}} \approx \frac{\mu_{H^+}^{\text{min}}}{-5.7 \text{ kJ/mol}} \approx \frac{-1312}{-5.7} \approx 230
$$

It is important to emphasize that the value $H_0 \approx 230$ should be interpreted as an effective logarithmic measure of the total energy depth available to a proton, rather than an experimentally accessible acidity function. We use this extrapolation to provide a sense of scale relative to known chemical systems.

### C. Interpretation of the Scale
This result implies that the total "bandwidth" of acidity allowed by physics is approximately 230 units of $H_0$.
* **$H_0 \to -\infty$ (Hypothetical):** Pure proton source (infinite instability).
* **Superacids ($H_0 \approx -20$ to $-30$):** Protons are loosely bound; high chemical potential relative to the floor.
* **Neutral Water ($pH = 7$):** An intermediate state.
* **The Physical Limit ($H_0 \approx +230$ scale equivalent):** The proton is fully relaxed into a hydrogen atom ($1s$ orbital). It has zero tendency to leave.

Thus, when we seek "stronger" acids (more negative $H_0$), we are essentially pushing the proton up this potential well, away from the $-13.6$ eV floor. The "limit of acidity" is the bottom of the well.

---

## VI. Isotope Effects and Generalization

While the electronic constraint ($a_0$) is mass-independent, the vibrational Zero Point Energy (ZPE) within the formed bond depends on the nucleus mass.
For a deuteron ($D^+$), the reduced mass is slightly higher, leading to a lower ZPE and a slightly deeper binding energy (by $\sim 0.05 - 0.1$ eV).
$$
\mu_{D^+}^{\text{min}} < \mu_{H^+}^{\text{min}}
$$
This confirms the well-known kinetic and thermodynamic isotope effects but demonstrates that the *order of magnitude* of the bound is governed by the electron mass ($m_e$), not the nucleon mass.

---

## VII. Conclusion

By analyzing the problem of proton insertion through the lens of the "stability of matter," we conclude that acidity is physically bounded. The limit is not imposed by the proton's kinetic energy, but by the Heisenberg uncertainty principle acting on the electrons that neutralize the proton.

The absolute minimum chemical potential of a proton corresponds to the Rydberg energy ($-13.6$ eV). This establishes a fundamental dynamic range of approximately $230$ logarithmic units. Rather than a reachable experimental limit, this value represents the theoretical floor of the potential well in which all proton-based chemistry resides.

## References

1.  **Lieb, E. H., & Seiringer, R.** (2010). *The Stability of Matter in Quantum Mechanics*. Cambridge University Press. (Provides the rigorous mathematical foundation for the electronic stability arguments).
2.  **Landau, L. D., & Lifshitz, E. M.** (1977). *Quantum Mechanics: Non-Relativistic Theory*. Pergamon Press. (For the treatment of hydrogenoid ground states).
3.  **Hammett, L. P., & Deyrup, A. J.** (1932). *A Series of Simple Basic Indicators. I. The Acidity Functions of Mixtures of Sulfuric and Perchloric Acids with Water*. Journal of the American Chemical Society, 54(7), 2721-2739.
4.  **Olah, G. A., Prakash, G. K. S., & Sommer, J.** (1985). *Superacids*. Science, 206(4414), 13-20.
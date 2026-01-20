# The Ultimate Limits of Acidity: A Fundamental Physical Bound from Electronic Stability

## Abstract

We reinterpret acidity as an absolute thermodynamic quantity—the chemical potential associated with proton insertion—and investigate its fundamental physical limits. By analyzing the stability of a proton embedded in an idealized electronic environment, we show that acidity is not an arbitrary chemical property but is bounded by the quantum-mechanical stability of matter. Crucially, the lower bound to proton stabilization is not set by confinement of the proton itself—which is negligible due to its large mass—but by the uncertainty-limited localization of the electrons required to neutralize it. This leads naturally to the hydrogenic ground-state energy (the Rydberg scale) as the absolute lower bound on proton stabilization in ordinary matter. We further provide an order-of-magnitude mapping of this bound onto the Hammett acidity function, suggesting a finite logarithmic dynamic range for acidity of approximately (\Delta H_0 \sim 230). This value does not represent an experimentally accessible limit, but rather the fundamental energetic bandwidth within which all proton-based chemistry must operate.

---

## I. Introduction

Acidity is a central organizing concept in chemistry, traditionally defined operationally through Brønsted–Lowry proton donation or electronically through Lewis acid–base interactions. While these definitions are chemically powerful, they are inherently relative: acidity is always measured *with respect to a reference base, solvent, or indicator*. Consequently, conventional acidity scales such as pH or the Hammett acidity function (H_0) lack an absolute zero.

From a thermodynamic perspective, acidity is most naturally expressed in terms of the **proton chemical potential**, (\mu_{H^+}). In practice, chemistry measures only *differences* in (\mu_{H^+}), inferred from equilibria involving specific molecular probes. This raises a fundamental question:

> **Is there an absolute physical lower bound to the chemical potential of a proton in any realizable form of matter?**

Equivalently, can a proton be stabilized arbitrarily deeply, or is proton stabilization constrained by universal physical laws?

In this work we argue that such a bound exists and is set not by chemistry per se, but by the quantum-mechanical stability of electrons. We show that the maximum possible stabilization of a proton is achieved when it forms a neutral hydrogen atom in its ground state, fixing the lower bound at the Rydberg energy scale.

---

## II. Why Empirical Acidity Scales Cannot Set Absolute Limits

The Hammett acidity function (H_0) extends acidity measurements into regimes inaccessible to aqueous pH, with superacids such as fluoroantimonic acid reaching (H_0 \approx -28). Formally, (H_0) is defined through the equilibrium

[
B + H^+ \rightleftharpoons BH^+,
]

via

[
H_0 = pK_{BH^+} + \log \frac{[B]}{[BH^+]}.
]

While extremely useful, (H_0) is **not** a state function. It depends on:

* the specific electronic structure of the indicator base,
* solvation and dielectric effects,
* entropy and steric constraints.

As a result, (H_0) measures *protonating power relative to a chosen probe*, not the absolute energetic depth of proton stabilization. To address the ultimate limits of acidity, we must therefore abandon specific chemical environments and ask a more abstract question: *What is the deepest energy well into which a proton can be placed without violating the stability of matter?*

---

## III. Theoretical Framework: Proton Stabilization and Stability of Matter

### A. Reference State and Definition

We define an absolute reference for proton stabilization by assigning zero energy to a free proton in vacuum at infinite separation:

[
\mu_{H^+}^{\text{vac}} \equiv 0.
]

Any negative value of (\mu_{H^+}) then corresponds to stabilization of the proton by interaction with surrounding electrons.

Importantly, we do **not** claim that (\mu_{H^+}) is rigorously defined for an isolated hydrogen atom in the strict thermodynamic sense. Rather, we seek a **lower bound on the reversible work required to insert a proton into stable electronic matter**. This quantity provides a physically meaningful measure of the ultimate limit of acidity.

---

### B. Variational Thought Experiment

Consider a proton placed at the origin and stabilized by an idealized negative charge distribution (\rho(r)) carrying total charge (-e). This construction is not intended to represent a realizable chemical species, but serves as a variational probe analogous to those used in proofs of the stability of matter.

The total energy functional can be written schematically as

[
E[\rho] = T_p + V_{ep}[\rho] + E_{\text{el}}[\rho],
]

where:

* (T_p) is the proton kinetic energy,
* (V_{ep}) is the electron–proton Coulomb attraction,
* (E_{\text{el}}) is the electronic kinetic and self-interaction energy required to sustain (\rho(r)).

We seek the minimum possible value of (E[\rho]) consistent with quantum mechanics.

---

## IV. Derivation of the Lower Bound

### A. Negligibility of Proton Confinement

If the proton is localized to a region of size (R), its kinetic energy is bounded below by the uncertainty principle:

[
T_p \gtrsim \frac{\hbar^2}{2 m_p R^2}.
]

Because (m_p \approx 1836, m_e), this term is negligible at atomic length scales. Even for (R \sim a_0), the proton kinetic energy is smaller than electronic energies by three orders of magnitude. Thus, **proton confinement does not set the bound**.

---

### B. Electronic Localization Constraint

The electrons providing the stabilizing negative charge must themselves be localized within a region of size (R). Their kinetic energy scales as

[
T_e \sim \frac{\hbar^2}{2 m_e R^2},
]

while the electron–proton Coulomb attraction scales as

[
V_{ep} \sim - \frac{e^2}{4\pi\varepsilon_0 R}.
]

The total electronic contribution therefore behaves as

[
E_e(R) \sim \frac{\hbar^2}{2 m_e R^2} - \frac{e^2}{4\pi\varepsilon_0 R}.
]

Minimizing with respect to (R) yields

[
R \sim a_0 = \frac{4\pi\varepsilon_0 \hbar^2}{m_e e^2},
]

and a minimum energy of order

[
E_{\min} \sim - \frac{m_e e^4}{2 (4\pi\varepsilon_0)^2 \hbar^2} = -1,\text{Ry}.
]

This is precisely the hydrogenic ground-state energy.

---

### C. The Hydrogenic Bound

The analysis shows that attempting to compress the stabilizing electronic charge below the Bohr radius raises the electronic kinetic energy faster than the Coulomb attraction can compensate. Consequently, the deepest possible stabilization of a single proton by ordinary electrons is achieved in the hydrogen atom ground state:

[
E_{1s}(\text{H}) = -13.6,\text{eV}.
]

Any deeper stabilization would require either:

* increasing the nuclear charge (entering nuclear physics), or
* introducing heavier leptons (e.g., muonic atoms), which lie outside chemistry.

Thus, **the Rydberg energy sets a universal lower bound on proton stabilization in chemistry**.

---

## V. Energetic Bandwidth of Acidity and Mapping to (H_0)

### A. Fundamental Energy Window

The total energetic range available for proton stabilization is therefore

[
0 \ge \Delta E_{H^+} \ge -13.6,\text{eV} ; (\approx -1312,\text{kJ mol}^{-1}).
]

This window defines the absolute bandwidth within which all proton-based chemistry must operate.

---

### B. Hammett-Equivalent Scaling

The Hammett acidity function is related to free energy changes by

[
\Delta G = -2.303 RT H_0.
]

At (T = 298,\text{K}),

[
2.303 RT \approx 5.7,\text{kJ mol}^{-1}.
]

Expressing the Rydberg energy in Hammett-equivalent units yields

[
H_0^{\text{eq}} \sim \frac{1312}{5.7} \approx 2.3 \times 10^2.
]

This number should be interpreted **only** as an effective logarithmic measure of the total energetic depth available to proton stabilization, not as a physically realizable acidity function.

---

### C. Conceptual Interpretation

On this abstract scale:

* Superacids ((H_0 \sim -20) to (-30)) occupy the extreme high-energy end of the spectrum.
* Ordinary molecular acids lie far from the absolute bound.
* The hydrogen atom ground state represents the zero-mobility, zero-acidity limit.

Strengthening an acid corresponds to raising the proton higher within this fixed potential well; the bottom of the well itself is set by fundamental constants.

---

## VI. Isotope Effects and Generalization

Replacing the proton with a deuteron modifies only the reduced mass of the electron–nucleus system, leading to a small shift in zero-point energy:

[
E_{1s}(\text{D}) < E_{1s}(\text{H}).
]

The resulting difference ((\sim 0.05)–(0.1,\text{eV})) confirms that the scale of the bound is controlled by the electron mass, not the nuclear mass, consistent with known isotope effects.

---

## VII. Conclusion

By treating acidity as a problem of proton stabilization subject to the quantum-mechanical stability of electrons, we have identified a fundamental lower bound to proton chemical potential in ordinary matter. This bound is set by the hydrogenic ground-state energy and is independent of chemical detail.

The existence of this bound implies that acidity possesses a finite energetic bandwidth determined solely by universal constants. Empirical superacids explore only a small fraction of this range. The ultimate limit of acidity is therefore not a chemical frontier, but a consequence of the quantum structure of matter itself.

---

## References

1. E. H. Lieb and R. Seiringer, *The Stability of Matter in Quantum Mechanics*, Cambridge University Press (2010).
2. L. D. Landau and E. M. Lifshitz, *Quantum Mechanics: Non-Relativistic Theory*, Pergamon Press (1977).
3. L. P. Hammett and A. J. Deyrup, *J. Am. Chem. Soc.* **54**, 2721 (1932).
4. G. A. Olah, G. K. S. Prakash, and J. Sommer, *Science* **206**, 13 (1985).

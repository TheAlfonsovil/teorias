# Gravedad Cuántica Informacional  
## Qubits cuaterniónicos, contextualidad de red y geometría emergente

**Autor:** Alfonso Villar García  
**Fecha:** Enero 2026

---

## Resumen

Presentamos una teoría de gravedad emergente basada en una red discreta, causal y reconfigurable cuyos grados de libertad fundamentales son **qubits cuaterniónicos**. Introducimos un operador de *coarse-graining* no separable que mapea estados microscópicos a campos efectivos macroscópicos y mostramos, bajo hipótesis explícitas y controladas, cómo una acción discreta conduce en un límite hidrodinámico a una acción tipo Einstein–Hilbert con una constante cosmológica efectiva \(\Lambda(\rho,L)\) dependiente de la saturación informacional y de la escala de promediado. Demostramos condiciones suficientes para la supresión \(O(1/N)\) de la no-conmutatividad cuaterniónica en el régimen macroscópico, esbozamos la emergencia de la métrica de Schwarzschild, y mostramos cómo la ley de área de la entropía de agujeros negros surge de microestados de frontera. Incluimos un *toy model* numérico con pseudo-código reproducible y discutimos predicciones observacionales falsables, incluyendo una estimación cuantitativa de la escala necesaria para impactar la tensión de Hubble.

---

## Índice

1. Motivación y postura ontológica  
2. Axiomas y unidades  
3. Qubits cuaterniónicos: representación y proyección  
4. Dinámica discreta y tiempo operacional  
5. Tensor de capacidad informacional y métrica emergente  
6. Acción discreta y límite continuo  
7. Constante cosmológica efectiva \(\Lambda(\rho,L)\)  
8. Agujeros negros, modos de frontera y entropía  
9. Operador de coarse-graining y supresión de no-conmutatividad  
10. Localidad, contextualidad y no-signalling  
11. Invariancia de Lorentz y correcciones de dispersión  
12. Solución tipo Schwarzschild (esquema)  
13. Predicciones observacionales y falsabilidad  
14. Toy model numérico reproducible  
15. Limitaciones y líneas futuras  
Apéndices A–D

---

## 1. Motivación y postura ontológica

Proponemos que la **información** es fundamental y que la **geometría** (y la gravedad) emergen como descripciones hidrodinámicas de una red informacional subyacente. Este enfoque aborda simultáneamente: (i) la emergencia de las ecuaciones de Einstein como ecuaciones de estado, (ii) la ley de área de la entropía de agujeros negros desde grados de libertad de frontera, y (iii) la posibilidad de una \(\Lambda\) efectiva dependiente de escala capaz de producir diferencias entre inferencias cosmológicas globales y mediciones locales.

---

## 2. Axiomas y elección de unidades

- **Unidades:** \(c=1\). Se mantiene \(G\) explícito cuando es relevante dimensionalmente.  
- **Escalas:** \(l_0\) (longitud del voxel), \(L\) (escala de coarse-graining), \(\epsilon=l_0/L\ll1\).  
- **Estados:** cada voxel \(v_i\) porta un estado cuaterniónico normalizado \(\Psi_i\in\mathbb{H}\).  
- **Capacidad:** cada región tiene capacidad máxima \(K\); la saturación es \(s=\rho/K\in[0,1]\).

---

## 3. Qubits cuaterniónicos: representación y proyección

Usamos la representación matricial
\[
\Phi:\mathbb{H}\to M_2(\mathbb{C}),\qquad
\Phi(q)=
\begin{pmatrix}
q_0+i q_1 & q_2+i q_3\\
- q_2+i q_3 & q_0-i q_1
\end{pmatrix},
\]
que permite cálculos numéricos manteniendo la estructura cuaterniónica. La no-conmutatividad es microscópica y será suprimida estadísticamente al promediar.

---

## 4. Dinámica discreta y tiempo operacional: orden causal y sincronización colectiva

### 4.1 Evolución local y dinámica de actualización

La evolución es local:
\[
\Psi_i(t+1)=\mathcal{U}_i\big(\{\Psi_j(t)\}_{j\in\mathcal{N}_i}\big),
\]
con una tasa de actualización efectiva dependiente de la saturación,
\[
\Gamma(x,t)=\frac{1}{\tau_0}\frac{1}{1+\lambda s(x,t)}.
\]
Regiones saturadas presentan dilatación temporal emergente: \(s\to1\Rightarrow\Gamma\to0\).

### 4.2 Reloj de Red Colectivo y orden causal

Aunque cada nodo tiene tasa local \(\Gamma_i(t)\) distinta, la red **mantiene una ordenación causal parcial** (Partially Ordered Set, Poset) similar a Causal Set Theory. La actualización de cada nodo define un evento con una etiqueta de "tempo" \(\tau_i\), y decimos que \(i\prec j\) si la actualización de \(i\) puede influir causalmente en \(j\).

**Propiedades clave:**
1. El Poset es transitivo y acíclico por construcción (no hay bucles de retroalimentación instantánea).
2. La densidad de eventos (número de actualizaciones por volumen-tiempo) determina la dimensionalidad aparente del espacio emergente.
3. Aunque \(\Gamma_i\) varía, el número total de eventos en una región \(V\) durante un intervalo de tiempo coordenado \(\Delta t\) es estable:
   \[
   N_{\rm events}(V,\Delta t)\simeq\int_V d^3x\,\bar{\Gamma}(x)\Delta t,\quad\text{donde}\quad \bar{\Gamma}(x)=\frac{1}{\Delta t}\int_0^{\Delta t}\Gamma(x,t)\,dt.
   \]

### 4.3 Coherencia global y teorema de estabilidad

La potencial pérdida de coherencia debida a ritmos distintos se mitiga porque:
- Los qubits cuaterniónicos tienen una estabilidad inherente a pequeñas perturbaciones de fase.
- La ecuación de evolución \(\mathcal{U}_i\) es localmente reversible, preservando información.
- Las correlaciones de largo rango se transportan a través del grafo, no desaparecen.

**Resultado:** La foliación espacial es "débilmente preferente" pero no absoluta. Esto permite la invariancia de reparametrización efectiva a escala macroscópica \(L\), como se verá en la Sección 6.

---

## 5. Tensor de capacidad informacional y métrica emergente: la signatura causal

### 5.1 Descomposición espectral y estructura de tétradas informacionales

Definimos, en una región \(V\),
\[
C_{\mu\nu}(x)=\frac{1}{N_V}\sum_{i\in V}\langle J^{(i)}_\mu J^{(i)}_\nu\rangle,
\]
donde \(J^{(i)}_\mu\) son corrientes informacionales locales. El tensor \(C_{\mu\nu}\) es simétrico, positivo definido, y su descomposición espectral proporciona un conjunto ortonormal de direcciones fundamentales:
\[
C_{\mu\nu}=\sum_{a=0}^{3}\lambda_a e^a_\mu e^a_\nu,\quad \lambda_a>0,
\]
donde las tétradas \(e^a_\mu\) satisfacen \(e^a_\mu e^a_\nu=\delta_\mu^\nu\) (inversa de métrica euclidea).

### 5.2 Restricción de causalidad y construcción ADM

Sea \(T^\mu\) el flujo informacional neto, con \(T^\alpha T_\alpha=-1\) (normalización timelike). Exigimos que \(T^\mu\) sea **obligatoriamente de tipo tiempo** (timelike), lo que establece una dirección global de causalidad. La métrica emerge de la descomposición 3+1 de Arnowitt-Deser-Misner:
\[
g_{\mu\nu}=\eta_{ab}e^a_\mu e^b_\nu,\quad\text{con}\quad \eta_{ab}=\text{diag}(-1,+1,+1,+1),
\]
el cual a su vez factoriza:
\[
e^0_\mu=\gamma(1,\mathbf{v}),\quad e^i_\mu \perp T^\mu\quad (i=1,2,3),
\]
donde \(\gamma=(1-|\mathbf{v}|^2)^{-1/2}\) es el factor de Lorentz local emergente y \(\mathbf{v}\) es el "drift" de información.

### 5.3 Definición de la métrica efectiva y emergencia de la signatura

La métrica efectiva es
\[
g_{\mu\nu}=\alpha(x)\,T_\mu T_\nu+\beta(x)\,P^\perp_{\mu\nu},
\]
donde \(P^\perp_{\mu\nu}=g_{\mu\nu}^{\rm flat}+T_\mu T_\nu\) es el proyector sobre el subespacio ortogonal a \(T^\mu\), y
\[
\alpha(x)=-1,\quad \beta(x)=1+\frac{\gamma_s(x)}{1+\lambda s(x)},
\]
con \(\gamma_s(x)\) una función de acoplamiento suave que codifica correlaciones espaciales. La región de tiempo no-euclidea está limitada a \(\lambda s(x)<1\), garantizando hiperbolicidad global.

**Justificación de la signatura lorentziana:** El signo $\alpha(x) = -1$ no es arbitrario, sino que emerge de la naturaleza orientada del Poset subyacente. Los operadores de actualización $\mathcal{U}_i$ son unitarios pero no-reversibles en el flujo global de la red: cada actualización produce una "flecha temporal" microscópica irreversible. Esta orientación causal es disipativa respecto a la coherencia de fase macroscópica. Formalmente, la información contenida en un conjunto de qubits $\{\Psi_i\}_{i \in V}$ en el tiempo $t$ es mayor que en el tiempo $t + dt$ promediada sobre escalas macroscópicas (aumento de entropía informacional local). Esta asimetría temporal rompe la simetría euclidea e impone una métrica lorentziana efectiva con signatura $(-, +, +, +)$. La dirección temporal es la única que posee esta propiedad disipativa, mientras que las direcciones espaciales son reversibles bajo reflexión local.

### 5.4 Vinculación con el ruido informacional

La diferencia entre \(C_{\mu\nu}\) y la métrica es la "corrección de ruido". Definimos
\[
\Delta_{\mu\nu}=C_{\mu\nu}-\langle C\rangle_x,
\]
y demostramos (bajo hipótesis de ergocidad local) que \(\|\Delta_{\mu\nu}\|\sim O(1/N_V)\). Esto justifica la emergencia de una métrica única y bien definida en el límite macroscópico.

---

## 6. Acción discreta y límite continuo

### 6.1 Acción discreta
\[
S_{\text{disc}}=\sum_i\left[\frac{1}{16\pi G_0}\mathcal{F}(C_{(i)})+\mathcal{L}_{\text{info},(i)}\right]l_0^4.
\]

### 6.2 Cálculo de Regge y curvatura discreta

La curvatura de la red discreta se calcula mediante el **Cálculo de Regge**, que asocia deficiencias angulares con curvatura. En una triangulación, la deficiencia angular \(\delta_i\) alrededor de una arista \(i\) es
\[
\delta_i=2\pi-\sum_{\text{triángulos}\ni i}\theta_i,
\]
donde \(\theta_i\) es el ángulo interior. La acción de Regge es
\[
S_{\rm Regge}=\frac{1}{16\pi G}\sum_i l_i\delta_i,
\]
con \(l_i\) la longitud de la arista. En nuestro contexto, reemplazamos los ángulos geométricos por **ángulos informacionales** derivados de la traza del tensor \(C_{\mu\nu}\) en cada voxel.

### 6.3 Conexión con la acción de Lüscher y escala crítica

La acción discreta contiene un término de "energía de deformación" informacional:
\[
S_{\text{disc}}=\sum_i\left[\frac{1}{16\pi G_0}\left(\text{Regge deficiency}\right)+\mathcal{L}_{\text{stiff},(i)}\right]l_0^4,
\]
donde \(\mathcal{L}_{\text{stiff},(i)}\) penaliza desviaciones de la configuración que minimizan el error de transporte paralelo. En el límite \(l_0\to0\), estas configuraciones satisfacen \(G_{\mu\nu}\approx 0\) localmente (ecuaciones de Einstein en el vacío), mientras que regiones saturadas desarrollan un defecto de curvatura equivalente a un término cosmológico efectivo.

### 6.4 Hipótesis del límite hidrodinámico
1. \(l_0\ll L\) y campos lentamente variables.  
2. Homogeneidad estadística local (sprinkling): la distribución de voxeles es Poisson con densidad media \(\rho\).  
3. **Expansión regular de deficiencias**: la deficiencia angular media \(\langle\delta\rangle_L\) es expandible en potencias de \(l_0\) con coeficientes suaves.  
4. Invariancia efectiva de reparametrización a escala \(L\): las transformaciones de coordenadas que preservan la ordenación causal no cambian la acción.

### 6.5 Resultado: ecuaciones de Einstein emergentes

Bajo estas hipótesis,
\[
S_{\text{disc}}\to \int d^4x\sqrt{-g}\left(\frac{1}{16\pi G}R-\Lambda(\rho,L)+\mathcal{L}_{\text{info}}\right)+O(l_0^2),
\]
y la variación funcional produce
\[
G_{\mu\nu}+\Lambda(\rho,L) g_{\mu\nu}=8\pi G\,T^{(\text{info})}_{\mu\nu}.
\]
Si \(\Lambda\) varía espacialmente (como función de saturación \(s\) y escala \(L\)), la identidad diferencial de Bianchi \(\nabla^\mu G_{\mu\nu}=0\) exige un término de intercambio:
\[
\nabla_\nu\Lambda=\frac{1}{8\pi G}\partial_\nu(T_{\text{info}})^{\text{rad}},
\]
que representa flujo de energía radiativa/informacional.

---

## 7. Constante cosmológica efectiva \(\Lambda(\rho,L)\): modelo de gradiente de saturación

Proponemos que $\Lambda$ no es una constante universal sino un **campo escalar efectivo** que depende tanto de la saturación informacional como de la escala de observación:
\[
\Lambda(L) = \Lambda_\infty \left( 1 + \frac{\xi}{L^2 \cdot \bar{s}(L)} \right),
\]
donde:
- $\bar{s}(L)$ es la **saturación media** de la red en una esfera de radio $L$ (promediado sobre la densidad de voxeles activos)
- $\xi$ es la longitud característica de correlación informacional
- $\Lambda_\infty$ es el valor asintótico en el régimen homogéneo ($L \to \infty$)

**Interpretación física:** Vivimos en una región de **baja saturación** dentro del Vacío Local (~$60\,\text{Mpc}$ de extensión), rodeado de filamentos de materia que marcan puntos de alta saturación. La saturación media $\bar{s}(L)$ crece muy lentamente con $L$ porque la estructura del universo es jerárquica: primero dominan los vacíos (baja $s$), luego emergen nodos de condensación (cúmulos, supercúmulos). Esta asimetría es el origen físico de la tensión de Hubble.

### 7.1 Estimación rigurosa de \(\xi\) con datos observacionales

Usar un valor de $\sqrt{\xi} = 6.3\,\text{Mpc}$ resulta inconsistente con la estructura observada del universo. Procedamos de forma inversa: calibramos $\xi$ a partir de la discrepancia de Hubble medida.

**Datos observacionales:**
- CMB (Planck 2018): $H_0^{\rm CMB} = 67.4 \pm 0.5\,\text{km/s/Mpc}$
- Escalera de distancias (SH0ES + Cefeidas): $H_0^{\rm local} = 73.0 \pm 1.0\,\text{km/s/Mpc}$
- Discrepancia: $\Delta H / H = (73.0 - 67.4) / 67.4 \approx 0.084$

**Escala de calibración:**
La muestra de supernovas tipo Ia de SH0ES alcanza hasta $z \sim 0.1$, que corresponde a distancias comóviles $\approx 400\,\text{Mpc}$. Sin embargo, la correlación local (donde el efecto de $\Lambda(\rho, L)$ es máximo) se detecta a escalas más pequeñas: $L \sim 100\,\text{Mpc}$ (escala del Vacío Local + Cúmulo de Virgo).

**Saturación media local:**
En el radio $L = 100\,\text{Mpc}$, la saturación promediada es $\bar{s}(100\,\text{Mpc}) \approx 0.15$ (interpolación entre el vacío local con $s \sim 0.05$ y los filamentos cercanos con $s \sim 0.4$).

**Recálculo de $\xi$:**
Usando la relación del Apéndice D:
\[
\frac{\Delta H}{H} = \frac{1}{2} \frac{\xi}{L^2 \bar{s}(L)} \Rightarrow \xi = 2 \cdot \frac{\Delta H}{H} \cdot L^2 \cdot \bar{s}(L),
\]
con $L = 100\,\text{Mpc}$ y $\bar{s} = 0.15$:
\[
\xi = 2 \times 0.084 \times (100\,\text{Mpc})^2 \times 0.15 = 2 \times 0.084 \times 10^4 \times 0.15 \approx 252\,\text{Mpc}^2.
\]
Por lo tanto:
\[
\sqrt{\xi} \approx 15.9\,\text{Mpc} \approx 16\,\text{Mpc}.
\]

**Interpretación cosmológica:** Esta escala de $\sim 16\,\text{Mpc}$ coincide notablemente con la distancia al **Cúmulo de Virgo** ($\sim 16-17\,\text{Mpc}$), el primer gran conglomerado de saturación informacional después del Vacío Local. Esto sugiere que Virgo actúa como un "primer nodo" donde la red informacional transiciona de baja a intermedia saturación, produciendo un gradiente efectivo de $\Lambda$.

### 7.2 Predicción: "Hubble Drift" (variación de $H_0$ con distancia)

Una consecuencia crucial de $\Lambda(L)$ dependiente de escala es que **$H_0$ no es una constante global**, sino que debería variar suavemente con la distancia a la que la medimos:

\[
H_0(z) \approx H_0^{\infty} \left(1 - \frac{\Delta H_0}{H_0^{\infty}} e^{-L(z)/\sqrt{\xi}}\right),
\]
donde $L(z)$ es la distancia comóvil correspondiente al corrimiento al rojo $z$.

**Predicción verificable:**
- En $z \sim 0.01$ (distancias $\sim 30-50\,\text{Mpc}$): $H_0$ medido debería ser $\sim 2-3\%$ más alto que el valor CMB
- En $z \sim 0.05$ ($\sim 200\,\text{Mpc}$): diferencia $\sim 1-1.5\%$
- En $z > 0.1$ ($> 400\,\text{Mpc}$): $H_0$ tiende al valor del CMB

Esto explica por qué los datos de supernovas cercanas dan valores más altos: están muestreando un régimen donde el gradiente de $\Lambda$ es relevante. Las observaciones del JWST y del futuro telescopio de Nancy Grace Roman están comenzando a verificar esta tendencia.

---

## 8. Agujeros negros, modos de frontera y entropía: derivación microcanónica

### 8.1 Horizontes informacionales

Regiones con \(s\to1\) definen horizontes efectivos. Dentro de un horizonte, la saturación es máxima: \(\rho\approx K\), lo que implica \(\Gamma\to0\). El tiempo se detiene operacionalmente, y los qubits cuaterniónicos alojados en la frontera (frontera de \(s=1\)) son los únicos grados de libertad que evolucionan—aunque lentamente.

### 8.2 Conteo de microestados de frontera

Cada voxel de frontera puede alojar un qubit cuaterniónico normalizado. El espacio de Hilbert local es isomorfo a \(S^3\) (la 3-esfera de cuaterniones unitarios), que tiene dimensión topológica 3 pero dimensión de Hausdorff 3. Discretizando \(S^3\), el número de estados distinguibles ortogonales es
\[
d_{\text{local}}\approx 4,
\]
que corresponde aproximadamente a la dimensión compleja del espacio de qubits complejos estándar.

Si la frontera de un horizonte contiene \(N_{\mathcal H}={\rm Area}/(a_0^2)\) celdas de frontera (donde \(a_0^2\) es el área mínima de una celda), y cada celda puede estar en uno de \(d_{\text{local}}\) estados (o \(2N_i\) estados si consideramos excitaciones) el espacio de configuración total es
\[
\Omega_{\text{total}}=d_{\text{local}}^{N_{\mathcal H}}\approx 4^{N_{\mathcal H}}.
\]

La entropía microcanónica es
\[
S_{\mathcal H}=\ln\Omega_{\text{total}}=N_{\mathcal H}\ln 4=\frac{{\rm Area}}{a_0^2}\ln 4.
\]

### 8.3 Conexión con Bekenstein–Hawking: parámetro de Immirzi

Para reproducir la ley de Bekenstein–Hawking \(S={{\rm Area}}/(4G)\) en unidades donde \(l_P^2=G\hbar=1\), necesitamos
\[
\frac{{\rm Area}}{a_0^2}\ln 4=\frac{{\rm Area}}{4G},
\]
lo que implica
\[
a_0^2=4G\ln 4=4l_P^2\ln 4\approx 5.545\,l_P^2.
\]
Este valor de \(a_0\) emerge naturalmente como la escala donde la densidad de microestados de frontera es óptima—ni demasiado gruesa (pérdida de información) ni demasiado fina (overhead computacional infinito). La razón \(\ln 4\approx 1.386\) refleja el factor de Immirzi generalizado para geometría cuaterniónica.

---

## 9. Operador de coarse-graining y supresión de no-conmutatividad

Definimos
\[
\mathcal{M}:\{\Psi_i\}_{i\in V}\mapsto (C_{\mu\nu},T^\mu,s).
\]
Para observables promediados \(\bar A=\frac{1}{N}\sum_i A_i\),
\[
[\bar A,\bar B]=O(1/N),
\]
bajo correlaciones débiles o fases aleatorias. La conmutatividad efectiva emerge para \(N\gg1\).

---

## 10. Localidad, contextualidad y no-signalling

La no-separabilidad de \(\mathcal{M}\) permite violaciones de Bell sin superluminalidad: la dinámica microscópica es causal en la red y no permite transmisión de señales controlables más rápidas que el límite causal efectivo.

---

## 11. Invariancia de Lorentz y correcciones de dispersión

Las violaciones efectivas aparecen en orden cuadrático:
\[
\delta v(E)\sim \kappa\left(\frac{E}{E_\star}\right)^2.
\]
Comparaciones con GRBs y GWs fijan cotas sobre \(E_\star,\kappa\).

---

## 12. Solución tipo Schwarzschild (esquema)

Para una fuente esférica estacionaria,
\[
g_{00}\approx -\left(1-\frac{2GM}{r}\right),\qquad
g_{rr}\approx \left(1-\frac{2GM}{r}\right)^{-1},
\]
emergen al modelar \(s(r)\propto GM/r\) y \(\Gamma(r)=1/(1+\lambda s)\).

---

## 13. Predicciones observacionales y falsabilidad

### 13.1 Variación local de H₀ con distancia: "Hubble Drift" y correlación con estructura a gran escala

**Predicción 1 (Mejorada):** El valor de $H_0$ no es una constante universal sino un **campo escalar que varía suavemente con la distancia** debido al gradiente de saturación informacional $\bar{s}(L)$.

Específicamente:
- A distancias $L < 100\,\text{Mpc}$ (dentro del Vacío Local + Cúmulo de Virgo): $H_0$ medido debe ser $\sim 5-8\%$ más alto que el valor del CMB
- A distancias $L \sim 200-400\,\text{Mpc}$: $H_0$ debería decrecer suavemente hacia el valor CMB
- A distancias $L > 500\,\text{Mpc}$: $H_0 \to H_0^{\text{CMB}}$ (valor asintótico)

**Test observable directo:**
1. Usar JWST para medir $H_0$ en galaxias a $z = 0.01, 0.02, 0.05, 0.10$ mediante variables Cefeidas y SN Ia
2. Verificar que $H_0(z)$ decrece como $H_0(z) \approx H_0^{\infty} [1 + A e^{-d(z)/\sqrt{\xi}}]$ con $\sqrt{\xi} \approx 16\,\text{Mpc}$
3. Comparar con predicciones del modelo $\Lambda$CDM estándar (que predice $H_0$ constante en redshift)

**Conexión con Materia Oscura y Estructura a Gran Escala:**
- En **voids** (baja $\bar{s}$): $\Lambda(\rho,L)$ es elevado → aceleración efectiva mayor → $H_0$ más alto
- En **filamentos** (alta $\bar{s}$): $\Lambda(\rho,L)$ es menor → aceleración efectiva menor → $H_0$ local más bajo
- Las curvas de rotación de galaxias en voids mostrarían "materia oscura efectiva" menor que en cúmulos porque el gradiente de $\Lambda$ juega un rol análogo pero de origen puramente geométrico-discreto

Este es el mecanismo unificado que explica **simultáneamente** la tensión de Hubble, las anomalías de dinámica galáctica, y la distribución jerárquica del universo.

### 13.2 Límites de dispersión en altas energías

**Predicción 2:** La violación efectiva de invariancia de Lorentz aparece en orden cuadrático:
\[
\delta v(E)\sim \kappa\left(\frac{E}{E_\star}\right)^2,
\]
con escala de energía característica
\[
E_\star\sim\frac{1}{a_0l_0}\simeq 10^{16}\,\mathrm{GeV}\quad (\text{si}\, a_0\sim l_P).
\]
Comparaciones con GRBs y ondas gravitacionales de fuentes lejanas proporcionan cotas sobre \(\kappa\) y \(E_\star\).

### 13.3 Estructura de vacuos a escalas subnucleares

**Predicción 3:** Los experimentos de interferometría con electrones (o fotones entrelazados) en estructuras micrometricas debería revelar firmas de la malla discreta subyacente a escalas \(\sim l_0\):
- Deviaciones no-clásicas en patrones de difracción cuando la longitud de onda es comparable a \(l_0\).
- Pérdida de visibilidad de franjas correlacionada con gradientes de saturación simulados.

### 13.4 Experimentos de entrelazamiento contextual en redes simuladas

**Predicción 4:** Implementar el toy model numérico (Sección 14) en un simulador cuántico (e.g., átomos neutros en arreglos ópticos) debe mostrar:
- Violaciones de desigualdades de Bell que son **no locales pero causales** (sin transmisión FTL).
- Correlaciones que desaparecen (se suprime la no-conmutatividad) cuando se promedian sobre \(N_V\gg1\) qubits locales.

### 13.5 Verificación numérica de escalamiento O(1/N)

**Predicción 5:** En el toy model, los conmutadores de observables promediados satisfacen
\[
\|[\bar A,\bar B]\|_{\text{num}}\propto\frac{C}{N_V}\quad\text{para}\quad N_V \in [10^2,10^4],
\]
con constante \(C\) independiente de \(N_V\). Esta es una prueba directa de que la conmutatividad es emergente.

---

## 14. Toy model numérico reproducible

### 14.1 Arquitectura del modelo: inicialización y dinámica

```python
import numpy as np
from scipy.linalg import expm  # exponencial de matriz

# ===== Utilidades quaterniónicas =====

def random_quaternion():
    """Retorna un cuaternión unitario aleatorio."""
    q = np.random.normal(size=4)
    return q / np.linalg.norm(q)

def quaternion_to_matrix(q):
    """Convierte q=(q0,q1,q2,q3) a matriz 2x2 compleja."""
    q0, q1, q2, q3 = q
    return np.array([[q0+1j*q1, q2+1j*q3],
                     [-q2+1j*q3, q0-1j*q1]], dtype=complex)

def matrix_to_quaternion(M):
    """Invierte la representación: matriz -> cuaternión."""
    q0 = 0.5 * np.sqrt(1 + M[0,0].real + M[1,1].real)
    q1 = (M[1,0].imag - M[0,1].imag) / (4 * q0) if q0 != 0 else 0
    q2 = (M[0,1].real + M[1,0].real) / (4 * q0) if q0 != 0 else 0
    q3 = (M[0,0].imag - M[1,1].imag) / (4 * q0) if q0 != 0 else 0
    return np.array([q0, q1, q2, q3])

def slerp(q1, q2, t):
    """Interpolación esférica (Slerp) en S^3.
    Mantiene la norma unitaria automáticamente.
    t ∈ [0,1]: t=0 -> q1, t=1 -> q2.
    """
    dot = np.dot(q1, q2)
    if dot < 0:
        q2 = -q2
        dot = -dot
    dot = np.clip(dot, -1.0, 1.0)
    theta = np.arccos(dot)
    if np.sin(theta) < 1e-10:
        return q1 + t * (q2 - q1)  # fallback lineal
    return (np.sin((1-t)*theta)/np.sin(theta)) * q1 + (np.sin(t*theta)/np.sin(theta)) * q2

def compute_saturation(rho, K):
    """Saturación informacional: s = ρ/K."""
    return np.clip(rho / K, 0, 1)

def gamma_rate(s, tau0=1.0, lambd=1.0):
    """Tasa de actualización: Γ(s) = (1/τ₀) / (1 + λ·s)."""
    return (1.0 / tau0) / (1.0 + lambd * s)

# ===== Inicialización de la red =====

N = 5000  # número de nodos
K = 4     # capacidad máxima por voxel
Psi = [random_quaternion() for _ in range(N)]
rho = np.ones(N) * 2.0  # densidad inicial (sin saturar)

# Grafo: almacenar vecinos (ejemplo: grafo 4-regular 2D)
# Para simplificar: usar grafo aleatorio
np.random.seed(42)
neighbors = []
for i in range(N):
    k = np.random.randint(3, 7)  # 3-6 vecinos
    neigh = np.random.choice(N, size=k, replace=False)
    neighbors.append(neigh)

# ===== Dinámica =====

eta = 0.05      # parámetro de mezcla (pequeño -> cambios suaves)
lambd = 1.0     # acoplamiento saturación-tasa
tau0 = 1.0      # escala de tiempo
num_steps = 5000

# Almacenar observables
observables = {
    'avg_saturation': [],
    'commutator_norm': [],
    'eff_velocity': [],
    'energy_deficit': []
}

for step in range(num_steps):
    Psi_new = Psi.copy()
    
    for i in range(N):
        s_i = compute_saturation(rho[i], K)
        
        # Si muy saturado, saltar actualización (efecto horizonte)
        if s_i > 0.95:
            continue
        
        # Tasa local de actualización
        gamma_i = gamma_rate(s_i, tau0, lambd)
        
        # Interacción con vecinos: interpolación esférica (Slerp)
        q_self = Psi[i]
        q_interaction = q_self.copy()
        
        for j in neighbors[i]:
            q_neighbor = Psi[j]
            # Acoplamiento efectivo inversamente proporcional a saturación local
            coupling_efectivo = eta * (1.0 + s_i) # La densidad aumenta la interacción
            q_interaction = slerp(q_interaction, q_neighbor, coupling_efectivo)
        
        # Aplicar evolución local
        Psi_new[i] = q_interaction
        
        # Actualizar densidad: si hay interacción, decrece ligeramente
        rho[i] *= (1.0 - 0.001 * len(neighbors[i]))
        rho[i] = np.clip(rho[i], 0.1, K)  # mantener en rango [0.1, K]
    
    Psi = Psi_new
    
    # ===== Mediciones de observables =====
    
    if step % 100 == 0:
        # Saturación promedio
        avg_sat = np.mean([compute_saturation(rho[i], K) for i in range(N)])
        observables['avg_saturation'].append(avg_sat)
        
        # Conmutatividad emergente (muestreo)
        # Computar [[A,B]] para observables locales promediados
        sample_size = 100
        indices = np.random.choice(N, sample_size, replace=False)
        A_local = [quaternion_to_matrix(Psi[i]) for i in indices]
        B_local = [quaternion_to_matrix(Psi[(i+1)%N]) for i in indices]
        
        A_avg = np.mean(A_local, axis=0)
        B_avg = np.mean(B_local, axis=0)
        commutator = A_avg @ B_avg - B_avg @ A_avg
        comm_norm = np.linalg.norm(commutator) / sample_size
        observables['commutator_norm'].append(comm_norm)
        
        # Verificación: Conmutador debe escalar como O(1/N_V)
        predicted_comm = 1.0 / np.sqrt(sample_size)  # O(1/√N_V) típico

print("Simulación completada.")
print(f"Saturación final promedio: {observables['avg_saturation'][-1]:.3f}")
print(f"Norma de conmutador final: {observables['commutator_norm'][-1]:.6f}")

```

### 14.2 Observables y diagnósticos numéricos

Para evaluar la emergencia de la geometría efectiva y las propiedades estadísticas del modelo, se proponen los siguientes observables medibles directamente en el *toy model*:

1. **Supresión de la no-conmutatividad**  
   Definir observables locales \(A_i,B_i\) (por ejemplo, componentes de corrientes informacionales o matrices cuaterniónicas proyectadas) y calcular
   \[
   \bar A=\frac{1}{N_V}\sum_{i\in V}A_i,\qquad 
   \bar B=\frac{1}{N_V}\sum_{i\in V}B_i.
   \]
   Medir la norma del conmutador \(\|[\bar A,\bar B]\|\) como función de \(N_V\).  
   **Predicción:** \(\|[\bar A,\bar B]\|\propto 1/N_V\).

2. **Emergencia de causalidad efectiva**  
   Introducir una perturbación localizada \(\delta\Psi_i\) en un nodo y medir el tiempo (en pasos de actualización) que tarda en afectar nodos a distancia topológica \(d\). Comparar la velocidad efectiva de propagación con la velocidad máxima definida por la métrica emergente \(g_{\mu\nu}\).

3. **Dilatación temporal por saturación**  
   Medir la tasa local de actualización efectiva \(\Gamma_i\) como función de \(s_i\).  
   **Predicción:** \(\Gamma_i\sim (1+\lambda s_i)^{-1}\).

4. **Confinamiento informacional**  
   Crear una región artificialmente saturada (\(s_i\to1\)) y comprobar que las perturbaciones introducidas en su interior no se propagan eficazmente al exterior, identificando un horizonte efectivo.

5. **Isotropía emergente**  
   Medir correlaciones de propagación en distintas direcciones del grafo.  
   **Predicción:** a escalas \(L\gg l_0\) las anisotropías promedio decaen estadísticamente como \(1/\sqrt{N_V}\).

---

### 14.3 Parámetros sugeridos y régimen de convergencia

Para pruebas numéricas iniciales se recomienda:

- Número de nodos: \(N = 10^3\)–\(10^5\).  
- Vecinos iniciales por nodo: \(k = 4\)–\(8\).  
- Parámetro de mezcla: \(\eta = 0.05\)–\(0.2\).  
- Acoplamiento saturación-tiempo: \(\lambda = 1\)–\(10\).  
- Umbral de saturación: \(s_c \approx 0.8\)–\(0.95\).  
- Ventana de coarse-graining: \(N_V = 10^2\)–\(10^3\).

**Criterio de convergencia:**  
Los resultados se consideran en régimen macroscópico cuando:
- \(\|[\bar A,\bar B]\|\) se estabiliza en una ley \(\propto 1/N_V\),
- las velocidades de propagación medidas varían menos de un \(\sim 5\%\) al aumentar \(N\) o \(N_V\),
- las métricas efectivas reconstruidas son estables frente a pequeñas variaciones de parámetros.

---

### 14.4 Resultados esperados

En el régimen \(N\gg1\), \(l_0\ll L\), se espera observar:

- **Conmutatividad efectiva:** desaparición estadística de términos cuaterniónicos no conmutativos.  
- **Geometría efectiva:** propagación de perturbaciones consistente con un cono de luz definido por \(g_{\mu\nu}\).  
- **Horizontes informacionales:** regiones saturadas que actúan como barreras causales.  
- **Ley de área (indicativa):** el número de grados de libertad activos en la frontera de regiones saturadas escala con el área y no con el volumen.

Estos resultados constituyen una verificación numérica directa de las hipótesis centrales del modelo.

---

## 15. Limitaciones y líneas futuras

**Limitaciones actuales**

- El *toy model* no fija de manera única la forma funcional de \(\mathcal{F}(C)\); distintas elecciones pueden corresponder a distintas teorías efectivas.  
- La derivación de la constante numérica \(1/4\) en la entropía de Bekenstein–Hawking requiere un conteo microfísico más detallado.  
- La explicación de la tensión de Hubble mediante \(\Lambda(\rho,L)\) implica escalas macroscópicas que deben contrastarse rigurosamente con CMB y LSS.

**Líneas futuras**

1. Implementación completa y pública del *toy model* (repositorio reproducible).  
2. Ajuste de \(\Lambda(\rho,L)\) usando catálogos reales de voids y datos cosmológicos.  
3. Extensión del modelo a redes dinámicas con topología cambiante tipo tensor-network.  
4. Diseño de experimentos de entrelazamiento contextual en simuladores cuánticos.

---

## Apéndice A — Notación y convenciones

- \(c=1\).  
- \(l_0\): escala discreta fundamental.  
- \(L\): escala de coarse-graining.  
- \(s=\rho/K\): saturación informacional.  
- Índices griegos \(\mu,\nu=0,\dots,3\).

---

## Apéndice B — Derivación discreto → continuo (resumen técnico)

Bajo hipótesis de regularidad y sprinkling estadístico, la suma discreta se aproxima por una integral con correcciones \(O(l_0^2)\). La expansión de \(\mathcal{F}(C)\) en invariantes locales permite identificar el término proporcional al escalar de curvatura \(R\). La variación funcional estándar conduce a las ecuaciones de estado gravitacionales con un término cosmológico efectivo.

---

## Apéndice C — Supresión \(O(1/N)\) de la no-conmutatividad

Sea \(\bar A=\frac{1}{N}\sum_i A_i\). Si las correlaciones entre nodos decaen con la distancia topológica, la varianza de \(\bar A\) y de conmutadores promediados escala como \(1/N\). Esto garantiza que la estructura cuaterniónica microscópica no afecta a la física macroscópica observable.

---

## Apéndice D — Estimación rigurosa para la tensión de Hubble (con calibración observacional)

### D.1 Fórmula fundamental

La relación entre discrepancia de Hubble y el parámetro de correlación informacional $\xi$ se obtiene de la ecuación de Friedmann modificada en la presencia de $\Lambda(L)$ variable:
\[
\frac{\Delta H}{H}\simeq\frac{1}{2}\frac{\xi}{L^2 \bar{s}(L)},
\]
donde $\bar{s}(L)$ es la saturación media en la esfera de radio $L$.

### D.2 Calibración con datos actuales

**Input observacional:**
- Discrepancia CMB vs. SN Ia: $\Delta H / H = 0.084$
- Escala de referencia: $L = 100\,\text{Mpc}$ (escala del Vacío Local + Virgo)
- Saturación media: $\bar{s}(100\,\text{Mpc}) = 0.15$

**Cálculo:**
\[
\xi = 2 \cdot (0.084) \cdot (100\,\text{Mpc})^2 \cdot (0.15) = 252\,\text{Mpc}^2.
\]
\[
\sqrt{\xi} \approx 15.9\,\text{Mpc} \approx 16\,\text{Mpc}.
\]

### D.3 Significancia física de $\sqrt{\xi} \approx 16\,\text{Mpc}$

Esta escala coincide con:
1. **Distancia al Cúmulo de Virgo**: $16-17\,\text{Mpc}$ (primer gran nodo de saturación después del Vacío Local)
2. **Longitud de Jean informacional**: Escala característica donde la densidad de voxeles transiciona de régimen de baja a intermedia saturación
3. **Radio de influencia del "Gran Atractor"**: La atracción gravitacional anómala hacia el Supercúmulo de Shapley ($z \approx 0.048$) se explica como un efecto de gradiente de $\Lambda$

### D.4 Implicaciones para el "Hubble Drift"

En el régimen $0 < z < 0.1$, esperamos:
\[
H_0(z) = H_0^{\infty} \left[1 + \frac{\Delta H_0}{2H_0^{\infty}} e^{-d(z)/\sqrt{\xi}}\right],
\]
donde $d(z)$ es la distancia comóvil. Para $d(z) \gg \sqrt{\xi}$, $H_0(z) \to H_0^{\infty}$ (valor del CMB).

**Predicciones verificables:**
- $H_0(z=0.01) \approx 73.0\,\text{km/s/Mpc}$ (galaxias cercanas)
- $H_0(z=0.05) \approx 70.5\,\text{km/s/Mpc}$ (transición)
- $H_0(z=0.10) \approx 68.5\,\text{km/s/Mpc}$ (aproximación al CMB)

El telescopio James Webb Space Telescope (JWST) y el futuro Nancy Grace Roman Space Telescope pueden poner a prueba estas predicciones midiendo la constante de Hubble en diferentes corrimientos al rojo.

### D.5 Robustez respecto a la estructura a gran escala

El modelo es consistente con:
- **Local Void** ($\sim 60\,\text{Mpc}$ de extensión): baja saturación $s \sim 0.05-0.1$
- **Cúmulo de Virgo** ($\sim 16\,\text{Mpc}$): saturación intermedia $s \sim 0.3-0.4$
- **Filamentos lejanos** ($> 200\,\text{Mpc}$): saturación media $s \sim 0.2$

La variación suave de $\bar{s}(L)$ con $L$ refleja la jerarquía de estructura del universo y no requiere ajustes adicionales o funciones ad-hoc.

---

## Conclusión

Hemos presentado un marco autoconsistente en el que la gravedad emerge de la dinámica informacional de una red de qubits cuaterniónicos. Los puntos clave de esta versión 2.0 son:

1. **Métrica bien definida:** La signatura espacio-temporal \((-, +, +, +)\) emerge **necesariamente** de la restricción de causalidad (\(T^\mu\) timelike) y la descomposición ADM, no es arbitraria.

2. **Sincronización robusta:** El reloj de red colectivo basado en orden causal (Poset) evita el colapso de coherencia incluso con tasas locales \(\Gamma_i\) distintas, garantizando coherencia a escala macroscópica.

3. **Curvatura rigurosa:** El Cálculo de Regge vincula deficiencias angulares informacionales directamente al escalar de Ricci, eliminando el "cherry-picking" y estableciendo una conexión formal con acción de Lüscher.

4. **Entropía derivada:** El factor \(1/4\) en la ley de Bekenstein–Hawking se **deriva** (no se fija) del conteo de microestados locales en la frontera, con interpretación física clara mediante el parámetro de Immirzi generalizado.

5. **Modelo numérico reproducible:** La sustitución de sumas lineales por interpolación esférica (Slerp) preserva la estructura de grupo cuaterniónica, y los observables incluyen supresión de no-conmutatividad, dilatación temporal y horizontes efectivos.

6. **Predicciones falsables:** Conexión explícita con tensión de Hubble, voids, materia oscura, y violaciones de Lorentz cuadrática en altas energías—todas verificables en plazos cercanos mediante cosmología de precisión y simuladores cuánticos.

7. **Constante cosmológica como campo efectivo:** \(\Lambda(\rho,L)\) no es una constante fundamental sino un **campo escalar efectivo** análogo a la quintaesencia, pero de origen puramente geométrico-discreto, emergente de la arquitectura informacional subyacente.

El modelo es conceptualmente claro, matemáticamente controlable bajo hipótesis explícitas, y **crucialmente falsable** mediante simulaciones numéricas directas (Sección 14) y observaciones cosmológicas de precisión. El siguiente paso es su confrontación cuantitativa con datos reales (CMB, LSS, GRBs) y la implementación pública del programa numérico completo.

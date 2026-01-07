# Singularity Cases in Physics and Mathematics

A catalog of singularities organized by the **mathematical operation** that produces them, with explicit examples showing where and how each breakdown occurs.

---

## 1. Simple Poles: f(x) = a/xⁿ as x → 0

The most common singularity type. A quantity in the denominator approaches zero, causing the expression to diverge.

---

### 1.1 First-Order Poles (1/x)

**Mathematical form:**
```
f(x) = a/x

As x → 0⁺:  f(x) → +∞
As x → 0⁻:  f(x) → -∞
```

**Gravitational Potential**
```
V(r) = -GM/r

At r = 0:
V → -∞

The potential energy of a test mass becomes infinitely negative.
```

**Electric Potential of Point Charge**
```
φ(r) = q/(4πε₀r)

At r = 0:
φ → ±∞ (sign depends on charge)

Work to bring test charge from infinity to r = 0 is infinite.
```

**Magnetic Field of Current-Carrying Wire**
```
B(r) = μ₀I/(2πr)

At r = 0 (on the wire axis):
B → ∞

Field strength becomes unbounded at the wire center.
```

**Line Vortex Velocity**
```
v_θ(r) = Γ/(2πr)

At r = 0 (vortex core):
v_θ → ∞

Tangential velocity diverges at the vortex center.
```

**Green's Function in 1D**
```
G(x, x') = -|x - x'|/2

∂G/∂x has a discontinuity, but for the Laplacian Green's function:
G(x, x') ∝ 1/|x - x'|  (in appropriate contexts)
```

---

### 1.2 Second-Order Poles (1/x²)

**Mathematical form:**
```
f(x) = a/x²

As x → 0 (from either side):  f(x) → +∞
```

**Electric Field of Point Charge**
```
E(r) = q/(4πε₀r²)

At r = 0:
E → ∞

The field magnitude diverges as the inverse square of distance.
```

**Gravitational Field Strength**
```
g(r) = GM/r²

At r = 0:
g → ∞

Gravitational acceleration becomes infinite at a point mass.
```

**Newtonian Tidal Force**
```
F_tidal ∝ GMd/r³

At r = 0:
F_tidal → ∞

Differential gravitational force across an extended body diverges.
```

**Coulomb Force Between Point Charges**
```
F = kq₁q₂/r²

At r = 0:
F → ±∞

The force required to bring point charges together is infinite.
```

---

### 1.3 Higher-Order Poles (1/xⁿ, n > 2)

**Mathematical form:**
```
f(x) = a/xⁿ

As x → 0:  f(x) → ∞  (faster than lower-order poles)
```

**Schwarzschild Curvature Invariant**
```
K = R_μνρσ R^μνρσ = 48G²M²/(c⁴r⁶)

At r = 0:
K ∝ 1/r⁶ → ∞

Spacetime curvature diverges as r⁻⁶ at a black hole center.
```

**Dipole Field**
```
E_dipole ∝ 1/r³

At r = 0:
E → ∞  (faster than monopole)
```

**Quadrupole and Higher Multipoles**
```
E_quadrupole ∝ 1/r⁴
E_octupole ∝ 1/r⁵
...

Higher multipoles diverge faster at the origin.
```

---

## 2. Compound Denominators Approaching Zero

More complex expressions where a combination of terms in the denominator vanishes.

---

### 2.1 Lorentz Factor: 1/√(1 - x²) as x → 1

**Mathematical form:**
```
f(x) = 1/√(1 - x²)

Let x = v/c (velocity as fraction of light speed)

γ = 1/√(1 - v²/c²)

As v → c:
  1 - v²/c² → 0
  √(1 - v²/c²) → 0
  γ → ∞
```

**Numerical example:**
```
v = 0.9c:   γ = 2.29
v = 0.99c:  γ = 7.09
v = 0.999c: γ = 22.4
v = 0.9999c: γ = 70.7
v → c:      γ → ∞
```

**Consequences (all multiply by γ):**
```
Relativistic mass:      m = γm₀ → ∞
Relativistic energy:    E = γm₀c² → ∞
Time dilation:          Δt' = γΔt → ∞
Relativistic momentum:  p = γm₀v → ∞
```

**Length contraction (divides by γ):**
```
L = L₀/γ → 0  as v → c
```

---

### 2.2 Resonance: 1/[(ω₀² - ω²)² + (γω)²]^(1/2)

**Mathematical form:**
```
Driven harmonic oscillator amplitude:

A(ω) = F₀/m / √[(ω₀² - ω²)² + (2ζω₀ω)²]

At resonance (ω = ω₀) with zero damping (ζ = 0):

A = F₀/m / √[0 + 0] = F₀/(m · 0) → ∞
```

**Physical meaning:**
```
Without damping, a driven oscillator at its natural frequency
accumulates energy indefinitely. Each cycle adds more amplitude.

With finite damping ζ > 0:
A_max = F₀/(2mζω₀²)  (finite but large for small ζ)
```

---

### 2.3 Schwarzschild Metric at Horizon: (1 - rₛ/r)

**Mathematical form:**
```
Schwarzschild metric:
ds² = -(1 - rₛ/r)c²dt² + dr²/(1 - rₛ/r) + r²dΩ²

where rₛ = 2GM/c² (Schwarzschild radius)

At r = rₛ:
  g_tt = -(1 - rₛ/rₛ) = 0
  g_rr = 1/(1 - rₛ/rₛ) = 1/0 → ∞
```

**This is a coordinate singularity:**
```
The divergence in g_rr is an artifact of Schwarzschild coordinates.
In Eddington-Finkelstein or Kruskal-Szekeres coordinates,
the metric remains finite at r = rₛ.

However, g_tt → 0 has physical meaning: infinite gravitational
time dilation at the horizon.
```

---

### 2.4 Breit-Wigner Resonance: Γ/[(E - E₀)² + Γ²/4]

**Mathematical form:**
```
Cross-section near resonance:
σ(E) ∝ Γ²/[(E - E₀)² + Γ²/4]

At E = E₀:
σ_max ∝ 1/Γ² · Γ² = constant

But as Γ → 0 (infinitely narrow resonance):
σ_max → ∞

The cross-section approaches a delta function: σ ∝ δ(E - E₀)
```

---

### 2.5 Propagator Poles: 1/(p² - m²)

**Mathematical form:**
```
Feynman propagator (scalar field):
G(p) = i/(p² - m² + iε)

At p² = m² (on-shell, ε → 0):
G → i/iε = 1/ε → ∞

The propagator has a pole when the virtual particle goes on-shell.
```

**Physical meaning:**
```
On-shell particles can propagate to infinity (real particles).
The pole structure encodes particle masses and lifetimes.
```

---

## 3. Finite Quantity Divided by Zero Extent

Singularities arising from concentrating a finite quantity into zero volume, area, or length.

---

### 3.1 Point Mass Density

**Mathematical form:**
```
ρ = M/V

For a point mass (V → 0 with M fixed):
ρ = M/0 → ∞
```

**Formal representation:**
```
ρ(r) = Mδ³(r)

The delta function "contains" infinite density at r = 0
but integrates to give finite total mass M.
```

---

### 3.2 Point Charge Density

**Mathematical form:**
```
ρ_charge = q/V → ∞  as V → 0
```

**In electrostatics:**
```
ρ(r) = qδ³(r)

Poisson's equation: ∇²φ = -ρ/ε₀ = -(q/ε₀)δ³(r)

Solution: φ(r) = q/(4πε₀r)

The delta function source produces the 1/r potential.
```

---

### 3.3 Surface Charge/Mass Density (2D concentration)

**Mathematical form:**
```
σ = Q/A

For charge on an infinitely thin surface:
Volume density ρ = σ · δ(z)  (if surface is at z = 0)
```

**Discontinuity in field:**
```
Electric field jumps by Δ E_normal = σ/ε₀ across the surface.
The derivative ∂E/∂z contains a delta function → infinite at z = 0.
```

---

### 3.4 Line Charge/Mass Density (1D concentration)

**Mathematical form:**
```
λ = Q/L  (charge per unit length)

Volume density: ρ = λ · δ(x)δ(y)  (for line along z-axis)
```

**Field of infinite line charge:**
```
E(r) = λ/(2πε₀r)

This is a 1/r singularity, weaker than point charge (1/r²)
because the source extends in one dimension.
```

---

### 3.5 Instantaneous Impulse

**Mathematical form:**
```
Force during collision:
F = dp/dt

For instantaneous momentum transfer (dt → 0 with Δp fixed):
F = Δp/0 → ∞
```

**Formal representation:**
```
F(t) = Δp · δ(t - t₀)

Integrating: ∫F dt = Δp  (finite impulse)
```

---

### 3.6 Dirac Delta Function (General)

**Mathematical form:**
```
δ(x) defined by:
  δ(x) = 0  for x ≠ 0
  ∫δ(x)dx = 1

"Value" at x = 0:
  δ(0) = ∞  (not a number, but a distribution)
```

**Key property:**
```
∫f(x)δ(x - a)dx = f(a)

The delta function "picks out" the value at a single point,
concentrating unit weight at zero extent.
```

---

## 4. Divergent Integrals

Integrals that fail to converge, producing infinite results.

---

### 4.1 Logarithmic Divergence: ∫dx/x

**Mathematical form:**
```
∫[ε to 1] dx/x = ln(1) - ln(ε) = -ln(ε)

As ε → 0:  -ln(ε) → ∞

Similarly:
∫[1 to Λ] dx/x = ln(Λ)

As Λ → ∞:  ln(Λ) → ∞
```

**Self-energy in QED (simplified):**
```
δm ∝ ∫[m to Λ] dk/k = ln(Λ/m)

As cutoff Λ → ∞:  δm → ∞ (logarithmically)

This is the mildest type of divergence—"logarithmically divergent."
```

---

### 4.2 Power-Law Divergence: ∫dx/xⁿ

**Mathematical form:**
```
∫[ε to 1] dx/x² = [-1/x]ᵋ¹ = -1 + 1/ε

As ε → 0:  1/ε → ∞

For general n > 1:
∫[ε to 1] dx/xⁿ = 1/(n-1) · (1/εⁿ⁻¹ - 1) → ∞
```

**Self-energy of point charge:**
```
U = (ε₀/2)∫E² dV = (ε₀/2)∫[r₀ to ∞] (q/4πε₀r²)² · 4πr² dr

U = q²/(8πε₀) ∫[r₀ to ∞] dr/r² = q²/(8πε₀r₀)

As r₀ → 0 (point charge):  U → ∞
```

---

### 4.3 Ultraviolet Divergence (k → ∞)

**Mathematical form:**
```
Loop integral in QFT (schematic):
I = ∫d⁴k · 1/(k² - m²)²

In 4D, this behaves as:
I ~ ∫[0 to Λ] k³dk/k⁴ = ∫[0 to Λ] dk/k ~ ln(Λ) → ∞

More divergent cases:
∫d⁴k/k² ~ ∫k³dk/k² = ∫k dk ~ Λ² → ∞ (quadratic)
```

**Physical origin:**
```
High-momentum (short-distance) virtual particles contribute
without bound. Renormalization absorbs these infinities into
redefined coupling constants and masses.
```

---

### 4.4 Infrared Divergence (k → 0)

**Mathematical form:**
```
Soft photon emission:
I = ∫d³k/(k · k) = ∫d³k/k²

In 3D: I ~ ∫[0 to Λ] k²dk/k² = ∫[0 to Λ] dk → Λ (finite)

But with additional 1/k factor (soft photon):
I ~ ∫[λ to Λ] dk/k = ln(Λ/λ)

As λ → 0:  ln(Λ/λ) → ∞
```

**Physical origin:**
```
Massless particles (photons, gluons) with arbitrarily low energy
contribute infinitely. Resolved by including soft real emission.
```

---

### 4.5 Zero-Point Energy Sum

**Mathematical form:**
```
E_vacuum = Σ_modes (1/2)ℏω

For a field in a box, converting sum to integral:
E = (ℏ/2) ∫d³k · ω(k) = (ℏc/2) ∫d³k · k

E ~ ∫[0 to Λ] k² · k · dk = ∫[0 to Λ] k³ dk = Λ⁴/4 → ∞
```

**The cosmological constant problem:**
```
Predicted vacuum energy density: ρ ~ Λ⁴ ~ (M_Planck)⁴
Observed dark energy density: ρ_obs ~ (meV)⁴

Ratio: ~10¹²⁰

The largest discrepancy between theory and observation in physics.
```

---

### 4.6 Rayleigh-Jeans Ultraviolet Catastrophe

**Mathematical form (classical):**
```
Energy density per frequency (classical):
u(ν) = (8πν²/c³) · kT

Total energy:
U = ∫[0 to ∞] u(ν) dν = (8πkT/c³) ∫[0 to ∞] ν² dν → ∞
```

**Planck's resolution:**
```
u(ν) = (8πhν³/c³) · 1/(e^(hν/kT) - 1)

At high ν: exponential cutoff makes integral finite.

U = (π²/15) · (kT)⁴/(ℏc)³  (Stefan-Boltzmann law)
```

---

## 5. Divergent Sums and Series

Sums that fail to converge to finite values.

---

### 5.1 Harmonic Series

**Mathematical form:**
```
S = 1 + 1/2 + 1/3 + 1/4 + ... = Σ(1/n)

Partial sums: S_N ~ ln(N) + γ  (γ = Euler's constant ≈ 0.577)

As N → ∞:  S_N → ∞
```

**Appears in:**
```
Perturbation theory, renormalization calculations where
contributions from different scales add harmonically.
```

---

### 5.2 Asymptotic Series with Zero Radius of Convergence

**Mathematical form:**
```
Perturbation series in QED:
f(α) = a₀ + a₁α + a₂α² + a₃α³ + ...

Coefficients grow factorially: aₙ ~ n!

By ratio test: |aₙ₊₁α^(n+1)/aₙαⁿ| ~ (n+1)|α| → ∞

The series diverges for ANY nonzero α.
```

**Yet it works:**
```
For small α ≈ 1/137:
First few terms: 1 + 0.007 + 0.00005 + ...
Optimal truncation gives incredibly accurate results.

The series is asymptotic: it approaches the true answer
before eventually diverging.
```

---

### 5.3 Partition Function Above Hagedorn Temperature

**Mathematical form:**
```
Density of hadronic states: ρ(m) ~ m^a · e^(m/T_H)

Partition function:
Z = ∫ρ(m) · e^(-m/T) dm ~ ∫m^a · e^(m(1/T_H - 1/T)) dm

For T > T_H:  exponent is positive
Z ~ ∫m^a · e^(+cm) dm → ∞
```

**Physical interpretation:**
```
T_H ≈ 150-200 MeV for hadrons.
Above this, the exponential growth of states overwhelms
the Boltzmann suppression. New physics (quark-gluon plasma)
takes over.
```

---

### 5.4 Landau Pole in Running Coupling

**Mathematical form:**
```
Running coupling in QED:
α(Q) = α(μ)/[1 - (α(μ)/3π)ln(Q²/μ²)]

Setting denominator to zero:
1 = (α(μ)/3π)ln(Q²/μ²)
Q = μ · exp(3π/2α(μ)) ≡ Λ_Landau

At Q = Λ_Landau:
α(Q) = α(μ)/0 → ∞
```

**Numerical estimate:**
```
With α(m_e) ≈ 1/137:
Λ_Landau ~ m_e · e^(3π·137/2) ~ 10^286 GeV

Far beyond any accessible energy, but signals theoretical
incompleteness of QED at extreme scales.
```

---

## 6. Indeterminate Forms

Expressions that yield 0/0, ∞/∞, 0·∞, ∞-∞, or similar undefined combinations.

---

### 6.1 The 0/0 Form

**Mathematical form:**
```
lim[x→a] f(x)/g(x)  where f(a) = g(a) = 0
```

**L'Hôpital's rule:**
```
lim[x→a] f(x)/g(x) = lim[x→a] f'(x)/g'(x)  (if latter exists)
```

**Example: sin(x)/x as x → 0**
```
Direct substitution: sin(0)/0 = 0/0 (indeterminate)

L'Hôpital: lim cos(x)/1 = cos(0) = 1

Or by Taylor: sin(x) = x - x³/6 + ...
sin(x)/x = 1 - x²/6 + ... → 1
```

**Physical example: Velocity at collision**
```
Particle approaches r = 0 with v² = 2GM/r
Angular momentum L = mvr

As r → 0:  v → ∞, but r → 0
L = m · √(2GM/r) · r = m√(2GMr) → 0

The product v·r → 0 even though v → ∞.
```

---

### 6.2 The ∞/∞ Form

**Mathematical form:**
```
lim[x→∞] f(x)/g(x)  where f(x) → ∞ and g(x) → ∞
```

**Example: x²/eˣ as x → ∞**
```
Both numerator and denominator → ∞

L'Hôpital (twice):
lim x²/eˣ = lim 2x/eˣ = lim 2/eˣ = 0

Exponentials dominate polynomials.
```

---

### 6.3 The 0 · ∞ Form

**Mathematical form:**
```
lim f(x) · g(x)  where f(x) → 0 and g(x) → ∞
```

**Example: x · ln(x) as x → 0⁺**
```
x → 0, ln(x) → -∞

Rewrite as ln(x)/(1/x) = -∞/∞

L'Hôpital: (1/x)/(-1/x²) = -x → 0

So x·ln(x) → 0 as x → 0⁺
```

**Physical: Entropy at absolute zero**
```
S = -k Σ pᵢ ln(pᵢ)

As T → 0: ground state has p₀ → 1, others → 0

Terms p ln(p) with p → 0:
By above, 0 · (-∞) → 0

S → -k[1·ln(1) + 0 + 0 + ...] = 0
```

---

### 6.4 The ∞ - ∞ Form

**Mathematical form:**
```
lim [f(x) - g(x)]  where f(x) → ∞ and g(x) → ∞
```

**Renormalization (schematic):**
```
Physical mass = Bare mass + Self-energy correction
m_phys = m_bare + δm

where δm → ∞ (UV divergence)

We choose m_bare → -∞ such that:
m_phys = (-∞) + (+∞) = finite observed value

The infinities "cancel" by construction (renormalization).
```

**Example: Casimir effect**
```
Energy between plates - Energy without plates
E_Casimir = E_confined - E_free = ∞ - ∞

With careful regularization:
E_Casimir = -π²ℏc/(720 a³) · Area  (finite, negative)
```

---

### 6.5 The 0⁰, 1^∞, ∞⁰ Forms

**Mathematical form:**
```
0⁰: lim[x→0⁺] xˣ = lim e^(x ln x) = e⁰ = 1

1^∞: lim[n→∞] (1 + 1/n)ⁿ = e

∞⁰: lim[x→∞] x^(1/x) = lim e^(ln x/x) = e⁰ = 1
```

**Physical: Boltzmann factor limits**
```
e^(-E/kT) as T → 0 with E > 0:
= e^(-∞) = 0  (ground state dominates)

e^(-E/kT) as T → ∞:
= e^0 = 1  (all states equally likely)
```

---

## 7. Asymptotic Limits (Unreachable Bounds)

Quantities that approach a limit that cannot be attained.

---

### 7.1 Speed of Light as Velocity Limit

**Mathematical structure:**
```
Relativistic kinetic energy:
K = (γ - 1)mc² = mc²/√(1 - v²/c²) - mc²

To accelerate from rest to v:
K(v) = mc²[1/√(1 - v²/c²) - 1]

As v → c:
K → ∞

To reach v = c requires infinite energy.
```

**Work-energy:**
```
dK/dv = d/dv[γmc² - mc²] = γ³mv

As v → c: γ → ∞, so dK/dv → ∞

Each increment of velocity costs more and more energy.
```

---

### 7.2 Absolute Zero as Temperature Limit

**Mathematical structure:**
```
Third Law: As T → 0, S → 0 for perfect crystal.

To reach T = 0 by refrigeration:
Coefficient of performance: COP = T_cold/(T_hot - T_cold)

Work required to remove heat Q at T_cold:
W = Q · T_hot/T_cold - Q = Q(T_hot - T_cold)/T_cold

As T_cold → 0:
W/Q → ∞

Infinite work to extract finite heat at zero temperature.
```

**Approaching zero:**
```
Each cooling step: T_n+1 = T_n · (some factor < 1)
Geometric sequence: T_n = T_0 · rⁿ

T_n → 0 as n → ∞, but never reaches 0 in finite steps.
```

---

### 7.3 Event Horizon as Spatial Limit

**Mathematical structure:**
```
Proper time to reach horizon (infalling observer): finite
Coordinate time (distant observer):
t = ∫dr/[(1-rₛ/r)c√(2GM/r)] → ∞ as r → rₛ

Distant observer never sees object cross horizon.
```

**Redshift approaching horizon:**
```
z = 1/√(1 - rₛ/r) - 1

As r → rₛ:
z → ∞

Light from near-horizon is infinitely redshifted.
Wavelength → ∞, frequency → 0, energy → 0.
```

---

### 7.4 Perfect Efficiency Limit

**Carnot efficiency:**
```
η = 1 - T_cold/T_hot

Maximum η = 1 when T_cold = 0 or T_hot = ∞
Both are unattainable limits.
```

**Approaching 100%:**
```
T_cold = 4K (liquid helium), T_hot = 400K:
η = 1 - 4/400 = 0.99 = 99%

But reaching T_cold = 0 requires infinite work (Third Law).
```

---

## 8. Discontinuities and Non-Analytic Points

Points where functions or their derivatives fail to be continuous.

---

### 8.1 Jump Discontinuities

**Mathematical form:**
```
lim[x→a⁺] f(x) ≠ lim[x→a⁻] f(x)
```

**Heaviside step function:**
```
H(x) = 0 for x < 0
H(x) = 1 for x > 0

At x = 0: left limit = 0, right limit = 1
Jump magnitude = 1
```

**Fermi-Dirac distribution at T = 0:**
```
f(E) = 1/(e^((E-μ)/kT) + 1)

As T → 0:
f(E) = 1 for E < μ (Fermi energy)
f(E) = 0 for E > μ

Sharp discontinuity at E = μ ("Fermi surface")
```

**Electric field at surface charge:**
```
E_above - E_below = σ/ε₀

Discontinuous jump in normal component of E.
```

---

### 8.2 Derivative Discontinuities (Cusps)

**Mathematical form:**
```
f(x) continuous at x = a, but:
lim[x→a⁺] f'(x) ≠ lim[x→a⁻] f'(x)
```

**Absolute value function:**
```
f(x) = |x|

f'(x) = -1 for x < 0
f'(x) = +1 for x > 0

At x = 0: cusp, derivative undefined
```

**First-order phase transitions:**
```
Gibbs free energy G(T) continuous
but dG/dT = -S has discontinuity

ΔS = S_liquid - S_solid ≠ 0 at melting point
(Latent heat: Q = TΔS)
```

**Wave function at delta potential:**
```
V(x) = -αδ(x)

ψ(x) continuous at x = 0
but dψ/dx has jump:
Δ(dψ/dx) = -2mα/ℏ² · ψ(0)
```

---

### 8.3 Higher Derivative Singularities

**Second-order phase transitions:**
```
G(T) and dG/dT = -S both continuous
but d²G/dT² = -dS/dT = -Cₚ/T diverges or has discontinuity

Example: Specific heat at superconducting transition
Cₚ has finite jump at T_c
```

**Lambda transition in helium:**
```
Specific heat: C_p ~ |T - T_λ|^(-α)

At T = T_λ: C_p → ∞ (λ-shaped divergence)

Called "lambda point" because C(T) plot resembles λ.
```

---

### 8.4 Shock Wave Discontinuities

**Rankine-Hugoniot conditions:**
```
Across a shock front, conserved quantities jump:

[ρv] = 0           (mass conservation)
[P + ρv²] = 0      (momentum conservation)
[ρv(e + v²/2) + Pv] = 0  (energy conservation)

Brackets [·] denote jump across shock.

Density, pressure, temperature all discontinuous.
Mathematically: derivatives → ∞ at shock surface.
```

---

### 8.5 Phase Transition Critical Points

**Order parameter near critical point:**
```
m ~ (T_c - T)^β  for T < T_c (ordered phase)
m = 0            for T > T_c (disordered phase)

Susceptibility: χ ~ |T - T_c|^(-γ) → ∞

Correlation length: ξ ~ |T - T_c|^(-ν) → ∞

At T = T_c: system has fluctuations at all scales.
```

**Ising model example:**
```
2D Ising: β = 1/8, γ = 7/4, ν = 1

Magnetization vanishes as m ~ (T_c - T)^(1/8)
Susceptibility diverges as χ ~ |T - T_c|^(-7/4)
```

---

## 9. Multi-Valued Functions and Branch Points

Points where functions become multi-valued and must be cut.

---

### 9.1 Square Root Branch Point

**Mathematical form:**
```
f(z) = √z

At z = 0: branch point
Going around z = 0: √z → -√z (picks up minus sign)

Need branch cut (usually along negative real axis)
to make function single-valued.
```

**In physics:**
```
Dispersion relation: ω = √(k² + m²)

Has branch points at k = ±im (in complex k-plane).
These encode particle mass and determine
analytic structure of propagators.
```

---

### 9.2 Logarithmic Branch Point

**Mathematical form:**
```
f(z) = ln(z) = ln|z| + i·arg(z)

At z = 0: branch point
Going around z = 0: ln(z) → ln(z) + 2πi

Each circuit adds 2πi (infinitely many sheets).
```

**In physics:**
```
Green's function in 2D:
G(r) = (1/2π)ln(r)

Branch point at r = 0 reflects the 2D nature
of the problem (different from 3D 1/r behavior).
```

---

### 9.3 Phase Singularity (Optical Vortex)

**Mathematical form:**
```
Complex field: E(r,θ) = f(r) · e^(imθ)

Amplitude: |E| = |f(r)|
Phase: φ = mθ (m = topological charge)

At r = 0:
|E| = |f(0)| = 0 (for proper vortex)
Phase = m · (undefined) = undefined

The phase winds by 2πm around the singularity.
```

**Physical realization:**
```
Laguerre-Gaussian beams, superfluid vortices,
quantum vortices in BEC.

Circulation: ∮∇φ · dl = 2πm (quantized)
```

---

### 9.4 Riemann Sheets in Scattering

**S-matrix structure:**
```
S(E) has branch cuts from particle production thresholds.

Below threshold E < E_threshold: bound states (poles)
Above threshold: scattering states (continuous spectrum)

Physical sheet: Im(k) > 0
Unphysical sheet: Im(k) < 0 (resonance poles live here)
```

---

## 10. Essential Singularities

Singularities that are neither poles nor branch points; exhibit wild behavior.

---

### 10.1 The e^(1/z) Type

**Mathematical form:**
```
f(z) = e^(1/z)

As z → 0 along positive real axis:
1/z → +∞, so e^(1/z) → +∞

As z → 0 along negative real axis:
1/z → -∞, so e^(1/z) → 0

As z → 0 along imaginary axis:
1/z is imaginary, so e^(1/z) oscillates wildly
```

**Key property:**
```
f(z) takes every complex value (except 0) infinitely
many times in any neighborhood of z = 0.
(Picard's theorem)
```

---

### 10.2 Non-Perturbative Effects (Instantons)

**Mathematical form:**
```
Tunneling amplitude: A ~ e^(-S/ℏ)

where S = action of instanton path.

In perturbation theory:
A(g) = Σ aₙ gⁿ  (all derivatives vanish at g = 0)

Because:
d^n/dg^n [e^(-1/g)]|_{g=0} = 0  for all n

Non-perturbative effects are "invisible" to any finite
order of perturbation theory.
```

**Physical examples:**
```
Quantum tunneling through barriers
Vacuum decay (bubble nucleation)
QCD instantons (θ-vacuum)
Schwinger pair production: rate ~ e^(-πm²c³/eEℏ)
```

---

### 10.3 Stokes Phenomenon

**Mathematical form:**
```
Asymptotic expansion of Airy function:
Ai(x) ~ (1/2√π) x^(-1/4) e^(-2x^(3/2)/3)  for x → +∞
Ai(x) ~ (1/√π) |x|^(-1/4) sin(2|x|^(3/2)/3 + π/4)  for x → -∞

The form changes discontinuously as arg(x) varies.
This is Stokes phenomenon: exponentially small terms
suddenly "switch on" across Stokes lines.
```

---

## 11. Topological Singularities

Singularities arising from topological rather than metric properties.

---

### 11.1 Vortex Cores (Winding Number)

**Mathematical form:**
```
Order parameter: ψ = |ψ|e^(iφ)

Around a vortex: ∮dφ = 2πn  (n = winding number)

At vortex core: |ψ| = 0 (necessary for single-valuedness)

Topologically protected: cannot remove vortex continuously
without |ψ| → 0 somewhere.
```

---

### 11.2 Magnetic Monopole (Dirac String)

**Mathematical form:**
```
Monopole field: B = g r̂/r²

Vector potential A cannot be defined globally.
Must have singular "Dirac string" along some axis.

Quantization condition (from single-valuedness of ψ):
eg = nℏc/2  (n integer)

If monopoles exist, electric charge is quantized.
```

---

### 11.3 Conical Singularities

**Mathematical form:**
```
Metric: ds² = dr² + r²dθ²

Normal flat space: θ ∈ [0, 2π]
Conical deficit: θ ∈ [0, 2π - Δ]

At r = 0: curvature is delta function:
R = (Δ/2π) · δ²(r)

Parallel transport around r = 0 rotates vectors by Δ.
```

**Physical examples:**
```
Cosmic strings: Δ = 8πGμ/c² (μ = mass per length)
Point particles in 2+1D gravity
Orbifold fixed points in string theory
```

---

## 12. Model Breakdown Points

Points where a model's assumptions fail rather than math diverging.

---

### 12.1 Classical Electron Radius

**The problem:**
```
Electromagnetic self-energy: U = q²/(8πε₀r₀)
Equate to rest mass energy: U = m_e c²

Solving: r₀ = q²/(8πε₀m_e c²) ≈ 1.4 × 10⁻¹⁵ m
```

**The breakdown:**
```
At scales r < r₀, classical electrodynamics predicts
the field energy exceeds the electron's rest mass.

This signals breakdown of classical point particle model,
not actual physics. Quantum mechanics takes over.
```

---

### 12.2 Planck Scale

**The problem:**
```
Combine quantum (ℏ), relativistic (c), gravitational (G):

Planck length: l_P = √(ℏG/c³) ≈ 1.6 × 10⁻³⁵ m
Planck time: t_P = √(ℏG/c⁵) ≈ 5.4 × 10⁻⁴⁴ s
Planck energy: E_P = √(ℏc⁵/G) ≈ 1.2 × 10¹⁹ GeV
```

**The breakdown:**
```
At Planck scale:
- Quantum fluctuations of spacetime ~ size of system
- Schwarzschild radius of energy ~ Compton wavelength
- Classical spacetime geometry becomes meaningless

All known physics breaks down here. Quantum gravity needed.
```

---

### 12.3 Mean Field Theory Breakdown

**Ginzburg criterion:**
```
Mean field valid when fluctuations ≪ order parameter:

|δφ|² / |⟨φ⟩|² ≪ 1

Near T_c: |δφ|² ~ kT/ξ^d, |⟨φ⟩|² ~ (T_c - T)^(2β)

Fluctuations dominate in "critical region":
|T - T_c|/T_c < Gi  (Ginzburg number)
```

**Example:**
```
Superconductors: Gi ~ 10⁻⁸ (mean field works well)
Helium-4 at λ-point: Gi ~ 1 (fluctuations dominate)
```

---

## Summary: Mathematical Operation Types

| Type | Mathematical Form | Behavior | Physical Examples |
|------|------------------|----------|-------------------|
| Simple pole | a/xⁿ | → ∞ as x → 0 | 1/r potentials, fields |
| Compound denominator | 1/√(1-x²) | → ∞ as x → 1 | Lorentz factor |
| Concentration | finite/0 | → ∞ | Point masses, delta functions |
| Divergent integral | ∫dx/x | → ∞ | Self-energies, UV/IR divergences |
| Divergent sum | Σaₙ | → ∞ | Zero-point energy, Hagedorn |
| Indeterminate | 0/0, ∞-∞ | undefined | Renormalization, limits |
| Asymptotic limit | f(x) → L | never reaches | v → c, T → 0 |
| Discontinuity | f(a⁺) ≠ f(a⁻) | jump | Phase transitions, shocks |
| Branch point | √z, ln(z) | multi-valued | Dispersion relations |
| Essential singularity | e^(1/z) | wild oscillation | Non-perturbative effects |
| Topological | winding number | discrete obstruction | Vortices, monopoles |
| Model breakdown | assumptions fail | physics changes | Planck scale, classical limits |

---

*Each singularity represents a mathematical statement about where expressions cease to have well-defined finite values. Whether this reflects physical reality or model limitations is the central question for analysis.*

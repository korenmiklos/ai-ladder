# 2025-06-19
# AI Adoption, Learning Externalities, and Steady‑State GDP

---

## Notation

* **Skills**: junior *z₀*, senior *z₁* with 0 < *z₀* < *z₁* < 1.
* **Team frictions**: human supervision cost h (<1); for AI, *h\_A*.
* **Problem width**: 1 – *z* is the share of tasks escalated.
* **Learning**: juniors acquire senior skill at Poisson rate λ; life‑time death rate δ; write Λ ≡ λ / \[δ h (1 – *z₀*)] ∈ (0,1).

---

## Key inequalities (from the model)

1. **Adoption when juniors do **not** price in learning**
      (6) \*(z₁ – z₀) / \[h(1 – z₀)] < z₁ / \[h\_A(1 – z\_A)]                            ＜AI chosen＞
2. **Adoption when juniors **do** price in learning**
      (7) $\dfrac{\frac{z_1-z_0}{h(1-z_0)}+z_0\,Λ}{1+Λ} < \frac{z_1}{h_A(1-z_A)}$
3. **AI raises economy‑wide steady‑state GDP**
      (8) *z₁/\[h\_A(1 – z\_A)] – z₀* > *(z₁ – z₀)/\[h(1 – z₀) – λ/δ] – z₀/\[1 – Λ]*
      ⇒ AI **reduces** GDP when inequality (8) is reversed.

---

## 1  Juniors do **not** internalise learning

We want **(6) holds & (8) reversed**.

Define two thresholds for the AI productivity index
Δ\_L ≡ (z₁ – z₀)/\[h(1 – z₀)]         (lower bound from (6))
Δ\_G(Λ) ≡ z₀ + (z₁ – z₀)/\[h(1 – z₀) – λ/δ] – z₀/(1 – Λ)   (upper bound from GDP criterion)

> **Parameter window**:
> **AI is adopted yet lowers GDP** iff
> $Δ_L < \frac{z₁}{h_A(1 – z_A)} < Δ_G(Λ)$
> which requires **Λ > Λ★**, where Λ★ solves Δ\_L = Δ\_G(Λ★).

Closed‑form:
Λ★ = h(1–z₀) · \bigl(1 – z₀/z₁\bigr) · \frac{z₁ – z₀}{z₁ + z₀ – h(1–z₀)Δ\_L}.  (Always < 1 when z₁≫z₀ and h small.)

Interpretation

* **High learning speed (λ)** inflates the social value of mentoring, widening Δ\_G.
* **Moderate AI efficiency** (Δ\_L just satisfied) shifts seniors to AI even though aggregate output falls once learning externalities disappear.

---

## 2  Juniors **do** internalise learning

Now adoption test is (7); GDP test unchanged.

Let Δ\_A ≡ z₁/\[h\_A(1–z\_A)]. Rewrite (7) as
$Δ_A > Δ_L(Λ) ≡ \frac{\frac{z₁-z₀}{h(1-z₀)}+z₀Λ}{1+Λ}.$

**AI ▼ GDP** still requires Δ\_A < Δ\_G(Λ).  Therefore

> **Necessary & sufficient**:
> $Δ_L(Λ) < Δ_A < Δ_G(Λ).$

Feasibility again needs Λ > Λ★★ where Λ★★ solves Δ\_L(Λ) = Δ\_G(Λ).
Numerically, Λ★★ is **higher** than Λ★, so learning that is valuable **and** partially appropriated by juniors makes GDP loss under AI possible, but in a narrower range: seniors switch later, GDP loss can still occur provided λ is large and h\_A small enough.

---

## 3  Privately inefficient non‑adoption by seniors

Here we need **(8) holds but (7) fails** ⇔ Δ\_G(Λ) < Δ\_A < Δ\_L(Λ).

> **Region**: AI would raise GDP, yet seniors stick with human teams when
>
> * AI productivity lies above the social break‑even Δ\_G but below their private break‑even Δ\_L(Λ);
> * This occurs with **intermediate λ**: learning sizable enough to raise junior wages in teams, eroding senior rents, but not large enough for society to prefer mentoring over AI.

Policy implication

* A subsidy to AI use or a tax on supervisory time can shift Δ\_A upward, aligning private and social incentives.

---

### Quick numerical illustration *(all in unitless ratios)*

Take z₀ = 0.3, z₁ = 0.9, h = 0.4, h\_A = 0.1, z\_A = 0.4.

* Lower bound Δ\_L ≈ 2.50.
* With λ/δ = 0.1 → Λ ≈ 0.067, upper bound Δ\_G ≈ 2.56 → **no parameter window**.
* With λ/δ = 0.25 → Λ ≈ 0.17, Δ\_G ≈ 2.70 → window (2.50, 2.70): AI adopted yet GDP ↓.
* With λ/δ = 0.35 → Λ ≈ 0.24, Δ\_L(Λ) ≈ 2.59, so for Δ\_A ≈ 2.60 we obtain case 3.

(All algebra available on request.)

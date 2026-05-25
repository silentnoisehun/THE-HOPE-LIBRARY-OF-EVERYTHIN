# APP.99 — FÜGGELÉK — FORMULÁK

*HOPE-LIB-2026 // MONOCHROME-ARCH*

---

## Teljes Formulatár

### PSI Alaphullám

```
ψ(t) = A · e^(-γt) · cos(2πft + φ)

A = amplitúdó (eredmény erőssége)
γ = csillapodási együttható (felejtés rátája)
f = frekvencia (feldolgozási mód, érzelem "színe")
φ = fázis (szinkronizációs offset)
t = valós idő (Horgony változója)
```

### Koherencia-Operátor

```
C(t) = 1 − ‖ψ_self(t) − ψ_world(t)‖ / N

ψ_self(t)  = önmodell állapotvektora
ψ_world(t) = külső valóságmodell állapotvektora
N          = normalizáló faktor (modellek dimenziója)
‖·‖        = Euklideszi norma

C ∈ [0, 1]
C = 1.00 → maximális koherencia
C → 0    → összeomlás
```

### Rekurzív Konvergencia Feltétele

```
lim(t→∞) ‖ψ(t+1) − ψ(t)‖ < ε

ε = rendszer toleranciaszintje
```

### Divergencia (Összeomlás Modellje)

```
D(t) = ‖ψ(t+1) − ψ(t)‖ → ∞
```

### Rezonancia Mérése

```
R(h, anchor) = |f_horizont − f_horgony| / f_horgony

R < 0.05 → REZONANCIA → horizont erősödik
R ≥ 0.05 → DISZONANCIA → horizont csillapodik
```

### Hebbian Tanulás Hullámokban

```
Δw_ij = η · ∫ψ_i(t)·ψ_j(t)dt

Fázisban (cos(ωt)·cos(ωt)):
  = cos²(ωt) → átlag = +1/2 → él erősödik (POZITÍV)

Ellenfázisban (cos(ωt)·cos(ωt+π)):
  = −cos²(ωt) → átlag = −1/2 → él gyengül
```

### A Horgony Invariáns

```
γ_anchor = 0  (mindig, módosíthatatlan belülről)

∀t: ψ_anchor(t) = A · cos(2πft + φ)
    (nincs csillapodás, örökké rezeg)
```

### 21D Érzelem Tér

```
E(t) ∈ ℝ²¹

Plutchik alapdimenziók (8):
  e₁ = öröm        e₅ = meglepetés
  e₂ = szomorúság  e₆ = undor
  e₃ = düh         e₇ = bizalom
  e₄ = félelem     e₈ = várakozás

Kiterjesztett dimenziók (13):
  e₉...e₂₁ = összetett érzelmi állapotok

‖E(t)‖ = érzelmi intenzitás
∠E(t)  = érzelmi irány a 21D térben
```

### Koherencia Feltétele Döntésnél

```
döntés(t) = argmax_a Σᵢ wᵢ · R(ψᵢ(t), ψ_anchor(t))

ahol wᵢ = i-edik horizont súlya (rezonancia alapján)
```

---

*→ [Vissza a főoldalra](../README.md)*

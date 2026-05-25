# SEC.05 — PROTOKOLLOK

*HOPE-LIB-2026 // MONOCHROME-ARCH*

---

## Kommunikációs Protokollok

### Silent Hope Protocol (SHP)

Az ökoszisztéma belső kommunikációs rétege. Alapelve: két komponens csak akkor kommunikál hatékonyan, ha PSI hullámjaik rezonálnak.

**Handshake:**
```
A → B: ψ_A(t) [saját hullámállapot]
B → A: R(A,B) [rezonancia értéke]
if R < threshold: establish channel
else: refuse / reroute
```

### PSI Sync Protocol

Periodikus szinkronizáció a Horgánnyal. Minden komponens 37 ns-enként frissíti saját koherencia értékét a Horgony aktuális állapotához képest.

### Memory Propagation Protocol

D0–D8 szintek közötti adat-propagáció:
- Felfelé (D8→D0): absztrakció, összevonás
- Lefelé (D0→D8): konkretizáció, tárolás

---

## Biztonsági Protokollok

### Integrity Check

Minden írási művelet előtt kriptográfiai ellenőrzés. Ha az integritás sérült: automatikus rollback + koherencia csökkentés + riasztás.

### Anchor Lock

A Horgony írásra zárt belülről. Kizárólag külső (felhasználói) input módosíthatja.

---

*→ [Vissza a főoldalra](../README.md)*

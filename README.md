# student-ctd-finder

A minimal educational calculator for understanding Cheapest-to-Deliver (CTD) mechanics in CME Treasury futures delivery baskets.

This is **NOT** a desk tool, production system, or delivery optimizer.

The goal is simple:

> Understand *why* a bond becomes CTD through clean delivery economics.

---

# Core Idea

Treasury futures contracts allow delivery from a basket of eligible Treasury securities.

Each bond in the basket has:
- a different clean price
- a different conversion factor
- different delivery economics

This project strips away institutional complexity and focuses on the core intuition:

# CTD is literally just the bond with the smallest net basis kek

---

# Inputs

## Futures Inputs
- Futures Price
- Days to Delivery
- Repo / SOFR assumption

## Deliverable Basket Inputs
- CUSIP
- Clean Price
- Conversion Factor (CF)

---

# Engine Logic

## Invoice Price

Invoice Price = Futures Price × CF

## Financing Cost

Financing = Clean Price × Repo × (Days / 360)

## Net Basis

Net Basis = Clean Price - Invoice Price + Financing

The bond with:
# the lowest net basis
is identified as:
# Cheapest-to-Deliver (CTD)

---

# Why This Matters

This project demonstrates:
- Treasury futures convergence
- delivery economics
- financing effects
- conversion factor mechanics
- why different bonds compete inside a delivery basket
- why Treasury futures are deeply tied to cash bond markets

It also shows something extremely important:

> Bonds inside the same delivery basket can have wildly different basis values.

That creates the foundation for:
- basis trading
- cash vs futures relative value
- CTD switching
- Treasury RV strategies

---

# Educational Philosophy

Most fixed income education either:
- oversimplifies into nonsense
OR
- turns into fake Bloomberg terminal cosplay

This project tries to sit in the middle:
- simple
- transparent
- visually clean
- economically real

The purpose is not to perfectly model dealer systems.

The purpose is:
# learning Treasury futures mechanics intuitively.

---

# Important Notes

This model intentionally excludes many real-world complexities such as:
- accrued interest
- delivery optionality
- wildcard optionality
- repo specialness
- coupon carry
- exact settlement conventions
- CTD switching dynamics
- curve/rate volatility effects

Real institutional CTD systems are vastly more complex.

This project is a student educational framework only.

---

# Future Ideas
- Advanced mode with repo specialness
- Accrued interest support
- CTD switch analysis
- Duration/DV01 visualization
- Implied repo calculations
- Futures-to-cash hedge analytics

---

# Built For
Students, aspiring rates traders, fixed income nerds, and anyone trying to make Treasury futures mechanics feel human-readable instead of impossible.

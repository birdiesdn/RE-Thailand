# Bangkok Land Watch — 7 September 2026 (weekly run)

Web-search run. Gmail: no portal alert emails. Google Drive: folder responsive
but still empty — no KML/KMZ tracings, so all footprint gauges remain assumed
squares.

## Network block — root cause identified

For the first time the proxy returned a specific diagnosis rather than a bare
timeout. All three test hosts (fazwaz.com, ddproperty.com,
server.arcgisonline.com) failed as:

```
connect_rejected — gateway answered 403 to CONNECT (policy denial or upstream failure)
```

This is an **organization-level egress policy denial**, not a portal bot-block,
not a transient network fault, and not something retrying will fix — the
proxy's own documentation says explicitly not to retry 403/407 policy denials
but to report them. Eight weeks of failures now have one cause.

**What this means practically:** the "network policy was opened" premise in the
weekly instruction is not in effect for this environment. Until an org admin
allows these hosts through the egress proxy, direct portal scraping and Esri
World Imagery tile stitching cannot run, and the aerial-snapshot feature cannot
be built at all. Everything else in the sweep is unaffected.

## New plots added (2) — both price-on-request

| Location | Area | Perimeter | Notes |
|---|---|---|---|
| On Nut Soi 63, Prawet | 2-0-50 rai · 850 sq.wah · 3,400 m² | ≈233 m | Two-rai plot on a named soi in the On Nut absorption zone. The register already carries Phra Khanong Nuea on this corridor at ฿73,515/m², so there is a comparable to price against. |
| Suan Luang, 533 sq.wah | 2,132 m² | ≈210 m (33 × 72 m stated) | Second Suan Luang plot after Rama 9 Soi 49 and far larger. **33 m frontage** is the useful detail — allows a road-facing multi-unit layout. |

**A discrepancy worth noting on the Suan Luang plot:** the listing's own figures
disagree. 533 sq.wah is 2,132 m², but the stated 33 m × 72 m computes to
2,376 m² — an 11% gap. The plot is probably irregular rather than rectangular.
The register records 2,132 m² (the sq.wah figure, being the authoritative Thai
unit) and flags the conflict on the card.

**Register now: 31 plots + 1 zone watch; 17 priced.** Median asking unchanged at
**฿26,455/m²** — both additions are unpriced, so the distribution did not move.

## The register's shape is now the story

**14 of 31 plots are price-on-request** — nearly half. That is no longer a
footnote; it is the main constraint on the tracker's usefulness. The three
largest unpriced parcels are, in order:

1. **Ratchaphruek, ≈14,400 m²** — the largest unpriced site, estate scale, on
   the Purple Line. Carried since 9 July without a number.
2. **Krungthep Kreetha new section, ≈12,296 m²** — subdividable, ultra-luxury
   pitch, in the strongest corridor on the register.
3. **Hua Mak, 8,088 m²** — freehold, marketed for logistics rather than
   residential, which is exactly why it may be mispriced.

Those three are the register's entire top end by land area, and none of them
has a price. Three phone calls would tell you more than another month of
sweeps.

## Outstanding items (owner action)

1. **Egress policy** — now diagnosed (403 at CONNECT, organization policy). An
   admin allowing the six portal hosts plus `server.arcgisonline.com` would
   restore both direct scraping and the aerial snapshots.
2. **Portal email alerts** — still not configured; would give true posted dates.
3. **Google Earth tracings** — folder still empty.

## Sources

- Thailand-Property Bangkok land: <https://www.thailand-property.com/land-for-sale/bangkok>
- Hipflat Bangkok land: <https://www.hipflat.com/land-for-sale/bangkok>
- DDproperty Bangkok: <https://www.ddproperty.com/en/property-for-sale/in-bangkok-th10>
- FazWaz Bangkok: <https://www.fazwaz.com/property-for-sale/thailand/bangkok>

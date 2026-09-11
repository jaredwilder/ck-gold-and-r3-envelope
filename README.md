# Finite `r_3` bounds and `C_k` computations

**380 verified finite bounds for `r_3`**, together with **36 finite `C_k` computations** whose search domains and witnesses are recorded explicitly.

Author: Jared Wilder. First public timestamp: 2026-09-10. Work dated 2026-07-29.

## The `r_3` envelope

`erdos142-envelope/derived-theorems.json` contains **380 derived bounds, all 380 rechecked**.

Every entry records the bound, the elementary rule used to derive it, the supporting value or witness, and any weaker bound it replaces. For example:

    "statement": "r_3(80) >= 19",
    "supersedes": "banked r_3(80) >= 15",
    "reason":  "r_3 is non-decreasing: a 3-AP-free subset of {1..m} is a 3-AP-free subset of
                {1..n} for every n >= m",
    "check_detail": "witnessed by r_3(60) >= 19"

and

    "statement": "r_3(18) <= r_3(9) + r_3(9) = 5+5 = 10",
    "family": "subadditivity_instance"

The mathematics here is a finite closure under explicit ingredients such as monotonicity and subadditivity. `all-campaign-lower-bounds.json` and `scan-9-60.json` contain the underlying finite data.

The asymptotic Erdős 142 question is separate. The Lean development containing the first exact values of Mathlib's `rothNumberNat` lives in `jaredwilder/erdos-close-campaigns`.

## The `C_k` computations

`gold-round/runs/` contains **36 completed finite searches**. The run identifiers are historical and non-contiguous; the directory listing is authoritative.

Each search records its exact finite universe. For example, OCG-001 studies `k = 3` over `n in [4,7]`, with distinct ordered variables, an optimum of 4, an explicit witness, and the SHA-256 of the finite atlas searched.

The mathematical statement attached to each run is simply the result within that declared finite domain. The stored execution metadata makes the computation reproducible but is not needed to interpret the bound itself.

## Files

- `erdos142-envelope/derived-theorems.json` — 380 verified derived bounds;
- `all-campaign-lower-bounds.json`, `scan-9-60.json` — underlying finite scans;
- `gold-round/runs/` — 36 finite `C_k` searches with witnesses and boundaries.

## License

Apache-2.0.
# ck-gold-and-r3-envelope

**380 machine-derived and machine-verified bounds on `r_3`**, plus **36 bounded-evidence campaign runs** on `C_k`-free structure.

Author: Jared Wilder. First public timestamp: 2026-09-10. Work dated 2026-07-29.

## The r_3 envelope

`erdos142-envelope/derived-theorems.json` carries **380 candidates, 380 verified**.

Every entry states its family, the bound, the reason, and what it supersedes. Two examples, verbatim from the file:

    "statement": "r_3(80) >= 19",
    "supersedes": "banked r_3(80) >= 15",
    "reason":  "r_3 is non-decreasing: a 3-AP-free subset of {1..m} is a 3-AP-free subset of
                {1..n} for every n >= m",
    "check_detail": "witnessed by r_3(60) >= 19"

    "statement": "r_3(18) <= r_3(9) + r_3(9) = 5+5 = 10",
    "family": "subadditivity_instance"

These are **closure derivations** from explicit ingredients such as monotonicity and subadditivity. Their value is that every strengthened bound carries its witness, derivation rule, and superseded weaker bound, making the envelope auditable end to end.

`all-campaign-lower-bounds.json` and `scan-9-60.json` hold the underlying scan.

The scope here is the finite `r_3` envelope produced by those rules and inputs. The asymptotic Erdős 142 question is a separate layer; the Lean development containing the first exact values of Mathlib's `rothNumberNat` is at `jaredwilder/erdos-close-campaigns`.

## The C_k gold round

`gold-round/runs/` holds **36 campaign runs**. Their ids run from OCG-001 to OCG-144 but are **not contiguous** — the 36 present are 001-003, 013, 014, 017, 037, 040, 049, 060, 063, 084, 097-108, and 133-144. Read the directory, not the range.

Every run carries verdict **`BOUNDED_EVIDENCE`** with an explicit `executionBoundary` naming the exact universe it ran in. OCG-001, for instance, records `bounded_canonical_Ck_micro_atlas` at `k = 3` over `n in [4,7]`, with tuple semantics stated as "distinct ordered variables; forbidden support canonicalized", an optimum of 4, an explicit witness, and a sha256 of the atlas it searched.

`BOUNDED_EVIDENCE` means a result established inside the declared finite boundary, with that boundary published alongside it. The operator traces record which adapter family executed and whether it ran on the boundary or was refused.

## License

Apache-2.0.
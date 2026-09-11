# ck-gold-and-r3-envelope

380 machine-derived and machine-verified bounds on r_3, plus 36 bounded-evidence campaign runs on
C_k-free structure.

Author: Jared Wilder. First public timestamp: 2026-09-10. Work dated 2026-07-29.

## The r_3 envelope

`erdos142-envelope/derived-theorems.json` carries **380 candidates, 380 verified.**

Every entry states its family, the bound, the reason, and what it supersedes. Two examples,
verbatim from the file:

    "statement": "r_3(80) >= 19",
    "supersedes": "banked r_3(80) >= 15",
    "reason":  "r_3 is non-decreasing: a 3-AP-free subset of {1..m} is a 3-AP-free subset of
                {1..n} for every n >= m",
    "check_detail": "witnessed by r_3(60) >= 19"

    "statement": "r_3(18) <= r_3(9) + r_3(9) = 5+5 = 10",
    "family": "subadditivity_instance"

**These are derivations, not discoveries.** Monotone closure and subadditivity are elementary. What
the file is good for is that each derived bound carries its witness, its reason, and the weaker
bound it replaces, so the chain is auditable end to end rather than asserted.

`all-campaign-lower-bounds.json` and `scan-9-60.json` hold the underlying scan.

Erdos 142 itself is **open**, and nothing here bears on the Theta-order question that carries the
prize. The Lean side, including the first exact values of Mathlib's `rothNumberNat`, is at
github.com/jaredwilder/erdos-close-campaigns.

## The C_k gold round

`gold-round/runs/` holds 36 campaign runs, OCG-001 through OCG-144.

Every one carries verdict **`BOUNDED_EVIDENCE`** with an explicit `executionBoundary` naming the
exact universe it ran in. OCG-001, for instance, records
`bounded_canonical_Ck_micro_atlas` at k = 3 over n in [4, 7], with tuple semantics stated as
"distinct ordered variables; forbidden support canonicalized", an optimum of 4, an explicit
witness, and a sha256 of the atlas it searched.

**`BOUNDED_EVIDENCE` is the verdict, and it means what it says:** a result established inside a
declared finite boundary, with the boundary published alongside it. None of these is a theorem
about all n.

The operator traces record which adapter family executed and whether it ran on the boundary or was
refused, which is the part worth reading if you care about whether the machine was honest with
itself.

## License

Apache-2.0.

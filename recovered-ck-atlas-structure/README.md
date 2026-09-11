# Recovered C_k atlas structure — release-day extraction

**Author:** Jared Wilder  
**Recovered source:** historical estate record for `oracle/evidence/atlas/ck-exact-atlas-extended.json`  
**Public extraction:** 2026-09-11

The historical dossier records a C_k atlas with **154 proven-optimal finite values** plus several
structural results. The original 154-value JSON has not yet been recovered as standalone bytes in
the current Library, so this release publishes only the exact structure that is independently
present in the surviving atlas registry. It does **not** fabricate the missing table.

## Semantics warning

The estate used `C_k` in multiple nearby experimental lanes. The results below refer to the
**alternating-binomial finite-difference avoidance** lane used by the verified C_k solver, with
ordered distinct tuple semantics and forbidden relation

\[
\sum_{j=0}^{k}(-1)^j\binom{k}{j}x_{j+1}=0.
\]

They must not be silently identified with the ordinary `k`-term arithmetic-progression extremal
function. The historical dossier itself flags notation cleanup as a publication requirement.

## Recovered exact structural results

### 1. Lipschitz-1 monotonicity for hereditary interval properties

For any hereditary property `P` of subsets of integer intervals, if `C_P(N)` is the maximum size of
a `P`-subset of `{1,...,N}`, then

\[
C_P(N+1)-C_P(N)\in\{0,1\}.
\]

The proof is immediate: an optimum at `N` remains admissible at `N+1`, while deleting the new point
from any optimum at `N+1` loses at most one element. The estate also brute-force checked the
relevant C_k instances for `k=3,4,5`, `N<=16` (33 adjacent pairs, zero violations).

### 2. Cross-k incomparability

Exact finite optimization gives

\[
C_4(7)=6>C_3(7)=4,
\qquad
C_5(7)=5<C_4(7)=6.
\]

The estate records independent witness verification and additional optimal checks at `N=14`. Thus
monotonicity in the order `k` fails in both directions already at the same ambient size.

### 3. Sidon / 3-AP interaction is existential, not universal

Within the exhaustive `N=3..18` census of maximum `B_2` Sidon sets, clean maximum Sidon sets that
are also 3-AP-free exist at

`N in {4,7,12,18}`,

but no `N` in the tested range has **every** maximum Sidon set 3-AP-free. This is a finite
classification statement only.

### 4. C_4 double mega-plateau

The recovered optimality ledger records

\[
C_4(N)=12\quad (20\le N\le27),
\]

and

\[
C_4(N)=16\quad (38\le N\le45).
\]

Both plateaus have length eight and both break immediately:

\[
C_4(28)=13,\qquad C_4(46)=17.
\]

The source states that 42 values in the relevant C_4 run were verified optimal by CP-SAT.

### 5. Onset rigidity inside the recovered finite range

For first occurrences of values `v<=16`, the number of optimal C_4 sets at the onset is exactly one
iff

\[
v\in\{6,8,12,16\}.
\]

The associated plateau lengths are `{2,4,8,8}`. The source reports a mean plateau length `5.5` for
these unique-onset values versus `2.1` for non-unique onsets inside the audited finite range.
This is a finite empirical/computational theorem about the enumerated range, not an asymptotic law.

## Missing artifact obligation

The historical provenance map names

`oracle/evidence/atlas/ck-exact-atlas-extended.json`

as containing **154 exact values and structure**. That file is not currently recovered as a
standalone Library object, so the full numerical atlas is still a release-recovery obligation.
The public record should say that plainly rather than reconstructing numbers from prose.

## Authority boundary

- The hereditary Lipschitz lemma is a general mathematical theorem.
- The numerical C_k values and plateau/onset statements are exact finite-computational claims at
  the source-declared scope.
- No asymptotic theorem is claimed from the observed plateau pattern.
- No historical novelty claim is made here without a separate prior-art audit.

## License

Apache-2.0 for repository-authored material.

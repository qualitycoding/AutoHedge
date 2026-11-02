# DEVIATIONS — v3.9 addendum amendment

**Repository:** `qualitycoding/AutoHedge` — 2026-11-02.

1. **Source-tip drift (D-901).** Planning source branch tip `d0b225c94a3c43df3a3a530ae1c5dc379656f607` is the
   rollout phase's addendum publication commit, a direct child of audited
   `72a325b5ad7e41ccbe019b69f5ef9c5d13e50f26`. The implementation branch descends from the tip; nothing newer
   was overwritten.
2. **Git transport unavailable (D-905).** `github.com:443` git transport is
   blocked from this sandbox; all reads used `codeload` tarballs and all
   commits/pushes used the authenticated GitHub Git database API. Remote SHAs
   were verified after every push via the refs API. The addendum's
   push-and-verify cadence is preserved in substance.
3. **No local build/test/mutation execution (D-905).** Estimates in
   `reviews/MUTATION.md` and the CI matrix are marked as estimates pending the
   first CI run; no unrun check is reported as passed.
4. **No fresh-context reviewer (D-906).** Cold read and adversarial review
   recorded as same-author substitutions with High risk, per S-ADD-090.
5. **Learning-store push deferred.** G-003 destinations requested; pushes
   await sign-off (do-not-push until then).

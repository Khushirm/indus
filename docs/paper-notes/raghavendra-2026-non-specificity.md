# On the Non-Specificity of Statistical Measures Used in Script Decipherment

- **Authors, year, venue:** Nikhil Raghavendra (independent researcher). arXiv:2608.02999v1 [cs.CL], 4 Aug 2026. Preprint, not peer-reviewed.
- **Link:** https://arxiv.org/abs/2608.02999 (full text: "HTML" or "View PDF" on that page)
- **Date read:** 2026-10-20

## In one sentence
A carefully built non-language (SIGIL) passes every statistical test that has been used as evidence that the Indus script is language, so those tests alone cannot establish that it is.

## Method
- SIGIL: a deterministic generator of emblem texts for a fictional administrative world. Every text has meaning (dedications, offices, entitlements, events), but no sign has a sound value.
- Core corpus: 3,000 texts, 13,717 tokens, 419 attested sign types (450 registered, 17 ligatures); plus a 350-text "outpost" corpus for regional variation.
- Built with Pitman-Yor urns (gives Zipf-like frequencies), optional slots, weighted epithets.
- Ran a registry of 54 methods from the literature; 6 scored exactly against published Indus outcomes, the rest reproduced descriptively.

## Data
SIGIL (synthetic) compared against published Indus results; dictionary-matching stress test against English, Sanskrit, Tamil.

## Results
- All 6 exactly-scored outcomes match Indus: Sproat's repetition ratio (0.646 vs Indus 0.575, both "non-linguistic"), right-to-left direction criteria, all three LNRE frequency models rejected.
- Descriptively also Indus-like: Zipf-Mandelbrot exponent 2.574 (Indus 2.59); Lee et al. rule labels SIGIL "writing: syllables" in all 27 configurations; conditional/block entropy, positional patterns, segmentation.
- Decipherment stress test: "readings" of SIGIL reach 83.0% dictionary coverage in English, 88.13% Sanskrit, 67.73% Tamil, though SIGIL encodes no language. Held-out coverage falls (74.23 / 61.01 / 44.05%), and six bootstrap keys agree on only 9.30% of sign values.

## What they claim, and what they don't
- Claim: these measures "do not, on their own, establish encoded speech"; "the burden of proof has moved".
- Not claimed: that Indus is non-linguistic. "Nothing here settles the status of the Indus script."
- No new discriminating test is proposed; the paper says none of the studies supplies a family of weighted non-linguistic alternatives.

## Recommended standard for any claim
Commit to sign values and predictions before testing; succeed on held-out inscriptions; prefer one language over matched alternatives; recover stable values across resamples; predict external archaeological or textual facts. Regularity-based claims need "a discriminative comparison against structured non-linguistic alternatives".

## How it affects our project
- Strongly supports our design: pre-registration, held-out split, resampling stability, structured null models.
- SIGIL-style generators should be one of our null models (check if the code is released).
- The dictionary-coverage result is a warning for LLM agents: fluent "readings" can be produced for a non-language. Our verifier must never accept on plausibility.
- Single-author preprint: cite as preprint; check later whether it gets peer-reviewed.

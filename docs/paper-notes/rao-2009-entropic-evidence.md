# Entropic Evidence for Linguistic Structure in the Indus Script

- **Authors, year, venue:** Rao, Yadav, Vahia, Joglekar, Adhikari, Mahadevan. *Science* 324:1165, 29 May 2009. doi:10.1126/science.1170391
- **Link:** https://homes.cs.washington.edu/~rao/ScienceIndus.pdf (main paper + supplementary)
- **Date read:** 2026-10-20

## In one sentence
The conditional entropy of Indus sign sequences matches natural languages and differs from the non-linguistic systems they tested, which "increases the probability" that the script encodes language.

## Method
- Conditional entropy: C = −Σᵢ P(i) Σⱼ P(j|i) log P(j|i), i.e. how uncertain the next sign is, given the current one.
- Bigram probabilities, smoothed with modified Kneser-Ney (the corpus is small).
- Plotted C against the number of most-frequent tokens used (20 → 400), so different-sized vocabularies can be compared (Fig. 1A).

## Data
- Indus: subset of Mahadevan (1977); 1,548 lines, 7,000 sign occurrences, 417 signs. Texts with ambiguous/missing signs, multi-line texts and duplicates removed.
- Languages: Sumerian (ETCSL), Old Tamil (Sangam Ettuthokai), Rig Vedic Sanskrit (Book 1, first 100 hymns), English words and characters (Brown corpus).
- Non-linguistic: DNA (human chr. 2), protein (E. coli), Fortran code, and two **synthetic** systems: Type 1 (any sign can follow any other, uniform) and Type 2 (each sign has a unique successor).

## What they claim, and what they don't
- Claim: Indus C falls inside the band of languages; closest to Sumerian and Old Tamil; between English words and characters.
- Not claimed: proof of language; a decipherment; Dravidian affinity (Old Tamil closeness is called "suggestive" but depends on writing Tamil alpha-syllabically; Sanskrit written alphabetically drops below Tamil).
- Supplement: single-sign (unigram) entropy can't separate the classes; the bigram model captures most of the structure (perplexity 68.82 → 26.69 from n=1 to n=2, then flat).

## Weaknesses / open questions
- Type 1 and Type 2 are extreme synthetic baselines (fully random / fully rigid). Anything with moderate structure lands "in between" with the languages. This is the core of Sproat's criticism.
- No real structured non-linguistic sign system of similar size was tested.
- Corpus is the 1977 concordance; ~1,000 texts found since.

## How it affects our project
- Stage 3 task: reproduce Fig. 1A (bigram conditional entropy with Kneser-Ney) on our corpus.
- Lesson: a verifier is only as good as its null models. Ours must include **structured** non-linguistic baselines, not only random/rigid ones. See [[raghavendra-2026-non-specificity]].

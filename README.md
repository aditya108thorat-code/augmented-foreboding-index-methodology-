# Augmented Foreboding Index (AFI)

### Research methodology overview

The **Augmented Foreboding Index (AFI)** is a news-based measure developed to examine how expressions of foreboding and assurance evolve in reporting on economic, financial, and geopolitical developments. It is intended as a descriptive indicator of the *tone of uncertainty in news coverage*, rather than a direct measure of economic losses or a forecast of asset prices.

This repository provides a concise methodological overview accompanying research communications about the AFI. Detailed dictionaries, scoring implementation, article-level outputs, and empirical specifications form part of the underlying research and are not reproduced here.

## 1. News universe and article selection

The research uses English-language Reuters reporting accessed through LSEG. For the July–September 2026 study period, the news-discovery query combined major Reuters news categories with source and language restrictions:

`(Topic:NEWS1 OR Topic:SREP OR Topic:EXCLSV) AND Source:RTRS AND Language:LEN`

The initial retrieval is deliberately broader than the analytical sample. Articles are then assessed for their relevance to material economic, financial, policy, and geopolitical developments. Selection gives particular attention to developments with plausible channels of transmission to financial conditions, including energy, monetary policy, international trade, capital flows, and geopolitical risk.

The processing workflow distinguishes alerts, major event stories, meaningful direct updates, and other material catalysts from routine or duplicative coverage. Repeated versions and substantially overlapping reports of the same development are consolidated to reduce multiple counting of a single underlying event. This is a research screening process, and the resulting sample is **not** a census of all Reuters publications.

## 2. Foreboding and assurance dictionaries

The AFI begins with two curated vocabularies:

- **Foreboding terms**, associated with threats, adverse developments, instability, escalation, or apprehension.
- **Assurance terms**, associated with reassurance, moderation, stability, resolution, or improving expectations.

These vocabularies build on the foreboding-index approach described in Roy Trivedi (2024), *Into the Unknown*. The augmented research framework also examines topic and sector context to help interpret the news environment. Dictionary matching is inherently sensitive to vocabulary and context; the index should therefore be interpreted as a structured textual indicator rather than a complete semantic reading of each article.

## 3. Article-level index

For an article with **F** matched foreboding terms and **A** matched assurance terms, the basic score is:

**AFI = F / (F + A)**

A score closer to **1** indicates a predominance of foreboding language among the matched terms; a score closer to **0** indicates a predominance of assurance language. Where **F + A = 0**, the score is treated as unavailable rather than assigned an artificial zero. The index is a relative measure of the two vocabularies within the text, not a probability that a negative event will occur.

## 4. Time aggregation and interpretation

Article-level observations can be examined at daily or weekly frequency. The research examines both the **average intensity** of foreboding and the **volume and distribution** of scored stories, since a day with relatively few strongly worded reports can differ substantially from a day with many moderately worded reports.

Daily views are useful for observing sharp changes around individual announcements or events. Weekly views make recurring clusters and broader episodes easier to inspect, although aggregation can smooth out short-lived fluctuations. For this reason, changes in the index should be read alongside the underlying news developments and the volume of observations.

## 5. Research considerations

The AFI reflects the content of a selected news sample and may be affected by editorial coverage, story availability, dictionary coverage, article revisions, and the treatment of overlapping events. It does not establish that a news event caused a particular market movement. Any association with financial variables requires separate statistical assessment, including the treatment of non-trading days, timestamps, and differences between contemporaneous and forward-looking effects.

The project is ongoing research. Descriptive charts and examples are illustrative and should not be interpreted as investment advice.

## Reference

Roy Trivedi, S. (2024). *Into the Unknown*.

## Scope of this repository

This page documents the broad research logic for public readers. The underlying Reuters text is subject to applicable data licensing; no licensed article text or proprietary market dataset is distributed here. Full lexicons, implementation code, and detailed empirical protocols are reserved for the associated research publication.

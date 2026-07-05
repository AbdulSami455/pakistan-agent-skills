---
name: pakistan-languages-demographics
description: Pakistan languages and linguistic-demographics skill. Use when looking up which languages are spoken in Pakistan, mother-tongue population shares by province, or the country's linguistic diversity and literature institutions, especially for census-based mother-tongue statistics distinct from ethnic or provincial population data.
---

# Pakistan Languages & Demographics

## Overview

Use this skill for Pakistan's linguistic landscape: which languages are spoken, mother-tongue population shares nationally and by province, and the institutions (e.g., Pakistan Academy of Letters) that support Pakistani-language literature. This is a reference skill for language/culture questions — for the full census population/household count itself, use `pakistan-census-bulletins`.

## Coverage

- National mother-tongue distribution: Punjabi is the largest mother-tongue group, followed by Pashto, Sindhi, Saraiki, Urdu, Balochi, and others, per the Pakistan Bureau of Statistics' census-based language reporting.
- Provincial linguistic profiles: each province has a distinct dominant-language composition (e.g., Punjab predominantly Punjabi with a significant Saraiki-speaking minority; Sindh split between Sindhi and Urdu speakers; Khyber Pakhtunkhwa predominantly Pashto with Hindko and other minorities; Balochistan with Balochi, Pashto, Brahui, and other languages).
- National language vs. mother tongue: Urdu is Pakistan's national language and lingua franca (widely understood/spoken as a second language across the country) despite being the mother tongue of a comparatively small share of the population.
- Linguistic diversity: Pakistan has dozens of indigenous languages beyond the major provincial ones (e.g., Hindko, Brahui, Kashmiri, Balti, Shina, Khowar, Kalasha, Wakhi), from multiple language families (Indo-European/Indo-Aryan, Iranian, Dravidian, Dardic, and others).
- Pakistan Academy of Letters (PAL): the national institution supporting literature and writers across Pakistan's major languages, including regional/minority languages, through publishing, awards, and translation activities.

## Use This Skill For

- looking up mother-tongue population shares nationally or by province
- explaining the distinction between Urdu as national/lingua-franca language versus mother-tongue share
- identifying which languages are spoken in a specific province or region
- providing general context on Pakistan's linguistic diversity and language families
- identifying which institution (PAL) supports literature in a specific Pakistani language

## When Not to Use This Skill

- For the full population/household count itself (total population, households, growth rate) — use `pakistan-census-bulletins` instead; this skill covers the linguistic breakdown specifically, not overall demographic totals.
- For ethnic-group data as distinct from language data — mother tongue and ethnicity are related but not identical categorizations; do not conflate them without checking which the source actually reports.
- For education-medium-of-instruction policy questions — use `pakistan-education-statistics` for schooling-system data instead.

## Routing Rules

- Use this skill for mother-tongue/language-distribution questions specifically; route to `pakistan-census-bulletins` for total population, household, or growth-rate figures from the same census round.
- If a question mixes language and ethnicity, clarify which classification the source actually uses before answering, since census language data is based on self-reported mother tongue, not a separate ethnicity classification.
- For literature/writers-focused questions, PAL is the relevant institution; for the underlying population language-share statistics, PBS's census-based language report is the source.

## Extraction Workflow

1. Identify whether the question needs a national mother-tongue share or a specific province's linguistic composition.
2. Confirm the census round/year the language data is drawn from, since mother-tongue shares are reported per census and can shift between rounds due to both real demographic change and methodology/question-wording differences.
3. Distinguish "mother tongue" (first language learned at home) from "national language" (Urdu, as lingua franca) and from any second/additional-language capability figures if the source reports them separately.
4. For literature/institutional questions, confirm whether PAL or another body (e.g., a provincial language authority/academy) is the correct reference.

## Technical Rules

- Preserve exact percentage/population figures alongside their census round/year; do not present a specific round's figures as a permanently fixed distribution.
- Mother tongue is a self-reported census category; it should not be treated as equivalent to ethnicity, religion, or citizenship classification.
- Urdu's role as national language/lingua franca (widely understood) is distinct from its mother-tongue population share (a relatively small percentage); do not conflate "official/national language" status with "most common mother tongue."
- Provincial linguistic compositions include meaningful minority-language populations; do not reduce a province to a single dominant language without noting significant minorities where the source reports them.

## Validation Checklist

- Confirm the census round/year for any cited mother-tongue percentage or population figure.
- Verify whether "national language" and "mother tongue" are being used correctly and not interchangeably.
- Check that provincial figures include noted minority-language populations rather than a single-language oversimplification.
- Confirm whether a question needs population/language-share data (PBS) or literature/institutional information (PAL) before selecting a source characterization.

## Common Pitfalls

- Treating Urdu's national-language status as if it were also the most common mother tongue.
- Citing a specific census round's language shares as a permanently fixed distribution rather than tied to that round.
- Reducing a province's linguistic profile to one language while ignoring significant minority-language populations reported in the same source.
- Conflating mother-tongue (language) classification with ethnicity in the census data.

## Reference

- See [Pakistan Languages Reference](references/pakistan-languages-demographics.md) for source structure and extraction notes.

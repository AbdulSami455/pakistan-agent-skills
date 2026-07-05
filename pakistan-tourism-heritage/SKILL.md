---
name: pakistan-tourism-heritage
description: Pakistan tourism and general heritage-sites skill. Use when looking up tourist destinations, regional attractions (mountains, valleys, historic cities, forts, shrines), or general travel/geography information about Pakistan, as distinct from the formal UNESCO World Heritage List or administrative-boundary data.
---

# Pakistan Tourism & Heritage

## Overview

Use this skill for Pakistan's tourism destinations and general cultural/geographic points of interest — mountain regions, historic cities, forts, shrines, and natural attractions — as promoted by the Pakistan Tourism Development Corporation (PTDC) and provincial tourism bodies. This is a general-interest travel/geography reference skill, distinct from the formal UNESCO World Heritage List (a narrower, internationally inscribed subset) and from administrative-boundary data.

## Coverage

- Major tourism regions: Gilgit-Baltistan (highest mountain concentration globally, including several "eight-thousander" peaks and dozens of peaks above 7,000m), Khyber Pakhtunkhwa's northern valleys (e.g., Swat, Chitral, Kalash valleys), Azad Jammu & Kashmir, and coastal/desert tourism in Sindh and Balochistan.
- Historic cities and monuments beyond the formal UNESCO List: forts, shrines, mosques, and colonial/Mughal-era architecture across Punjab, Sindh, and other provinces.
- Adventure and nature tourism: trekking, mountaineering, white-water rafting, jeep safaris, and wildlife/national-park tourism.
- Provincial tourism bodies: PTDC operates at the federal level, while some provinces run their own tourism development corporations/departments with region-specific promotion and infrastructure (e.g., motels, tour operator listings).
- General geography/travel-planning context: major cities, provinces, and their broad cultural/geographic character, to the extent useful for general orientation rather than as a substitute for administrative-boundary data.

## Use This Skill For

- identifying notable tourist destinations or attractions in a specific region or province of Pakistan
- providing general cultural/historical context on a specific city, valley, fort, or shrine popular with tourists
- describing adventure-tourism opportunities (trekking, mountaineering) in a specific region
- distinguishing PTDC's federal tourism promotion from a specific province's own tourism body
- providing general orientation on Pakistan's geography for a non-specialist audience (e.g., a student or a prospective visitor)

## When Not to Use This Skill

- For Pakistan's formally inscribed UNESCO World Heritage Sites or Tentative List — use `pakistan-unesco-heritage-sites` instead; that is a narrower, internationally formalized list with specific inscription criteria and years, while this skill covers the broader universe of tourist attractions (most of which are not UNESCO-inscribed).
- For precise administrative-boundary codes/names (province, division, district, tehsil) needed for geocoding or data-joining — use `pakistan-admin-boundaries` instead.
- For visa, travel-advisory, or safety/security-specific guidance — outside this skill's scope; this is a general cultural/destination reference, not a travel-advisory or safety-briefing service.

## Routing Rules

- Use this skill for general tourist-destination and cultural-heritage questions; if a site's formal UNESCO inscription status specifically matters (e.g., for a citation requiring inscription year/criteria), route to `pakistan-unesco-heritage-sites` instead, since most tourist attractions in this skill's scope are not UNESCO-inscribed.
- If precise administrative codes are needed (e.g., joining a destination to district-level statistics), route to `pakistan-admin-boundaries`.
- Do not present this skill's general destination information as official travel-safety or visa guidance; recommend checking current official/consular advisories for that.

## Extraction Workflow

1. Identify the specific region, city, or type of attraction (mountain/adventure tourism, historic/cultural site, coastal/desert tourism) the question concerns.
2. If the question involves a UNESCO-related claim (inscription status, year, criteria), confirm whether the site is actually on the formal UNESCO list before answering — many well-known tourist sites are not UNESCO-inscribed despite popular perception.
3. Provide general orientation (province/region, notable character of the destination) rather than asserting precise, time-sensitive logistical details (opening hours, current road conditions, entry fees) that change frequently and are better sourced from current provincial tourism department listings.
4. Note whether PTDC (federal) or a specific provincial tourism body is the more relevant authority for a given destination.

## Technical Rules

- Do not conflate a general tourist attraction with UNESCO World Heritage status; only a small, specific set of Pakistani sites are formally UNESCO-inscribed (see `pakistan-unesco-heritage-sites`), while many other well-known sites (e.g., popular valleys, forts, shrines) are not.
- Treat specific logistical details (fees, hours, road/travel conditions) as time-sensitive and likely to change; do not present them as fixed facts without flagging the need for current verification.
- Distinguish federal-level tourism promotion (PTDC) from provincial tourism development bodies, which may have their own destination lists and services.

## Validation Checklist

- Confirm whether a site being discussed is actually UNESCO-inscribed before making that claim; if uncertain, route the UNESCO-specific question to `pakistan-unesco-heritage-sites`.
- Verify which province/region a destination belongs to.
- Flag time-sensitive logistical details (fees, access conditions) as needing current verification rather than presenting them as fixed.
- Confirm whether PTDC or a specific provincial body is the more relevant source for a given destination.

## Common Pitfalls

- Asserting UNESCO World Heritage status for a popular tourist site that is not actually on the formal UNESCO list.
- Presenting time-sensitive logistical details (fees, road conditions, seasonal access) as permanently fixed facts.
- Conflating this general tourism/heritage reference with precise administrative-boundary data needed for data-joining tasks.
- Treating general destination information as authoritative travel-safety or visa guidance.

## Reference

- See [Pakistan Tourism & Heritage Reference](references/pakistan-tourism-heritage.md) for source structure and extraction notes.

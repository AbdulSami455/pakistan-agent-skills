---
name: pakistan-school-infrastructure-wash
description: Pakistan school infrastructure and WASH skill. Use when analyzing, summarizing, comparing, or extracting information from official school-facility datasets and education-management reports in Pakistan, especially for electricity, drinking water, toilets, boundary walls, classrooms, and other facility-access indicators by geography and school type.
---

# Pakistan School Infrastructure and WASH

## Overview

Use this skill for school facility conditions in Pakistan: water, sanitation, electricity, buildings, boundary walls, classrooms, and basic service access. This is the right skill when the task is about whether schools have essential infrastructure rather than how many schools or students there are overall.

## Coverage

- AEPAM/NEMIS or PIE school-census facility tables where published.
- Provincial EMIS or school-education department facility reports.
- UNICEF-supported or officially adopted school WASH and infrastructure references where Pakistan government reporting is the anchor.
- Facility access dimensions such as drinking water, toilets, electricity, boundary walls, classrooms, laboratories, ICT labs, and disability-access infrastructure where available.
- Public/private, rural/urban, and province/district splits where the source supports them.

## Use This Skill For

- extracting facility-access percentages or counts for schools in a region
- comparing WASH or electricity access across provinces or school types
- identifying gaps in basic school infrastructure
- separating school availability from school-condition indicators
- sourcing school-facility evidence for planning or equity analysis

## When Not to Use This Skill

- For total institution, enrollment, or teacher counts, use `pakistan-education-statistics` instead.
- For learning outcomes, use `pakistan-learning-assessments` instead.
- For curriculum and subject-content questions, use `pakistan-national-curriculum-textbooks` instead.

## Routing Rules

- Use this skill when the question is about conditions inside schools rather than school-system size.
- If a source mixes school counts and facility rates, preserve which metric is being quoted.
- If the task is specifically about child WASH outcomes rather than school-facility provision, `unicef-pakistan-data` may provide complementary household-level context, but this skill remains the school-facility source.
- Keep district-level infrastructure gaps distinct from province-level national summaries.

## Extraction Workflow

1. Identify the facility type and geography required.
2. Confirm whether the source reports counts of schools, percentages of schools, or both.
3. Preserve the denominator if known: all schools, public schools, girls' schools, primary schools, and so on.
4. Note the school year or reporting edition.
5. If multiple facilities are compared, keep each indicator separate rather than building a composite unless the source does.

## Technical Rules

- A school with a toilet is not the same as a school with functional sanitation; preserve the exact source wording.
- Facility-access indicators may differ by school level and gender composition; do not silently mix boys', girls', and co-education schools.
- Percentage indicators require denominator clarity; avoid quoting them as raw counts.
- Infrastructure deficits and enrollment deficits are different problems even when they correlate.

## Validation Checklist

- Confirm the facility indicator and denominator.
- Verify the geography and reporting year.
- Check whether the measure is a count or percentage.
- Preserve school-type splits where the source uses them.

## Common Pitfalls

- Quoting a facility percentage as if it were a count of schools.
- Ignoring whether the data is for public-only schools or all schools.
- Treating presence of infrastructure as proof of service quality or functionality.
- Mixing school infrastructure indicators with student learning outcomes.

## Reference

- See [Pakistan School Infrastructure and WASH Reference](references/pakistan-school-infrastructure-wash.md) for source structure and extraction notes.

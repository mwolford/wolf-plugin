# Field Value Guide (plain English -> ADO values)

Ask 1-2 short questions, propose a value with a one-line reason, let the user confirm. Never write to ADO without approval.
Sources: MS Learn "Define, capture, triage, and manage work item fields (Agile)" and "Agile process work item types".

## Priority (Epic, Feature, Story)
| Ask / answer | Value |
|---|---|
| Can we ship without it? "No, it's required" | 1 |
| Important, but could slip a release | 2 |
| Nice to have | 3 |
| Only if there's spare time | 4 |

## Risk (Epic, Feature, Story)
Count the "yes" answers: unknowns/spike needed? depends on another team or new data source? effort hard to estimate? new tech?
- 2+ yes, or any would block delivery -> `1 - High`
- 1 yes -> `2 - Medium`
- 0 yes, well understood -> `3 - Low`

## Value Area (Epic, Feature, Story)
- Users, customers, revenue, or business decisions benefit directly -> `Business`
- Platform, tech debt, enablers, infrastructure -> `Architectural`

## Time Criticality (Epic, Feature only)
Is there a date it loses value after (regulatory, event, contract)? Higher number = more time-critical; none = low/blank.

## Dates
Epic and Feature: Start and Target dates. Stories: use Iteration instead.

## Always
State the mapping used ("Can't ship without it -> Priority 1") so the user learns the scale.

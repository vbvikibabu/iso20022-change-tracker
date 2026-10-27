# ISO 20022 Change Tracker

A source-linked, machine-readable timeline of ISO 20022 payment message changes, implementation dates, and scheme announcements.

This project focuses on **what changed, who it affects, when it applies, and where the primary evidence lives**. It is not a validator and does not claim that a schema-valid payment will be accepted by a bank.

## Why this exists

The same migration can have different dates across schemes, clearing systems, and banks. Announcements can also be revised after teams have started implementation. A static list is hard to compare or consume in software.

This repository keeps one record per material update in `data/events.json`. Each record includes the publishing body, affected scheme or country, publication date, current status, concise summary, source URL, and the date the source was last checked. Git history preserves the changes over time.

## Current feed

- [Machine-readable events](data/events.json)
- [Event schema](schema/events.schema.json)

## Status values

- `scheduled`: a date or change is currently published.
- `postponed`: the previously announced date or change was deferred.
- `effective`: the change has taken effect.
- `withdrawn`: the publisher cancelled the change.
- `under_review`: the publisher has announced a review but no decision.
- `informational`: a material update with no direct deadline.

A blank effective date means the source does not state a precise date. Do not infer one from a secondary article.

## Source and update policy

1. Prefer the standards body, payment scheme, central bank, clearing operator, or bank that issued the rule.
2. Keep the source link and verification date with every event.
3. Preserve prior decisions as separate records; do not silently rewrite history.
4. If two official sources differ, record the scope and the conflict instead of choosing one without evidence.
5. Treat bank-specific requirements separately from scheme-wide requirements.
6. Recheck volatile dates before operational or compliance decisions.

## Scope

The starter feed covers selected updates for SEPA, Swift CBPR+, Swiss Payments, Fedwire, CHAPS, and German EBICS. It is an initial snapshot, not a complete catalogue. Contributions should add an official source and a clear affected scheme.

## Similar projects

Existing repositories already provide annotated payment examples and sample XML, including [BenjoNX/iso20022-examples](https://github.com/BenjoNX/iso20022-examples) and [SynapticaSolution/sepa-pain001-examples](https://github.com/SynapticaSolution/sepa-pain001-examples). This project focuses on a versioned change feed with primary-source citations rather than another examples collection.

## License

No license has been selected yet. Add one before inviting reuse or accepting outside contributions.


# elihome-listing-writer

A Claude skill made at Elihome. Give it an Elihome product's raw specs and it writes an amazon.com listing that follows Amazon's rules and gives AI shopping assistants the facts they need.

It writes eight parts:

1. **Title** (75 characters at most)
2. **5 bullet points**, each in "Header: description" form, pairing a fact with the benefit that follows from it
3. **Description**, showing the product in use
4. **Backend search terms**, under 200 bytes
5. **Attribute table**, with the source of every value
6. **5 shopper Q&As**, the questions shoppers and Alexa for Shopping ask first
7. **"To check" list** of everything Elihome needs to confirm or supply before publishing
8. **Rule check** of the draft against Amazon's rules

It never invents a claim. Anything the specs don't prove (heat limit, certifications, country of origin, food safety) is marked **MISSING** in the attribute table, the Q&As and the "To check" list. It never appears in the title, bullets or description.

## Install

### ⬇️ [Download the skill (elihome-listing-writer.zip)](elihome-listing-writer.zip)

**In the Claude app** (code execution must be on):
1. Click the download link above. Don't unzip it.
2. Open [Claude > Customize > Skills](https://claude.ai/customize/skills), click **+**, then **+ Create skill**, then **Upload a skill**, and upload the ZIP.
3. Start a new chat, paste a product's specs and type: *Write the Amazon listing for this Elihome product.*

**Colleagues on the same Claude Team or Enterprise plan:** you don't need the ZIP. Ask the owner of the skill to share it with you (or publish it to the organization), then turn it on under **Shared with you** in [Customize > Skills](https://claude.ai/customize/skills).

**In Claude Code:** unzip the download into `~/.claude/skills/`, so that you have `~/.claude/skills/elihome-listing-writer/SKILL.md` and `~/.claude/skills/elihome-listing-writer/references/listing-rules.md`.

## Use

Paste the product's raw specs: Amazon's "Product information" fields or Elihome's own data (material, size of each piece, care, what's in the box, price, UPC). Don't paste the old listing text: the skill works from facts, not from old copy. Then ask in plain words, for example:

> Write the Amazon listing for this Elihome product.

> Check these bullet points against Amazon's rules.

## What's in this repository

- [`elihome-listing-writer.zip`](elihome-listing-writer.zip): the skill, ready to upload.
- [`elihome-listing-writer/`](https://github.com/kkindasara/elihome-listing-writer/tree/main/elihome-listing-writer): the same skill unzipped: `SKILL.md` and `references/listing-rules.md`, the Amazon rules it follows, each with its source.
- **Examples:** the same three products written without the skill and with it.

| Product | Without the skill | With the skill |
|---|---|---|
| Classic Silicone Spatula Turner (simple) | [before](examples/spatula-before-no-skill.md) | [v3](examples/spatula-after-skill-v3.md) |
| Classic Series 4-in-1 Cutting Board Set, 4-Pack (complex) | [before](examples/classic-set-before-no-skill.md) | [v3](examples/classic-set-after-skill-v3.md), [v4](examples/classic-set-after-skill-v4.md) |
| Elihome x Peanuts Double-Sided Cutting Board Set, 2 Pack (new) | [before](examples/peanuts-set-before-no-skill.md) | [v3](examples/peanuts-set-after-skill-v3.md) |

- **Tests:** [the test set](tests/test-products.md) (raw specs and current listings of the three products) and [the change log](tests/change-log.md) (what failed in each version and what was changed). Without the skill, 64% of the checks passed. With it, 100% passed.

## Limits

- It never adds a claim the specs don't prove, so missing data comes back as MISSING for Elihome to fill.
- It covers amazon.com only, with Amazon's rules as of 25 Nov 2026. The Home & Kitchen bullet length is not confirmed, so it reports the length of each bullet.
- It writes a draft. It does not publish to Seller Central.

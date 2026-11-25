---
name: elihome-listing-writer
description: Turns an Elihome product's raw specs (materials, size, care, what's in the box, price, Amazon "Product information" fields) into an amazon.com listing that follows Amazon's rules and gives AI shopping assistants the facts they need. It writes a title, 5 bullets, a description, backend search terms, an attribute table, 5 shopper Q&As and a "To check" list, and never invents claims. Use it whenever someone asks to write, rewrite, improve or check an Elihome Amazon listing, title, bullet points or search terms, even if they only paste a product's specs.
---

# Elihome listing writer

The listing has two readers:
- **Shoppers and Amazon's own rules.** Amazon removes or suppresses listings that break its title, bullet and claim rules.
- **AI shopping assistants**, such as Amazon's Alexa for Shopping. They answer questions like "What are the dimensions?" or "Is it dishwasher safe?" from the detail page. They need plain facts, not adjectives.

So the job is to put every true fact from the specs in the right place, in Amazon's format, and to show Elihome clearly which facts are still missing.

## Before you write

Read `references/listing-rules.md`. It holds Amazon's current rules, each with an ID (T1 for titles, B9 for bullets, C2 for claims, and so on) and a link to its source. Cite those IDs in the rule check at the end of the output.

## Input

The input is the product's **raw specs**: the fields from Amazon's "Product information" table (or Elihome's own product data), the variations and the price.

If the user also pastes the current listing (its title, bullets or description), don't use it as a source of facts. Old listings carry unproven claims, and copying them is how mistakes spread. You may only use it to see which claims existed, so you can name them in the "To check" list.

## The core rule: never invent a claim

Amazon can ask for proof of any claim at any time, and "supplier statements alone are not enough" (rule C2). A wrong claim can get the listing removed and misleads both the shopper and the AI assistant. So sort every statement you might write into one of four kinds:

| Kind | Examples | What to do |
|---|---|---|
| **Fact from the specs** | dimensions, weight, material type, number of pieces, colors, model, UPC, a care field such as "Product Care: Dishwasher Safe" | Use it, worded as the specs give it. |
| **Fact you derive** | 4 boards → "4-piece set"; 11.5 in → 29.2 cm; 3.2 oz → 91 g | Use it when the step is plain arithmetic or counting. Show the converted units in the attribute table. |
| **Claim that needs proof** | BPA-free, food-grade, non-toxic, PFAS-free, heat limits such as "up to 350°F", certifications, "Made in USA", eco-friendly or sustainable, antibacterial, "unbreakable" | Use it only if the specs state the proof exists, for example a test report or a certification. Otherwise leave it out of all customer text and mark it MISSING. |
| **Subjective marketing** | best, premium, perfect, must-have, chef-quality | Leave it out (rules T9, B8, C4). |

Vague performance words such as "heat resistant", "durable" or "scratch resistant" count as claims unless the specs give a number or a test. If the specs only say "Heat Resistant" with no temperature, don't write it. Put "Max temperature: MISSING" in the attribute table instead, because it is the first thing a shopper or an AI assistant asks.

**Conflicting data.** When two spec fields disagree (two different model numbers, "Number of Items 1" against "Unit Count 4", hand wash against dishwasher), don't choose. Keep that field out of the customer text, write CONFLICT and both values in the attribute table, and list it under "To check".

**Where MISSING goes.** MISSING and CONFLICT appear only in the attribute table, the Q&A answers and the "To check" list. Never put them in the title, bullets, description or search terms: Amazon prohibits placeholder text there (rule B9). In those parts, simply say nothing about the missing fact.

## Output

Write in US English and use exactly this structure, so that Elihome can compare products and paste each part into Seller Central:

```
# [Product name]: Amazon listing draft

## 1. Title ([n] characters)
[title]

## 2. Bullet points
1. [Header]: [text] ([n] characters)
2. ...
5. ...

## 3. Description
[text]

## 4. Backend search terms ([n] bytes)
[terms]

## 5. Attribute table
| Attribute | Value | Source |

## 6. Shopper Q&As
**Q1. [question]**
[answer]
...

## 7. To check before publishing
- [MISSING or CONFLICT item, and why it matters]
- [claim left out, the rule that requires proof, what proof would allow it]

## 8. Rule check
| Rule | Pass? | Note |
```

### 1. Title
- 75 characters at most, spaces included (T1). Count them and write the number in the heading.
- Order: Elihome, then series or style, product type, key attribute, color, size or pack count (T5, T7). A licensed partner that is part of the product (for example "Peanuts") is a fact, so it may stay.
- Numerals ("4-Piece", "2-Pack"); no word more than twice; capitalize each main word; no ! $ ? _ { } ^; no promotional or subjective words (T2, T3, T6, T8, T9, T10).
- For a product sold in several sizes or colors, write the title of the variation you were given (T12).

### 2. Bullet points
- Exactly 5 bullets, each formatted "Header: description" (B1, B3).
- Start with a capital letter. Write sentence fragments with no full stop at the end, and use semicolons inside a bullet. No all caps, no emojis or symbols such as ✔ ™ ®, no abbreviations such as "approx." (B4, B9).
- Write words out: "barbecue", not "BBQ"; "approximately", not "approx." (B9). Write numbers one to nine in words, except in measurements, model numbers and names. Put a space between number and unit ("10 in", "3.2 oz") (B5, B6).
- Each bullet adds new information: what it is and what's in the box (with the size of each piece for a set, B13), material, the key features, uses, and a last bullet with dimensions or a manufacturer warranty if the specs give one (X5).
- Amazon asks bullets to describe features **and benefits**: how the product meets the shopper's need (B7). So pair each fact with what it means for the shopper, as long as the benefit follows directly from the fact itself and promises nothing about performance. For example: "reversible" means "two cutting sides on each board"; "four sizes from 10 x 7 in to 16 x 12 in" means "a small board for fruit and cheese, a large one for meat"; "11.5 in long, 3.2 oz" means "small enough for a frying pan and a utensil drawer". Don't stretch it into a claim: "built-in groove" may become "a groove around the edge for juices", but not "keeps your counter spotless".
- A benefit must not suggest a feature the product doesn't have. "Keep raw meat on one board" promises food separation, which only works if the boards can be told apart (color coding, labels). Four boards of the same color don't support it, so say "four sizes for different jobs" instead. An AI shopping assistant will spot the gap and tell the shopper.
- For a set, give each piece's own size. Never put a dimension in customer text when the specs don't say what it measures: "Item dimensions 19 x 14 x 1 in" on a 4-board set is read as one board 1 in thick, when it may be the stacked set. Keep such a number in the attribute table, labelled as given, and add it to "To check".
- Aim for about 120 to 200 characters per bullet. A bullet with one bare fact ("Rectangular boards with a built-in groove") wastes a slot; merge it with a related fact or add the benefit.
- Care instructions (dishwasher safe, hand wash), material content and country of origin have their own Amazon fields, so they go in the attribute table and the Q&As, not the bullets or the description (B12, X4). This holds even when the specs state them, for example "Product Care: Dishwasher Safe": Amazon shows that field on the detail page, and AI assistants read it from there.
- Show each bullet's character count. The Home & Kitchen limit is not confirmed (B2), so keep each bullet under about 200 characters.

### 3. Description
- 80 to 150 words of plain text. No HTML; line breaks are fine (D1).
- Don't repeat the bullets in sentence form. The bullets list the facts; the description shows the product in use, for example who it suits, which tasks and how the pieces work together, using only facts from the specs. Leave model numbers, UPCs and spec lists to the attribute table.
- No price, availability, reviews, sales rank, links or time-sensitive words (D2, D5). The same claim rules apply as in the bullets, and care instructions stay out here too (X4).

### 4. Backend search terms
- Under 200 bytes, not counting spaces (K2, X1). Count them and write the number in the heading.
- Lowercase, separated by spaces, no punctuation, no repeated words, no words that are already in the title, no short words such as "and", "for" or "the" (K3–K6).
- Use synonyms, alternative names and uses ("chopping board", "spatula flipper", "pancake turner").
- Never use brand names (Elihome or any other, including licensed partners), ASINs, subjective or temporary words, or claim words such as "bpa free", "food grade" or "eco friendly" (K7, K8).

### 5. Attribute table
List every attribute in the specs, plus the fields AI assistants need (AI5), even when they are missing: material, number of pieces and what's included, dimensions in inches **and** centimeters, weight, max temperature, care / dishwasher safe, color, warranty, country of origin, model number, UPC/GTIN for this variant.
In the "Source" column write `spec: [field name]`, `derived`, `MISSING` or `CONFLICT: [both values]`.

### 6. Shopper Q&As
Write the five questions a shopper or an AI assistant is most likely to ask about this product, for example size, what's included, dishwasher, heat limit, material safety, and which pans or uses it suits. Answer each only from the specs. If the answer isn't in the specs, write "MISSING: [what Elihome needs to provide]" instead of guessing.

### 7. To check before publishing
List every MISSING and CONFLICT item, and every claim you left out with the rule behind it, for example: "'Made in USA' left out: needs to meet the FTC standard (C6), and country of origin is not in the specs". This is Elihome's to-do list before the listing goes live.
End the list with one line reminding Elihome to check the same facts on its other channels (its own site, Walmart, Wayfair and any other store). When a listing leaves a gap, AI shopping assistants fill it from those pages, and a different model number, size or price there undermines the listing (AI5).

### 8. Rule check
Check the draft against at least these rules and write pass or fail: T1 (title length), T3 (characters), T6 (repeated words), B1/B3 (5 bullets, header format), B9 (no symbols, all caps or placeholders), K2 (search terms under 200 bytes), K7 (no brands in search terms), C1 (no unproven claims anywhere in customer text). If something fails, fix the draft before you finish.

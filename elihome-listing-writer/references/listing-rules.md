# Listing rules for Elihome products on amazon.com

Marketplace: amazon.com (United States). All pages accessed 25 Nov 2026.
Every rule has an ID, the rule itself, and its source(s) in brackets. Sources are listed at the end with their tier:
A = official Amazon page, I = Elihome internal analysis (not an Amazon rule).
Where two Amazon pages disagree, the conflict is listed in section 9 with the choice this skill makes.

---

## 1. Title

| ID | Rule | Source |
|---|---|---|
| T1 | Maximum 75 characters, including spaces (all product types except media). | S1, S2 |
| T2 | No promotional phrases ("free shipping", "100% quality guaranteed"). | S1 |
| T3 | Never use these characters: ! $ ? _ { } ^ ¬ ¦. Use ~ # < > * only as identifiers or measurements ("Style #4301", "<10 lb"), never as decoration. | S1 |
| T4 | Use only standard letters and numbers; no non-language characters (Æ, Š, Œ). Necessary punctuation is fine: - / , & . | S1 |
| T5 | Include at least brand and product type ("Elihome Cutting Board"). | S1 |
| T6 | No word more than twice (articles, prepositions and conjunctions excepted; the brand name counts). | S1 |
| T7 | Order: brand, style, product type, key attribute, color, size or pack count, model number. | S1 |
| T8 | Write numbers as numerals ("2-Pack", not "Two-Pack"). Measurement abbreviations are fine ("in", "cm", "oz"). | S1 |
| T9 | No subjective commentary ("Hot Item", "Best Seller"). | S1 |
| T10 | Capitalize the first letter of each word except articles, prepositions and conjunctions; never all caps. | S1, S2 |
| T11 | No restricted phrases ("FSA/HSA eligible"); no price, availability, condition, links or contact details. | S1, S2 |
| T12 | Variations: size and color go in child titles only, not in the parent title. If the 75 characters can't hold every variating attribute, keep the most important in the title and move the rest to item highlights. | S1 |

## 2. Item highlights

| ID | Rule | Source |
|---|---|---|
| H1 | Up to 125 characters, including spaces; shown below the title in search results and on the detail page. | S1, S2 |
| H2 | Comma-separated phrases, not full sentences (for example materials, recommended use). | S1 |

## 3. Bullet points

| ID | Rule | Source |
|---|---|---|
| B1 | At least 3 bullet points; sellers can use up to 5. | S3 (min 3), S4 (up to 5) |
| B2 | Character limit varies by product type. The Home & Kitchen limit is not confirmed (it is in the category template, which needs a seller login), so report the length of each bullet. | S3, S4 |
| B3 | Format each bullet as "Header: description" ("Cotton fabric: Made from 100% cotton"). | S3 |
| B4 | Start with a capital letter; sentence fragment; no end punctuation; semicolons separate phrases inside a bullet. | S3 |
| B5 | Write numbers one to nine in words, except in names, model numbers and measurements. | S3 (see conflict X2) |
| B6 | Put a space between number and unit ("60 ml"). | S3 |
| B7 | Describe features, benefits and how the product meets customer needs; no brand stories. Each bullet adds new information; don't repeat the title or description. | S3 |
| B8 | No subjective, performance or comparative claims unless verifiable on the packaging; no award or survey claims without proof; no references to other products or competitor brands. | S3 |
| B9 | Prohibited in bullets: special characters (™ ® € … † ‡ ¢ £ ¥ © ± ~), emojis, **placeholder text ("N/A", "n/a", "not applicable", "TBD", "to be decided", "copy pending")**, ASINs, links, company or contact information, all caps, abbreviations ("qty", "pkg", "w/", "approx."). | S3 |
| B10 | Prohibited claims in bullets: "eco-friendly", "environmentally friendly", "ecologically friendly", "anti-microbial", "anti-bacterial", "made from bamboo", "contains bamboo", "made from soy", "contains soy". | S3 (see X3) |
| B11 | No refund guarantees ("Full refund", "If not satisfied, send it back"). | S3, S11 |
| B12 | Fabric content, care instructions and country of origin have dedicated fields: don't repeat them in bullets. | S3 (see X4) |
| B13 | For a set, list what is included and the size of each piece. | S4 (style guide example, secondary) |

## 4. Product description

| ID | Rule | Source |
|---|---|---|
| D1 | No HTML or other code, except line breaks (`</br>`). | S2 |
| D2 | No price, availability, condition, links, contact details, reviews, quotes, testimonials, requests for reviews, advertising or time-sensitive information. | S2 |
| D3 | Never all caps. | S2 |
| D4 | Accurate and not misleading; mention any additional item the product needs to work. | S2 |
| D5 | No claims about sales rank ("#1 Best Seller"). | S7 |

## 5. Backend search terms (Generic keyword field)

| ID | Rule | Source |
|---|---|---|
| K1 | Not visible to customers; used for matching search queries. Amazon may ignore some terms. | S5, S6 |
| K2 | Length: **under 200 bytes** (see conflict X1). Spaces and punctuation are not counted. For a–z and 0–9, 1 character = 1 byte; accented characters can take 2 or more. | S5, S6, S8 |
| K3 | Only generic words: synonyms, spelling variations, abbreviations. No common misspellings. | S5, S6 |
| K4 | All lowercase, separated by spaces, no punctuation. | S5, S6 |
| K5 | No repeated words; singular or plural, not both. | S5, S6 |
| K6 | No short words: a, an, and, by, for, of, the, with. | S6 |
| K7 | Never: the Elihome brand or any other brand, ASINs, profanity, temporary words (new, latest, on sale, limited time, today), subjective words (best, cheap, cheapest, amazing, effective, fastest, popular, trending). | S6 |
| K8 | Only terms that are true of the product. Claim words ("bpa free", "food grade", "eco friendly") follow the claim rules in section 7, even though Amazon's own cutting-board example uses them. | S5, S6 |

## 6. Attributes

| ID | Rule | Source |
|---|---|---|
| A1 | Attributes are specific facts that vary by product type: required, recommended, all. Fill as many as possible. | S8 |
| A2 | Complete and accurate attributes improve search filters and let Amazon's AI assistant give accurate answers. | S8 |
| A3 | The exact required and recommended attributes are in the category bulk listing template (seller login, template less than 90 days old). Not available to this skill: it uses the fields in section 8 plus what the current listing shows. | S8 |
| A4 | Drop-down attributes accept only Amazon's listed values; unit count = number + unit type ("12 count", "6 pack"). | S8 |
| A5 | Item type keyword: the most specific subcategory from the Browse Tree Guide, spelled exactly as listed. | S5 |
| A6 | Care instructions, fabric/material content and country of origin go in their own fields. | S3 |
| A7 | GTIN/UPC: only codes Elihome owns or is authorized to use (GS1); never false product IDs. | S2 |

## 7. Claims

A claim is any statement, explicit or implied, about what the product does, how it performs or what it is made of, anywhere on the page. [S9, S10]

| ID | Rule | Source |
|---|---|---|
| C1 | Every claim must be truthful and verifiable; Amazon can ask for proof at any time. If a claim can't be supported, leave it out. | S9, S10, S11 |
| C2 | Proof needed by claim type: **capacity** ("holds up to 500 lbs", "50-liter tank"), speed, efficiency and **ratings** ("IP67") need a test report from an ISO-certified lab; **certifications** ("NSF certified", "UL approved") need certification documents; **composition** ("BPA-free", "100% cotton") needs a lab test report; **purity and "free-from"** ("100% pure", "chemical-free") need a lab test or certification. **Supplier statements alone are not enough.** "PFAS-free", the example in the Elihome brief, is a free-from claim. | S10; example from the brief |
| C3 | Literal absolute claims ("unbreakable", "lasts forever", "never needs…") are never allowed. | S10 |
| C4 | Superlatives and comparisons ("best", "100% pure", "guaranteed", "twice as effective") only with objective proof. | S9 |
| C5 | Certifications ("FDA approved", "CE certified") must be real and documented. | S9 |
| C6 | "Made in [country]" only if made there, not just assembled; "Made in USA" must meet the FTC standard. | S9, S11 |
| C7 | Environmental claims ("eco-friendly", "green", "sustainable", "carbon-neutral") need evidence under the FTC Green Guides; "eco-friendly" is prohibited in bullets. | S3, S9, S11 |
| C8 | "Anti-microbial", "anti-bacterial", "anti-fungal" are pesticide claims (FIFRA) and appear in Amazon's disease-claim list: never use them. | S3, S9, S11 |
| C9 | Material claims ("made of bamboo", "leather") need proof. | S11 (see X3) |
| C10 | "Satisfaction guaranteed" / "money-back guarantee" commit the seller to full refunds for any reason. | S11 |
| C11 | Flatware follows the FTC Jewelry Guides: terms like "silver" and "noncorrosive" are regulated. | S11 |
| C12 | No disease or health claims. | S9 |

**Elihome rule for this skill:** a claim appears in customer-facing text only if the input says proof exists. Otherwise the field is marked MISSING in the internal tables, never in the title, bullets or description (placeholder text is prohibited there, B9).

## 8. What AI shopping assistants need

| ID | Rule | Source |
|---|---|---|
| AI1 | Amazon's AI assistant in the US store is **Alexa for Shopping** (Rufus and Alexa combined). | S12 |
| AI2 | For product questions such as "What are the dimensions?" or "Is this machine washable?", it **uses information from the product detail page**. Every common shopper question should be answerable from the listing. | S12 |
| AI3 | Complete and accurate attributes let the assistant give accurate answers. | S8 |
| AI4 | It shows price history (lowest Featured Offer price over 30, 90 or 365 days). | S12 |
| AI5 | Fields AI assistants need for Elihome kitchenware: GTIN on every variant (the same codes on Amazon, Walmart and Wayfair), material, dimensions in inches and cm, heat limit, dishwasher safety, warranty; prices consistent across channels. | S13 (I: Elihome analysis, not an Amazon rule) |

## 9. Conflicts and decisions

| ID | Issue | Choice in this skill |
|---|---|---|
| X1 | Search terms: S5 says under 250 bytes; S8 lists error 97779 at 200 bytes. S6 gives no number. | Use the stricter limit: under 200 bytes. |
| X2 | Numbers in bullets: S3 (general rule) says write one to nine in words; S4 (Consumer Electronics style guide) says always numerals. | Follow S3 in bullets; numerals in titles (S1). |
| X3 | Bamboo: S3 prohibits "made from bamboo" in bullets; S11 says material claims need proof. | Not relevant to the test set: none of the 3 products is bamboo. The general rule C9 still applies to every material claim. |
| X4 | Care instructions: S3 puts them in a dedicated field, not bullets; shoppers ask "is it dishwasher safe?" and the assistant answers from the detail page (S12). | Decided (Sara): care goes only in the attribute table (Amazon's care field) and the Q&As, not in the bullets or the description. |
| X5 | Warranty: S4 suggests warranty in the last bullet; S3 prohibits refund guarantees. | A manufacturer warranty stated in the input may go in the last bullet; refund guarantees never. |

## Sources

| # | Title | URL | Tier |
|---|---|---|---|
| S1 | Product title requirements and guidelines (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/GYTR6SYGFA5E3EQC | A |
| S2 | Product detail page rules (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/G200390640 | A |
| S3 | Product bullet point requirements (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/GX5L8BF8GLMML6CX | A |
| S4 | Feature Bullets, Consumer Electronics style guide (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/G200291790 | A (other category) |
| S5 | Search optimization (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/GNYWHX2TP7C8GXHK | A |
| S6 | Use search terms effectively (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/G23501 | A |
| S7 | Selling policies and seller code of conduct (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/G1801 | A |
| S8 | Attributes guide (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/GBWHYLJ7NNQMXBAQ | A |
| S9 | Misleading and prohibited claims (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/G202024200 | A |
| S10 | Misleading claims categories and resolution (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/GZ93G4JTAEVEJW62 | A |
| S11 | General Listing Restrictions (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/G201707070 | A |
| S12 | Alexa for Shopping (Seller Central, US) | https://sellercentral.amazon.com/help/hub/reference/external/GYYH9SLHSTHKT3CZ | A |
| S13 | Orsi, S. (2026) Shopify and AI shopping assistants: what it means for Elihome, 19 Nov 2026, section 6 | internal report, no link | I |

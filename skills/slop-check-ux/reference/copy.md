# Copy (UX)

Text tone, copywriting, message rules

- **Total canonical rules**: 16
- **Sub-categories**: 8

---

## Contents
- Clear notation — 3 canonical
- Labels and guidance copy — 4 canonical
- Conciseness — 2 canonical
- Intuitive symbols — 1 canonical
- Consistency and standards — 2 canonical
- Brand copy — 2 canonical
- Multilingual and localization — 1 canonical
- Empty state copy — 1 canonical

---

## Clear notation (3 canonical)

### [COPY-CLEAR-001] Use unambiguous date and time formats
- **Platform**: Mobile
- **Frequency weight**: 3
- **Sub-category**: Clear notation

**Principle**: Write date and time copy in unambiguous formats (e.g., 'October 16', '3:00 PM'). Avoid abbreviations and mixing of 24-hour and 12-hour formats.

**Why**: Ambiguous time notation leads to errors in critical decisions such as appointments, payments, and reservations.

**Anti-pattern**: Notations lacking context, such as '10.16' or '3 o'clock'.

---

### [COPY-CLEAR-002] Specify the billing cycle for subscription pricing
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Clear notation

**Principle**: Always specify the monthly or annual billing cycle for subscription service pricing.

**Why**: Without a cycle, new users may mistake the price for a one-time charge, damaging trust.

**Anti-pattern**: Showing only '78,100 KRW' leads users to mistake it for a one-time payment.

---

### [COPY-CLEAR-003] Prefer full expressions over abbreviations
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Clear notation

**Principle**: Use complete expressions like 'Men's Fashion' instead of 'Men' for navigation and category text.

**Why**: Abbreviations can be interpreted in multiple ways when context is lacking.

**Anti-pattern**: Category abbreviations like 'Men' or 'Women'.

---

## Labels and guidance copy (4 canonical)

### [COPY-LABEL-001] Pair non-intuitive icons with text labels
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Labels and guidance copy

**Principle**: Display text labels alongside non-intuitive function icons to improve recognizability.

**Why**: Text serves as a safety net for functions like reset or filter, where symbols are not yet standardized.

**Anti-pattern**: Showing a reset icon alone forces users to guess its function.

---

### [COPY-LABEL-002] Add supporting body copy to onboarding
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Labels and guidance copy

**Principle**: On onboarding and setup screens, add concise supporting copy beneath the title (selection limits, whether changes can be made later, etc.) to reduce user anxiety.

**Why**: Reducing psychological burden lowers drop-off rates.

**Anti-pattern**: Onboarding with only a title leaves users unsure of what to do or how to do it.

---

### [COPY-LABEL-003] Communicate password requirements upfront
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Labels and guidance copy

**Principle**: Display allowed password requirements (length, special characters, etc.) upfront on the input field to prevent errors.

**Why**: Informing users in advance has a lower UX cost than surfacing rules only after an error.

**Anti-pattern**: Revealing password requirements only after an error occurs.

---

### [COPY-LABEL-004] Reflect the actual format in placeholders
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Labels and guidance copy

**Principle**: Placeholder examples for fields like username and email must accurately reflect the actual accepted format (lowercase, allowed special characters, etc.).

**Why**: Incorrect examples create a flawed mental model for users.

**Anti-pattern**: Including uppercase letters or spaces in a username placeholder example.

---

## Conciseness (2 canonical)

### [COPY-CONCISE-001] Remove redundant words
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Conciseness

**Principle**: Keep only the words essential to meaning in UI copy, removing redundant expressions (verbs, particles, modifiers).

**Why**: Shorter copy reduces visual burden and improves readability and scan speed.

**Anti-pattern**: Verb and noun duplication, such as 'Visited. 3,600 people entered.'

---

### [COPY-CONCISE-002] Avoid unnecessary spacing
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Conciseness

**Principle**: Avoid unnecessary spacing or extra whitespace in UI copy. It makes text appear visually scattered and untidy.

**Why**: Mismatch between design intent and reader perception degrades readability.

**Anti-pattern**: Inserting spaces between characters without an emphasis purpose, such as 'U s e r  R e g i s t e r'.

---

## Intuitive symbols (1 canonical)

### [COPY-SYMBOL-001] Use '-' for discounts and '+' for rewards
- **Platform**: Mobile
- **Frequency weight**: 2
- **Sub-category**: Intuitive symbols

**Principle**: Explicitly mark discount amounts with '-' and reward amounts with '+'. Symbols are an intuitive device for conveying meaning quickly.

**Why**: Users can immediately recognize deductions and additions from the number alone, reducing cognitive load.

**Anti-pattern**: Using identical formats like 'Discount 25,000 KRW' and 'Reward 2,700 KRW' makes the direction unclear.

---

## Consistency and standards (2 canonical)

### [COPY-CONSIST-001] Unify synonyms
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Consistency and standards

**Principle**: Unify synonyms into a single term in UI text. Do not list the same meaning as two separate items using different words.

**Why**: Users assume that different words signify different meanings.

**Anti-pattern**: Listing 'Midweek' and 'Weekdays' as separate options confuses users.

---

### [COPY-CONSIST-002] Follow official guidelines
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Consistency and standards

**Principle**: For buttons that integrate with external platforms such as social login, follow the official copy guidelines provided by each platform.

**Why**: Maintains user trust and brand consistency while avoiding violations of terms or design guidelines.

**Anti-pattern**: Using arbitrary copy instead of the prescribed 'Start with Kakao'.

---

## Brand copy (2 canonical)

### [COPY-BRAND-001] Place the emphasized title last when listing roles
- **Platform**: PC
- **Frequency weight**: 1
- **Sub-category**: Brand copy

**Principle**: When listing multiple roles in a title, place the role you want to emphasize last. The final word leaves the strongest impression on the reader.

**Why**: In Korean word-order perception, the final word is read as the primary one.

**Anti-pattern**: Writing 'Designer Publisher' causes the reader to perceive the person primarily as a Publisher.

---

### [COPY-BRAND-002] Pair the logo with the brand name in text
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Brand copy

**Principle**: Display the brand name as text alongside the logo image to improve readability and recognition.

**Why**: New users or lesser-known brands are difficult to identify from a logo alone.

**Anti-pattern**: Showing a new brand's logo by itself, with no accompanying name.

---

## Multilingual and localization (1 canonical)

### [COPY-LOC-001] Pair each language with the user's current language
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Multilingual and localization

**Principle**: In the language settings list, pair each language with its name in the user's current language (or English) to improve readability.

**Why**: Showing only unfamiliar scripts prevents users from finding the language they want.

**Anti-pattern**: Showing only '日本語' or '中文' in a Korean-language app.

---

## Empty state copy (1 canonical)

### [COPY-EMPTY-001] Strengthen first impressions with emotive copy
- **Platform**: Mobile
- **Frequency weight**: 1
- **Sub-category**: Empty state copy

**Principle**: Add copy or visuals that convey the service's value or emotional tone on login and empty screens to strengthen the brand's first impression.

**Why**: Hollow empty screens lower trust; emotional resonance is a differentiator.

**Anti-pattern**: A login screen left bare with only input fields.

---

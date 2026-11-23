# Accessibility Audit Report — Before and After

## Website tested
- City Care Hospital Patient Appointment Management Website

## Before Refactoring

| Check | Result | Issue Identified |
|---|---|---|
| Page language | Fail | `lang` attribute was missing |
| Semantic structure | Fail | Excessive `div` elements were used |
| Heading hierarchy | Fail | `div` elements were used instead of proper headings |
| Landmark regions | Fail | `header`, `nav`, `main`, and `footer` were missing |
| Skip link | Fail | No skip-to-content link was available |
| Form labels | Fail | Form fields did not have associated labels |
| Input types | Fail | Email and phone fields used `type="text"` |
| Date field | Fail | Date field used `type="text"` instead of `type="date"` |
| Field grouping | Fail | No `fieldset` or `legend` was used |
| Required-field identification | Fail | Required fields were not marked |
| Keyboard navigation | Partial | Native links and inputs were present, but structure was unclear |
| Screen-reader experience | Fail | Landmarks, headings, and labels were missing |

## After Refactoring

| Check | Result | Improvement Made |
|---|---|---|
| Page language | Pass | `lang="en"` added |
| Semantic structure | Pass | `header`, `nav`, `main`, `section`, `article`, `aside`, and `footer` used |
| Heading hierarchy | Pass | One `h1`, followed by `h2` and `h3` headings |
| Landmark regions | Pass | Proper landmark regions added |
| Skip link | Pass | “Skip to main content” link added |
| Form labels | Pass | Every form control has an associated label |
| Input types | Pass | `type="email"` and `type="tel"` used |
| Date field | Pass | `type="date"` used |
| Field grouping | Pass | `fieldset` and `legend` used |
| Required-field identification | Pass | `required` and `aria-required` used |
| Keyboard navigation | Pass | Native HTML controls support keyboard access |
| Screen-reader experience | Pass | Landmarks, headings, labels, and helper text improve navigation |

## Screen-Reader Testing

| Test | Before | After |
|---|---|---|
| Page title announcement | Unclear | Clear and descriptive |
| Navigation landmarks | Not announced | Properly announced |
| Form field purpose | Not announced | Clearly announced using labels |
| Required fields | Not identified | Clearly identified |
| Error prevention | Limited | HTML validation and input types improve error prevention |

## WCAG Criteria Addressed
- 1.3.1 Info and Relationships
- 2.4.1 Bypass Blocks
- 2.4.6 Headings and Labels
- 3.3.1 Error Identification
- 3.3.2 Labels or Instructions
- 4.1.2 Name, Role, Value

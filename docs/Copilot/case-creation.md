# Case Creation Assistance

Case Creation Assistance is a Copilot-assisted workflow for creating a new PrintVis case by using patterns from prior cases. It extends standard **Case Management** and the **Advanced Case Card** with guided drafting support. It does not replace normal case entry or approval.

## Scope

- Help users describe a new case in natural language from the case card or advanced case card
- Reuse relevant patterns from cases created in the last 12 months
- Draft a new case with suggested header, job, and planning details
- Keep the user in control of review, edits, and final creation

## Historical Data Pipeline

The historical data pipeline should extract the last 12 months of cases and normalize the fields that are most useful for reusing prior work.

Recommended case and job data includes:

- Case number and status
- Sell-to and bill-to customer
- Order type and product group
- Case and job descriptions
- Requested shipment date and lead time
- Quantities, versions, page counts, and format sizes
- Component types, colors, sheets, and routing or list of units
- Estimated and quoted price values
- Archive, completion, and close indicators

The pipeline should:

- Exclude duplicates and merge repeated imports by source identifier
- Distinguish active, archived, cancelled, and closed cases
- Normalize text, dates, units of measure, product naming, and customer naming
- Keep the source snapshot so imported values can be audited later

## Database Model

Store the imported and generated data in separate but related structures so the process stays auditable.

Recommended logical entities:

- **Historical Cases** for imported case headers
- **Historical Jobs** for imported job and component details
- **Derived Features** for normalized values used by pattern recognition
- **Pattern Results** for scored similarity matches and reusable signals
- **Prompt Sessions** for user prompts and Copilot follow-up questions
- **Draft Cases** for proposed case headers, jobs, and field values
- **Approvals** for user review, edits, approval, or rejection actions

## Pattern Recognition

Pattern recognition should compare the new prompt with prior cases and rank the best matches. Useful signals include:

- Customer and customer segment
- Product group and order type
- Quantity bands and version structure
- Format size, page count, and component mix
- Routing, press or finishing patterns, and job-item structure
- Pricing tendencies and quoted ranges
- Requested shipment date patterns and typical lead times

The result should highlight which historical cases influenced the draft and how confident Copilot is in the recommendation.

## Chat on the Case Card

Users should have a Copilot chat option available from the standard case card and the advanced case card. In chat, the user can provide information such as:

- customer
- product
- quantity
- due date
- delivery constraints
- special production notes

## Drafting Workflow

1. The user opens Copilot from the case card or advanced case card.
2. The user describes the new case in natural language.
3. Copilot converts the prompt into structured case data.
4. Copilot searches the historical case data and derived features for similar work.
5. Copilot creates a draft case proposal with suggested jobs and core fields populated.
6. Copilot shows confidence and the historical patterns used to create the draft.

## Review and Approval

Draft cases should always require human review before creation. Users should be able to validate or change:

- customer assignment
- order type and product group
- pricing and contribution assumptions
- requested dates and scheduling details
- routing, materials, and production-critical values

Only after approval should the new case be created.

## Fallback for Low Confidence

If Copilot does not have enough information or the historical match is weak, it should stay in chat mode and ask follow-up questions instead of creating a draft immediately.

Typical follow-up areas include:

- missing customer details
- unclear product definition
- incomplete quantity or version information
- missing due date or delivery expectations
- conflicting production constraints

## Governance

The feature should follow the same control standards as other business-critical workflows.

Key governance areas include:

- permissions for who can use drafting, approve drafts, and create cases
- retention rules for imported data, prompts, and draft history
- audit logging for source cases, prompt sessions, edits, approvals, and creation events
- protection of customer-sensitive data used in prompts and pattern analysis

## Success Criteria

Success should be measured with operational and adoption metrics such as:

- ingestion completeness for the prior 12 months of case data
- quality of similarity matches
- draft accuracy for key case and job fields
- approval rate versus manual rework rate
- time saved compared with manual case creation

## See also

- [Case Management](../Pages/pvscasemanagement.md)
- [Advanced Case Card](../Legacy/Estimation/AdvancedCase.md)
- [Capacity Optimization](./capacity-optimization.md)

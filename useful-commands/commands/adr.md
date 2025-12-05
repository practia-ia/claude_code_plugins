---
description: Create an Architecture Decision Record (ADR)
---

# Create ADR

Create an Architecture Decision Record (ADR) in the project's `/docs/adrs` directory.

## Instructions

You are tasked with creating an ADR to document an architectural decision. Follow these steps:

1. **Ensure Directory Exists**

   - Check if `/docs/adrs` directory exists
   - If not, create it

2. **Determine ADR Number**

   - List existing ADR files in `/docs/adrs`
   - ADR files follow the pattern `NNNN-title-in-kebab-case.md` (e.g., `0001-use-postgresql.md`)
   - Calculate the next number (e.g., if `0003-*.md` is the highest, next is `0004`)
   - If no ADRs exist, start with `0001`

3. **Gather Information**

   Ask the user for the following information (if not already provided):
   - **Title**: Short descriptive title of the decision
   - **Context**: What is the issue that we're seeing that is motivating this decision?
   - **Decision**: What is the change that we're proposing and/or doing?
   - **Consequences**: What becomes easier or more difficult to do because of this change?

4. **Create ADR File**

   Create the file with the following template:

   ```markdown
   # [NNNN]. [Title]

   Date: [YYYY-MM-DD]

   ## Status

   Proposed

   ## Context

   [Context provided by user - describe the issue, forces at play, and why a decision is needed]

   ## Decision

   [Decision provided by user - describe what was decided and why]

   ## Consequences

   [Consequences provided by user - describe the resulting context, both positive and negative]

   ## Alternatives Considered

   [If provided, list alternatives that were considered and why they were not chosen]

   ## References

   [Optional: links to related documents, discussions, or resources]
   ```

5. **Output Result**

   - Show the path to the created ADR file
   - Display the ADR content
   - Suggest next steps (e.g., "Change status to 'Accepted' after team review")

## ADR Status Values

| Status | Description |
|--------|-------------|
| Proposed | Decision is proposed and under discussion |
| Accepted | Decision has been accepted and is in effect |
| Deprecated | Decision is no longer relevant |
| Superseded | Decision has been replaced by another ADR |

## Important Notes

- ADR numbers are zero-padded to 4 digits (0001, 0002, etc.)
- File names use kebab-case (lowercase with hyphens)
- The date should be the current date in ISO format (YYYY-MM-DD)
- Keep the Context, Decision, and Consequences sections focused and concise
- If the user provides partial information, ask for the missing pieces before creating the ADR

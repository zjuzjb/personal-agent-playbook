# Model Routing Rules

Use model strength according to risk, ambiguity, and cost.

## Raise Strength

Use a stronger model or higher reasoning when:

- Product direction is ambiguous.
- Architecture or data correctness is central.
- A wrong result could corrupt user trust, data, money, or workflow.
- UI quality depends on taste and information hierarchy.
- The task spans multiple modules or unknown failure modes.

## Lower Strength

Use a smaller or faster model when:

- The task is explicit, local, reversible, and easy to test.
- The work is mechanical.
- The branch owner has a narrow brief and no product judgment.

## Reviewer Routing

- Low risk: reviewer can usually be skipped with a recorded reason.
- Medium risk: reviewer recommended.
- High risk: reviewer mandatory before human final approval.

High risk includes financial data, metric calculation, valuation, investment
conclusions, data pipelines, auth, permissions, secrets, migrations, production
config, CI/CD, and broad architecture changes.


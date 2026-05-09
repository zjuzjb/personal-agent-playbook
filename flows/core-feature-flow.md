# Core Feature Flow

Use for important product, architecture, data, or workflow changes.

1. Clarify the user problem and why the existing system is insufficient.
2. Define durable objects, ownership boundaries, and acceptance criteria.
3. Run product, engineering, and design review as relevant.
4. Split execution into bounded workstreams if it improves quality or isolation.
5. Require stronger verification than a normal feature.
6. Run Completion Gate in the main thread.
7. Run mandatory Risk Gate for high-risk changes.
8. Update docs when behavior, commands, architecture, or operating rules change.
9. Stop for human acceptance before merge when the project requires it.


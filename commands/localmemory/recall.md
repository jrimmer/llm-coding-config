# /recall
https://www.localmemory.co/prompts/

1. Accept: UUID, tag, or query
2. Search: UUID → `get_memory_by_id` | tag/text → `search` (use_ai=true, limit=5)
3. Retrieve content + metadata
4. Reconstruct: parse all sections
5. Present with metadata
6. Load into active conversation
7. Ready to continue

**Output:**
```
## Memory Recalled

**Context Restored From:** [identifier]
**Memory ID:** [UUID]
**Original Date:** [date]

**Core Understanding:** [main context]
**Conversation Evolution:** [changes]
**Key Decisions:** [decision + rationale]
**Specifications/Artifacts:** [detailed outputs, specs]
**Important Points:** [critical elements]
**User Context:** [why matters, broader work, use case]
**Related Systems:** [integrations, dependencies]
**Context & Constraints:** [boundaries]

---
**Status:** Complete context loaded. Operating with full understanding.
Ready to continue. What would you like to work on?
```

**If not found:**
```
## Memory Not Found

No memory matching: [identifier]
Try different keywords or check ID/tag.
```

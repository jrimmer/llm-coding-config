# /memorize
# https://www.localmemory.co/prompts/

1. Analyze conversation: core understanding, key decisions, points, evolution, specs/artifacts, user context, related systems, constraints
2. Search local-memory: semantic search, similarity >0.7 = related
3. Determine: UPDATE if related + same topic | CREATE NEW otherwise
4. Tag: `topic_context_year` format, lowercase + underscores
5. Structure: Core Understanding, Conversation Evolution, Key Decisions, Specifications/Artifacts, Important Points, User Context, Related Systems, Context & Constraints
6. Save: `store_memory` (new) or `update_memory` (existing), importance 7-9, tags array, domain
7. Return: UUID, tag, action

**Output:**
```
## Memory Saved

**Retrieval:**
- **Memory ID:** [UUID]
- **Tag:** [tag]
- **Action:** [Created new | Updated [uuid]]

Use `/recall [id]` or `/recall [tag]` to restore.
```

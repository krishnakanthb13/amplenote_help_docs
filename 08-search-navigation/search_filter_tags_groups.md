# Search queries: tag filters & other searchable symbols

> [← Help Index](../00-index.md) · Category: [Search, Lookup & Navigation](./index.md) · [Source ↗](https://www.amplenote.com/help/search_filter_tags_groups)

## Filtering by keywords

By default, full search matches similar words. You can now use double quotes and advanced keywords for more granular filtering on desktop and mobile.

| Query | Result | Explanation |
|-------|--------|-------------|
| `apple` | Matches "apple," "apples," "application," and similar words | No modifiers = many similar matches |
| `"apple"` | Only exact word "apple" | Double quotes restrict to exact matches |
| `"apple" AND "orange"` | Both words present | AND operator applies to neighboring keywords |
| `"apple" OR "orange"` | Either word present | OR operator applies to neighboring keywords |
| `"apple" NOT "orange"` | Has "apple" but excludes "orange" | NOT operator applies to neighboring keywords |
| `"apple and orange"` | Exact phrase match | Operators inside quotes don't function |
| `"apple" AND "orange" OR "Jim"` | (apple AND orange) OR Jim | AND executes first |
| `"Jim" OR "apple" AND "orange"` | Same as above | Operator precedence |
| `"apple" AND ("orange" OR "Jim")` | (apple AND orange) OR (apple AND Jim) | Parentheses override default order |

**Important:** Keywords must be CAPITALIZED for proper function.

## Filtering by tags

Tag filtering works in Jots Mode, Notes Mode, Quick Open, and Tasks Mode.

### Search query syntax for filtering by tags

- **Single tag:** `in: my-tag-name`
- **Child tags:** `in: my-parent-tag/my-child-tag`
- **All subtags:** `in: my-parent-tag/`
- **Multiple tags:** `in: my-first-tag,my-second-tag`
- **Combined with search:** `in: my-tag-name My search keyword`
- **Exclude tag:** `in: ^daily-jots`
- **Exclude from list:** `in: ^daily-jots,work`
- **Exclude subtags:** `in: my-parent-tag,^my-parent-tag/`
- **Complex filtering:** `in: ^daily-jots,work My search keyword`

## Filtering by categories (group queries)

Category-based filtering works in Notes Mode and Quick Open.

### General purpose queries

| Option | Syntax | Description |
|--------|--------|-------------|
| Archived | `group: archived` | Archived or auto-archived notes |
| Task Lists | `group: taskLists` | Notes containing tasks |
| Un-tagged | `group: untagged` | Notes without tags |
| Vault Notes | `group: vault` | Encrypted notes |
| Deleted Notes | `group: deleted` | Notes deleted in past 30 days |
| Active plugin notes | `group: plugin` | Currently active plugin notes |

### Queries on shared notes

| Option | Syntax | Description |
|--------|--------|-------------|
| Created by me | `group: created` | Notes created by current user |
| Shared publicly | `group: public` | Published to web via public URL |
| Shared notes | `group: shared` | Created by anyone, shared with others |
| Notes shared with me | `group: shareReceived` or `group: notCreated` | Created by others, shared with current user |
| Notes I shared with others | `group: shareSent` | Created by user and shared with others |

### Queries on note creation & update date

| Option | Syntax | Description |
|--------|--------|-------------|
| This week | `group: thisWeek` | Updated in previous 7 days |
| Today | `group: today` | Edited in current day |

### Advanced & low-level queries

| Option | Syntax | Description |
|--------|--------|-------------|
| Notes Saving | `group: saving` | Pending changes to push to server |
| Notes Downloading | `group: stale` | Pending changes to pull from server |
| Notes Indexing | `group: indexing` | Currently being indexed for search |

### Combining group queries

Separate keywords with commas for AND logic:
`group: untagged,taskLists`

### Combining group and in queries

`in: amplenote group: notCreated` — notes with "amplenote" tag shared with you

`in: ^daily-jots group: taskLists,archived` — archived notes with tasks, excluding "daily-jots" tag

## Creating links to searches

### Links to searches in Notes Mode

**Word searches:** `https://www.amplenote.com/notes?query=word`

- Spaces become `%20`
- Example: `https://www.amplenote.com/notes?query=multiple%20words`

**Tag filters:** `https://www.amplenote.com/notes?tag=my-tag-name`

- Nested tags use `%2F`: `https://www.amplenote.com/notes?tag=my-tag-name%2Fmy-subtag`
- Multiple tags use `%2C`: `https://www.amplenote.com/notes?tag=my-tag-name%2Cmy-other-tag-name`

**Note groups:** `https://www.amplenote.com/notes?group=archived`

**Mixed searches:** Use `&` separator

- `https://www.amplenote.com/notes?group=archived&query=word`
- `https://www.amplenote.com/notes?group=shared&query=word&tag=my-tag-name`

### Searches in Tasks Mode

**Tag filters:** `https://www.amplenote.com/notes/tasks?tag=my-tag-name`

**Note Reference filters:** `https://www.amplenote.com/notes/tasks?references=91ec67d6-2ff9-11eb-8515-fea7a2498118`

- Exclude reference: `https://www.amplenote.com/notes/tasks?references=%5E91ec67d6-2ff9-11eb-8515-fea7a2498118`
- Multiple references use `%2C`

**Mixed searches:** `https://www.amplenote.com/notes/tasks?references=1fd27a46-d593-11ec-b49c-56e83c2ff761&tag=my-tag-name`

### Searches in Calendar Mode

Only `references=` parameter available: `https://www.amplenote.com/calendar?references=<note-uuid>`

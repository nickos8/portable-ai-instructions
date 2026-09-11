# Changelog

Record meaningful changes so you can understand or reverse them later.

## 1.5.0 - 2026-09-11

### Changed

- Concrete examples must now come from the actual open/attached project's real classes, files, and names when one is available. If no matching real example exists, or no project is attached, the example must be labeled plainly as generic
- Applied to Master Instructions sections 2 and 9, the Teaching and Review module, and the Quick Start prompt

### Reason

- A real test invented a `Student`/`Grade` example while teaching Eloquent relationships inside a project that has neither, and presented it without flagging it as generic. This is confusing to tell apart from forgotten project code and must never happen unlabeled.

## 1.4.1 - 2026-09-11

### Changed

- Removed emoji from the required output template's section labels and from the section 3 priority labels; both now use plain bold text

### Reason

- User preference after testing the template in a real chat

## 1.4.0 - 2026-09-11

### Added

- Required output template for the Feynman loop in Master Instructions section 2: labeled `📘 Simple explanation`, `🎯 Why it matters`, `🔄 Cause -> Process -> Result`, `💡 Example`, `🗣️ Your turn` sections, plus labeled diagnosis/repair/confirm responses
- Same labeled template referenced in the Teaching and Review module and folded into the Quick Start prompt

### Reason

- A real test run showed lessons rendering as one long block of bold text with no visual separation between Feynman steps. Labeled sections make each step scannable at a glance instead of requiring the reader to parse paragraph breaks.

## 1.3.0 - 2026-09-11

### Changed

- Marked the Feynman teaching method (section 2) and ADHD-friendly delivery (section 3) in Master Instructions, the Teaching and Review module, and the Quick Start prompt as mandatory rather than optional style preferences

### Reason

- This teaching style is confirmed to work; prevent an assistant from quietly skipping, shortening, or merging steps to save time or because a topic seems simple

## 1.2.0 - 2026-09-07

### Added

- Usage and session efficiency section in Master Instructions (section 20)

### Reason

- Reduce wasted messages: finish a full step in one message, batch independent tool calls and clarifying questions, cut filler, use available files/tools directly instead of asking the user to fetch them, and skip confirmation on low-stakes reversible actions. This governs overhead only; the one-concept-at-a-time teaching pace in section 3 still applies during real teaching.

## 1.1.0 - 2026-08-20

### Added

- Learning documentation module
- Topic-based learning knowledge base
- Session note structure
- Mastery tracker
- Reusable learning entry template

### Changed

- Master and quick-start instructions now require teach-back before recording confirmed learning
- README now explains how to use the learning system

### Reason

- Keep durable learning portable, searchable, verifiable, and reusable across AI accounts and projects

## 1.0.0 - 2026-08-20

### Added

- Master portable AI instructions
- Short custom-instruction prompt
- Teaching and review module
- Coding and project module
- Career support module
- Communication style module
- Security checklist
- Project context template
- Session handoff template

## Future entry template

```text
## X.Y.Z - YYYY-MM-DD

### Added
- ...

### Changed
- ...

### Removed
- ...

### Reason
- ...
```


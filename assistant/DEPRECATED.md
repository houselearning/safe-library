# SafeAI Assistant Files - DEPRECATED

**Status:** This directory is no longer in active use.

## Migration to HouseLearning-home

As of 2026-09-13, SafeAI has been consolidated to use the canonical source from the HouseLearning-home repository.

**Why?**
- Eliminate code duplication
- Single source of truth for SafeAI logic
- Easier maintenance and version management
- Consistent experience across both platforms

## Current Architecture

SafeLibrary pages now reference:
```html
<script src="/assistant/assistant.js"></script>
```

Which resolves to:
```
https://houselearning.org/assistant/assistant.js
```

The local `assistant/` folder files in this repository are **no longer loaded** by SafeLibrary pages.

## For Developers

If you need to modify SafeAI behavior:
1. **For HouseLearning-home only:** Edit `/Volumes/Other Storage/GitHub Projects/houselearning-home/assistant/*`
2. **For both platforms:** Edit files in `houselearning-home/assistant/` only
3. **Do NOT edit files in this directory** - they will be removed in a future cleanup

## Version Info
- **HouseLearning-home assistant version:** 1.1.4
- **SafeLibrary assistant status:** Using remote v1.1.4 from HouseLearning-home
- **Last consolidation:** 2026-09-13

## Next Steps
- [ ] Archive/delete this directory after confirming no broken links
- [ ] Update deploy scripts to skip copying assistant files to SafeLibrary

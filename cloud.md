# Obsidian Knowledge Base Configuration
## Progressive Learning Philosophy

### Front Matter Properties
Each note should include these properties:
```yaml
---
difficulty: beginner|intermediate|advanced
prerequisites: ["concept1", "concept2"]
learning_objectives: ["objective1", "objective2"]
tags: ["topic", "category"]
last_reviewed: YYYY-MM-DD
confidence: 1-5
connections: ["related-note1", "related-note2"]
---
```

### Node Creation Strategy
1. **Start Simple**: Begin with fundamental concepts before complex ones
2. **Build Dependencies**: Always create prerequisite nodes first
3. **Link Intentionally**: Every note should connect to at least 2 others
4. **Test Understanding**: Include practice questions or examples

### Linking Guidelines
- Use `[[double brackets]]` for internal links
- Create forward links to advanced topics: "Next: [[Advanced Concept]]"
- Create backward links to prerequisites: "Requires: [[Basic Concept]]"
- Add contextual links within content, not just at the end

### Teaching-Focused Content Structure
```markdown
## Core Concept
Brief, clear explanation of the main idea

## Why It Matters
Real-world relevance and motivation

## Step-by-Step
Progressive breakdown with examples

## Common Mistakes
What learners typically struggle with

## Practice
Immediate application opportunities

## Next Steps
Clear path forward: [[Related Topic]]
```

### Content Guidelines
- **Teach, Don't Document**: Focus on understanding over completeness
- **Progressive Disclosure**: Introduce complexity gradually
- **Active Learning**: Include exercises and reflection prompts
- **Spaced Repetition**: Reference earlier concepts regularly
- **Visual Learning**: Use diagrams and code examples liberally

### Node Relationship Types
- **Prerequisites**: `requires::`
- **Next Steps**: `leads-to::`
- **Related**: `connects-to::`
- **Examples**: `demonstrated-in::`
- **Practice**: `applied-in::`
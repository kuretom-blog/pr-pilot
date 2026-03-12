# my-first-plugin

Claude Code plugin that provides automated PR review suggestions.

## Features

The `/review` skill analyzes diffs or code snippets from three perspectives:

- **Readability** - naming, structure, clarity improvements
- **Performance** - inefficiencies, unnecessary allocations, algorithmic concerns
- **Security** - potential vulnerabilities, unsafe patterns

## Installation

```bash
claude plugin add /path/to/my-first-plugin
```

Or install from GitHub:

```bash
claude plugin add kuretom-blog/my-first-plugin
```

## Usage

```
/review <diff or code snippet>
```

### Arguments

| Argument   | Required | Description              |
|------------|----------|--------------------------|
| `diff`     | Yes      | Diff text or code to review |
| `language` | No       | Language hint (auto-detected if omitted) |

### Examples

Review a git diff:

```
/review $(git diff HEAD~1)
```

Review a code snippet with language specified:

```
/review language:python def foo(): pass
```

## Project Structure

```
.claude-plugin/
  plugin.json        # Plugin metadata
skills/
  review/
    SKILL.md         # Review skill definition
```

## License

MIT License. See [LICENSE](LICENSE) for details.

## Author

kuretom

# CTDPTool

A minimalist command line tool based on the focus method [**CTDP Protocol** by \@edmond](https://www.zhihu.com/question/19888447/answer/1930799480401293785)

Site: <https://ittekngxrokdzxrok.github.io/ctdptool>

### Quick Start

### Commands

| Command | Description |
|-------|-------|
| !sign [minutes] [task] | Start a "Sign" countdown (default: 20 minutes) |
| !seat [minutes] [task] | Start a "Seat" countdown (default: 45 minutes; requires an active "Sign" session) |
| !stop | Stop the countdown and initiate the reset process |
| !clear | Clear the screen output |
| !import | Import JSON data (requires confirmation to overwrite existing data) |
| !export chat | Export command history as a .txt file |
| !export json | Export data as a JSON file |
| !dogoitagain | Append a rule with a timestamp |

### Workflow

- "Sign" ends → Prompt for a new name for the "Flare pistol"; archive the previous record.
- "Seat" ends → Prompt to confirm task completion (y/n)
    - 'y' archives the record and increments the counter;
    - 'n' triggers a reset of the main sequence.

### Data Format

```json
{
"signname": "string", "seatname": "string", "number": 1,
"task": "string", "archive": "string", "rule": "string",
"signStart": "YYYY-MM-DD", "seatStart": "YYYY-MM-DD"
}
```

### Known Issues

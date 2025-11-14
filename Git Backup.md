Add this to your `.git/config` file:

```
[alias]
        backup = "!git add -A && git commit -m \"Backup - $(date '+%B %d, %Y at %-I:%M %p')\" && git push"
```

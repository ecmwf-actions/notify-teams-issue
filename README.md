> [!CAUTION]
> This repository was moved to https://github.com/ecmwf/notify-teams-issue. Do not update!
> 
# Notify Teams - New Issue

A GitHub Action that notifies of a new Issue via Microsoft Teams.

See `action.yml` for required inputs.

## Usage

Create a file `.github/workflows/notify-new-issue.yml`

```
name: Notify new issue

on:
  issues:
    types:
      - "opened"

jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      - name: Notify new issue
        uses: ecmwf-actions/notify-teams-issue@v1
        with:
          incoming_webhook: ${{ secrets.MS_TEAMS_INCOMING_WEBHOOK }}
```

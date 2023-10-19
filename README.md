The raw markdown notes for my til website (TODO add link)

> Note: Image files aren't included here so viewing notes in the git repo will be incomplete. 

### TODOs
- [ ] script/hook for build upon push to main
- [ ] warning for wikilinks

## Usage notes to future me:

**`Obsidian-Git` Plugin Notes**
Usage: ① Run `Commit all changes` then ② Run `Push` 

## First Time Setup

### Obsidian Setups
- set default attachment location
- set default links to markdown
- plugins: 
	- Templater
	- Obsidian Git

### Template
The template isn't included in the remote so it doesn't copy over to the Hugo site. I place this file in the `Templates` folder (e.g. `Templates/t-til.md`). This uses the Templater plugin to create a new post with the correct frontmatter used by hugo.

```
---
title: <% tp.file.title %>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
description: 
tags: 
math: false
---
```
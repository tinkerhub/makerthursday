---
title: 'How to Document a Maker Thursday Session'
date: 2026-01-13
pin: true
authors: [salman]
slug: how-to-document
description: >
  Guide on how to document a maker thursday journal.
---

Maker Thursday is a weekly, community driven gathering at TinkerSpace where people connect, share, and build.

From 2026 onwards, every session should have a short journal entry, usually written by the host.

# Why we document Maker Thursday

Maker Thursday is a weekly community gathering, but the conversations, demos, and learnings should not end when the session ends.

By documenting each Maker Thursday, we:

- Keep a clear log of what was discussed and built
- Help members who could not attend stay updated
- Make it easy for new members to understand the community’s direction
- Create a shared reference for ideas, projects, and follow ups
- Build a long term archive of our maker journey

These short journal entries are not meant to be detailed reports. They are lightweight snapshots of each session, written so that any community member can quickly read, catch up, and continue the conversation.

## Documentation steps

1. Set up MkDocs Material on your computer
2. Run the site locally
3. Add a new journal post using the template
4. Push changes and raise a pull request

---

### Setup on your computer

First, you need setup the computer to run the `mkdocs` locally.

#### Prerequisites

- Install Python and pip - follow the guide [here](https://www.python.org/downloads/)
- Install MkDocs  - follow the guide [here](https://squidfunk.github.io/mkdocs-material/getting-started/).
- Install Git - follow the guide [here](https://git-scm.com/install/)

---

### Fork, clone, and run locally

1) Fork the repository

- Open the upstream repository: [tinkerhub/makerthursday](https://github.com/tinkerhub/makerthursday)
- Click Fork (creates your copy under your GitHub account)

2) Clone your fork

```
git clone https://github.com/<your-username>/makerthursday.git
cd makerthursday
```

3) Start the local dev server

Run this from the folder that contains `mkdocs.yml`:

```
mkdocs serve
```

MkDocs will serve the site locally (usually on `http://127.0.0.1:8000/`)

---

### Create a new Maker Thursday journal entry

The site journal is powered by the Material blog feature (you can see it live at [/blog/](https://github.com/tinkerhub/makerthursday/tree/main/docs/blog))

1) Create a new branch

```
git checkout -b add-makerthursday-journal-YYYY-MM-DD
```

2) Add a new post file

Follow the existing pattern in the repository for where posts live.

- `docs/blog/posts/YYYY-MM-DD-title.md`

3) Add front matter

Add metadata for your Journal post,

```
---
title: 'MakerThursday 0xXX: Name for the Maker Thursday'
date: YYYY-MM-DD
authors: [autor]
slug: maker-thursday-0xXX
description: >
  A Small Description
---
```

If this is your first time contributing, please add your details to the authors file before submitting your post.

open the file `docs/blog/authors.yml` and add new entry

```
  author-username:
    name: Author Full Name
    description: Author tag line
    avatar: https://avatars.githubusercontent.com/u/xxxxxxxx
    url: Tinkerhub App profile URL

```

In the avatar section, replace the `xxxxxxx` to your github profile id.

---

### Journal template (copy paste)

Use this template inside your post:

```
---
title: 'MakerThursday 0xXX: Name for the Maker Thursday'
date: YYYY-MM-DD
authors: [autor]
slug: maker-thursday-0xXX
description: >
  A Small Description
---

## Overview
Write 3 to 6 lines on what happened this week. Mention the theme and the general vibe.

## Topics
- Topic 1
- Topic 2
- Topic 3

## Project Presentation
- Name – project title (one line summary if needed)
- Name – project title

## Photos
### Group photo
![Group photo](../assets/YYYY-MM-DD-title/group-photo.jpg)

### Activity photo
![Activity photo](../assets/YYYY-MM-DD-title/activity-photo.jpg)

## Highlights
- One key takeaway (learning, decision, win, or community moment)

## Next Week
- Topic: TBD
- Host: TBD

```

#### Notes for photos:

- Keep filenames simple and consistent.
- Store images in the same place the repo already uses for images.
- Always add meaningful alt text.

---

### Preview your changes

While mkdocs serve is running, open the local site and check:

- The post appears in the journal list.
- Images load.
- Headings look correct and spacing is clean.

---

### Commit, push, and open a pull request

1) Commit and push to your fork

```
git add .
git commit -m "Add Maker Thursday journal for YYYY-MM-DD"
git push -u origin add-makerthursday-journal-YYYY-MM-DD
```

2) Create a pull request to upstream

On GitHub, open your fork and you should see a prompt to create a PR. GitHub’s flow for PRs from forks is documented here

PR checklist:

- Title includes the date and session name.
- Post follows the minimum structure.
- Photos included or clearly marked pending.
- Previewed locally.

---

Suggested style (keep it consistent)

- Prefer short paragraphs and bullet lists.
- Avoid long intros.
- Name people and projects clearly (credit matters).
- If something is TBD, write “TBD” instead of leaving it blank.

---








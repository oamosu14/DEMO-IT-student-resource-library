# Contributing Guide

Thanks for helping improve the Resource Library!

## Ways to Contribute
- Add or improve **lab guides** (Linux, Networking, Cybersecurity, Windows/AD)
- Add **study notes** or practice questions to certifications folders
- Fix broken links, typos, formatting

## Workflow
1. **Fork** this repository and create a feature branch:  
   `git checkout -b feat/<topic>-<short-desc>`
2. Make your changes and **preview** markdown locally.
3. **Commit** with a clear message:  
   `git commit -m "labs: add nginx+ufw+ssl self-signed walkthrough"`
4. **Push** and open a **Pull Request**.
5. A maintainer will review. Please be responsive to feedback.

## Lab Template
Copy this header into new labs:

```
# <Lab Title>
**Estimated time:** <e.g., 45 min>  
**Prereqs:** <VM/OS, tools>  
**Objective:** <what you’ll achieve>

## Steps
1) ...
2) ...
3) ...

## Validation
- ...
- ...

## Cleanup
- ...
```

## Content Guidelines
- Favor **short, step-by-step** instructions with copy‑paste commands.
- Call out **prereqs, risks, and cleanup**.
- Keep security labs **legal and ethical** (see `SECURITY.md`).

## Code of Conduct
Be kind, be helpful. See `CODE_OF_CONDUCT.md`.

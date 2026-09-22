# The DevForge Workbook

This is where the **10 PR Journey** starts. Milestone 1 is to open a pull request here that signs the workbook: you add one file with your name on it.

Your first PR goes to us, not to a stranger. If something goes wrong, it costs a teammate five minutes, not a maintainer's afternoon.

📖 The full journey, all ten milestones: **https://www.devforge.club/workbook**

---

## What you'll do

You'll create **one new file**, `signatures/<your-github-username>.md`, and open a pull request to add it.

Each person gets their own file, so a whole batch can sign on the same evening without anyone hitting a merge conflict.

## Step by step

### 1. Fork this repository

Click **Fork** at the top right of this page. That gives you your own copy at `github.com/<you>/workbook`.

### 2. Clone *your fork*, not this repo

```bash
git clone https://github.com/<your-github-username>/workbook.git
cd workbook
```

### 3. Make a branch before you touch anything

```bash
git checkout -b sign/<your-github-username>
```

> ⚠️ **The #1 mistake:** committing on `main`. If your PR ends up showing other people's files, close it, make a fresh branch from an up-to-date `main`, and start again.

### 4. Create your signature file

Copy the template and rename it to your **exact** GitHub username. Letter case matters.

```bash
cp signatures/_template.md signatures/<your-github-username>.md
```

Then open it and fill it in:

```markdown
# Your Name

- **GitHub:** @your-github-username
- **Batch:** 2026
- **I'm here to:** one honest line about what you want from open source
- **One thing I've built:** a link, or "nothing yet" — both are fine
```

The two things most people get wrong:

- **`# Your Name` is a placeholder.** Replace *Your Name* with your real name and keep the `# `, for example `# Asha Rao`.
- **Keep the `@`.** The line must read `- **GitHub:** @your-username`, exactly as shown. The automated check reads it.

### 5. Commit and push

```bash
git add signatures/<your-github-username>.md
git commit -m "Sign the workbook: <your name>"
git push -u origin sign/<your-github-username>
```

### 6. Open the pull request

Go to your fork on GitHub and click **Compare & pull request**. Check that:

- **base repository:** `NST-DEVFORGE/workbook` · **base:** `main`
- **head repository:** `<you>/workbook` · **compare:** `sign/<your-github-username>`
- the **Files changed** tab shows **exactly one file**

Fill in the PR template and open the PR.

### 7. Wait for the checks and a review

- An automated check (**Validate signature**) runs on every PR. If it fails, open the check's log. It tells you exactly what to fix.
- A governance council member is requested as reviewer automatically. You can also post your PR link in the club group.

### 8. Respond to the review on the *same* PR

Make the requested changes on the same branch, then commit and push. The PR updates by itself.

```bash
git add .
git commit -m "Address review"
git push
```

> ⚠️ Do **not** close the PR and open a new one. Pushing a follow-up commit is part of what this milestone teaches.

### 9. Merged? Log it on the portal

Copy your PR URL (`https://github.com/NST-DEVFORGE/workbook/pull/<number>`), paste it into **Milestone 1** on the workbook page, and write your reflection. The portal checks the PR against GitHub before recording it.

---

## Done when

- [ ] You worked on a branch, not on `main`, and your PR shows **one file changed**
- [ ] The **Validate signature** check is green
- [ ] A senior member left at least one review comment
- [ ] You pushed a follow-up commit that addressed it (not a new PR)
- [ ] Merged

## Rules for this repo

- **Only add your own file.** Don't edit anyone else's signature, this README, or the template.
- **One PR per person.** If you get stuck, ask in the club group. Don't open a second PR.
- **Be yourself.** "Nothing yet" is a perfectly good answer. Nobody here is grading your CV.

## Stuck?

| Problem | Fix |
| --- | --- |
| PR shows lots of files | You committed on `main`. Sync your fork, `git checkout -b` a new branch from `main`, re-add your file, open a new PR, and close the old one. |
| Check says the filename is wrong | The filename must be your GitHub username exactly, in `signatures/`, ending in `.md`. |
| Check says the GitHub line is wrong | It must read `- **GitHub:** @<your username>`, matching the account that opened the PR. |
| `git push` asks for a password | GitHub no longer accepts passwords here. Use [GitHub CLI](https://cli.github.com/) (`gh auth login`) or a personal access token. |
| Your fork is behind `main` | Click **Sync fork** on your fork's GitHub page, then `git pull` on `main` locally. |

---

Maintained by [DevForge](https://github.com/NST-DEVFORGE). Reviews come from senior members of the club.

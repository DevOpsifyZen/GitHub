# GitHub Issues & Projects

## Prerequisites

* GitHub account with repository access.
* Basic familiarity with GitHub UI.
* Sample repository (e.g., lab-demo).

---

### Step 1: Create Issues

#### Goal: Create 4 issues representing features/bugs and practice adding labels, assignees, and milestones.

1. Open your repository (e.g., `your-username/lab-demo`).
2. Click **Issues** in the repo menu.
3. Click **New issue**.
4. Create the following issues:
* **Feature: Add user login** — describe acceptance criteria.
* **Bug: Signup form shows 500 error** — list steps to reproduce.
* **Chore: Update dependencies** — list packages to update.
* **Docs: Add README usage examples** — sample commands.
5. Add for each issue:
* **Assignee:** yourself.
* **Labels:** enhancement, bug, chore, documentation.
* **Milestone:** create v0.1.
6. Close one issue (e.g., the Docs issue).

✅ **Check:** 4 issues created (3 open, 1 closed) with labels and milestone.

---

### Step 2: Work with Issue Features

#### Goal: Create checklists, draft issues, and link pull requests.

1. Open **Feature: Add user login** issue.
2. Add a markdown checklist:
```
- [ ] Backend endpoint
- [ ] UI form
- [ ] Tests
```

3. Create a draft issue from **New issue →** prefix title with `[Draft]`.
4. Link a PR by creating a branch `feature/login`, pushing, and opening a PR with body `Fixes #1`.

✅ **Check:** Issue displays checklist and linked PR.

---

### Step 3: Create a Project and Add Items

#### Goal: Create a new project (Table view), add issues, and draft items.

1. Go to your **Profile → Projects** or organization → **Projects.**
2. Click **New project →** choose **Table.**
3. Name it `Sprint Lab — v0.1` → click **Create project.**
4. Add existing issues:
* In the bottom row, paste each issue URL and press Enter.
5. Add a draft issue by typing a title and pressing Enter.

✅ **Check:** Project lists all issues and draft issue.

---

### Step 4: Customize Fields and Views

#### Goal: Add custom fields and create new views (Board, Roadmap).

1. In Table view, click + **(New field)**.
2. Create fields:
* **Iteration —** type Iteration, set duration (e.g., 2 weeks).
* **Priority —** type Single select (`High`, `Medium`, `Low`).
* **Estimate —** type Number.
3. Populate these fields for each item.
4. Create **Board view**:
* Click **Views → New view → Board.**
* Group by **Status** (To Do, In Progress, Done).
5. Create **Roadmap view** using **Timeline** grouped by Iteration.

✅ **Check:** Switch between Table, Board, and Roadmap views.

---

### Step 5: Configure Automations and Insights

#### Goal: Add automations to move items and create charts.

1. Open **project → menu (⋯) → Automation.**
2. Add automation: `When issue closed → Move to Done.`
3. Create chart:
* **Charts → New chart → Count of items by Priority.**
4. View **Insights** tab for progress.

✅ **Check:** Closing an issue moves it to Done, chart updates.

---

### Step 6: Advanced (Optional)

* Add multiple Iterations and assign items.
* Create custom automation with GitHub Actions or API.
* Export project data → open in spreadsheet.

---

### Step 7: Cleanup

1. Archive or close the project.
2. Close or delete lab issues.


---
### References:

GitHub Issues Quickstart  https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/quickstart

GitHub Projects Quickstart  https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/quickstart-for-projects

# Git Assignment

## Section A: Git Basics + Setup

## Q1. Check if Git is installed. What version do you have?

**Command:**

```bash
git --version
```

**Output:**

```bash
git version 2.50.1.windows.1
```

![Q1 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20143649.png)

## Q2. Set your name and email in global config.

**Commands:**

```bash
git config --global user.name "Dashami Ghosalkar"
git config --global user.email "dashamighosalkar691@gmail.com"
git config --global --list
```

**Output:**

```text
user.name=Dashami Ghosalkar
user.email=dashamighosalkar691@gmail.com
```

![Q2 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20143905.png)

## Q3. Create a new folder `git-assignment-YourName` and run `git init` inside it. Check the status.

**Commands:**

```bash
mkdir git-assignment-Dashami
cd git-assignment-Dashami
git init
git status
```

**Output (example):**

```text
Initialized empty Git repository in C:/Users/dasha/git-assignment-Dashami/.git/

On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

![Q3 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20144622.png)

## Q4. Create a `README.md` file with content `# Git Assignment - YourName`. Stage it and commit with message `"Initial commit"`.

**Commands:**

```bash
echo "# Git Assignment - Dashami Ghosalkar" > README.md
git add README.md
git commit -m "Initial commit"
git log --oneline
```

**Output (example):**

```text
[master (root-commit) abc1234] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

abc1234 Initial commit
```

![Q4 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20145657.png)

## Q5. Run `git log` and copy the hash ID of your first commit into `answers.md`.

**Command:**

```bash
git log
```

**Commit Hash ID:**

```text
a1b2c3d4e5f67890123456789abcdef12345678
```

> Replace the above hash with the actual commit hash shown on your system.

![Q5 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20145855.png)

## Q6. Perform a few changes and make five commits.

**Commands:**

```bash
git add .
git commit -m "Commit message"
```

**Output (example):**

```text
[master abc1234] Commit message
 1 file changed, 1 insertion(+)
```

![Q6 Screenshot 1](screenshots/outputs/Screenshot%202026-06-27%20153156.png)
![Q6 Screenshot 2](screenshots/outputs/Screenshot%202026-06-27%20153407.png)

## Section B: Branching & Commits

## Q7. Create a new branch named `dev` and switch to it. Show the branch list.

**Commands:**

```bash
git branch dev
git switch dev
git branch
```

**Output (example):**

```text
* dev
  master
```

![Q7 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20155959.png)

## Q8. On the `dev` branch, create `features.txt`. Add 3 lines: "Login", "Signup", "Dashboard". Commit the changes.

**Commands:**

```bash
printf "Login\nSignup\nDashboard\n" > features.txt
git add .
git commit -m "Add features file"
```

**Output (example):**

```text
[dev abc1234] Add features file
 1 file changed, 3 insertions(+)
 create mode 100644 features.txt
```

![Q8 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20162328.png)

## Q9. Switch back to the `main/master` branch. Is `features.txt` visible? It should not be. Write the reason.

**Commands:**

```bash
git switch master
ls
```

**Output (example):**

```text
README.md
answers.md
notes.txt
```

`features.txt` is **not visible**.

**Reason:**

`features.txt` was created and committed only on the `dev` branch. Since the `main/master` branch does not have that commit, the file is not present after switching back.

![Q9 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20161222.png)

## Q10. Merge `dev` into `master`. After merging, take a screenshot of `git log --oneline`.

**Commands:**

```bash
git switch master
git merge dev
git log --oneline
```

**Output (example):**

```text
Updating 3f4a2b1..7d8e9f0
Fast-forward
 features.txt | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 features.txt
```

```text
7d8e9f0 Add features file
6c5b4a3 Update notes
5b4a3c2 Add notes file
4a3b2c1 Update README with project description
3a2b1c0 Update answers.md with title
2b1c0d9 Add answers.md
1a0b9c8 Initial commit
```

![Q10 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20161444.png)

## Q11. Create a `.gitignore` file. Add `node_modules/` and `*.log` to it. Commit the file.

**Commands:**

```bash
printf "node_modules/\n*.log\n" > .gitignore
git add .
git commit -m "Add .gitignore"
```

**Output (example):**

```text
[master abc1234] Add .gitignore
 1 file changed, 2 insertions(+)
 create mode 100644 .gitignore
```

**Screenshot:** *(Paste the screenshot of the commands and commit output here.)*
![Q11 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20161723.png)

## Section C: GitHub Remote + Push/Pull

## Q12. Create a new empty repository on GitHub named `git-assignment-YourName`. Do not initialize it with a README.

**Steps:**

1. Sign in to GitHub.
2. Click **New Repository**.
3. Enter the repository name:

   ```
   git-assignment-Dashami
   ```
4. Select the repository visibility.
5. Leave **"Add a README file"** unchecked.
6. Click **Create repository**.

![Q12 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20163257.png)

## Q13. Connect your local repository to the GitHub remote.

**Commands:**

```bash
git remote add origin https://github.com/DashamiCI/git-assignment-Dashami.git
git branch -M main
git push -u origin main
```

**Output (example):**

```text
To https://github.com/DashamiCI/git-assignment-Dashami.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

![Q13 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20163609.png)

## Q14. Push your local code to GitHub.

**Command:**

```bash
git push -u origin main
```

**Output (example):**

```text
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 8 threads.
Compressing objects: 100% (15/15), done.
Writing objects: 100% (20/20), done.
Total 20 (delta 5), reused 0 (delta 0)
To https://github.com/<your-github-username>/git-assignment-Dashami.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

![Q14 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20163816.png)

## Q15. Go to GitHub and paste your repository link.

**Repository Link:**

```text
https://github.com/DashamiCI/git-assignment-dashami
```

![Q15 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20164130.png)

## Q16. Create a file directly on GitHub named `bugfix.txt` with content `Bug 1 fixed`. Run `git pull` locally to fetch that file.

**Command:**

```bash
git pull origin main
```

**Output (example):**

```text
From https://github.com/<your-github-username>/git-assignment-Dashami
 * branch            main       -> FETCH_HEAD
Updating abc1234..def5678
Fast-forward
 bugfix.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 bugfix.txt
```

![Q16 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20164546.png)

## Section D: Undo, Conflicts & Collaboration

## Q17. Add a line **"Testing undo"** to `README.md`. Do not stage it. Discard the changes using `git restore README.md`. Verify it worked.

**Commands:**

```bash
echo "Testing undo" >> README.md
git status
git restore README.md
git status
```

**Output (example):**

Before `git restore`:

```text
On branch main
Changes not staged for commit:
  modified: README.md

no changes added to commit
```

After `git restore`:

```text
On branch main
nothing to commit, working tree clean
```

**Verification:** The changes to `README.md` were successfully discarded, and the working tree is clean.

![Q17 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20165536.png)

## Q18. The last commit message was wrong. Change it to **"Initial commit - Added README"**.

**Commands:**

```bash
git commit --amend -m "Initial commit - Added README"
git log --oneline -1
```

**Output (example):**

```text
[main abc1234] Initial commit - Added README
 Date: Sat Jun 27 15:30:10 2026 +0530
 1 file changed, 2 insertions(+)
```

```text
abc1234 Initial commit - Added README
```

![Q18 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20165838.png)

## Q19. Conflict Task

### Commands:

```bash
# On main
echo "Line from main" > conflict.txt
git add .
git commit -m "Add conflict file on main"

# Create branch
git switch -c conflict-branch
echo "Line from branch" > conflict.txt
git add .
git commit -m "Update conflict file on branch"

# Back to main
git switch main
echo "Line from main updated" > conflict.txt
git add .
git commit -m "Update conflict file on main"

# Merge
git merge conflict-branch
```

**Conflict Output (example):**

```text
Auto-merging conflict.txt
CONFLICT (content): Merge conflict in conflict.txt
Automatic merge failed; fix conflicts and then commit the result.
```

**Resolve the conflict:**

Edit `conflict.txt` to:

```text
Line from main
Line from branch
```

Then run:

```bash
git add .
git commit -m "Resolve merge conflict"
cat conflict.txt
```

**Final Output:**

```text
Line from main
Line from branch
```

![Q19 Screenshot 1](screenshots/outputs/Screenshot%202026-06-27%20170601.png)
![Q19 Screenshot 2](screenshots/outputs/Screenshot%202026-06-27%20170636.png)
![Q19 Screenshot 3](screenshots/outputs/Screenshot%202026-06-27%20170943.png)

## Q20. Fork a colleague's repository and clone it locally. Write the repository name in `answers.md`.

**Command:**

```bash
git clone https://github.com/DashamiCI/conflict-drill-team.git
```

**Output (example):**

```text
Cloning into '<repo-name>'...
remote: Enumerating objects: 25, done.
remote: Counting objects: 100% (25/25), done.
Receiving objects: 100% (25/25), done.
Resolving deltas: 100% (5/5), done.
```

**Repository Name:**

```text
conflict-drill-team
```

![Q20 Screenshot 1](screenshots/outputs/Screenshot%202026-06-27%20171434.png)
![Q20 Screenshot 2](screenshots/outputs/Screenshot%202026-06-27%20165838.png)

## Q21. Add a collaborator to your `git-assignment-YourName` repository.

**Steps:**

1. Open the GitHub repository.
2. Go to **Settings**.
3. Click **Collaborators** (or **Collaborators and teams**).
4. Click **Add people**.
5. Enter the collaborator's GitHub username or email.
6. Click **Add** / **Invite**.

![Q21 Screenshot](screenshots/outputs/Screenshot%202026-06-27%20171932.png)

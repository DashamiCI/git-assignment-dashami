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


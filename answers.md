# Git Assignment

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
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

**Screenshot:** *(Paste the screenshot of the command and its output here.)*

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

**Screenshot:** *(Paste the screenshot of the commands and their output here.)*

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

**Screenshot:** *(Paste the screenshot of the terminal showing the commands and output here.)*

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

**Screenshot:** *(Paste the screenshot of the commands and output here.)*

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

**Screenshot:** *(Paste the screenshot of the `git log` output here.)*

# Git Kata: Basic Staging

This kata will examine the staging area of git.

In git we are working with three different areas:

* The working directory where you are making your changes
* The staging area where all changes you have added through `git add` will stay
* The repository where every commit ends up, making your history. To put your staged changes in here you issue the `git commit` command.

A file can have changes both in the working directory and staging area at the same time.
These changes do not have to be the same.

We will also work with `git restore` to restore the staged changes of a file, and `git checkout` to return a file to a previous state.

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

You live in your own repository. There is a file called `file.txt`.

1. What's the content of `file.txt`?
   
  ![1q](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/95388fc3-0710-4d2e-85aa-5bc7806e7679)

3. Overwrite the content in `file.txt`: `echo 2 > file.txt` to change the state of your file in the working directory (or `sc file.txt '2'` in PowerShell)

   ![q2](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/b7b77367-dc4f-4b2b-8108-17c0a2077be2)

5. What does `git diff` tell you?
6. What does `git diff --staged` tell you? why is this blank?
7. Run `git add file.txt` to stage your changes from the working directory.
8. What does `git diff` tell you?
9. What does `git diff --staged` tell you?
10. Overwrite the content in `file.txt`: `echo 3 > file.txt` to change the state of your file in the working directory (or `sc file.txt '3'` in PowerShell).
11. What does `git diff` tell you?
12. What does `git diff --staged` tell you?
13. Explain what is happening
14. Run `git status` and observe that `file.txt` are present twice in the output.
15. Run `git restore --staged file.txt` to unstage the change
16. What does `git status` tell you now?
17. Stage the change and make a commit
18. What does the log look like?
19. Overwrite the content in `file.txt`: `echo 4 > file.txt` (or `sc file.txt '4'` in PowerShell)
20. What is the content of `file.txt`?
21. What does `git status` tell us?
22. Run `git restore file.txt`
23. What is the content of `file.txt`?
24. What does `git status` tell us?

## Useful commands

- `git add`
- `git commit`
- `git commit -m "My lazy short commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `git restore --staged`

## Aliases

You can set up aliases as such:
`git config --global alias.lol 'log --oneline --graph --all'`
This might be useful to you.

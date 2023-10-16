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

   ![q3](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/1c372879-87bc-4d11-bb48-531c368e9f8a)

7. What does `git diff --staged` tell you? why is this blank?

   ![q4](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/54a1f6a3-ef89-48a9-9142-8584259271a6)

9. Run `git add file.txt` to stage your changes from the working directory.

   ![q5](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/edb95907-affc-4cd2-9f06-4feec11427a3)

11. What does `git diff` tell you?
12. What does `git diff --staged` tell you?
13. Overwrite the content in `file.txt`: `echo 3 > file.txt` to change the state of your file in the working directory (or `sc file.txt '3'` in PowerShell).
14. What does `git diff` tell you?
    ![q6](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/98cff215-e463-4313-9c96-af196647ba5e)

16. What does `git diff --staged` tell you?
    ![q7](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/c6bfc078-88dd-40d1-a3cf-b1836d45711d)

18. Explain what is happening
19. Run `git status` and observe that `file.txt` are present twice in the output.
    ![q12](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/2508fc0b-74eb-479b-9b32-ce640f4a67a5)

21. Run `git restore --staged file.txt` to unstage the change
22. What does `git status` tell you now?
    ![q13](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/74f47e03-101a-4fe5-ae53-d9d9a01211b6)

24. Stage the change and make a commit
25. What does the log look like?
    ![q14](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/ca762226-fc53-4df6-ba6d-8931912075b8)

27. Overwrite the content in `file.txt`: `echo 4 > file.txt` (or `sc file.txt '4'` in PowerShell)
28. What is the content of `file.txt`?
29. What does `git status` tell us?
    ![q15](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/9906c85c-bfa1-46eb-a737-078f415fab70)

31. Run `git restore file.txt`
32. What is the content of `file.txt`?
33. What does `git status` tell us?
   ![q16](https://github.com/NesrinAbuMnezel/basic-staging/assets/95749191/a6b1cc93-7e69-4faa-8bf8-fddd79a8de1e)

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

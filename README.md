# Gitting to Know Git!

**Author**: Justin Del Vecchio

**Edited by**: Jon Mrowczynski

## Industry Rationale

Version control systems are the cornerstone of life in industry. Without version control systems, modern application development would not be possible. Understanding, familiarity, and ease of use with git is essential.

## Objectives

- Introduction to Version Control
- Overview of Git + GitHub
- Installation
- Setting up a GitHub Account
- Basic Git Commands
- GitHub Repository Setup

## Scoring Rubric

| Task | Full Credit | Partial Credit |	Zero Credit |
|-|-|-|-|
| 1. Create GitHub Account | Creates account and is accessible from the Internet. |	Creates account but supplies incorrect account name. | Does not create an account. |
| 2. Basic Git Commands	| Clones public repo correctly and follows directions in the txt file. | Clones repo, but does not follow directions correctly in the txt file. | Fails to clone the public repo. |
| 3. Setting up SSH with GitHub | Correctly sets up SSH with GitHub | N/A | Does not setup SSH |
| 4. GitHub Public Repo Setup | Creates a public repo, is correctly named, and contains the correct files. | Creates a public repo, but incorrectly named or doesn't contain the correct files. | Fails to create a public repo. |

### Task 1 (5 pts)

Create a GitHub account. If you already have one, great! Either way:

- [Setup
  2FA](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication)
  if it isn't already! 
    - This helps to keep your GitHub account secure and out of the hands of would-be hackers! (This genuinely saved my butt once O_o!?).
- list your username below:

[Username]

### Task 2 (5 pts)

Locally clone this public repository with the following command: 

`git clone https://github.com/JonMrowczynski/CSC213Lab1.git`

Notice we are using HTTPS! This is a beginner-friendly approach and is fine if you just need to
download a repo from GitHub.

It's generally better to utilize SSH. Especially if you also need to push commits to remote repos! We'll handle this
soon, though.

Anyway, this repo has a single encrypted zip file in it. Open it with the password: 

CSC213!whiz

to find a single text file inside that contains a secret word! Copy and paste that word below:

[Secret Word]

### Task 3 (10 pts)

It ends up being relatively awkward in the long-term to use HTTPS. You will have to create a Personal Access Token (PAT) on
GitHub and then enter your username and that token in place of your password every time you want to push commits to remote
repos! For better long-term convenience, it's useful to know how to setup SSH with GitHub.

Instructions to do so can be found in [Using SSH with GitHub.md](./Using%20SSH%20with%20GitHub.md)


### Task 4 (10 pts)

Create and share a GitHub project by doing the following:

1. Create a new, public project **exactly** named: `CSC213Lab1` in your GitHub account.
2. Clone that project locally using SSH.
3. Create a folder named `src` in that project.
4. Add a file named `HelloWorld.java` in that folder.
5. When run, this file should print `Hello World` to the terminal.
6. Add and commit the file and directory.
7. Push the committed updated code to GitHub.

List the project’s HTTPS URL so that it can be cloned:

[URL]

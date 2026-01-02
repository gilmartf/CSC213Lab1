 
# Gitting to Know Git!

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
| 3. GitHub Public Repo Setup | Creates a public repo, is correctly named, and initialized with correct files. | Creates a public repo, but incorrectly named or initialized incorrectly. | Fails to create a public repo. |

### Task 1 (5 pts)

Create a GitHub account. If you already have one, great! Either way, just list your username below:

[Username]

### Task 2 (5 pts)

Locally clone this public repository with the following command: 

`git clone https://github.com/JonMrowczynski/CSC213Lab1.git`  

It has a single encrypted zip file in it. Open it with the password: 

CSC213!whiz

to find a single text file inside. Open that file to find the secret word! Write that word (case sensitive!) below:

[Secret Word]

### Task 3 (10 pts)

Create and share a GitHub project by doing the following:

1. Create a new, public project **exactly** named: `CSC213Lab1` in your GitHub account.
2. Clone that project locally.
3. Create a folder named `src` in that project.
4. Add a file named `HelloWorld.java` in that folder.
5. When run, this file should print `Hello World` to the terminal.
6. Add and commit the file and directory using git:

    `git add /path/to/HelloWorld.java` 

    `git commit -m "Initial commit."`

7. Push the committed updated code to GitHub with the command:

    `git push -u origin main`

List the project’s HTTPS URL so that it can be cloned:

[URL]

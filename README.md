# Case research process: database performance

Use this repository to keep all information, code, and results of your research project about database performance. Use [Markdown](https://guides.github.com/features/mastering-markdown/) for reports, procedures, etc. (all files with formatted text that you would probably want to use Word for). A template for the final paper and file for the bibliographic database is also provided.

## TODOs

- [ ] Each team member clones this repository (see below)
- [ ] Fill out the names and contact information of team members in the table below
- [ ] Adjust the name of the LaTeX document for the final paper into `lastname-etal-2017-dbperf.tex` with the last name of the team member that comes first alphabetically.

## Teamleden

| Name     | Github                        | Email                               |
| :---     | :---                          | :---                                |
| student1 | <https://github.com/student1> | <mailto:student1@student.hogent.be> |
| student2 | <https://github.com/student2> | <mailto:student2@student.hogent.be> |
| student3 | <https://github.com/student3> | <mailto:student3@student.hogent.be> |
| student4 | <https://github.com/student4> | <mailto:student4@student.hogent.be> |

## Git workflow for a team

When working with Git in a team, chances are that you create conflicts when several contributors change the same file independently and push their version to Github. A few tips to avoid this, and the most important commands to use follow below. Most students may prefer a graphical tool like SourceTree or Github Desktop, but the command line tool is actually pretty good and also explains every time what the next step should be and how to undo a step. Error messages, when read carefully and interpreted, usually give a good idea of what went wrong and how to solve it.

Don't hesitate to ask for help. The advantage of Git is that pretty much everything can be fixed or undone when necessary. Try to become proficient with Git as soon as possible, you will need it continually.

Commit regularly, multiple times per session that you're working on the project. Provide a descriptive commit message, your fellow team members and your future self will be grateful.

Working with branches is probably unnecessary and will no be discussed here.

### Installing and configuring Git

When installing [Git for Windows](https://git-scm.com/download/), ensure that Git Bash is included. To simplify syncing with Github, it is recommended to use an [SSH key pair](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/). When prompted for a passphrase, you can leave it empty. Follow Github's instructions to [register your SSH-key](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/).

Start a text console and issue the following commands for the basic configuration of Git. Use the email address that you have used to register your Github accound.

```
$ git config --global user.name "FIRST_NAME SURNAME"
$ git config --global user.email "NAME@EXAMPLE.COM"
$ git config --global push.default simple
```

### Project start

Each team member creates a local copy (clone) of the Github repository.

1. Go to the Github repository, click the green button "Clone or Download" on the right. Ensure that "Use SSH" is selected. Copy the URL (starts with `git@github.com:HoGentTIN`)
2. Open Git Bash in a directory where you want to keep the local repository
3. `git clone git@github.com:HoGentTIN/TEAM-REPO.git`

You can change the name of the local repository into one you choose yourself, and move the directory to another location without affecting the repository, or synchronisation with Github.

### Workflow

1. Before you start making changes, first pull any new commits from Github

    ```
    $ git pull
    ```

2. Make your changes, commit them locally

    ```
    $ git add .
    $ git commit -m "Descriptive message"
    ```

3. To be sure, fetch any changes from Github, but this time "in the background" (i.e. no attempt is made yet to apply those changes to your local code):

    ```
    $ git fetch origin master
    ```

4. *If* changes were fetched, attempt to apply your own changes *on top of* those from Github. If not, skip this step.

    ```
    $ git rebase master
    ```

5. Resolve any conflicts and commit. Follow the suggestions made by the Github command line client
6. Send your changes to Github

    ```
    $ git push
    ```

This workflow will keep the history of the project linear, without diverging and merging. By making good arrangements and distributing tasks efficiently, merge conflicts can be kept to a minimum.


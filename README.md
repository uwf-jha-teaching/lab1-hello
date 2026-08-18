# Lab 1
![Points badge](../../blob/badges/.github/badges/points.svg)

## Purpose
The purpose of this lab is to get hands-on experience with Github classroom and
create and submit a simple application for practice.

## Register with GitHub
- Refer to the document provided in the course about GitHub to correctly set up
  git.
- If you do not have a GitHub (https://www.github.com) account yet, you will
  need to register in order to complete the assignments for this course. If you
  already have an account but want to keep the two separate, you can create a
  new account to use for this course.
- You will need to setup one of the two authentication methods to access the
  repositories in the future.

  - [Generate your GitHub personal token][1] to use HTTPS protocol in the
     future (Recommended).
  - [Setup an SSH key ][2] to use SSH protocol in the future.


[1]:https://docs.github.com/en/enterprise-server@3.4/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

[2]:https://docs.github.com/en/authentication/connecting-to-github-with-ssh

## Create a directory for this course
Somewhere on your system, create a directory that you intend to use for this
course if you have not done so already. It is nice to have one place to look
for all of your work. Giving it an obvious name such as **cop3530** will make
it easier to find until you get used to your setup. You make create a
subdirectory like **projects** and **labs** for better organization of course
related contents.

## Github
Here is a [cheat sheet][2] of git commands that will be helpful in working with
the git version control system.

[2]: https://education.github.com/git-cheat-sheet-education.pdf

- When you are prompt a roster, find your name and select it to link your
  GitHub account that you are currently logged in to the name shown in the
  roster. **Never skip this step!** If your name is not listed, skip this step
  and email me your GitHub account name and your full name, so I can add you
  manually.
- Click "Accept this assignment". This will create a new private repository in
  Github for you to submit your work. You will need to wait a couple second for
  the system to create your repository and refresh to see the link to your
  repository.
- Near the top right of your browser, you'll see a green "Code" button.
- Click the button and copy the URL of your repository. You have HTTPS and SSH
  protocols to choose from. HTTPS is preferred in this course for simplicity
  but you will need to generate a personal token to be used in the place of
  password.
- In the command line environment (terminal), change into the directory you
  created for this course to hold all projects.
- Run `git clone URL_COPIED_ABOVE`.
- You will be prompt for user name and password to authenticate. Use your
  username and personal token to authenticate log in using HTTPS.

This will create a directory called lab-hello-world-YOUR_ID that will contain this
README.md file along with some supporting files.

If you have never used Git before, you'll need to run a few one-time
configuration commands.

- Add your name and email, at a minimum.

  - For example, type the following (substitute your details for the
    placeholders):

    ```
    git config --global user.name "Your Name"
    git config --global user.email youremail@students.uwf.edu
    ```

    **Please use your UWF email account rather than a personal one here.** It
    does not need to match the email used used to register your GitHub account.

This setup process should only have to be done once, not each time you make a
repository.

## Hello
[![funny hello video](https://img.youtube.com/vi/PUjvaMWKeBI/0.jpg)](https://www.youtube.com/watch?v=PUjvaMWKeBI)

Using a text editor of your choice, create a Hello World application that
prints your Github handle, followed by a colon and your last name, first name
in **camel case**.

Print **Hello World!** in the next line. **Case and format matter!**

If your GitHub handle were UsEr123 (case matters) and your name was John Doe,
your output would look like this:

```
UsEr123:DoeJohn
Hello World!
```

**A Makefile is provided in this repository that will build an executable named
`main` by compiling your work in a file called `main.cpp`. To create the
executable, type `make` at the command line. Then, run the file named main,
e.g. `./main`, or debug compiler errors if there were any.**

## "Saving" work
Once your program is working as expected, go back to your command line. Type
`git status`. You should see your new files. Type `git add -A`, to tell git to
stage all changes.

The stage is basically a list of files (or blocks of code if using advanced
features such as patches) that you intend to commit to the repository.

Now if you type `git status` again, you should see all updated files added to
the stage.

You may also use `git commit -m "message"` to provide a message directly in the
command. Substitute `message` with your commit message, which is the short
description you what you have added in this commit.

The "add, commit" process outlined above isn't something that you need to wait
until your done with the whole project to do.

Much like any other aspect of programming, incremental is best. If you add a
new function and it compiles and tests successfully, go ahead and commit. That
way if you start making some changes and break your entire program, you can go
back to your last "stable" code and start again, or compare via `git diff HEAD`
with the last stable commit to help narrow down the bug.

## Submitting work
To post the work you've completed back to Github for me (or a TA) to review and
grade, simply run `git push origin main` (assuming you already committed the
code locally).

For projects, which are graded against a rubric.

## Important notes
You should add and commit frequently and provide clear commit comments to be
able to trace your changes later.

Push your code when you are asking my help or when you passed all local tests
and want to summit. As pushing will trigger auto-grading, **DO NOT PUSH TOO
FREQUENTLY** so we will run out of quota for auto-grading. You can use push and
pull to synchronize your code for convenience but do not use it too frequently!


## Grading Information:
- Breakdown 10 total

  + 10 GitHub Auto-grading

    - 3 program compiles
    - 2 prints the id:name line
    - 5 prints the Hello World! line

- Auto-grading results can be checked at the top of this document like as a
  badge ***40/80***.
- View details:
    1. On your GitHub repo page, Click the :arrow_forward: **Actions** tab to
       see your graded results.
    1. If it isn't a green check mark (:heavy_check_mark:) then at least part of
       the testing failed.
    1. Click the commit message for the failing version then click "Autograding"
       on the left side of the page.
    1. Follow the :x: path and expand things to see what errors exist.
    1. It is usually **education/autograding@v1** and you can expend this path to
       view the detail.

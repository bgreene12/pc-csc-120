Lab 1: R Markdown
================

This first lab is a continuation of what you’ve done for Assignment 1.
I’ve intentionally left images out to force you to slow down and
explore things. But feel free to ask for help, or to surreptitiously
look over your neighbor’s shoulder to find out where that tiny “Commit”
button is located.

## Clone your repository

In this week’s assignment, we cloned the course repository from within
GitHub Desktop. Today we will do it a bit differently, cloning your
personal repository from within your browser. Go to the
[`willwerscheid-teaching` organization
page](https://github.com/willwerscheid-teaching), accept my invitation
to join if you haven’t done so yet, and locate your repository under the
Repositories tab. Click into it. Find the green “Code” button, which
opens a menu that includes the option “Open with GitHub Desktop.” Click
it, give the necessary permissions, and voilà.

## Claim your repository

Go to RStudio and open a project within your personal repository. Now go
to the Git tab in the upper-right pane and notice that a new .Rproj file
was added to the project home directory (you should see it in the Files
tab in the lower-right pane as well). This file is used locally by
RStudio, but we don’t actually want to put it online since it stores
options that are specific to each user. Instead, we will tell git to
ignore it by adding it to the .gitignore file (which you should also see
in the Files tab).

## Modify .gitignore

Open the .gitignore file by clicking on it. A new pane will open showing
the contents of the file. Go to the last line and add `*.Rproj` (the
asterisk is a wildcard character that stands for any number of any
characters; basically, adding this line tells git to ignore every file
that ends in `.Rproj`). Save your changes. If you did everything
correctly, then the .Rproj file should disappear from the Git tab, and
instead you will see the .gitignore file. We do want to move this change
online, so check the “Staged” box next to .gitignore in the Git tab and
click “Commit” (it’s a small button in the bar on top of the Git tab). A
window will pop up showing your change in green. Add a descriptive
message such as “added .Rproj file to .gitignore” and again click
“Commit.”

Congratulations\! You’ve made your first commit — that is, you’ve
confirmed some changes on your local copy of the repository that you
want to keep in the main repository. If you view the main repository
online, however, they won’t appear there yet. To move the changes from
your computer to the online repository, you’ll need to “push” them. You
can do this within RStudio, but I find it easiest to do from GitHub
Desktop — if you go there, you will notice that the “Fetch origin”
button now says “Push origin.” If you click it (do so\!), your changes
will be incorporated into the online repository, so that it is now in
sync with your local copy. Pushing is, as you might expect, the opposite
of pulling: pushing moves your local changes to the main online
repository; pulling moves someone else’s changes from the main
repository to your own local copy.

## Create an R Markdown document

Maybe you aren’t as excited as I am about changing .gitignore. Fine. To
add a little more personality to your repository, we’ll add an R
Markdown file that introduces you to the rest of the class. Keep in mind
that all personal repositories are visible to the class, but only you
(and I) have the ability to make changes to them. Return to RStudio and
create a new R Markdown document (.Rmd file) by selecting File \> New
File \> R Markdown… Give the report a title (e.g., “Introduction to
Myself”; you can change this later) and add your name. You can select
whatever you like for the default output format; we’ll be using a
different option anyway.

After creating the file, change `output: html_document` to `output:
github_document` (this will make the document viewable on the GitHub
website; otherwise it will appear as basically unreadable code). Save
the file as `Introduction.Rmd`. Please do not deviate from this file
name. If you’ve already screwed up and need to rename the file, check
the file in the Files tab, click the Rename button, and do it right this
time.

## Knit your document

Read through the example text that was added to your new .Rmd file. Try
out that “Knit” button and watch the markdown code get converted into a
nice, readable report with embedded code and figures (this will appear
in the Files tab as an .md file). Not too shabby, eh?

Now erase the example text (everything under `## R Markdown`; keep the
first code chunk as it sets global options) and use that space to tell
us a little bit about yourself. Consult the R Markdown cheatsheet for
formatting options (I plan to hand out copies, but if I forget or if you
lose it you can find it in the course repository). R Markdown certainly
doesn’t make RStudio into a fancy word processor but there are a few
basic things you can do (bold, italics, section headers, lists, etc.).

Once you’ve finished, knit your document, commit your changes (you will
need to commit both the .Rmd and .md files), and push them online. If
you can view the .md file on the GitHub website, you’re done\! Now go
see if any of your classmates need help. And feel free to revise as much
as you like later by simply committing anew and pushing your changes.

## Review

Know how to answer the following:

1.  What does the .gitignore file do?

2.  What is the difference between committing and pushing?

3.  What does adding `output: github_document` to the R Markdown header
    do?

4.  What does it mean to “knit” your document?

# AUVIC Mechanical Repository

Welcome to the mechanical team. One rule: do not push directly into master. Please talk with the lead if you dont understand why.

## Getting started (bottom up)

We use solidworks prolifically in this university. I will assume everyone is using a windows machine. Before continuing, please make a [github](https://github.com/) account.  

- Go to [gitforwindows.org](https://gitforwindows.org/) to download git. Follow instalation guidelines but enable "use git from the command line"
- After completing the installation, open CMD (shortcut: WIN+R , enter 'cmd') and enter these two commands
    - git config --global user.name "*your name*"
    - git config --global user.email "*github email*"
- Next we want to clone the repository:
    - Open cmd and in your user directory, type "*mkdir auvic*"
    - Type "cd auvic"
    - In the mechanical team repository, click the green "clone or download" button and copy the address.
    - Type "git clone https://github.com/uvic-auvic/Mechanical-Team.git *name_of_folder*"

You are ready to go (but not really).

## Really getting started

Before you rush into a project there is one major rule that must be followed at all times:

**Do not push directly into master**

Now that you have a copy of the repository on your device, it is yours. Nobody but you can edit it's contents. But there is a procedure that must be followed before beginning and finishing a project, which is branching.

### What is branching?

Branching is the way how multiple people can be working in one project and not impede one another. If everyone worked in a single branch, you will find some files moved, disabled, or deleted everytime someone pushes to the remote repo. In large projects, this makes work much more difficult. This is why clever people created branching, basically having two "timelines" of the same project that merge once the project manager accepts the changes.

In the case of no branching, say Evan was working on the main enclosure assembly of the submarine and decided to use a part that Peyton originally made for the frame. At first everything is fine, but after a little while later Peyton finds the frame design is fundamentally incorrect and deletes all his files and update the remote repo. Evan, seeing the repo being updated, pulls a fresh copy. All of sudden, parts randomly disapeared from his assembly. After several hours of checking the folders for the missing parts with no luck, he decides to remake them ground up; wasting time and energy. 

Using branching, Peyton and evan would be working on their own branches, while the master branch stays clean and only contains reviewed and approved parts. Any pushes Peyton makes would only affect his branch and Evan can complete his work safely.

### How to switch branches

To switch into different branches, you will need to use the keyword *checkout*. First check the current list of branches and choose the one you want to download locally. See the list of common git commands below to download and switch branches.

- Check the current list of branches: "git branch -a"  
- Download a remote branch: "git checkout *name_of_branch*"
- To peek at the contents of a branch: "git checkout origin/*name_of_branch*"
- To make your own branch and checkout into it: "git checkout -b *name_of_branch*"
    - Creating a local branch and pushing it into a remote repository is a more involved and much more than I expect from a mechanical student. I prefer you create the branches on the web client rather than on the command line, if needed.

After switching into your branch, you can now begin.

## Saving your work on the local repository

There are two ways you can save your work: committing and stashing. There isnt really any rules following commiting and stashing, but my only concern is dont *commit* an incomplete part. If for any reason you need to switch branches to work on another project, you should *stash* your work. A commit is basically a save point, in case you mess up bad, you want to be able to return to your last working copy of your project. An example where you would stash rather than commit is if you didnt finish building a part and you needed to switch projects.

You can stash multiple time and also on different branches. Here are a list of some commands:

- To stash your work: "git stash"
- To view all your stashes: "git stash list"
- To retrieve your stash: "git stash apply"
- to retrieve a specific stash: 
    - Get its name with "git stash list"
    - use "git stash apply *stash@{2}*"
- To commit your work: 
    - navigate to the repo
    - git add *
    - git commit -m "*enter message here*"
    **NOTE:** files need to be "Staged" to be commited by using the *add* command. 

## Pushing your work to the rmeote repository/branch

After you commited your work. Use the command: "git push" and that is it.

## After completing your assembly

Use the command: "git pull-request" for the lead to review your assembly. 
Now repeat.



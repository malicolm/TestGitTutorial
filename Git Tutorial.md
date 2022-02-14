# Command-Line Git Tutorial 
<br>

## Step One: Connect to your GitHub account

Open a new terminal shell and type in: 

    git config --global user.name "username"

followed by:

     git config --global user.password "password"

replacing "username" and "password" with you current GitHub username and password, respectively. 

## Step Two: Create a respository

Go to [GitHub](https://github.com/new) and create a new repository.

Once the repository is created, copy the repository link - typically in the form:


    https://github.com/YOUR_USERNAME/REPOSITORY_NAME.git


With your GitHub username and the name of the new repository as YOUR_USERNAME and REPOSITORY_NAME, respectively. 

## Step Three: Navigate to the directory

Using the command line command:

    cd

navigate through the folders on your local computer until you are in the root directory of the hangman project. 

For example if your HelloWorld project folder is stored on your desktop you would write: 

    cd desktop
    cd HelloWorld

Make sure only files that you want uploaded to GitHub are in the folder.
    
## Step Four: Connect local project repository to GitHub

</br>

Assuming you have navigated to the project directory, in your commandline type:

    git init

followed by:
    
    git remote add origin https://github.com/YOUR_USERNAME/REPOSITORY_NAME.git

 and 
    
    git add .

The git add . adds all files that have been changed since the last push in the directory to be "staged". 

Alternatively, if you want to add specific individual files you can type

    git add filename.filetype

Next, you need to commit those changes by typing

    git commit -m "message about changes"

then,

    git branch -M main
    git push -u origin main

Now, if you go to your github repository you should see all of the files that were in your project directory.

</br>

## Later project changes

Whether you are modifying existing files or adding new ones, making changes to your project can be made easier with the use of pushing, pulling, stashes, branches, and merging.

</br>

## General project updating

When you want to make changes and push them to GitHub there are a few useful commands, some of which we already used to intially set up the repository.

Once changes are made to a file, if you want to push those changes to git hub you must first add the file to be staged by typing:

    git add filename.filetype

Then, assuming you have added all of the files you want to commit you should commit your changes by typing:

    git commit -m "commit message"

To push those changes to GitHub type:

    git push

To pull new changes made by others or pull old changes type:

    git pull




</br>

## Stashing

Stashing is useful if you want to clear your working tree, to pull new changes or move to a different branch but save your unfinished(not ready to be committed) changes for later. 

In order for changes to be stashed they must first be staged using:

    git add files_to_be_staged.filetype

then to stash them type:

    git stash 

you can make sure those changes were stashed and view them by typing:

    git stash list

or 

     git stash show

Your working tree is now free of the stashed changes which can be popped and re-added to your working tree at any time by typing:

    git stash pop

or 

    git stash apply

Git stash apply applies your changes and leaves the stashed changes in the stash stack. Git stash pop applies your changes and removes (pops) them from the stash stack. 

To discard your stashed changes without applying them, you can type:

    git stash clear

</br>

## Branching and merging

Branching is most often used when you want to begin working on a new feature and do not want to tamper with the master branch. 

To create and switch to a new branch type:

    git checkout -b branch_name

once you are working on this branch, the committed changes will not be merged with the master branch until you choose to merge them. This allows you to work on a new feature over time without pushing an unfinished product to the main branch. 

To navigate to other branches use:

    git checkout branch_name

To list all branches type:

    git branch

</br>

To merge two branches together, type:

    git merge branch_name

to merge the specified branch with the current branch

If you want to merge two branches together that you are not in type:

    git merge sourcebranch_name targetbranch_name


When merging, if there are no merge conflicts youre good to go, however if there are conflicts you will have to go into your text editor and choose which changes you want to keep.  

</br>

## More
These commands are enough to get the ball rolling but git has the power to do more. For more documentation on useful commands to view, store, edit, and share code in git, check out the full git [documentation](https://git-scm.com/docs).






















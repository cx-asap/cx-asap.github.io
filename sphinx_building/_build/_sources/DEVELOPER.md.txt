# Contributing to CX-ASAP

*Welcome to the CX-ASAP team!* To maintain our code on GitHub, we need to ensure that there are no conflicts between code versions being worked on independently by collaborators. Please read the below guidelines if you are actively contributing.

## Ways to Contribute

Before contributing to this project, please familiarise yourself with git and be confident in its usage (see below). 

The main ways you can contribute to this project are by adding new modules/pipelines and fixing bugs/improving upon existing code. 

If you have an idea for a new module, you will need to add it into the commandline interface. This can be done by editing the file 'cxasap.py'. Instructions for doing this are commented at the top of this script.

## Rules

1. Please don't delete existing modules. 
2. Never edit the master branch or the dev branch - always work on your own branch (forked from the dev branch). 
3. Never merge your edits into the master branch or the dev branch - please submit your code for review (instructions included in 'CXASAP GitHub Guide'). This is to ensure that your edits do not break other sections of the code. 

## How to write a new module 

**Step 1. Have a scan of the utils.py file**

In the *system_files* folder, there is a python script called:

`utils.py`

It is a good idea to have a look at this file before writing any code within CX-ASAP, as it contains some common functions used throughout the software package to avoid repetitive code. 

In particular, the *Directory_Browse*, *File_Check*, *Cell_Import* and *File_Sorter* functions may be of use. Investigate the code currently in CX-ASAP for examples of how these functions should be used. 

**Step 2. Write your code :)**

In the *system_files* folder, there is a python script called: 

`class_template.py`

This is the easiest way to start writing code within CX-ASAP, as this template includes the standard yaml set up. Once you have found this file, write away :) 

**Step 3. Add your code to the commandline interface**

First, open the file:

`cxasap.py` 

You will need to import your code into this script. 

Then, you will need to figure out which of your input variables will need to be configurable by the user and import into the code using the conf.yaml file. Add these parameters into the below file found in *system_files*:

`parameter.yaml`

This yaml file will essentially store all of the required parameters as a *list* 

First heading should be the name of your module or pipeline as you will call it in the commandline interface. After the heading, enter your required input parameters as a list

You will then need to add a new *click command* - click is the python library used to create the commandline interface. There is a template for this at the top of the *cxasap.py* file. 

Make sure you fill out descriptions for your yaml parameters, and in the *run* function, create your class and call the functions from your module/pipeline. (If you are unsure, look at examples already in place for how to configure this) 

Finally, at the bottom of the *cxasap.py* file, add your new click command to the interface. 

## How to contribute your code

**CX-ASAP GitHub Structure**

The master branch is for official releases, while the dev branch is for code that is in active development. Active contributors will each have their own branch forked from the dev branch rather than the master. 

**Step 1. Clone the repository onto your computer**

Log into your GitHub account and navigate to the [cx-asap repo](https://github.com/AustralianSynchrotron/cx-asap). 

Go to the green *code* button and copy the link (you will use this to clone the repository). It is recommended that you clone from the dev branch if you are actively contributing. 

Clone by navigating in your terminal where you want the code to be and type the below:

`git clone https://github.com/AustralianSynchrotron/cx-asap.git`

**Step 2. NEVER TOUCH THE MASTER BRANCH**

Once you have CX-ASAP cloned to your computer, the first thing you should do is make a branch for your own changes. Do this by typing the below code (replace ‘your_name’ with your name for ease of identification)

`git checkout -b cxasap_your_name`

For example, if your name is Amy, please call your branch ‘cxasap_Amy’. This command both creates a new branch and also switches to it. 

Verify you are on your own branch by typing:

`git branch`

There should be an asterisk next to the name of your new branch. 

Once you are on your new branch, check what files have been changed, add and commit frequently using the below commands:

`git status`
`git add path/to/changed/file/here`
`git commit -m 'enter descriptive message here'`

Ideally, these last two commands would be run for each individual file to ensure that the descriptive messages are written specifically for what changed in each file. 

If you have run the CX-ASAP test, do not add the altered test files to your branch! If you do, your changes likely won’t be accepted into the master branch :)

**Step 3. Test your Changes**

Before pushing your branch to GitHub, please run the 'cxasap test' command, to ensure that your changes do not break the primary functions of the software package :) 

As your new modules will likely not be included in this test command, either add it in, or ensure that you perform your own independent testing. 

There are also some unit tests built in. These will be run through the GitHub Actions when pushed to Git. 

**Step 4. Pushing your branch to GitHub**

Once you are happy that your code works without bugs (to the best of your knowledge, there will always be secret mystery bugs), push your changes to GitHub.

First you will need to configure Git so that it will always push changes to the current branch (which in this case, should be your own personal branch!). Do this by running the below command:

`git config --global push.default current`

Then you can push using the below command:

`git push`

Running this command will not actually change the master branch. Rather, your new branch will appear on GitHub as a separate branch. 

**Step 5. Requesting that your branch be merged into the master/dev branch**

Your branch should be highlighted at the top with a green button that says ‘compare and pull request’. Click on this button and submit a new pull request. Otherwise you can navigate to ‘pull requests’ and set it up from scratch.

In this request screen, you will need to write a small but detailed description of the changes you have made and select ‘Amy Thompson’ to be the reviewer. 

Once you have entered the required information, finalise the pull request, and Amy will handle the merge. This is to ensure that the additions are compatible with the dev branch and/or additional code written by other collaborators. Amy will wither accept the pull request, or add in some comments for things that need to be changed or fixed before your branch can be merged with the dev branch. 

Note: Please merge your edits with the dev branch! The master branch is for large updates only!

**Step 6. Updating your code from the master or dev branch**

You should regularly check whether changes have been made to the master or dev branch. Someone else might also be making changes which have been merged. You can update your code to the current master branch using the below command:

`git pull origin master`

You can update your code to the current dev branch using the below command:

`git pull origin dev`

It is recommended that you wait to do this until you have made a pull request with your most recent updates. This will help avoid any conflicts while pulling the branch to your computer. 
 
## Questions

As always, please use the GitHub 'Issues' feature if you find bugs that you are unable to fix, or otherwise have questions relating to the code structure. 



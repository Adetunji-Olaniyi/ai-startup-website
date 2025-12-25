# Part 1: Setup and Initial Configuration

## 1. Install Git

Visit the official Git website and download the version of Git for your operating system. Follow the intallation instructions.

## 2. Create a Github Repository:

- Sign up or log in to Github.

- Click the "+" icon in the top-rightt corner and select "New repository."

![NewRepository](./Img/Screenshot%201.png)

- Name your repository (e.g., "ai-startup-website") and initialize it witth a README file. 

- Click "Create repository"

![CreateRepository](./Img/Screenshot%202.png)

## 3. Clone the Repository

- On your repository's page on GitHub, click the "Code" button and copy the HTTPS URL.

![CloneRepository](./Img/Screenshot%203.png)

- Open your terminal or command prompt 

- Create a folder named "git-project" in the folder where you are storing all DAREY.IO related work. For example in the Desktop folder on your laptop, you may create a folder called "darey-training"

- Change directory into the "git-project"

- Clone (Download) the repository from Github using

`git clone [Past the URL copied from GitHub]`

![Clone](./Img/Screenshot%204.png)

- Since you just clonned your repository, your main branch is `main`

- Navigate into the repository you clonned

`cd ai-startup-website`

- Create an empty file "index.html"

- Add the content below

This is the Admin creating an index.html file for Tom and Jerry.

![Index.html](./Img/Screenshott%206.png)

- Check changes has nott been staged

`git status`

![Gitstatus](./Img/Sceenshot%205.png)

Stage changes:

`git add index.html`


Confirm changes have been staged for commit:

`git status`

Now, after staging the changes, the file name will appear in green in tthe terminal output. This colour change signifies that the file has been successfully staged, making it ready for the next step, which is committing these changes to the project's history.

- Commit changes

git commit -m "This is my first commit" 

This takes the changes and records them in the repository's history with a message describing twhat was done. This commit is a milestone, marking a specific point in the project's development

![Git Commit](./Img/Screenshot%205.png)

- Push main branch to Github:

`git push origin main` 

![Gitpush](./Img/Screenshot%207.png)

This sends commit from your main branch on your laptop to GuitHub (Remote Repository).

# Part 2: Simulating Tom and Jerry's Work

To simulate both Tom and Jerry working on the same laptop, you'll switch between two branches, making changes as each character 

1. Tom's Work

- Navigate to the project directory you just cloned: 

`cd ai-startup-website`

![Navigatetodirectory](./Img/L2%20Snapshot%201.png)

This moves you into the folder containing the cloned GitHub repository on your local machine. It's like stepping into the project's workspace.

- Check the current branch: This shows you a list of all branches in your local repository. initially, you'll see only the "main" branch because that's the default starting point and no other branches because that's the default starting point and no other branches have been created yet. 

`git branch`

![gitbranch](./Img/L2%20Screenshot%202.png)

- Create a new branch for Tom's work:

`git checkout -b update-navigation`

![gitcheckout](./Img/L2%20Screenshot%203.png)

This creates a new branch named "update-navigation" (You can name it whatever you want) The command also automatically switches to the "main" branch. This branch "updatye-navigation" is where you'll simulate Tom's updates to the website without affecting whatever is in the main branch

- Check the branch again tto see your newly created branch

`git branch` 

![gitbranch](./Img/L2%20Screenshot%204.png)

Running git branch again now shows your newly created branch, indicating you're now working in this new "workspaces" dedicated to Tom's navigation updates. 

Recall you created an empty file "index.html" in the main. The file will also exist in tthe `update-navigation-branch`: Open `index.html` and add the content below

- Add the content below
This is Tom adding Navigation to the AI-website


![gitstatus](./Img/L2%20Screenshot%205.png)


This simulates Tom's contribution to tthe project. This text represents the work he's doing on tthe navigation bar. In tthe real world, tthis will be an actual software code. 

-Check changes has not been staged

![gitstatus](./Img/L2%20Screenshot%206.png)

At this stage, Tom has modified the file, but these changes haven't been prepared for a commit in Git. This is indicated by the file name appearing in red in the terminal output, signaling that the changes are recognized by Git but not yet staged.

- Stage Tom's changes:

`git add index.html`

![Stagechanges](./Img/L2%20Screenshot%207.png) 

This tells Git that you want to include the updates made to index.html in the next commit. It's like saying, "Okay, i'm happy with these changes and ready to record them"

Confirm changes have been staged for commit 

`git status` 
![](./Img/L2%20Screenshot%208.png)

Now, after staging the changes, the file name will appear in green in the terminal output. This colour changes signifies that the file has been successfully staged, making it ready for the next step, which is committing these changes to the project's history.

Commit Tom's changes 

`git commit -m "Update navigation bar"`

![](./Img/L2%20Screenshot%209.png)

This takes the staged changes and records them in the repository's history with a messgae describing what was doen. This commit is a milestone, marking a specific pointt in the project's development 

- Push Tom's branch to Github:

`git push origin update-navigation`

![](./Img/L2%20Screenshot%2010.png)


This sends Tom's commits from your local branch on your laptop to GitHub (Remote Repository). It's like publishing your work so that others (or in this case, Jerry") can see and interactt with it.  This step updates the remote repository with Tom's contributions 
![](./Img/L2%20Screenshot%2011.png)

After completing Tom's workflow, you will now simulate Jerry's contribution to the project. To do tthis, you'll

-Switch back to the main branch
Create a new branch for Jerry
Make changes, and then
Stage, commit and push these changes to GitHub.

2. Jerry's Work:

Switch back to the Main Branch:

`git checkout main`

![](./Img/L2%20Screenshot%2012.png)

This command switches your current working directory to the main branch, ensuring that jerry start from the latest version of the project.

- Pull the latest changes:

`git pull origin update-navigation`

![](./Img/L2%20Screenshot%2013.png)

This ensures that you have the latest updates from the repository, including Tom's merged changes, if any.

Create a New Branch for Jerry's Work:

`git checkout -b add-contact-info`

![](./Img/L2%20snapshot%2014.png)

This creates a new branch where jerry will make his changes, keping them separate from the main project until they're ready to be merged.

Open index.html and Add Contact Information: Make your changes to the index.html file by adding contact information. This simulates Jerry' task.



![](./Img/L2%20Screenshott%2015.png)

Stage jerry's Changes 

`git add index.html`

This command stages the changes Jerry made to the index.html file, preparing them for commit.

- Commit Jerry's Changes:

git commit -m "Add contact information"

This saves Jerry's changes in the branch's history, with a message describing what was done.

-Push jerry's Branch to GitHub:

`git push origin add-contact-info`

![](./Img/L2%20Screnshot%2017.png)

This command uploads Jerry's branch tot he GitHub repository, making it available for review and merging into the main project.



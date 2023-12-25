# Programming Cheatsheet

## Command Line
Change directory
```bash
cd PATH
```
Move or rename file or directory
```bash
mv CURRENT_PATH NEW_PATH
```

Copy contents of folder into another folder
```bash
cp -R PATH_TO_CURRENT_FOLDER/. PATH_TO_NEW_FOLDER
```

Zip a file or directory
```bash
zip -r NEW_PATH.zip CURRENT_PATH
```

## Conda
Create an environment
```bash
conda create --name ENV_NAME
```

Create an environment at ```PATH```
```bash
conda create --prefix PATH
```

Activate an environment at ```PATH```
```bash
conda activate PATH
```

Add package to conda environment at ```PATH```
```bash
conda install -p PATH PACKAGE
```

Remove an environment at ```PATH```
```bash
conda env remove --prefix PATH
```

## Git
Clone an existing repository for the purpose of modifying it
```bash
git clone HTTPS_URL
```

List all branches
```bash
git branch
```

Switch to ```BRANCH``` and create it if it does not exist
```bash
git checkout -b BRANCH
```

Check which branch you are on
```bash
git branch
```

Switch to ```BRANCH```
```bash
git checkout BRANCH
```

Check the status of changes you have made
```bash
git status
```

Move changes from your working directory to the staging area
```bash
git add .
```

Commit changes
```bash
git commit -m "MESSAGE"
```

Push changes to GitHub
```bash
git push origin main
```
If necessary, enter your GitHub email as your ```username``` and a personal access token as your ```password```.

Push a new branch to GitHub
```bash
git push -u origin BRANCH
```

Merge a branch with the main branch starting on ```main```
```bash
git merge OTHER_BRANCH
```

Push a new branch
```bash
git push --set-upstream origin BRANCH
```

Delete a branch
```bash
git branch -d BRANCH
```

See log of changes and press ```Q``` to exit
```bash
git log --oneline
```

Get the current version of the GitHub repository
```bash
git fetch
```

Get the current version of the GitHub repository and merge it with the local repository
```bash
git pull
```

Initialize a local folder as a Git repository
```bash
git init -b main
```

Link a local Git repository with a remote GitHub repository
```bash
git remote add origin https://github.com/USERNAME/REPOSITORY-NAME.git
```

Set your git email as your GitHub email
```bash
git config --global user.email "GITHUB_EMAIL"
```

Set your git name
```bash
git config --global user.name "NAME"
```

## Harvard FASRC Cluster
Open home folder
```bash
ssh USERNAME@login.rc.fas.harvard.edu
```

Check memory usage of home folder
```bash
df -h ~
```

Check memory breakdown within a directory
```bash
du -sh * .[^.]* | sort -rh
```

Copy file from local machine to cluster
```bash
scp PATH_TO_FILE USERNAME@login.rc.fas.harvard.edu:NEW_PATH
```

Copy directory from local machine to cluster
```bash
scp -r PATH_TO_FOLDER USERNAME@login.rc.fas.harvard.edu:NEW_PATH
```

View all available partitions
```bash
spart
```

View all jobs
```bash
jobs
```

View jobs that are running
```bash
squeue -u USERNAME -t RUNNING
```

Submit an interactive CPU job
```bash
salloc PARTITION -t MINUTES -n NUMBER_OF_NODES --mem MEMORY_IN_MB
```

Submit an interactive GPU job
```bash
salloc PARTITION -t MINUTES -n NUMBER_OF_NODES --mem MB --gres gpu:NUMBER_OF_GPUs
```

Cancel all submitted jobs
```bash
scancel -u USERNAME
```

Resources
* [Documentation](https://docs.rc.fas.harvard.edu)
* [Email](mailto:rchelp@rc.fas.harvard.edu)
* [Office Hours Wednesdays 12-3 pm EST](https://harvard.zoom.us/j/97676134704)

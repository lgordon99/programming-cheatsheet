# Programming Cheatsheet
[Command line](#command-line)

[Conda](#conda)

[Tmux](#tmux)

[Git](#git)

[Vim](#vim)

[Harvard FASRC Cluster](#harvard-fasrc-cluster)

## Command line
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

Check memory breakdown within a directory
```bash
du -sh * .[^.]* | sort -rh
```

Copy file from local machine to remote server
```bash
scp PATH_TO_FILE USERNAME@SERVER:NEW_PATH
```

Copy directory from local machine to remote server
```bash
scp -r PATH_TO_FOLDER USERNAME@SERVER:NEW_PATH
```

Copy large directory
```bash
rsync -ah --progress --stats DIRECTORY_PATH NEW_PATH
```

Copy large directory from remote server to local machine
```bash
rsync -avzP USERNAME@SERVER:DIRECTORY_PATH NEW_PATH
```

## Conda
Create an environment
```bash
conda create --name ENV_NAME
```

Create an environment at ```PATH``` with pip
```bash
conda create --prefix PATH pip
```

Activate an environment at ```PATH```
```bash
conda activate PATH
```

Install packages from a `requirements.txt` file
```bash
pip install -r requirements.txt
```

Add ```PACKAGE``` to conda environment at ```PATH```
```bash
conda install -p PATH PACKAGE
```

Remove an environment at ```PATH```
```bash
conda env remove --prefix PATH
```

List all environments
```bash
conda env list
```

## Tmux
Create a new session with ```NAME```
```bash
tmux new -s NAME
```

Attach to an existing session with ```NAME```
```bash
tmux attach -t NAME
```

See list of active sessions
```bash
tmux ls
```

Detach from a session: ```Ctrl-B``` ```D```

Move one pane up: ```Ctrl+B``` ```up-arrow```

Move one pane down: ```Ctrl+B``` ```down-arrow```

Enter scroll mode: ```Ctrl+B``` ```[```

Exit scroll mode: ```q```

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

Merge a branch with another, starting on the branch you want to merge INTO
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

Delete a git folder locally
```bash
rm -rf FOLDER
```

Stop tracking a file but keep it in your local folder
```bash
git rm --cached FILE
```

Stop tracking a folder but keep it in your local folder
```bash
git rm -r --cached FOLDER
```


## Vim
Open a file at PATH with Vim
```
vim PATH
```

Enter edit mode
```
i
```

Exit edit mode
```
esc
```

Save changes and close file
```
:wq
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

View all available partitions
```bash
spart
```

View jobs that are running
```bash
squeue -u USERNAME -t RUNNING
```

Check the status of a particular job
```bash
sacct -j JOB_NUMBER
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

Cancel a particular job
```bash
scancel JOB_NUMBER
```

Resources
* [Documentation](https://docs.rc.fas.harvard.edu)
* [Email](mailto:rchelp@rc.fas.harvard.edu)
* [Office Hours Wednesdays 12-3 pm EST](https://harvard.zoom.us/j/97676134704)

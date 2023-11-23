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

Zip a file or directory
```bash
zip -r NEW_PATH.zip CURRENT_PATH
```

## Conda
Create an environment
```bash
conda create --name ENV_NAME
```

Activate an environment at ```PATH```
```bash
conda activate PATH
```

Add package to conda environment at ```PATH```
```bash
conda install -p PATH PACKAGE
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


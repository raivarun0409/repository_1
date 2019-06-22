# Repository_1

A test repository to see how git works

Steps to be taken to check and upload any changes to the repository:

1. git status (to check the untracked change to the repo on the machine)
2. git add <filename.ext> (track the file, staging also a name to this step)
3. git commit -m "Initial commit" (commited a file or directory but not yet sent)
4. git push origin master


Remember:
1. git diff <filelanme> (this is to see the new changes done in the already exixting file on github)

########################################################################################################################

1. git init (to create a new repository on a local machine)
2. git clone (to copy (download) an already existing repository from github)
3. git remote add origin "link_to_the_remote_repository" (connecting the local repository made by 'git init' command to the remote repository)
4. git pull origin master (to copy the content of remote repository to the local repository)
5. git add -A (adding all the new and modified files to the index at once)
6. git commit -a -m "message_here" (commiting all the new and modified files at once)
7. git log (this shows all the stored commits and with a 14 digit hex-code)

Branching are pointers to a specific commit. They are of two types: 
1. Local branches (these ate these branches which are going to be created in our workspace and are going to be be work with the files in the local repository)
2. Remote tracking branches (these are the branches which are going to connect the branches from the local repository to the central repository)


8. git branch <branch_name> (create a new branches containing all the content of the branch from which it was created)
9. git checkout <branch_name> (to enter another branch and the process is called checking-out)



########################################################################################################################

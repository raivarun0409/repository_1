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
8. git branch <branch_name> (create a new branches containing all the content of the branch from which it was created)
9. git checkout <branch_name> (to enter another branch and the process is called checking-out)
10. git merge <branch_name> (merges and modifies the content in the current branch, can be main, but keeps the branch as it is and keeps its content as it is. So, can still access that branch and modify it)
11. git rebase <branch_name> (att the conent of the branch_name got merged in the curent branch, but with an extra thing of the head being reattached to the head in the master)
12. git push origin <branch_name> (push all the changes, or, commits (maybe of, confirm, current branch only) on the local to the central repository in 'branch_name' branch. If it does not exist already, then a new repository will be created with the name 'branch_name'. It can also be master if the content is supposed to be copied in the master branch)

## Non-linear development: (branching, merging, rebasing, pulling, commiting)

# Branching
Branching are pointers to a specific commit. They are of two types: 
1. Local branches (these ate these branches which are going to be created in our workspace and are going to be be work with the files in the local repository)
2. Remote tracking branches (these are the branches which are going to connect the branches from the local repository to the central repository)

# Stashing
Git stashing is a process in which if you are not sure about the branching in which the changes are done, you can save it differently by stashing away from your main content and can access the data when you want later.
1. git stash (stashing the current directory as a whole)
2. git stash pop (to open the saved stash later when you are done with the editing and see the previous content where stashed)

# Rebasing
Rebasing is same as merging but, it is made to reduce the number of branches to reduce complexity of the project. The rebasing is different from merging as merging just merges the changes in a particular branch to main and does not changes the structure of the repository i.e., not hindering the branch and main file flow structure. But, the rebasing chnages the tip of the commits of the branch to the main file to make the structure simple:
Original Structure:
C1---------C2---------C3-----------Master
           C2-----------new_branch

Structure after rebasing:
C1---------C2----------C3-----------C4
                    Master        new_branch

# SSH key:
1. see the option of SSH at the url place and see the option of clone with SSH there
2. To connect with SSH, generate a public SSH key on the device and add that key to the github account after which we can start pushing changes:
    a. ssh-keygen
    b. cat 'ssh_key_path_(id_urname.pub)' (to copy the ssh key in the file)
    c. On github, go to settings->SSH and GPG key->Nwe SSH Key->paste the key and add
    d. On device terminal: ssh -T git@github.com

# Git Flow:
1. Local: 1. Working directory; 2. Staging area; 3. local repo
2. Remote repo

git add: working directory to staging area
git commit: staging area to local repo
git push: local repo to remote repo
git pull: remote repo to local repo
git checkout: local repo to working directory
git merge: local repo to working directory

# Reverting:
1. git log (shows the hex of all the commits done till now. Find the commint to where you want ot revert to)
2. Copy the first 8 digits of the hex code 
3. git checkout <8_digits_copied_code_part> <file_name.ext> (reverts back to the situation when in the given commit situation only for the file called 'file_name.ext')

## Note:
1. If you are already having a file indexed earlier, you can directly use the commit command and it will do the indexing and comming all at once with single command and no need to give 'add' command
2. git pull (extarcts all the content of the central repository and adds everything in the local repository and at the right place where it belongs)
3. git fetch (extracts all the changed and new things from central repository and adds it into another branch, local, but not changing the content of the main branch of the local repository. Make sure that we are merging that in to main after fetch))
4. git pull = git fetch + git merge
5. As our repository is public, they can ,make changes also, but, to avoid such thing, we can connect central and local repository via SSH to make it secure and restricted so that the others in github community can clone or download the content, but, can't make changes to the original repository.

########################################################################################################################

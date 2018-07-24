•• Why do we use Git?<br/>
    Git is a version control system and we need to use one, especially for when a bug accidentally gets introduced into a project. Because Git is a really powerful, but also because it's free and is  open source. Version control systems allow users to create revisions of a project, view previous revisions of a project, and revert to a previous revision of a project. Imagine being able to use a VCS for your life...
<br/>

• What is the difference between Git and Github<br/>
    First, they're not the same thing (Oops, just realized that very similar sentence is on the Intro to Git page...). Github is a web-based service that acts as a remote backup service for git repositories by hosting repositories on a server and allows people (not just developers) to collaborate easily. Git is a powerful (and free!) version control system  
<br/>

• How does Git work?<br/>
    Git takes a repository that has been initialized with Git VCS and takes the data within the repository to store like a series of snapshots over time. Within this, files can be in three states: unstaged, staged, and committed. When you modigy files in your working tree, they become unstaged (i.e. they won't be saved on your remote repo). Then, you selectively stage those changes (git add [files or "."]) that you want to be within your next commit. Selectively meaning only those files with those changes will move to the staging area. From there, you do a commit (git commit -m "Something useful about your commit for future reference") and this takes the files from the staging area and stores that snapshot permanently to your Git directory. You can then "push" that commit to Github where you can keep track of those commits!  
<br/>

• What is a Git repository?<br/>
    A repository ("repo") is a directory on a laptop's file system that's been initialized with Git version control system. It's like a project that you have attached to this version control system so that you can continue to keep track of and update it. It's also helpful to go back and look at old versions within a repository to see how your code has become refined over time.
<br/>

• Initialize a Git repository<br/>
    Before doing this, you need to make sure that you're in the directory that your files exist within (cd [githubStuff]). Then, type 'git init'. You'll also need an uninitialized GitHub repo to connect it to. 
<br/>

• add and commit changes to a Git repository<br/>
    Any files that are brand new to the repository or that have been changed will need to be added so that git can start tracking them. To do this, either type "git add <filename>" or "git add ." The period adds all new files and changes in the directory. 
<br/>

• Add remote destinations to your local Git repository<br/>
    Adding a remote destination: "git remote add origin git@github.com:gracehartzell/GIT-assessment.git". You can also add a remote Git repo as a shortname that you can reference easily by running "git remote add <shortname> <url>". 
<br/>

• Push commits from your local Git repository to a remote repository<br/>
    If using GitHub or collaborating with another git repo, push new commits to the default remote by using "git push". From there, you can see any changes on the GitHub page. 
<br/>



Explain and be able to do the following:
- `Fork and Clone`  → `git clone` creates a Git repo copy from a remote source and adds the original location as a remote so that you can fetch from it again and push to it if you have permissions.
- `git add` → Adds the new files to the index content found in the working tree to prepare content staged for the next commit. 
- `git push` → "pushes" committed changes from your git repo to GitHub. Dubbed as the "launch" in Git:Rocketship::Github:Mars. After pushing, you should be able to see the changes you've made on your GitHub page.
- `git commit -m 'some message'` → 
If something is committed, the change was included in a previous revision (revision ≈ commit). The -m is a commit message to help track your changes (like the subject line of an email). If multiple -m options are given, their values are concatenated as separate paragraphs. *Committed changes still need to get pushed*
- `git push origin master` → sends the changes to the master branch of the remote repository. 
- `git remote -v` → Lists all currently configured remote repos. It's common practice to name the remote repository 'origin'.
- `git status` → Lists the files that you've changed and those that you still need to add or commit. 
- `git remote add [remote url here] ` → adds a new remote in the directory where your repo is stored. The options for git remote add are to either add origin as the remote name or add the remote URL (which is what this bullet is asking for). In this case, you can get the remote URL from GitHub using HTTPS or SSH (but use SSH because HTTPS isn't considered secure.)
- `git remote remove origin` → remove the remote repository named origin. All remote-tracking branches and configuration settings for the remote are then removed.
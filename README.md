# kaggle-aptos19-challenge
Repository for Udacity Facebook Secure and Private AI Scholarship Challenge scholars to collaboratively compete in the Kaggle APTOS 2019 Blindness Detection challenge 

# Getting Started with Git and GitHub
1. Download and install Git client from [here](https://git-scm.com/downloads)


2. Setup your Git client as explained in [this](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) article


3. Clone this repository by typing `git clone https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git`

  *If you're having trouble copy-paste ing using Ctrl-C Ctrl-V, use Ctrl-Insert Shift-Insert*



4. Enter `cd kaggle-aptos19-challenge` to move into the project directory


5. Try executing `git remote --v`. You'll get this output

    ```
    origin  https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git (fetch)
    origin  https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git (push)
    ```
    This means that the remote repository(github repo) corresponding to the local git repo we have in our computer is at this address *https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git*

    * *fetch* - git for get-ting :) info about any updates from your remote repo
    * *push* - git for syncing the remote repo with new updates in your local repo

    Nb: No, *fetch* isn't opposite of *push*. Don't be dumb even a toddler will tell you it's **pull** :). The caveat being *fetch* only gets info about any update of your remote repo but doesn't add those updates to your local repo and in case you're wondering 
    > pull = fetch + merge


6. Now try this `git status`

    If you haven't made any changes to the files or folders after cloning the repo you'll get this output
    ```
    On branch master
    Your branch is up-to-date with 'origin/master'.
    nothing to commit, working directory clean
    ```
    Line 1: Mentions that we're currently in a branch called **Master**.

    Git allows to create different branches for a project. For example, we could have a *development branch* and a *production branch*. In most cases, the main branch will be **Master** and we can create other branches for working on new updates and merge these branch to the **Master** branch once we have tested all our updates and made sure the code doesn't break

    Line 2: Denotes that our *master* branch is up-to-date with the *origin/master* which is the *master* branch of our remote repo

    Line 3: Points to the fact that we haven't made any changes to our *local* branch after the last *commit*

    * *commit* - is like a save of our current work to Git
    * One or more commits form a *push* where we update the remote repo with our local updates


7. Now, let's make some changes. Add your jupyter notebook to the git folder. Let me add **APTOS19.ipynb** to the *kaggle-aptos19-challenge* folder. Ok, try executing `git status` again - no you won't get the earlier message or rather you shouldn't - Things doesn't happen the same way twice in life :)
    ```
    On branch master
    Your branch is up-to-date with 'origin/master'.
    Untracked files:
      (use "git add <file>..." to include in what will be committed)

            APTOS19.ipynb

    nothing added to commit but untracked files present (use "git add" to track)
    ```
    We have some familiar lines in there and there are some newcomers too!

    Line 3: Untracked - you aren't tracking those files in your repo
    Line 4: That's *git* being a good *Samaritan*. It's kind enough to tell us that we have to add files to the *staging* area to track them for including in the next *commit*
    Line 5: Lists out all new files. Welcome, Messieurs and Mesdames!
    Line 6: Yeah, I know you understand what that is.


8. We'll use the command kindly suggested by *Git* to track the new files for committtttttttting - sorry bad keyboard(P.S Patreon link below - just kidding :) - it's actually on the top)


    Enter `git add APTOS19.ipynb` or your filename in place of *APTOS19.ipynb* to track that file

    * For all those who are wondering what if - yes what if we have multiple files - just enter the command multiple files. But, there's always a *BUT*, this is *Computer Science* we're talking about and there's always an easy way(or two):
    1. `git add newfile1 newfile2 newfileinfinity`
    Or if you are like me and don't wan't to copy paste the file names - magic!
    2. `git add .` - yes `.` is powerful! But be aware that it adds all new files even the pesky files system files - for example .git, .ipynb_checkpoints - and no it isn't `.` adding all it's relatives but because `.` is generally used in bash to denote the current folder and here it just adds all new files in the current folder

    Nb: You might get a warning saying that *LF will be replaced by CRLF in APTOS19.ipynb*. It's sort of converting how line endings are stored internally - differs with operating systems.


9. Now, what? Yes, `git status` and 
      ```
      On branch master
      Your branch is up-to-date with 'origin/master'.
      Changes to be committed:
        (use "git reset HEAD <file>..." to unstage)

              new file:   APTOS19.ipynb
      ```
      Line 4: Suggests to use the command `git reset HEAD filename` to remove any files from the staging area(stack of files to be committed)
      P.S I wasn't referring to the *STACK* but the english *stack*. Actually, now that I think of it I should check how staging area is implemented

      Nb: *HEAD* is like a pointer to our most recently committed state of the repo

      Now would be a good time to get some Git lessons (Credits: https://git-scm.com/book/en/v1/Getting-Started-Git-Basics) :
      * Git has three main states that your files can reside in: 
              1. Modified - means that you have changed the file but have not committed(saved) it to your database yet
              2. Staged - means that you have marked a modified file in its current version to go into your next commit
              3. Committed - means that the data is safely stored in your local database
      * This leads us to the three main sections of a Git project: 
              1. The *Git directory*:
                      * Where Git stores the metadata and object database for your project
                      * The most important part of Git, and it is what is copied when you clone a repository from another computer
              2. The *working directory*:
                      * A single checkout of one version of the project
                      * These files are pulled out of the compressed database in the Git directory and placed on disk for you to use or modify
              3. The *staging area*:
                      * A simple file, generally contained in your Git directory, that stores information about what will go into your next commit
                      * It’s sometimes referred to as the index, but it’s becoming standard to refer to it as the staging area

      * The basic Git workflow goes something like this:

              1. You modify files in your working directory
              2. You stage the files, adding snapshots of them to your staging area (`git add file`)
              3. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory (`git commit file`)

      * If a particular version of a file is in the Git directory, it’s considered *committed*. If it’s modified but has been added to the staging area, it is *staged*. And if it was changed since it was checked out but has not been staged, it is *modified*


      P.S Where were we? I seriously can't find the last step... Ah, found it. We had added files for committing or with our newly acquired knowledge allow me to say *staged*


10. Now, from the Git workflow from above, we need to commit the staged files. You do that by entering `git commit`. So, the thing is commits are like checkpoints and for us to navigate back and forth(if required) it's better we add a *title* to our commit. But, don't worry our good friend Git will remind you(or should I say force) to add a title for your commit.

      If you have a default text editor configured it will open up, enter some info about what your commit has/is and close it.

      Nb: If you don't want to wait for your fancy editor to show it's glorious face, use `git commit -m "This is my new commit"` - Told you na, there's always a workaround


      Let's take a step back and recall why we did all this. Hmm... Hmm...
         > Yes, got it. We wanted to include our ground-breaking update to the exisiting Github repo


11. Syncing the remote repo with our local updates(commits) - **Push**. And the command is 'git push origin master` i.e, we need to push our local updates to the *master* branch in the repo denoted by *origin*

    For all those who was excited enough to execute the above command - you would have either got an error() or you will have got - yes an error for you too - because you don't have the permission to update the remote repo


You will be prompted to confirm that you authenticity of the host - why wouldn't you :) - enter *yes* 

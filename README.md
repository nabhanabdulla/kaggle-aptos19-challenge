# kaggle-aptos19-challenge
Repository for Udacity Facebook Secure and Private AI Scholarship Challenge scholars to collaboratively compete in the Kaggle APTOS 2019 Blindness Detection challenge 

# Getting Started with Git and GitHub
1. Download and install Git client from [here](https://git-scm.com/downloads)
2. Setup your Git client as explained in [this](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) article
3. Clone this repository by typing `git clone https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git`
4. Enter `cd kaggle-aptos19-challenge` to move into the project directory
5. Try executing `git remote --v`. You'll get this output
```
origin  https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git (fetch)
origin  https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git (push)
```
This means that the remote repository(github repo) corresponding to the local git repo we have in our computer is at this address *https://github.com/nabhanabdulla/kaggle-aptos19-challenge.git*

6. Now try this `git status`
If you haven't made any changes to the files or folders after cloning the repo you'll get this output
```
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```
Line 1: Mentions that we're currently in a branch called **Master** Git allows to create different branches for a project. For example, we could have a *development branch* and a *production branch*. In most cases, the main branch will be **Master** and we can create other branches for working on new updates and merge these branch to the **Master** branch once we have tested all our updates and made sure the code doesn't break

Line 2: Denotes that our *master* branch is up-to-date with the *origin/master* which is the *master* branch of our remote repo

Line 3: Points to the fact that we haven't made any changes to our *local* branch after the last *commit*

* *commit* - is like a save of our current work to Git
* One or more commits form a *push* where we update the remote repo with our local updates



You will be prompted to confirm that you authenticity of the host - sure you do - enter *yes* 

# Free Code Camp -- Git: 0 To Production

<div align="center">
   <div style="float: left; margin-right: 10px; padding-left: 20%;">
      <img height="200px" width="200px"src="img/fcc.jpeg"/>
   </div>
   <div style="float: left;">
      <img height="200px" width="200px"src="img/git.png"/>
   </div>
</div>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## What To Expect From This Talk

---

1. Learn about some basic git commands
2. helpful git paradigms (Branching)
3. Git workflows for both personal and collaborative settings
4. To get inspired to learn more about leveraging Version Control for your work

All presented materials will be available at [[[This Link]]](https://github.com/BryanJenksCommunity/Talks/tree/main/2021-05-15-FCC-Git-0-to-Production)

---

## Who Am I?

---

- TallGuyJenks
  - (DevOps) Information Technology Associate @ Covered California
    - [CV](https://github.com/tallguyjenks/CV/blob/master/CV.pdf)
  - [YouTuber](https://www.youtube.com/c/BryanJenksTech?sub_confirmation=1)
    - [General Social Media Person](https://streamerlinks.com/tallguyjenks)

---

## Jumping Right In

---

### What Is Git?

---

> Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
> -- <https://git-scm.com/>

---

### Where Did Git Come From?

---

Linus Torvalds, Creator of the Linux kernel.

<https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git>

---

### Why Is Git Useful?

#### In General

---

- Distributed collaborative work
- fast, efficient, small snapshots
- & CLI tools are hyper efficient

---

#### In Practice

---

- Allows people to work independently of each other
- No check in/check out system where you have to wait on each other to work on code
- Complete history of the code (Retention & roll back)
- Branching is cheap
- can be efficiently used on the CLI while also having a plethora of GUI based tools to simplify the process

---

### Differences Between Git For Personal Projects & Git For Production

---

### Personal

---

Personal projects depending on size and scope might not need to do much more than make changes to the master/main branch i.e. "Production".

No one else is really touch the code, so you make your changes, and push them up and that's the end of it.

You may branch to do feature branching and after merging you are still done.

Lets work through that.

**NOTE:** *All instances of brackets indicate a piece of input to be replaced, brackets and all text inside them should be replaced with your input.*

0. Have git installed
1. Make an empty repo on github: <https://github.com/new>
2. open your CLI
   1. recommend git bash on windows: <https://git-scm.com/downloads>
   2. Linux: anything should work
   3. MacOS: Terminal, iTerm2, etc
3. Navigate to where you want your repo placed using the CLI commands:
   1. `cd`, `pwd`, `ls`
4. Pull the repo down to your machine: 
   1. `git clone <URL>`
   2. `git status`
   3. `git branch`
5. Now we're ready to get started!
   1. from here on we can use VSCode to open the repo directory or continue with Vim in the CLI
6. Make a document `README.md`
7. Add some content to it then save it
8. check the repo status `git status`
9. Changes have been made from the snapshot we want to publish those to production. How?
    1. `git add README.md`
    2. `git commit -m "< MY COMMIT MESSAGE>"`
    3. `git push`
    4. check remote (what does remote v.s. local mean?)
10. You're done! thats basically the personal workflow.

---

Making changes, staging, committing, and pushing them to the remote.

If we had a more robust personal workflow we could add branching into the mix. What is branching? Why is it useful? What does it mean in the context of my repo and my work?

<div align="center">
   <div style="float: left; margin-right: 10px;">
      <img height="300px" width="300px"src="img/branch2.png"/>
   </div>
   <div style="float: left;">
      <img height="300px" width="300px"src="img/branch.png"/>
   </div>
</div>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<!-- Source: https://www.nobledesktop.com/image/gitresources/git-branches-merge.png -->
<!-- And: https://blog.seibert-media.net/wp-content/uploads/2015/07/Git-Branches-1.png -->

---

1. check your current branch `git branch`
2. make a new branch `git branch <BRANCH-NAME>` (no spaces)
   1. alternatively combine the next step with this one using: `git checkout -b <BRANCH-NAME>`
3. switch to your new branch `git switch <BRANCH-NAME>`
4. Then repeat your workflow above **WITH A NEW FILE** until you get to step 11.3, the `git push`

---

The branch `<BRANCH-NAME>` doesn't exit on the remote repo only the local, your machine. You need to push not just you commit, but the whole branch up to the remote repo. Why? The PR (pull request) process, How?

---

1. at this point you're on `<BRANCH-NAME>`, you've staged (`git add <YOUR NEW FILE>`), committed (`git commit -m "<YOUR COMMIT MESSAGE>"`) and are ready to push your branch to the remote.
2. to push the branch to the remote repo so the remote reflects your local repo branches and all, push the branch with: `git push origin <BRANCH-NAME>`
3. Now the branch is on github ready for the PR process and to be merged.
4. Before requesting a merge or after getting feedback you want to make some final revisions to the code, for this all you need to do is:
   1. make sure you're on the feature branch `git branch`
   2. make your changes
   3. stage them `git add <FILE NAME>`
   4. commit them `git commit -m "<YOUR COMMIT MESSAGE>"`
   5. push them `git push`
5. Merge on Github or you can always merge locally by
   1. return to "production" branch (master/main) with `git switch master`
   2. then merge `git merge <BRANCH-NAME>`
6. If merging on the remote repo (Github) You'll want to update your local copy of "Production" with `git pull`
7. if you're done with that branch and have no further use for it, tidy up with `git branch -d <BRANCH-NAME>`
8. You'll want to have an updated work tree (this is very easy to see in the Git Graph Extension) so also run `git fetch --prune` to prune the tree of deleted branches.

---

And thats the branching workflow. Extra effort, but more control of features and merging code into production. Rollback on entire features, but just individual commits.

There are many codified workflows, but this "work in prod" is probably the most common personal workflow. So how would a workflow look like in production?

Honestly, much the same as the personal branch workflow. KISS method. Add a few more "Production-like" branches and you're set.

---

<img src="img/multi_branch_prod_workflow.png"><br>
<!-- Source: https://i.stack.imgur.com/F00b8.png -->

---

1. `git branch dev`
2. `git push origin dev`
3. `git branch test`
4. `git push origin test`
5. `git branch feature dev`
6. `git switch feature`
7. make a new doc, add, stage, commit
8. `git push origin feature`
9. on GitHub review the PR, if approved; Merge someones feature to the `dev` branch
   1. `git switch dev`
   2. `git merge feature`
10. after further development and maybe unit test creation etc. merge to `test`
    1. `git switch test`
    2. `git merge dev`
11. Nothing broke? the code is ready for production? then merge it into production!
    1. `git switch master`
    2. `git merge test`

---

In essence, the branching workflow is the same, but instead of merging straight to production, you marge into staging branches and cascade those merges into production.

Having everyone branching from a specific branch with `git branch <NEW-BRANCH> <FROM-BRANCH>` like the `dev` branch makes it so that `dev` is where all the action is like `master`/`main` for the personal workflow, but we're not in the wild west shooting from the hip, we can't impact users and the business, so we don't move straight to production.

We first move the code to staging areas for information and formal release. Merge to `test` so we can test the code in a gold copy of production, and finally once ready merge your tested code from `test` into `master`/`main` and give it a tag as a format release to your Organization/users.

---

### Making It Easier

---

Now they you've used Git on the command line and worked through the whole process, you might still not be really pleased with the experience. Understandable, the command line is not for everyone. There are a few Git tools that i've used in production that i think are incredibly helpful and greatly simplify the experience.

- GitLens: `eamodio.gitlens`
- Git Graph: `mhutchie.git-graph`
- Git History: `donjayamanne.githistory`
- Git Tags: `howardzuo.vscode-git-tags`

---

### BONUS: Stashing

---

Stashing is incredibly handy when you made changes to some files on the wrong branch and you want to pick up all those changes and just dump them onto the correct branch with minimal effort.

---

1. On your current branch run `git stash push -u`
2. see your current stashed changes `git stash list`
3. switch to desired branch `git switch <BRANCH-NAME>`
4. apply the stashed changes to current branch `git stash pop`

---

Easy way to quickly transfer some changes around branches when you forgot to switch to the right one.

---

### More Advanced Topics Not Covered

---

- interactive rebasing
- Cherry picking
- Git BARE repo's with work trees
- Git Aliases
- Git Hooks

---

### Resources

#### Documentation, Tutorials, Information

---

- <https://git-scm.com/book/en/v2>
- <https://git-scm.com/docs>
- <https://learnxinyminutes.com/docs/git/>
- <https://ndpsoftware.com/git-cheatsheet.html>
- <https://learngitbranching.js.org/>

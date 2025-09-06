### Answer the following questions in you own words.

> It's not necessary that you havee to know and answer all the questions. Just answer the ones
> you know and write in your own words.

1. Give the difference between the remotes - upstream and origin - with an example.

You answer: Origin is your forked repository, while upstream is the main repository which you fork from.

2. You have two branches A and B and you have currently made some changes in branch A.
You want to move into branch B but do not want to commit the current changes in branch A.
What will you do?

You answer: I would stash the changes using the git stash command, use git checkout to change the branch to B, make the changes there and then move back to branch A using git checkout again.

3. You were assigned a work to implement a feature and create a PR to your organization's remote repository.
For this you made a branch (say A) and made some changes and commited them. Now you moved to some other branch 
(say B) to do some other assigned work. But later you realisd that have to complete the task assigned earlier 
first and commited some changes in branch B which are meant for branch A. How will you use git to bring the 
changes from branch B to branch A?

You answer: I would use git cherry-pick followed by the hash of the commit which i want to move and move the commit from the given branch to another branch.

3. What is the difference between fetching changes and pulling changes?

Your answer: Git fetch just downloads the commits etc from the Git repository from the repository to your local copy, while git pull is a is basically git fetch + git merge command in one, as it also merges the changes and you'll have to resolve the conflicts too.

4. What does -i flag stand for? What is it's significance in git?

You answer: The -i flag stands for interactive, I've used this flag for the git rebase command.

5. You are working in an organization that follows very strict guidelines for PRs and commits.
You made three commits in your PR and the maintainer says you were supposed to make a single commit.
What will you do in this case?

You answer: You can squash the commits using git rebase.

6. Explain `git merge` and `git rebase` with example(s).

You answer: git merge does not change the commits, while git rebase is used to change the commits, merge is quite the opposite of rebase if you think about it, since merge is quite literally used to preserve the commits, while rebase is used to change them. Example: you can use the git merge to merge changes in two branches, while you can use the git rebase to change up the commit history.

7. Write the flow how you create a repository and push changes to it. Also mention the commands used at each step.

You answer: You can initiate a repository on your local machine by navigating to the folder then using the git init command, this command would add a .git directory, which will help git in tracking the changes, next you can add files and make whatever changes you want, then make the repository on your github account and copy the link of the repository and use the command to add the origin which is git remote add origin followed by the link that you copied, then you use the git add . command to stage all the files for commiting, then you use git commit -m followed by commit message of your choice, then push the changes using git push origin main.

8. How would you prevent a file or folder from getting tracked by git?

Your answer: Put it in the .gitignore file

9. You did not implement the step you mentioned in question 8 and now you have committed and pushed your database's
secret key to the github. How will you remove the key from your git's commit history to avoid any misuse?

You answer: You can use the git filter -repo command followed by the --path and the path of the actual file in your repository, it'll remove the existence of that file from the entire history, and then force push the changes, then after that you can put that file in the .gitignore to prevent it from getting tracked in the future commits.

---
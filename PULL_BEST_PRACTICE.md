How To Make Good Pull Request
=============================

* Fork a repository
* Clone locally
* Branch

> git checkout -b my-feature-branch

or

> git branch --track my-feature-branch origin/my-feature-branch
> git push -u

* modify the branch with the new feature
* Commit

> git commit -am 'Leave helpful description here'

* make more commit if needed

> git commit -am 'Leave helpful description here'

* check how many commit you have done, and rebase head~ with the same number (if 3 commit, use HEAD~3)

> git rebase -i HEAD~3

* "pick" the first commit, and "squash" the other. if you need to change the log message, "reword" instead, then redo the rebase command.

* Push the branch

> git push origin my-feature-branch

* from GitHub go to the branch now created and submit a pull request following the details needed until
* From your forked repository, select your branch, which contains the changes that you're going to submit and click the Pull Request button. The original repository that you originally forked from will be highlighted below the current repository's name.
* Provide a brief description that explains your contribution and why you are making the pull request. Make sure you add "CONTRIB:" in the title of the pull request. Click the Send pull request button to complete the submission.
* The owner of the original repository will receive your pull request notification. The owner can then test and choose whether or not to merge the changes into the original repository.

> git merge --no-ff my-feature-branch

> git branch -D my-feature-branch

> git push origin :my-feature-branch

* Smile and wave, just smile and wave... 

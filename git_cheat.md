if you fork a repo and the original repo get updated how will the fork repogets the lastest update

When you fork a repo on GitHub, you create a copy of the original repository (called the upstream repo). If the original (upstream) repo gets updated, your forked repo doesn't automatically receive those updates. 
You need to manually sync your fork with the upstream repository.

https://chatgpt.com/share/68833de9-d368-8006-80f2-eee50cf1ac60

git cheat sheet
When you fork a repo on GitHub, you create a copy of the original repository (called the upstream repo). 
If the original (upstream) repo gets updated, your forked repo doesn't automatically receive those updates.
You need to manually sync your fork with the upstream repository.

1. Add the original repo as a remote (upstream)
```
git remote add upstream https://github.com/ORIGINAL_OWNER/REPO_NAME.git

Check the remotes to confirm:
git remote -v
You should see:

ng
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
upstream  https://github.com/ORIGINAL_OWNER/REPO_NAME.git (fetch)
2. Fetch the latest changes from the upstream repo

git fetch upstream
3. Merge upstream changes into your local branch (e.g., main)

git checkout main
git merge upstream/main
Or if you want a cleaner history:

git checkout main
git rebase upstream/main
4. Push the updated branch to your GitHub fork

git push origin main
🧠 Summary
Action	Command
Add original repo	git remote add upstream ...
Fetch changes	git fetch upstream
Merge to your local main	git merge upstream/main
Push to your fork	git push origin main
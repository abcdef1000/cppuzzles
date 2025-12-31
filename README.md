# cppuzzles

A minimal collection of competitive programming puzzle prototypes. Open `index.html` in your browser to try the centroid decomposition direction-finding puzzle. Use the node count control to pick the tree size, then click nodes to accumulate directional arrows until you locate the hidden centroid.

## Resolving merge conflicts (cheat sheet)
If GitHub warns about conflicts when you try to merge changes, pull the branch locally and resolve the markers before pushing:

1. `git fetch origin` then check out the branch you want to merge and run `git merge origin/main` (or the target branch).
2. Run `git status` to see conflicted files. Open each file and look for markers like `<<<<<<<`, `=======`, and `>>>>>>>`.
3. Decide which pieces to keep—often parts from **both** sides—then delete the markers manually. Avoid blindly choosing “Accept incoming/current” for every hunk unless you intend to discard the other side.
4. Once a file is fixed, stage it with `git add <file>`.
5. When all conflicts are staged, complete the merge with `git commit` (or `git merge --continue` if using `rebase`/`pull --rebase`).
6. Push the branch and open/refresh the pull request; GitHub should now show it as mergeable.

If you accidentally accepted the wrong side everywhere, you can restart the merge with `git merge --abort` and try again, or restore a specific file from the target branch with `git checkout --theirs <file>`.

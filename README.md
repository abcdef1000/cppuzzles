# cppuzzles

A minimal collection of competitive programming puzzle prototypes. Open `index.html` in your browser to try the puzzles:

- **Centroid decomposition direction finder:** Pick the node count, then click nodes to grey out impossible regions until you locate the hidden centroid. After you win, the page shows your attempt count and replays the optimal centroid-decomposition search so you can compare strategies. Centroid edges use a simple styling so the grey-out hints stay clear.
- **Dijkstra shortest-path tracer:** Pick the graph size, then click edges from node 0 toward node N. Edges off any shortest route turn red; optimal choices turn green. Reveal the full Dijkstra visitation order and the optimal path with the answer button. Dijkstra edges alone carry the hover and glow effects.
- **Saved examples for both puzzles:** Each puzzle includes two editable example slots. Choose an example tab to view its text definition, click **Save** to persist it in your browser, and **Load into puzzle** to use it immediately. Formats:
  - Centroid: first line is `N`, followed by one edge `a b` per line.
  - Dijkstra: first line is `N E`, followed by weighted edges `a b w` per line.

## Resolving merge conflicts (cheat sheet)
If GitHub warns about conflicts when you try to merge changes, pull the branch locally and resolve the markers before pushing:

1. `git fetch origin` then check out the branch you want to merge and run `git merge origin/main` (or the target branch).
2. Run `git status` to see conflicted files. Open each file and look for markers like `<<<<<<<`, `=======`, and `>>>>>>>`.
3. Decide which pieces to keep—often parts from **both** sides—then delete the markers manually. Avoid blindly choosing “Accept incoming/current” for every hunk unless you intend to discard the other side.
4. Once a file is fixed, stage it with `git add <file>`.
5. When all conflicts are staged, complete the merge with `git commit` (or `git merge --continue` if using `rebase`/`pull --rebase`).
6. Push the branch and open/refresh the pull request; GitHub should now show it as mergeable.

If you accidentally accepted the wrong side everywhere, you can restart the merge with `git merge --abort` and try again, or restore a specific file from the target branch with `git checkout --theirs <file>`.

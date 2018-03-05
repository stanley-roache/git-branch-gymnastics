# git-branch-gymnastics

Just going to keep a list here of my experiments..

1. Create two branches off the master branch, make a different file in each, then see what happens on merge

- I created two branches, b1 and b2 locally with checkout -b
- I added a different file to each of these
- I set push.default to matching to see if I could push both branches at once
- On push, neither branch showed up on the remote!
- back locally, I used git push -u origin 'branch name' once for each branch to create those branches remotely
- for some reason both new files showed up on the b2 branch!
- I used git checkout 'branch_to_steal_from' path/to/file/to/steal to copy one of the files to it's intended branch
- I couldn't figure out how to push all respective changes to their branches, still had to do one push within each branch.

Now I have a situation where the readme file (this) is furthest forward on the master (changes made since point of branching) and the branches formed each have one new file.

The challenge is to somehow merge both branches into master in a way that keeps the updated readme file.

From what I can gather, a merge request from the master branch will automatically combine a new commit with all the changes included, a merge-commit, a commit with more than one parent that combines branches. See what happens...

Success! Well that's pretty straight forward. An interesting point to go to from here would be to investigate cases where simple merges don't work ie. conflict

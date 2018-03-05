# git-branch-gymnastics

Just going to keep a list here of my experiments..

1. Create two branches off the master branch, make a different file in each, then see what happens on merge

- I created two branches, b1 and b2 locally with checkout -b
- I added a different file to each of these
- I set push.default to matching to see if I could push both branches at once
- On push, neither branch showed up on the remote!
- back locally, I used git push -u origin <branch> once for each branch to create those branches remotely
- for some reason both new files showed up on the b2 branch!
- I used git checkout <branch_steal_from> path/to/file/to/steal to copy one of the files to it's intended branch
- I couldn't figure out how to push all respective changes to their branches, still had to do one push within each branch.


Now I'll see what happens on merge!

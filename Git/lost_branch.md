#### Have you ever lost a git branch?

Don't worry, it's probably still there until git does a GC. It's just not visible because nothing is pointing to that commit.
When this happens don't panic, just execute this command:
```Bash
git reflog
```
This will show a log of all the operations done, with the most recent at the top. You can write down all the hashes that look familiar to recover the branch.
```Bash
git branch tmp <your_hash_here>
```

This will create the branch "tmp" at the specified hash.
```Bash
git checkout tmp
```

Check out this branch make sure it's the one you're looking for and you can move or create the old one back where it belonged before everything went ballistic.
A: If you still have the old branch:
```Bash
git checkout oldBranch
git reset --hard tmp
```
B: If you don't have the old one you can simply recreate it
```Bash
git branch tmp oldBranch
```

And of course we delete the temporary branch.
```Bash
git branch -d tmp
```

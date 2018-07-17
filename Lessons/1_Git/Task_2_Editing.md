## The first changes
Working with git isn't that much different than your normal workflow.
You edit files, probably break something, try to make it work, spend a day on debugging a small thing until eventually you notice a missing variable assigment... Err, where was I?

Oh, right, and when eventually things do sorta work, you *commit*. Committing means telling git
you want to save your changes, and it's really important to do often and reglary.  
We'll get to that in a moment, but there's one thing I want you to do before that:

### Branching out
Let's say you want to try out a new idea, but you *really* don't want to mess up the code that already works.
That's where branches come into play.

Imagine it like a "Time-Out Box" for code. Everything you do stays in the box, safe and away, until you are satisfied with it. That way, you *can't* break anything!

Let's make such a box right now, shall we?
Branches are easy to create and do. All you have to do is:
- `git checkout -b NAME`
	- The `-b` here tells git to make a new branch. Usually, you leave that out :>

Choose whatever name you like - best is something descriptive, so it's clear what you're working on!

## Making a difference
Now that we have our little protective timeout box around us, why don't we do something useful? :D  
If you look closely, there's a small typo in this file. "reglary" doesn't make much sense after all!
Open it in whatever editor you want, and put in the correct word :>

And ... Done! Run `git status`, and you'll see that it *has* seen that you've changed something, but isn't doing anything with that.  
*Hint: If you want even more detail, you can always run `git diff`. It'll tell you exactly what lines were changed in a file :>*

This is where the other commands into play. Write:  
`git add Lessons/1_Git/Task_2_Editing.md`  
This will add the file to our next commit. You can still make other changes, but you'll have to `git add` those too.  
Now, let's `git commit`, and write a descriptive message.
Git will take a snapshot of everything you changed, and allow others to see what you have done. Your changes can now also be reverted, if you need to, or you could go back to this exact point in time and look at your code now. All in all, pretty useful, so commit your code often and frequently!

*Hint: You can also use `git commit -a`, which automatically adds all changes - but not new files!*

## And puuuuuuusssh
Now that you got your new code, you wanna share it, right? Luckily, that's really quite simple! Just run `git push -u`  
Usually the `-u` isn't necessary, but since we have a new branch, we need to tell git that it should go to github :>

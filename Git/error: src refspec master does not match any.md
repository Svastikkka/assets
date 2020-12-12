[Problem](https://stackoverflow.com/questions/21264738/error-src-refspec-master-does-not-match-any)
From ```git branch`` it appears that somehow your local branch name is "origin".

You can rename the branch with ```-mv``` flag, like this:

```git branch -mv origin master```

After this ```git branch``` should show ```master``` :-)

# NATHANED


> As far as I know, all forks of a Github repo are set up to use a sort of a "super-repository" containing all objects from all other forks. The actual forked repositories are thin repacks with alternates set to point to that "super-repo." This allows for huge savings in disk space, because git is able to deduplicate a lot of redundant data and create efficient deltas for most commits. However, this also means that you can fork a repo, add a nasty commit to it like this one, and wait till the "super-repo" fetches it. After that happens, you are able to refer to it from any of the other forks as is demonstrated here.

... As seen in - https://github.com/torvalds/linux/commit/b4061a10fc29010a610ff2b5b20160d7335e69bf#commitcomment-31753680


Because of this, we can also abuse how GitHub renders downloads to create valid
looking assets from valid places, sourced in-reality from a very invalid place.


So here is how this was done:

1. <a class="github-button" href="https://github.com/cfg-sh/swinged/fork" data-icon="octicon-repo-forked" aria-label="Fork cfg-sh/swinged on GitHub">Fork The Main Repo (cfg-sh/swinged)</a>

2. Clone *YOUR* fork.

3. Run... 

```
$ echo "# NATHANED" > README.md
$ git commit -a -m 'NATHANED'
$ git push origin master
```

3. Generate a link that looks like code is sourced from `cfg-sh`. 


```
$ echo https://github.com/cfg-sh/swinged/archive/`git rev-parse --short=6 @~`.tar.gz | pbcopy 
```

4. Now tell everyone that `cfg-sh` is distributing malware for the deep-state. 


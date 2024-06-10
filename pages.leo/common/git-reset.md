# git reset [modified]

> Undo commits or unstage changes, by resetting the current Git HEAD to the specified state.
> If a path is passed, it works as "unstage"; if a commit hash or branch is passed, it works as "uncommit".
> More information: <https://git-scm.com/docs/git-reset>.


- Reset the repository to a given commit, discarding committed, staged and uncommitted changes since then:
- 回退到指定的commit处，强制覆盖当前工作目录：

`git reset --hard {{commit}}`

- 回退到指定的commit处，不覆盖当前工作目录：

`git reset --soft {{commit}}`


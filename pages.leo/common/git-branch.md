# git branch [modified]

> Main Git command for working with branches.
> More information: <https://git-scm.com/docs/git-branch>.

- 列出所有分支，当前分支用 * 标注：

`git branch -a`

- 查看当前分支的名称：

`git branch --show-current`

- 创建新分支（基于当前的commit）：

`git branch {{branch_name}}`

- 创建新分支（基于指定的commit）:

`git branch {{branch_name}} {{commit_hash}}`

- 重命名分支 (must not have it checked out to do this):

`git branch -m {{old_branch_name}} {{new_branch_name}}`

- 删除分支 (must not have it checked out to do this):

`git branch -d {{branch_name}}`


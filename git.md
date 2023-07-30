### git clone 

git clone 命令不仅仅只能拉取 master 分支。它默认会将远程仓库的所有分支都拉取下来，并在本地创建相应的分支。你可以使用 `git branch` 命令查看所有本地分支，以及使用 `git branch -r` 命令查看所有远程分支。要切换到其他分支，可以使用 `git checkout` 命令，例如 `git checkout branch_name` 切换到指定的分支。

如果要拉取远程仓库的特定分支，也可以使用 `git clone -b branch_name` 命令，例如 `git clone -b develop https://github.com/user/repo.git`，这样就可以将 develop 分支克隆到本地。

### 查看分支和切换分支

你可以使用 `git branch` 命令查看所有本地分支，以及使用 `git branch -r` 命令查看所有远程分支。 `git clone -b develop https://github.com/user/repo.git`

### `git clone -b branch_name` 和 `git pull origin branch_name` 是两个不同的 Git 命令，它们有不同的作用和使用场景：

1. `git clone -b branch_name`: 这个命令用于克隆远程仓库，并且指定要克隆的分支。通常情况下，`git clone` 默认会克隆远程仓库的所有分支，并在本地创建对应的分支。但是，如果你只想克隆特定的分支，可以使用 `-b` 参数来指定分支名，这样只会克隆指定的分支到本地。例如：`git clone -b develop https://github.com/user/repo.git` 会将远程仓库的 `develop` 分支克隆到本地。

2. `git pull origin branch_name`: 这个命令用于从远程仓库拉取（即获取）指定分支的最新更新并合并到当前分支。在执行这个命令之前，你需要先切换到要更新的本地分支，然后执行 `git pull origin branch_name`，Git 会从远程仓库的 `branch_name` 分支拉取最新的提交，然后尝试将这些提交合并到当前所在的本地分支。这样可以保持你的本地分支和远程分支同步。

总结区别：
- `git clone -b branch_name` 是在克隆时指定要克隆的特定分支，只会拉取该分支的内容到本地。
- `git pull origin branch_name` 是在当前所在分支的基础上，从远程仓库拉取指定分支的最新提交并进行合并，用于保持本地分支和远程分支同步。

### git commit

```
git commit -m "Add new feature"
```

这条命令会将提交信息设为 "Add new feature"，表示你在本次提交中添加了一个新的功能。

如果不使用 `-m` 选项，Git 会启动默认的文本编辑器（通常是 Vi 或 Vim）来编辑提交信息，需要在编辑器中输入提交信息后保存并关闭才能完成提交。使用 `-m` 选项可以省去这个步骤，使提交过程更加简便。

### git pull

`git pull` 命令用于从远程仓库获取最新的提交，并将这些提交合并到当前所在的本地分支。这样可以将本地分支与远程分支同步，确保你的本地代码是最新的。

使用 `git pull` 的基本语法如下：

```
phpCopy code
git pull <remote> <branch>
```

其中：

- `<remote>`：指定要拉取代码的远程仓库的名称，通常为 "origin"，这是默认的远程仓库名称。
- `<branch>`：指定要拉取代码的远程分支的名称，例如 "main"、"master"、"develop" 等。

### git push

`git push` 命令用于将本地仓库中的更改推送到远程仓库。在使用 `git push` 前，需要先进行一次提交（commit），确保本地仓库有待推送的更改。

使用 `git push` 的基本语法如下：

```
git push <remote> <branch>
```

其中：

- `<remote>`：指定要推送的远程仓库的名称，通常为 "origin"，这是默认的远程仓库名称。
- `<branch>`：指定要推送的本地分支的名称，例如 ："main"、"master"、"develop" 等。
# GIT NOTE

## Init Git for your project

```command
git init
git branch -M main
git add .
git commit -m "first commit"
git remote add origin https://github.com/username/repo.git
git push -u origin main
```

## Push your poject to mutiple git repo

```command
git remote add github_repo_1 https://github.com/username/repo1.git
git remote add github_repo_2 https://github.com/username/repo2.git
git remote add gitlab https://gitlab.com/username/repo_on_gitlab.git

```

## Add file

```command
1. Add single file
  git add file_name

2. Add mutiple file
  git add file_name_1 file_name_2 folder/file_name_3 ...

3. add all [recommend =))]
  git add .
```

## Delete branch

```command
git branch -d <branch_name>
git branch -D <branch_name>
```
- The -d option is an alias for --delete, which only deletes the branch if it has already been fully merged in its upstream branch.
- The -D option is an alias for --delete --force, which deletes the branch "irrespective of its merged status." [Source: man git-branch]


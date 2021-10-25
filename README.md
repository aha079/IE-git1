# IE-git1
Q3-1: git commit --amend \
Q3-2: git add . \
      git commit -m "env is created" \
      git push -u origin master \
      git filter-branch --tree-filter "rm -rf .venv" --prune-empty HEAD \
      git for-each-ref --format="%(refname)" refs/original/ | xargs -n 1 git update-ref -d \
      echo .venv/ >> .gitignore \
      git status \ 
      git add .gitignore \
      git commit -m 'Removing .venv from git history' \
      git gc \
      git push origin master --force \

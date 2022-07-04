# Github Exercise

### Part 1 : Test on git branching and commit
```bash
git clone git@github.com:kennyvoo/github-test.git
cd github-test/
git checkout -b feature-1
# Add feature1.py
git add feature1.py
git commit -m "Added Feature 1"
# Add utils.py
git add utils.py
git commit -m "Added helper function" 
git push --set-upstream origin feature-1
```

### Part 2 : Test on git merge
```bash
git checkout main
git checkout -b feature-2
# commit 2 changes
git add feature2.py
git commit -m "Added feature 2"
git add feature2.py
git commit -m "Refactored code of feature 2"
git merge origin/feature-1
git push --set-upstream origin feature-2
# directly change content of README.md file at github server
git pull origin feature-2:feature-2
```

### Part 3 : Test on git rebase
```bash
git checkout main
git checkout -b feature-2
git add feature3.py
git commit -m "Added feature 3"
git add feature3.py
git commit -m "Added Hi function"
git push --set-upstream origin feature-3
git rebase feature-1
git rebase -i HEAD~2
git push --force origin feature-3
```

### Part 4: Test on git cherry pick
```bash
git checkout main
git checkout -b feature-4
git add feature4.py
git commit -m "Added feature 4"
git add feature3.py
git commit -m "Added hello function"
# find the hash from feature-1 branch
git log 
git cherry-pick 77946568075a62347de524b70bfdd20fceaca07c
git push --set-upstream origin feature-4

```


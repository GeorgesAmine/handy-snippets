## To clean up .DS_Store from git repo locally:
Run this in terminal:
'''console
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
'''
Add '.DS_Store' to .gitignore file

the run:
'''console
git add .
git commit -m "cleaned DS_Store"
'''

## To clean up .DS_Store from git repo locally:
Run this in terminal:
```bash
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
```
Add `.DS_Store` to `.gitignore` file

then run:
```bash
git add .
git commit -m "cleaned DS_Store"
```

## To create and start a virtual env for python projects:
Run this in terminal in the main project directory:
```bash
python3 -m venv venv
source venv/bin/activate
```
if a ```requirements.txt``` file exists you can add packages to your venv by running:
```bash
pip install -r requirements.txt
```

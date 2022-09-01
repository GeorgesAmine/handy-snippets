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

## To add configuration variables to environment on mac using zsh:
Run this in terminal in your home directory to open .zshenv in VS code:

```zsh
code .zshenv
```
In VS code add this line and save:
```zsh
export VARIABLE_NAME='top_secret_config'
```
Restart a new terminal session. Run this code:
```zsh
echo $VARIABLE_NAME
```
The output should be ```top_secret_config```
Now you can use this in python Config class:
```python
import os
VARIABLE_NAME = os.environ.get('VARIABLE_NAME')
```

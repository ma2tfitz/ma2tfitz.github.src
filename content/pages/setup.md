---
Title: Pelican Setup Notes
---

Create GitHub repos for ma2tfitz.github.src (these sources) and ma2tfitz.github.io (the generated GitHub pages). Will publish to 'output' as usual, but make that a submodule so that when we push from that diretcory it updates ma2tfitz.github.io).

```
git clone git@github.com:ma2tfitz/ma2tfitz.github.src
git submodule add git@github.com:ma2tfitz/ma2tfitz.github.io.git output
pelican-quickstart # or whatever to create the structure
make html serve # check at localhost:8000
make publish
cd output # add 'output' *first*
git add .
git commit -m 'Initial commit'
git push -u origin master
cd ..
# put *~ *.elc \#*\# *.pyc etc into .gitignore
git dd .
git commit -m 'Initial commit'
git push -u origin master
```





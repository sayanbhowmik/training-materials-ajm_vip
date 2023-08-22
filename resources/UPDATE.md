To make updates to the Jupyter book:

* Commit and push to the Github repo (permissions required)
* pip install jupyter-book
* pip install ghp-import
* jb build ./mini-book
* ghp-import -n -p -f _build/html

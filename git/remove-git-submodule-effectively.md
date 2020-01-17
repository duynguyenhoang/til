# How to delete git submodule effective

To remove a submodule you need to:

*Note*: Relevant section should be module name and path

* Delete the relevant section from the `.gitmodules` file.
* Stage the `.gitmodules` changes by running `git add .gitmodules`
* Delete the relevant section from `.git/config`
* Run `git rm --cached path_to_submodule` (no trailing slash).
* Run `rm -rf .git/modules/path_to_submodule` (no trailing slash).
* Commit `git commit -m "Removed submodule"`
* Delete the now untracked submodule folder/files `rm -rf path_to_submodule`

Source: https://gist.github.com/myusuf3/7f645819ded92bda6677

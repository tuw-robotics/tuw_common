# tuw_common 
tuw_common is a meta package to simplify the checkout of the tuw_* framework
## checkout procedure
Be aware that this repository holds submodules (links to other git repositories with a specific version)
### Checkout
To clone the repo
```git clone git@github.com:tuw-robotics/tuw_common.git```
To pull the submodules
```git submodule update --init --recursive```
Be aware that the submodules are not nessesarly the last avalibe version. 

### Update a submodule to latest commit on origin
The git submodule update command actually tells Git that you want your submodules to each check out the commit already specified in the index of the superproject. If you want to update your submodules to the latest commit available from their remote, you will need to do this directly in the submodules. [source: https://stackoverflow.com/questions/5828324/update-git-submodule-to-latest-commit-on-origin]


#### Update submodule:
```
cd your_root_folder_with_submodules

# time passes, submodule upstream is updated
# and you now want to update

# change to the submodule directory
cd submodule_dir

# checkout desired branch
git checkout master

# update
git pull

# get back to your project root
cd ..

# now the submodules are in the state you want, so
git commit -am "Pulled down update to submodule_dir"
```
#### Commit submodule update:
```
cd your_root_folder_with_submodules
git push
```


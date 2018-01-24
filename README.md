# tuw_common 
tuw_common is a meta package to simplify the checkout of the tuw_* framework
## checkout procedure
Be aware that this repository holds submodules (links to other git repositories with a specific version)
### Checkout
To clone the repo
```
git clone git@github.com:tuw-robotics/tuw_common.git
```
To pull the submodules
```
git submodule update --init --recursive
```
Be aware that the submodules are not nessesarly the last avalibe version. 

### Update a submodule to latest commit on origin
The git submodule update command actually tells Git that you want your submodules to each check out the commit already specified in the index of the superproject. If you want to update your submodules to the latest commit available from their remote, you will need to do this directly in the submodules. [source: https://stackoverflow.com/questions/5828324/update-git-submodule-to-latest-commit-on-origin]

```
cd $TUW_COMMON_DIR
git submodule update --init --recursive

cd tuw_control 
git checkout master
git pull origin master

cd ../tuw_geometry
git checkout kinetic
git pull origin kinetic

cd ../tuw_msgs
git checkout master
git pull origin master

cd ../tuw_rviz
git checkout master
git pull origin master

cd ../tuw_teleop
git checkout master
git pull origin master
```


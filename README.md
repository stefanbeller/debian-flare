# README

This is the repo holding all relevant files to build a (hopefully) proper Debian package for the game flare (see Links section).


This repo uses 4 branches:

* master
holds the current upstream + the debian folder that's needed to build the package
* upstream
holds the releases of flare
* pristine-tar
pristine-tar is used to be able to rebuild an orig.tar.gz from the upstream branch. Thus I don't have to keep all upstream tarballs here
* readme_first
is basically here for the README file you are just reading :)

If you want to build a flare package on your own, follow these steps:

<pre>
# clone the repo
git clone git@github.com:hennr/debian-flare.git

# ...
cd debian-flare

# make git follow the repo's branches locally
git checkout -b master origin/master
git checkout -b upstream origin/upstream
git checkout -b pristine-tar  origin/pristine-tar

# move to master repo and build it!
git checkout master

# build the package with the tool you prefer
git-buildpackage
dpkg-buildpackage
...
</pre>

## Links

Homepage  http://clintbellanger.net/rpg
Source    https://github.com/clintbellanger/flare
Forums    http://opengameart.org/forums/projects/flare

## Thanks

A thanks goes out to Matthias Schmitz for helping me with my first Debian package.
Another thanks goes to Loic Dachary for sponsoring this package (aka uploading it to Debian).

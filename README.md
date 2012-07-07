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
only exists for the README file you are just reading :)

If you want to build a flare package on your own, follow these steps:

<pre>
# clone the repo
git clone git://github.com/hennr/debian-flare.git

# ...
cd debian-flare

# make git follow the relevant remote branches locally
git checkout -b master origin/master
git checkout -b upstream origin/upstream
git checkout -b pristine-tar  origin/pristine-tar

# checkout the master branch...
git checkout master

# ... and build the package with the tool of your choice
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
Another thanks goes to Loic Dachary for sponsoring this package (aka uploading it to Debian)  
and to Manuel A. Fernandez Montecelo for helping and uploading this package again and again and ... :)

## Support

If you'd like to support us, you can flattr this package:  

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=hennr&url=https://github.com/hennr/debian-flare&title=debian-flare&language=en_GB&tags=github&category=software) 
  
Thanks!

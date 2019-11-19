# ppa-changelog-assembly-descriptor [![Build Status](https://travis-ci.com/agrica/ppa-changelog-assembly-descriptor.svg?branch=master)](https://travis-ci.com/agrica/ppa-changelog-assembly-descriptor)


## OSS Releasing
```bash
git co -b prepare-release
mvn versions:set -DnewVersion=$VERSION
mvn clean install
git commit -am "Prépare Release version $VERSION"
git tag -a ossrh-$VERSION -m "Release version $VERSION"
git push origin ossrh-$VERSION
git checkout master
git branch -D prepare-release
```

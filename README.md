# dvmhost-compiled

This repository contains a pipeline to compile the dvmhost binary for various architectures.

## Releases

All compiled binaries can be found on the [releases](https://github.com/northern-trunked/dvmhost-compiled/releases) page.

## Making New Releases

Upon observing the creation of a new tag on [dvmhost's tags page](https://github.com/DVMProject/dvmhost/tags), create a new tag in this repository with the same name as the tag in dvmhost's repository. For instance, if a new tag named `2023-03-01` is created, the following command will trigger the pipeline to build a new release for this tag:

```shell
git tag 2023-03-01
git push origin --tags
```

If you created an incorrect tag or would like to retry the build of the same tag on a new commit, use the following command to delete a tag on an old commit and create a new tag on HEAD:

```shell
git tag -d 2023-03-01
git push --delete origin 2023-03-01

git tag 2023-03-01
git push origin --tags
```

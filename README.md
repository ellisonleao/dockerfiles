## dockerfiles

[![Travis CI](https://img.shields.io/travis/ellisonleao/dockerfiles.svg?style=for-the-badge)](https://travis-ci.org/ellisonleao/dockerfiles)

This is a repo to hold various Dockerfiles for images I use. It's a small subset from [jesse's dockerfiles](https://github.com/jessfraz/dockerfiles) awesome repo with some small changes for a few of them.

### Using the `Makefile`

```
$ make help
build                          Builds all the dockerfiles in the repository.
dockerfiles                    Tests the changes to the Dockerfiles build.
image                          Build a Dockerfile (ex. DIR=telnet).
latest-versions                Checks all the latest versions of the Dockerfile contents.
run                            Run a Dockerfile from the command at the top of the file (ex. DIR=telnet).
shellcheck                     Runs the shellcheck tests on the scripts.
test                           Runs the tests on the repository.
```

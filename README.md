# FLINT.docker

This repository contains all the dockers required to build a FLINT library on various platforms (currently only Bionic).

Each platform requires the base image, and then the platform build on that base

Image names take the form:

```docker
mojaglobal/[image]:[platform]
```

So...

```docker
mojaglobal/flint-baseimage:bionic
mojaglobal/vscode-baseimage:bionic
mojaglobal/flint:bionic
```


## Bionic flint-baseimage

A Bionic based base image to build moja global libraries and executables

## Bionic flint

A Bionic image of the built moja global libraries and executables

## Bionic vscode-baseimage

A Bionic based base image to use in Visual Studio Code remote containers

## cmake

A make has been provided in each folder to help with the docker builds.

It takes the following coommands:

```
cmake help
help                           This help.
build                          Build the containers
build-nc                       Build the container without caching
release                        Make a release by building and publishing the `$(TAGNAME)` and `latest` tagged containers to docker hub
publish                        Publish the `$(TAGNAME)`and `latest` tagged containers to docker hub
publish-latest                 Publish the `latest` taged container to docker hub
publish-version                Publish the `$(TAGNAME)` taged containers to docker hub
tag                            Generate container tags for the `$(TAGNAME)` and `latest`
tag-latest                     Generate container `latest` tag
tag-version                    Generate container `$(TAGNAME)` tag
```

with defaults:

### filnt-baseimage

```bash
DOCKER_REPO=mojaglobal
APP_NAME=flint-baseimage
BRANCH=develop
TAGNAME=bionic
CPUNUM=8
```

### filnt

```bash
DOCKER_REPO=mojaglobal
APP_NAME=flint
BRANCH=develop
TAGNAME=bionic
CPUNUM=8
```

### vscode-baseimage

```bash
DOCKER_REPO=mojaglobal
APP_NAME=vscode-baseimage
BRANCH=develop
TAGNAME=bionic
CPUNUM=8
```

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)): 

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/leitchy"><img src="https://avatars0.githubusercontent.com/u/3417817?v=4" width="100px;" alt=""/><br /><sub><b>James Leitch</b></sub></a><br /><a href="https://github.com/moja-global/About_moja_global/commits?author=leitchy" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/mfellows"><img src="https://avatars0.githubusercontent.com/u/8548157?v=4" width="100px;" alt=""/><br /><sub><b>Max Fellows</b></sub></a><br /><a href="https://github.com/moja-global/About_moja_global/commits?author=mfellows" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!  

moja global would like to recognise the contribution of the Government of Canada to support the development of its open-source repositories and frameworks.
  
  
## Maintainers Reviewers Ambassadors Coaches

The following people are Maintainers Reviewers Ambassadors or Coaches

<table><tr><td align="center"><a href="https://github.com/leitchy"><img src="https://avatars0.githubusercontent.com/u/3417817?v=4" width="100px;" alt=""/><br /><sub><b>James Leitch</b></sub></a><br /><a href="https://github.com/moja-global/About_moja_global/commits?author=leitchy" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/mfellows"><img src="https://avatars0.githubusercontent.com/u/8548157?v=4" width="100px;" alt=""/><br /><sub><b>Max Fellows</b></sub></a><br /><a href="https://github.com/moja-global/About_moja_global/commits?author=mfellows" title="Code">💻</a></td></tr></table>

**Maintainers** review and accept proposed changes  
**Reviewers** check proposed changes before they go to the Maintainers  
**Ambassadors** are available to provide training related to this repository  
**Coaches** are available to provide information to new contributors to this repository  


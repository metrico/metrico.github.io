<img src="https://avatars.githubusercontent.com/u/21342216?s=200&v=4">

## 📦 [metrico package repo](https://metrico.github.io)

[![Debian and RPM Repo](https://github.com/metrico/metrico.github.io/actions/workflows/repo.yml/badge.svg)](https://github.com/metrico/metrico.github.io/actions/workflows/repo.yml)

This `deb`/`rpm` repository is powered by [Github Actions](https://github.com/metrico/metrico.github.io/tree/main/.github), [Github Pages](https://jon.sprig.gs/blog/post/2835) and [nfpm](https://nfpm.goreleaser.com/)

<!-- update: 202305111130 -->


## Installation Script
### DEB System
```bash
wget -q -O - https://github.com/metrico/metrico.github.io/raw/main/libchdb_installer.sh | sudo bash
sudo yum install -y libchdb
```
### RPM System
```bash
wget -q -O - https://github.com/metrico/metrico.github.io/raw/main/libchdb_installer.sh | sudo bash
sudo apt install libchdb
```

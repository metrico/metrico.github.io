---
layout: home
title: Metrico Package Repository
---

### Add a Debian Repository

Download the [public key](metrico.gpg)
```
wget -qO- {{ site.url }}/metrico.gpg | sudo tee /etc/apt/trusted.gpg.d/metrico.gpg >/dev/null
```

Next, create the source in `/etc/apt/sources.list.d/`

```
echo "deb [arch=all signed-by=/etc/apt/trusted.gpg.d/metrico.gpg] {{ site.url }}/deb stable main" | sudo tee /etc/apt/sources.list.d/metrico.list >/dev/null
```

Then run `apt update && apt install -y` followed by the names of the packages you want to install.

```
apt install libchdb
```

### Add a RPM Repository

Download the repo file `cd /etc/yum.repos.d ; curl {{ site.url }}/metrico.repo -LO`

Then you can do `yum install -y` followed by the names of the packages you want to install.

```
yum install libchdb
```

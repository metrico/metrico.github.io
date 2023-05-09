---
layout: home
title: Metrico DEB/RPM Package Repository
---

### Add a Debian Repository

Download the [public key](metrico.gpg) and put it in
`/etc/apt/keyrings/metrico.gpg`. You can achieve this with:

```
wget -qO- {{ site.url }}/metrico.asc | sudo tee /etc/apt/keyrings/metrico.asc >/dev/null
```

Next, create the source in `/etc/apt/sources.list.d/`

```
echo "deb [arch=all signed-by=/etc/apt/keyrings/metrico.asc] {{ site.url }}/deb stable main" | sudo tee /etc/apt/sources.list.d/metrico.list >/dev/null
```

Then run `apt update && apt install -y` followed by the names of the packages you want to install.

### Add a RPM Repository

Download the repo file `cd /etc/yum.repos.d ; curl {{ site.url }}/metrico.repo -LO`

Then you can do `yum install -y` followed by the names of the packages you want to install.


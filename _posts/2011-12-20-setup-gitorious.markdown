---
layout: default
title: Get started with the UFZ internal Gitorious
description:
categories: advanced
---

## Gitorious Overview ##

[Gitorious](http://www.gitorious.org) is a Git based development platform similar to Github. It can only be used for Open Source projects. But Gitorious itself is open source, so everybody can download it and install it on its own server.

A test server was setup on one of the Vislab machines. *So it is only accessible within the UFZ  net*.

The Gitorious server has the following features:

- Git repository hosting (both team and personal (only writable by its owner) repositories)
- Many views:
  - [Commit log](http://vismac02.local:8080/ogs5/sources/commits/ff)
  - [Commit tree view](http://vismac02.local:8080/ogs5/sources/graph/ff)
  - [Commit view](http://vismac02.local:8080/ogs5/sources/commit/68f2a74554ee0a97959f590e04f7970040964f9d)
  - [Browse the source](http://vismac02.local:8080/ogs5/sources/trees/ff)
  - [Blame view (who did what)](http://vismac02.local:8080/ogs5/sources/blobs/blame/046275e618be222238766b40240728a7afb4ce5b/FEM/rf_bc_new.h)
- Merge requests with code review (but this functionality is far less elegant than this feature on Github)
- You can subscribe to other people or repositories and get all recent activity in a nice dashboard view

## Get started ##

- [Setup an account](http://vismac02.intranet.ufz.de:8080/users/new) on the Gitorious server
- Upload your public ssh key (normally found in ~/.ssh/id_rsa.pub) to your Gitorious account (found under Manage SSH Keys on your Dashboard page)
- Edit ~/.ssh/config:

{% highlight bash %}
Host vismac02.intranet.ufz.de
  HostName 141.65.34.28
  Port 2222
{% endhighlight %}

*Note*: You have to use different ports for both the webserver (8080) and the ssh connection (2222) because the Gitorious server runs in a virtual machine on vismac02.

Clone an existing repository to your pc or create a new one inside Gitorious and then clone it to your pc.

## Subversions Sync ##

The branch *master* of the [OGS main repository](http://vismac02.local:8080/ogs5/sources) is automatically synced (hourly) to the [sources-directory in the Subversion trunk](https://svn.ufz.de/ogs/browser/trunk/sources).

To get the lastest changes from the Subversion trunk simply merge the branch *master* of the main repository.

To push changes from Git to Subversion simply push to the branch *master* of the main repository. It has to be decided who has write permission to the main repository.
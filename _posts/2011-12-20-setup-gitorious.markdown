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

- If you have not done before: [install and setup Git](https://help.github.com/articles/set-up-git)
- [Setup an account](http://vismac02.intranet.ufz.de:8080/users/new) on the Gitorious server (you will get a confirmation email with a link, insert `:8080` into the link url after `ufz.de`)
- Upload your public ssh key (normally found in ~/.ssh/id_rsa.pub) to your Gitorious account (found under Manage SSH Keys on your Dashboard page)
- Edit ~/.ssh/config
 - To create this file type `touch ~/.ssh/config`
 - Now edit this file with a text editor or use *vim* (`vim ~/.ssh/config`, press *i*-key, enter the following, press *ESC*-*:*-*w*-*q*-*ENTER*):
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


## Workflow ##

![Gitorious Workflow](/images/gitorious-workflow.png "Gitorious Workflow")

### Fetch upstream changes ###

In the Git world the repository where a project originated is often called as the ***upstream*** repo. In our case the upstream repo is [Gitorious OGS5/sources][ogs5-sources-link]-repo. Most developers will not have write but read access to it. This means it is no problem to stay up-to-date with it.

#### To create a git remote to the upstream repo: ####

This only need to be done once. On the Git bash type:

    git remote add upstream git://vismac02.intranet.ufz.de/ogs5/sources.git

This registers a new git remote with the url to the repository. You now have two remotes on your local git repo:

    git remote
    > origin
    > upstream

#### To fetch and merge upstream changes: ####

First fetch all changes from upstream:

    git fetch upstream

Then you can merge the contents of the master branch of the upstream repo:

    git merge upstream/master

Eventually you have to resolve conflicts.


### Fetch changes from another developer ###

The procedure is the same as above for the upstream repository. First create a new git remote which points to the other developers repo on the server:

    git remote add norihiro git://vismac02.intranet.ufz.de/~watanabe/ogs5/watanabes-sources.git

Now you have another remote called *norihiro* from where you can fetch and merge changes:

    git fetch norihiro
    git merge norihiro/master

### Prepare a new release ###

To do a release you first have to merge in all changes from upstream (see above). Afterwards tell one of the integrator persons (which have write access to  the upstream repo) to push your changes into the upstream repo.

[ogs5-sources-link]: http://vismac02.intranet.ufz.de:8080/ogs5/sources

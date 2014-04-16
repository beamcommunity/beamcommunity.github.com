This is the BEAM Community page for 2013 projects.

In this page we review all accepted projects as well all the Open Source Projects that took part in the 2013 edition!

## Accepted Projects

This page lists down the projects accepted in GSoC 2013, in the BEAM community. You can navigate through the following and track the status of each project-

* [Elixir - Debugger and Inspection](#elixir---debugger-and-inspection)
* [Erlang Package Manager (epax)](#erlang-package-manager-epax)
* [MongooseIM: XEP-0313 Message Archive Management](#mongooseim-xep-0313-message-archive-management)
* [Rebalancing for Disco’s Distributed File System](#rebalancing-for-discos-distributed-file-system)
* [Zotonic Moules Repository Integration](#zotonic-moules-repository-integration)

### Elixir - Debugger and Inspection

The student worked on pretty printing for Elixir along the community. In particular, the community had already started working on pretty printing, however it was based on Wadler's work for Haskell (a lazy language) and the performance was not optimal for Elixir. The student ported the work to an OCaml based implementation as described in the "Strictly Pretty" paper by Christian Lindig.

The remaining of the student work went into an interactive/debugging tool and some of it was merged back as well. In particular, the discussions and proof of concepts developed by the student were helpful to improve Elixir's debugging facilities. He is still working on the project as part of his thesis.

* **GSoCer:** Gustavo Brunoro
* **Mentor:** José Valim

### Erlang Package Manager (epax)

The idea of a new package manager for Erlang is to have the concept of publisher. Epax allows managing any Erlang package/application maintained using git, bzr, svn. The basic features adding a new repo, removing a repo, bundling the dependencies, searching for a package, showing the details of a package have been implemented. As of now, no separate config file is required. The package is assumed to follow standard OTP structure.

Now, we will add the concept of publisher into Epax before we launch the first version. This will allow a user to add trusted publishers and their packages will be downloaded when required without any manual intervention unless of course absolutely necessary.

* **GSoCer:** Aman Mangal
* **Mentor:** Eric Merritt, Jordan Wilberding

### MongooseIM: XEP-0313 Message Archive Management

The extension development was continued by Erlang Solutions. Major part of the code developed by the student was merged. Based on benchmark results, several bottlenecks were removed and new optimizations were introduced. Redesigned module structure makes its behavior more flexible. Experimental Cassandra back-end was added.

* **GSoCer:** Uvarov Michael
* **Mentor:** Stefan Strigler

### Rebalancing for Disco’s Distributed File System

The goal of this project is to implement a rebalancing mechanism for DDFS clusters to solve imbalance. Patrik started with implementing a feature which lets the master node collect diskinfo from the nodes. This information is later used to compute the average utilization and over/under-utilized nodes. He, then, added a blob selection functionality for the selection of write nodes such that nodes with the lowest disk utilization are chosen.

Data objects are deleted from a node to free up space if the objects have enough replicas. He added logic to remove the references to the deleted replicas from the tags containing them. He also made changes to how the garbage collection is started so that the most over-utilized node will call `is_orphan` for all its objects to free up space. Locations of blobs that are reported as non existing during the build_map phase are now stored in the gc_blobs table and later removed from the tags containing those locations during the updating of tags. Patrik's work will be merged into the develop branch after disco 0.5 is released and resolving a couple of issues in the code.

Update:
This work is now merged into the develop branch of Disco with this [pull request](https://github.com/discoproject/disco/pull/492).


* **GSoCer:** Patrik Pettersson
* **Mentor:** Prashanth Mundkur, Harry Nakos

### Zotonic Moules Repository Integration

A new command line tool and admin module was developed, integrating the management of modules on a site with those available online from the zotonic modules repository. The admin module manager works by spawning an Erlang process to the command line module manager. By default, the modules are installed in $ZOTONIC_ROOT/priv/modules. Part of the work has been merged with the zotonic [master branch](https://github.com/zotonic/zotonic/commit/5675a76e47a4480aa87045354e0ffcd95244cab6). The admin module manager is available [here](https://github.com/mawuli-ypa/mod_zmm). Mawuli will continue on the project as there are some enhancements to make.

* **GSoCer:** Mawuli Adzaku
* **Mentor:** Andreas Stenius

## Participating OSS projects

All participating OSS projects are listed here (alphabetically). Click on the project below to see all proposals/ideas related to that project for 2013:

* [Disco proposals](/2013/Project:-Disco.md) - Disco is a distributed computing framework based on the MapReduce paradigm
* [ejabberd proposals](/2013/Project:-ejabberd.md) - ejabberd is robust, efficient, scalable modular XMPP servers, it is the most largely used server in the world, running both small personal installation and huge scale deployments
* [Elixir proposals](/2013/Project:-Elixir.md) - Elixir is a functional meta-programming language that runs on the Erlang VM
* [Erlware proposals](/2013/Project:-Erlware.md) - Erlware is a community to oversee the develop of strategic Erlang tools and libraries
* [MongooseIM proposals](/2013/Project:-MongooseIM.md) - MongooseIM is a robust and efficient XMPP server aimed at large installations (This is a modified version of ejabberd)
* [Tsung proposals](/2013/Project:-Tsung.md) - Tsung is a flexible, extensible and large scale benchmark tool
* [Zotonic proposals](/2013/Project:-Zotonic.md) - Zotonic is a high speed, real-time web framework and content management system


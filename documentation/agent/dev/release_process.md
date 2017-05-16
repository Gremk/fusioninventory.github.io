---
layout: page
title: Release process
---

# Changes list validation

Ensures the Change file contains references to all majors changes since latest release, with references to all resolved bugs.

Fix the date of the release in the Changelog. The date can be generated with the following command:

    date -R

The changelog section entry must start with a line in the following format:

    2.2.5  Thu, 16 Aug 2012 12:03:30 +0200

* version
* 2 spaces
* date -R

# Test suite validation

Ensures the full test suite, with developper tests enabled, executes correctly on the following platforms:

* Linux
* Windows

    make test TEST_AUTHOR=1

# Repository tagging

    git tag -s X.Z.Z
    git push --tags

# Tarball creation

    ./tools/updatePciids.sh # For the agent
    perl Mafile.PL
    make distsign
    make disttest
    make manifest
    make dist

# Tarball upload

Tarball has to be uploaded on the forge and on CPAN.

# Mark bugs as closed

Go on the [forge](http://forge.fusioninventory.org/) and change the status of the fixed from to closed.

# Release announcement

Publish official announcement:

* [Get the wiki source]({{ site.baseurl }}/documentation/wiki.html)
* Go in fusioninventory.branchable.com directory
* Launch `./create-release-post.pl <URL tarball on the forge>`

At the end the process this should be done:

* as a post to the user mailing-list
* as a news on the website

# Bugtracker update

Switch all bugs resolved by the latest release from 'resolved' to 'closed state'.
Move all still open bugs to next planned version if you still believe they will be fixed in a timely fashion. Otherwise you should unset the “planned version” field of the bugs.

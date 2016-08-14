---
layout: page
title: Guidelines to dev
redirect_from:
 - /documentation/dev.html
---

# Agent specific

* [Release process]({{ site.baseurl }}/documentation/agent/dev/release_process.html)

[![Build Status](https://travis-ci.org/fusioninventory/fusioninventory-agent.png?branch=master)](https://travis-ci.org/fusioninventory/fusioninventory-agent)

# Get the sources

* [Source]({{ site.baseurl }}/documentation/agent/installation/source.html)
* Git: [UNIX]({{ site.baseurl }}/documentation/agent/dev/git_unix.html), [Windows]({{ site.baseurl }}/documentation/agent/dev/git_windows.html)

* [Official download location]({{ site.baseurl }}/documentation/dev/official_download_location.html)

# Standalone server

* [Stand alone server]({{ site.baseurl }}/documentation/dev/standaloneserver.html)

# Fusioninventory plugin for GLPI

* Branches: <br/>
  › [master](https://github.com/fusinv/fusioninventory-for-glpi/tree/master)  › [![Build Status](https://travis-ci.org/fusioninventory/fusioninventory-for-glpi.png?branch=master)](https://travis-ci.org/fusioninventory/fusioninventory-for-glpi) [![Coverage Status](https://coveralls.io/repos/fusioninventory/fusioninventory-for-glpi/badge.svg?branch=master&service=github)](https://coveralls.io/github/fusioninventory/fusioninventory-for-glpi?branch=master)

* Roadmaps: <br/>
  › [Task Redux]({{ site.baseurl }}/documentation/dev/plugin-glpi/task_redux.html)

  › [New page of Plugins > FusionInventory]({{ site.baseurl }}/documentation/dev/plugin-glpi/new_home_page.html)

# Run unit tests for GLPI plugin

* [How to run unit tests for plugin FusionInventory for GLPI]({{ site.baseurl }}/documentation/dev/pluginglpi_unit_test.html)

# Technical documentation

## Agent-server communication protocol

Current agent-server communication is a mix of legacy XML and new JSON messages.

Generic task-scheduling protocol:

* [Original task scheduling specification]({{ site.baseurl }}/documentation/dev/spec/protocol/rest.html)
* [Current task scheduling specification]({{ site.baseurl }}/documentation/dev/spec/protocol/scheduling.html)

Module-specific communication protocols:

* [ESX module]({{ site.baseurl }}/documentation/dev/spec/protocol/esx.html)
* [Deploy module]({{ site.baseurl }}/documentation/dev/spec/protocol/deploy.html)
* [Collect module]({{ site.baseurl }}/documentation/dev/spec/protocol/collect.html)
* [Inventory module]({{ site.baseurl }}/documentation/dev/spec/protocol/inventory.html)
* [Network discovery module]({{ site.baseurl }}/documentation/dev/spec/protocol/netdiscovery.html)
* [Network inventory module]({{ site.baseurl }}/documentation/dev/spec/protocol/netinventory.html)
* [Wake on lan module]({{ site.baseurl }}/documentation/dev/spec/protocol/wakeonlan.html)
* [Vocabulary]({{ site.baseurl }}/documentation/dev/spec/protocol/vocabulary.html)

## Code documentation of plugin for GLPI

[Plugin FusionInventory for GLPI code documentation]({{ site.baseurl }}/documentation/dev/plugin_doc_code/index.html)

## Others

* [New directory layout (partially implemented)]({{ site.baseurl }}/documentation/dev/spec/new-directory-layout.html)
* [Load configuration from external places]({{ site.baseurl }}/documentation/dev/spec/load_ext_cfg.html)
* [POIP inventory with HTTP]({{ site.baseurl }}/documentation/dev/spec/poip.html)
* [Switch stack inventory]({{ site.baseurl }}/documentation/dev/spec/switch_stack.html)

## Events

* [Mini Codecamp March 14]({{ site.baseurl }}/documentation/dev/events/2014-03-14_Mini_CodeCamp.html)
* [meeting 18 february 2015]({{ site.baseurl }}/documentation/dev/events/2015-02-18_meeting.html)

+++
title = "chef-shell (executable)"
draft = false

aliases = ["/chef_shell.html"]

[menu]
  [menu.docs]
    title = "chef-shell (executable)"
    identifier = "chef_workstation/chef_workstation_tools/chef_shell.md chef-shell (executable)"
    parent = "chef_workstation/chef_workstation_tools"
    weight = 20
+++    

[\[edit on GitHub\]](https://github.com/chef/chef-web-docs/blob/master/content/ctl_chef_shell.md)

{{% chef_shell_summary %}}

The chef-shell executable is run as a command-line tool.

Modes
=====

{{% chef_shell_modes %}}

Options
=======

This command has the following syntax:

``` bash
chef-shell OPTION VALUE OPTION VALUE ...
```

This command has the following options:

`-a`, `--standalone`

:   Run chef-shell in standalone mode.

`-c CONFIG`, `--config CONFIG`

:   The configuration file to use.

`-h`, `--help`

:   Show help for the command.

`-j PATH`, `--json-attributes PATH`

:   The path to a file that contains JSON data.

    Use this option to define a `run_list` object. For example, a JSON
    file similar to:

    ``` javascript
    "run_list": [
      "recipe[base]",
      "recipe[foo]",
      "recipe[bar]",
      "role[webserver]"
    ],
    ```

    may be used by running `chef-shell -j path/to/file.json`.

    In certain situations this option may be used to update `normal`
    attributes.

    {{< warning >}}

{{% node_ctl_attribute_text %}}

{{% node_ctl_attribute_code_block_1 %}}

will result in a node object similar to:

{{% node_ctl_attribute_code_block_2 %}}

    {{< /warning >}}

`-l LEVEL`, `--log-level LEVEL`

:   The level of logging to be stored in a log file.

`-o RUN_LIST_ITEM`, `--override-runlist RUN_LIST_ITEM`

:   Replace the current run-list with the specified items. Only
    applicable when also using `solo` or `server` modes.

`-s`, `--solo`

:   Run chef-shell in chef-solo mode.

`-S CHEF_SERVER_URL`, `--server CHEF_SERVER_URL`

:   The URL for the Chef Infra Server.

`-v`, `--version`

:   The Chef Infra Client version.

`-z`, `--client`

:   Run chef-shell in Chef Infra Client mode.

Configure
=========

{{% chef_shell_config %}}

chef-shell.rb
-------------

{{% chef_shell_config_rb %}}

Run as a Chef Infra Client
--------------------------

{{% chef_shell_run_as_chef_client %}}

Debugging Cookbooks
===================

{{% chef_shell_breakpoints %}}

Step Through Run-list
---------------------

{{% chef_shell_step_through_run_list %}}

Debug Existing Recipe
---------------------

{{% chef_shell_debug_existing_recipe %}}

Advanced Debugging
------------------

{{% chef_shell_advanced_debug %}}

Manipulating Chef Infra Server Data
===================================

{{% chef_shell_manage %}}

Examples
========

The following examples show how to use chef-shell.

"Hello World"
-------------

{{% chef_shell_example_hello_world %}}

Get Specific Nodes
------------------

{{% chef_shell_example_get_specific_nodes %}}

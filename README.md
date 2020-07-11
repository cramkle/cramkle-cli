# cramkle-cli

> Based off on the [`magic-cli`](https://github.com/slackhq/magic-cli) by Slack

Utility functions to make working with Cramkle infra easier.

## Adding new commands

When you run `cramkle`, it will look for executables in the same directory as itself which have filenames that begin with `cramkle-`. If there's an executable called `cramkle-build`, you could run it by typing `cramkle build`.

Now, when you type `cramkle`, you'll see `cramkle build` in the list of supported subcommands. 

For extra credit, you can add a human-readable description in that list by putting a comment immediately under the `#!` line:

```bash
#!/usr/bin/env bash
# This line will be shown in the list of commands.
```

You can also define any extra parameters that are required for the script with a `# @param` line for each parameter:

```bash
#!/usr/bin/env bash
# This line will be shown in the list of commands.
# @param <command_param> - Longer Description of the Parameter
# @param - If you don’t give a parameter name, a default one will be created for you
```

## Installation

This repository includes a Makefile that will install `cramkle-cli` and all of its subcommands into `/usr/local/bin`:

```bash
$ make install
```

You can also use it to uninstall `cramkle-cli`:

```bash
$ make uninstall
```

## Updates

A script for updating the tools is already included; it makes installing the latest tools into a single step process:

```bash
$ cramkle update
Updated tools to 01ec2ef (2016-03-30 16:20:30 -0700)
```

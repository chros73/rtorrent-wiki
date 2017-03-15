# rTorrent Scripting Explained

:warning: | This guide is still very incomplete — the best way to remedy that is to contribute what you know.
---: | :---

You can use the quite powerful GitHub search to find information on commands, e.g. their old vs. new syntax variants, what they actually do (i.e. “read the source”), and internal uses in predefined methods, handlers, and schedules. 
Consider the [view.add](https://github.com/rakshasa/rtorrent/search?utf8=%E2%9C%93&q=%22view.add%22) example.

 * [[RPC Setup XMLRPC|RPC-Setup-XMLRPC]]
 * [[Sending commands with XMLRPC2SCGI|RPC-Utility-XMLRPC2SCGI]]
 * Auto-generated list of [[options|RPC-Option-Strings]] used with some commands.
 * [[Migration to 0.9 command syntax|RPC-Migration-0.9]]


## Commands Reference

Command (Group) | Short Description
---: | :---
[[method.*|COMMAND-Methods]] | Define new commands based on existing ones.
[[branch & if|COMMAND-Conditional]] | Execute different commands depending on conditions.
[[execute[.*]|COMMAND-Execute]] | Call operating system commands, possibly catching their output for use within rTorrent.
[[schedule|COMMAND-Scheduling]] | Repeatedly execute commands, either in a given frequency, or at certain times.
[[system.*|COMMAND-System]] | Commands related to the operating system and the XMLRPC API.
[[ui.*|COMMAND-UserInterface]] | These commands control aspects of the ‘curses’ UI.


## Variable types

This is a summary about the possible variable types in [command_dynamic.cc](https://github.com/rakshasa/rtorrent/blob/master/src/command_dynamic.cc) (applies to v0.9.6).

Available types:

 * multi (with subtypes: static, private, const, rlookup)
   * TODO: what is it
 * simple (with subtypes: static, private, const)
   * TODO: why is it "simple"
 * value, bool, string, list (with subtypes: static, private, const)
   * Standard types, "value" is an integer.
# dvz_secure_content for myBB 1.6

Backport of @Devilshakerz's [dvz_secure_content](https://community.mybb.com/mods.php?action=license&pid=450) myBB 1.8 plugin to support myBB 1.6. As the original plugin states, it:

> Filters user-generated content from insecure protocols (non-HTTPS).

## A word of caution

> ⚠️⚠️ **WARNING** ⚠️⚠️
>
> You should already know this, but **myBB 1.6 is not supported anymore**. Running it
**is probably not secure**, and you should _really_ consider upgrading to the latest
supported version.
>
> ⚠️⚠️ **WARNING** ⚠️⚠️

## Installation

The usual myBB installation instructions:

1. Copy the files to the `inc/` directory of your myBB installation
2. Go to your board's Admin CP/Configuration/Plugins
3. Look for \[this version of\] DVZ Secure Content & click "Install & Activate"
4. Go to Admin CP/Settings/DVZ Secure Content & configure the proxy

In addition, it seems there's [a bug in myBB 1.6 that makes it try to word-wrap URLs](https://community.mybb.com/thread-40223.html). The result of that is that spurious `&#8203;` characters get added in the middle of the generated (camo'ed) URL if your forum has word wrap enabled with a length shorter than the generated URLs. So you should either increase the word wrap value or disable it (making it 0) by going to Admin CP/Settings/Posting and changing the "Number of Characters before Word Wrapping Occurs" value.

If you need some instructions about setting up HTTPs on your forum, take a look at [this official myBB guide](https://docs.mybb.com/1.8/administration/security/https/). Don't forget it was written for myBB 1.8 - and _this version_ of the plugin works in 1.6 - so there _might be_ some differences between the guide and your setup. Sorry about that ¯\\\_(ツ)\_/¯

## Attribution

I've made just enough effort to make this plugin work in an old myBB version - the plugin itself was created by @Devilshakerz, so go thank him!

If there's any bug in the code - it's probably my bad, so don't get mad at him!

## Copyright

dvz_secure_content by Tomasz 'Devilshakerz' Mlynski [devilshakerz.com]; Copyright (C) 2015-2017
released under Creative Commons BY-NC-SA 4.0 license: https://creativecommons.org/licenses/by-nc-sa/4.0/
myBB 1.6 compatibility by Matias Garcia Isaia (https://github.com/mgarciaisaia)

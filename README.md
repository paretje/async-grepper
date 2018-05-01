[![Build Status](https://travis-ci.org/paretje/async-grepper.svg?branch=master)](https://travis-ci.org/paretje/async-grepper)

Use your **favorite grep tool**
([ag](https://github.com/ggreer/the_silver_searcher),
[ack](http://beyondgrep.com), [git grep](https://git-scm.com/docs/git-grep),
[ripgrep](https://github.com/BurntSushi/ripgrep),
[pt](https://github.com/monochromegane/the_platinum_searcher),
[sift](https://sift-tool.org),
[findstr](https://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/findstr.mspx),
grep) to start an **asynchronous search**. Matches will be added to the
quickfix list **as they are found**.

This plugin works with Vim and Neovim. It's based on
[vim-grepper](https://github.com/mhinz/vim-grepper), but used
[asyncrun.vim](https://github.com/skywind3000/asyncrun.vim) to execute the
grepper commands, and append the results asynchronously to the quickfix list.

_Disclaimer: using the location list, appending to an existing quickfix list
and stopping search after a certain number of results have been returned are
currently unsupported. PR's welcome._

---

- [Prompt](https://github.com/mhinz/vim-grepper/wiki/using-the-prompt): Use
  `:Grepper` to open a prompt, enter your query, optionally cycle through the
  list of tools, fire up the search.
- [Operator](https://github.com/mhinz/vim-grepper/wiki/using-the-operator): Use
  the current visual selection to pre-fill the prompt or start searching right
  away.
- [Commands](https://github.com/mhinz/vim-grepper/wiki/using-the-commands):
  `:Grepper` supports a wide range of flags which makes it extremely flexible.
  All supported tools come with their own command for convenience:
  `:GrepperGit`, `:GrepperAg`, and so on. They're all built atop of `:Grepper`.
- [Custom tools](https://github.com/mhinz/vim-grepper/wiki/Add-a-tool): Changing
  the behaviour of the default tools is very easy. And so is adding new tools.

---

_If you like [vim-grepper](https://github.com/mhinz/vim-grepper), you will love
async-grepper._

## Documentation

This README is only the tip of the iceberg. Make sure to read `:h grepper` and
[the wiki](https://github.com/mhinz/vim-grepper/wiki) to learn about every
feature.

Example configurations be be found
[here](https://github.com/mhinz/vim-grepper/wiki/example-configurations-and-mappings).

_The truth is out there._

## Installation

Use your [favorite plugin
manager](https://github.com/mhinz/vim-galore#managing-plugins), e.g.
[vim-plug](https://github.com/junegunn/vim-plug):

    Plug 'skywind3000/asyncrun.vim'
    Plug 'paretje/asyc-grepper'

If you prefer lazy loading:

    Plug 'skywind3000/asyncrun.vim', { 'on': 'AsyncRun' }
    Plug 'mhinz/vim-grepper', { 'on': ['Grepper', '<plug>(GrepperOperator)'] }

## Demo

General usage:

![vim-grepper](https://github.com/mhinz/vim-grepper/blob/master/pictures/grepper-demo.gif)

Grepping only files currently loaded in Vim:

![vim-grepper](https://github.com/mhinz/vim-grepper/blob/master/pictures/grepper-demo2.gif)

## Feedback

If you like this plugin, star it! It's a great way of getting feedback. The same
goes for reporting issues or feature requests.

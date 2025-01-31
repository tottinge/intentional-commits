# intentional-commits

An [intentional commit](https://intentionalcommits.org/) tool for git users.

# Installation

Once you have cloned this repo, source the `gnext` file into your
zshell session.

> source gnext

As a convention, I put the `gnext` file in `$HOME/bin/` and set  my `.zshrc` to source the file, so it's always active.

# Commands Provided

> gnext "commit message"

... for planning your next commit

Stashes the commit message in `~/.gnext-intentions` in a file named after the current project's root folder.


> gdone

... for committing the work you've just completed.

Shows the git status, retrieves the commit message, gives you the option to edit the message or accept it as-given, then performs `git commit -am "${message}"`

> gnope

... for abandoning the work done since the last commit.

Deletes the stashed commit message and performs `git reset --hard`


# See also:

* [What's This About Microcommits](https://www.industriallogic.com/blog/whats-this-about-micro-commits/)
* [An Example of Usage](https://www.industriallogic.com/blog/gilded-rose-with-ai-and-pycharm/)


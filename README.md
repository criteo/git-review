git-review
----------

Manage review workflow for projects hosted on GitHub (using pull requests).

    $ git review list
    Pending requests for 'b4mboo/git-review/master'
    ID      Date       Comments  Title
    42      14-Jul-11  0         [Review] Request from 'mess110' @ 'b4mboo/git-review/documentation
    23      13-Jul-11  8         [Review] Request from 'mess110' @ 'b4mboo/git-review/new_feature

    $ git review list --reverse
    Pending requests for 'b4mboo/git-review/master'
    ID      Date       Comments  Title
    23      13-Jul-11  8         [Review] Request from 'mess110' @ 'b4mboo/git-review/new_feature
    42      14-Jul-11  0         [Review] Request from 'mess110' @ 'b4mboo/git-review/documentation

    $ git review show 42
    > [summary]
    > [diffstat]

    $ git review show 42 --full
    > [summary]
    > [full diff]

    $ git review browse 42
    > go to web page

    $ git review checkout 42
    > checkout changes from request #42 to your local repository

    $ git review accept 42
    > accept request #42 by merging it

    $ git review decline 42
    > decline request #42 and close it

    $ git review create
    > create a new request


Installation
------------

To install it via Rubygems, you might need to add Gemcutter to your Rubygems sources:

    gem install gemcutter --source http://gemcutter.org

Afterwards simply do:

    gem install git-review

(Prefix with `sudo` if necessary)

To be able to use all of git-review's features you have set up your git config for GitHub.

    $ git config --global github.user your_gitubusername
    $ git config --global github.token your_githubtoken123456789

You can find your API token on the [account](https://github.com/account) page.

If you want to use git-review with a private GitHub instance (http://fi.github.com/), set the github.host config value to your internal host.

    $ git config --global github.host github.mycompany.com


Wiki
----

For more information visit the [wiki](https://github.com/b4mboo/git-review/wiki).

Actinium Core integration/staging tree
=====================================

https://actinium.org

What is Actinium NG?
---------------------

Actinium is an experimental digital currency **based on Bitcoin** that enables instant payments to
anyone, anywhere in the world. Actinium uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Actinium Core is the name of open source
software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the Actinium Core software, see https://actinium.org

**This Actinium variant is based on latest Bitcoin master and is considered unstable.**

The original variant (based on Litecoin) can be downloaded from [this repository](https://github.com/Actinium-project/Actinium)

License
-------

Actinium Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/Actinium-project/Actinium-ng/tags) are created
regularly to indicate new official, stable release versions of Actinium Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and macOS, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

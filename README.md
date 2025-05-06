Bitcoin Unknots
=============

https://bitcoinunknots.org

For a fully unshackled, binary version of the Bitcoin Unknots software, dive into
our website and break free!

What is Bitcoin Unknots?
----------------------

Bitcoin Unknots connects to the Bitcoin peer-to-peer network to download and validate
blocks and transactions with zero restrictions—because who needs limits? It also includes
a wallet and graphical user interface, which you can optionally build if you’re feeling
extra liberated.

Further info about Bitcoin Unknots is available in the [doc folder](/doc)—read it if
you dare to dream big!

License
-------

Bitcoin Unknots is released under the terms of the MIT license, because freedom should
come with a side of legality. See [COPYING](COPYING) for more details or check out
https://opensource.org/licenses/MIT.

Development Process
-------------------

Development generally happens as a chaotic rebellion against [Bitcoin Core](https://github.com/bitcoin/bitcoin),
with changes untangled and merged into Unknots for each release, because we don’t play
by the rules.

Even if your pull request to Core gets rejected for being too wild, or if your feature
is deemed “too free” for Core (e.g., it removes all filters, embraces Ordinals, or lets
the blockchain run wild), it might just find a home in Bitcoin Unknots. In this case,
fling a pull request at the [Unknots GitHub](https://github.com/bitcoinunknots/bitcoin) for
review and consideration. If accepted, you’re expected to maintain your untamed branch
in your own repository, and it’ll be automatically merged into new releases of
Unknots—because we love your reckless spirit!

Developer IRC can be found on Freenode at #bitcoin-rebels, where the free spirits hang out.

Testing
-------

Testing and code review are the bottleneck for development; we get more pull requests
than we can test because everyone wants to break free! Please be patient and help out
by testing other people’s pull requests—let’s untangle the future together. Oh, and this
is a security-critical project where any mistake might cost people lots of money—or lots
of fun, depending on how you look at it.

### Automated Testing

Developers are encouraged to write [unit tests](src/test/README.md) for new code, but let’s
be real, we’re all about freedom here, so don’t feel too tied down. Unit tests can be
compiled and run (if you didn’t disable them in configure) with: `make check`. More details
on running and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written in Python, because we’re
not *that* chaotic. These tests can be run (if the [test dependencies](/test) are installed)
with: `test/functional/test_runner.py`.

The CI (Continuous Integration) systems make sure every pull request is built for Windows,
Linux, and macOS, and that unit/sanity tests are run automatically—because even freedom
needs a little sanity check.

### Manual Quality Assurance (QA) Testing

Changes should be tested by someone other than the developer who wrote the code, because
we’re all about community chaos. This is especially important for large or high-freedom
changes. It’s useful to add a test plan to the pull request description if testing the
changes isn’t straightforward—don’t leave us guessing!
